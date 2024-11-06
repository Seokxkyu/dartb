## 틀린 코드 이유 분석(정답 코드 참고)

**틀린 코드**

```sql
SELECT *
FROM (SELECT FOOD_TYPE, REST_ID, REST_NAME, MAX(FAVORITES) AS FAVORITES
FROM REST_INFO
GROUP BY FOOD_TYPE
ORDER BY FOOD_TYPE DESC
```

**틀린 이유**
```
- GROUP BY와 SELECT 컬럼 불일치: GROUP BY를 사용하면 집계되지 않은 컬럼은 선택할 수 없어, FOOD_TYPE별 최대 즐겨찾기 수를 가진 REST_ID와 REST_NAME을 반환할 수 없다.

- MAX(FAVORITES)와 원본 데이터 간 매칭 문제: MAX(FAVORITES)는 최대 즐겨찾기 수를 구하지만, 해당 레코드의 REST_ID와 REST_NAME을 식별하지 못해, 원본 테이블에서 다시 조회해야 한다.
```

- 정답 코드
    
    ```sql
    SELECT FOOD_TYPE, REST_ID, REST_NAME, FAVORITES
    FROM REST_INFO
    WHERE (FOOD_TYPE, FAVORITES) IN (
        SELECT FOOD_TYPE, MAX(FAVORITES)    
        FROM REST_INFO
        GROUP BY FOOD_TYPE
    ) 
    ORDER BY FOOD_TYPE DESC;
    ```
    

## 개선된 쿼리 학습

또한, 이 문제에서는 아래 **개선된 쿼리**로도 조회될 수 있습니다. 

**ROW_NUMBER 윈도우 함수**를 사용합니다.
### 성분으로 구분한 아이스크림 총 주문량

```sql
WITH RankedRest AS (
    SELECT 
        FOOD_TYPE, REST_ID, REST_NAME, FAVORITES,
        ROW_NUMBER() OVER (PARTITION BY FOOD_TYPE ORDER BY FAVORITES DESC, REST_ID) AS rnk
    FROM REST_INFO
)
SELECT 
    FOOD_TYPE, REST_ID, REST_NAME, FAVORITES
FROM RankedRest
WHERE rnk = 1
ORDER BY FOOD_TYPE DESC;
```

- 임시로 데이터를 저장하는 방식 활용하여, 복잡한 쿼리에 대한 가독성을 높임
- ROW_NUMBER 함수 통해서 각 FOOD_TYPE 그룹 내에서 순위를 매깁니다.
- ORDER BY FAVORITES DESC, REST_ID 사용하여 각 그룹 내에서 즐겨찾기 수가 가장 높은 순으로 정렬 수행
- CTE RankedRest에서 rnk = 1 조건을 사용해 각 FOOD_TYPE 그룹 내에서 즐겨찾기 수가 가장 많은 식당 필터링