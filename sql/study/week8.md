## PIVOT절
```행을 열로 전환한다```
- aggregate_function은 집계할 열을 지정한다.
- FOR 절은 PIVOT할 열을 지정한다.
- IN 절은 PIVOT할 열 값을 지정한다.

## UNPIVOT절
```열이 행으로 전환된다```
- UNPIVOT Column 절은 UNPIVOT된 값이 들어갈 열을 지정한다.
- FOR절은 UNPIVOT된 값을 설명할 값이 들어갈 열을 지정한다.
- IN절은 UNPIVOT할 열과 설명할 값의 리터럴 값을 지정한다.

### 문제
```sql
WITH NumberedOccupations AS (
    SELECT
        Name,
        Occupation,
        ROW_NUMBER() OVER (PARTITION BY Occupation ORDER BY Name) AS RowNum
    FROM OCCUPATIONS
),
PivotedOccupations AS (
    SELECT
        MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor,
        MAX(CASE WHEN Occupation = 'Professor' THEN Name END) AS Professor,
        MAX(CASE WHEN Occupation = 'Singer' THEN Name END) AS Singer,
        MAX(CASE WHEN Occupation = 'Actor' THEN Name END) AS Actor,
        RowNum
    FROM NumberedOccupations
    GROUP BY RowNum
)
SELECT 
    COALESCE(Doctor, 'NULL') AS Doctor,
    COALESCE(Professor, 'NULL') AS Professor,
    COALESCE(Singer, 'NULL') AS Singer,
    COALESCE(Actor, 'NULL') AS Actor
FROM PivotedOccupations
ORDER BY RowNum;
```
- Occupation별로 이름을 열로 변환. 
- `CASE문`과 집계 함수 `MAX` 활용
- `ROW_NUMBER()`를 사용하여 행 정렬
- `GROUP BY`를 사용한 Pivot 실행, 같은 `RowNum` 기준으로 그룹화


## 성능 최적화 기법
**1. 적절한 인덱스 설정**
- 인덱스는 쿼리 성능을 크게 개선하는 가장 중요한 요소.
- 자주 사용하는 검색 조건(WHERE), JOIN 키, 정렬(ORDER BY) 컬럼에 인덱스를 생성.
- 과도한 인덱스는 쓰기 성능 저하 및 저장 공간 낭비를 초래하므로 필요 최소한으로 관리.

**2. SELECT * 지양**
- 불필요한 데이터를 포함하지 않도록, 반드시 필요한 컬럼만 명시적으로 지정.
- 데이터 전송량과 쿼리 처리 시간을 줄이는 데 효과적.

**3. 쿼리 실행 계획 분석**
- EXPLAIN이나 EXPLAIN ANALYZE를 사용해 쿼리 실행 흐름을 파악.
- 어떤 인덱스가 사용되는지, 병목 구간이 있는지 확인.
- 성능 저하의 원인을 정확히 진단하고 개선 방향 설정.

**4. JOIN 최적화**
- 큰 테이블끼리의 `JOIN`을 최소화하고, 필요한 데이터만 `JOIN`.
- JOIN 조건에 인덱스를 적용하여 성능을 개선.

**5. LIMIT로 데이터 양 제어**
- 불필요한 대량 데이터를 가져오지 않도록 `LIMIT`을 활용.
- 특히 페이징 처리나 일부 데이터만 필요한 경우 유용.

**6. 데이터 파티셔닝 및 샤딩**
- 대용량 테이블은 `파티셔닝`을 통해 데이터를 물리적으로 분할해 접근 성능 향상.
- `샤딩`은 데이터를 여러 데이터베이스에 분산해 처리 부하를 줄임.

### 문제
```sql
UPDATE customers c
SET
    avg_order_value = (
        SELECT AVG(od.quantity * od.unit_price)
        FROM order_details od
        JOIN orders o ON od.order_id = o.order_id
        WHERE o.customer_id = c.customer_id
    ),
    total_spent = (
        SELECT SUM(od.quantity * od.unit_price)
        FROM order_details od
        JOIN orders o ON od.order_id = o.order_id
        WHERE o.customer_id = c.customer_id
    ),
    num_orders = (
        SELECT COUNT(DISTINCT o.order_id)
        FROM orders o
        WHERE o.customer_id = c.customer_id
    ),
    repurchase_rate = (
        SELECT
            COUNT(DISTINCT CASE WHEN od.product_id IN (
                SELECT product_id
                FROM order_details
                JOIN orders o ON order_details.order_id = o.order_id
                WHERE o.customer_id = c.customer_id
                GROUP BY order_details.product_id
                HAVING COUNT(order_details.product_id) > 1
            ) THEN od.product_id END) * 1.0 / COUNT(DISTINCT od.product_id)
        FROM order_details od
        JOIN orders o ON od.order_id = o.order_id
        WHERE o.customer_id = c.customer_id
    );
```