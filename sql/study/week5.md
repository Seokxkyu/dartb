## 문제 1
### 성분으로 구분한 아이스크림 총 주문량

```sql
SELECT
    i.INGREDIENT_TYPE,
    SUM(f.TOTAL_ORDER) AS TOTAL_ORDER
FROM
    FIRST_HALF AS f
JOIN
    ICECREAM_INFO AS i ON f.FLAVOR = i.FLAVOR
GROUP BY
    i.INGREDIENT_TYPE
ORDER BY
    TOTAL_ORDER ASC;

```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image5.png)


> 배운 점
- `FIRST_HALF`와 `ICECREAM_INFO` 테이블을 JOIN 구문을 이용하여 `FLAVOR`열을 기준으로 결합
- `INGREDIENT_TYPE`별로 데이터를 그룹화하고, 총 주문량을 계산하기 위해 SUM 함수를 사용


## 문제 2
### 즐겨찾기가 가장 많은 식당 정보 출력하기

```sql
SELECT
    r.FOOD_TYPE,
    r.REST_ID,
    r.REST_NAME,
    r.FAVORITES
FROM
    REST_INFO AS r
JOIN (
    SELECT
        FOOD_TYPE,
        MAX(FAVORITES) AS MAX_FAVORITES
    FROM
        REST_INFO
    GROUP BY
        FOOD_TYPE
) AS m ON r.FOOD_TYPE = m.FOOD_TYPE
       AND r.FAVORITES = m.MAX_FAVORITES
ORDER BY
    r.FOOD_TYPE DESC;

```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image7.png)

> 배운 점
- `REST_INFO` 테이블에서 `FOOD_TYPE`별로 가장 높은 즐겨찾기 수를 MAX 활용해 계산하는 서브 쿼리
- 서브 쿼리를 통해 생성한 테이블의 경우에는 반드시 별칭 alias를 지정 필요
- 각 테이블의 동일한 `FOOD_TYPE`에 대하여, r.FAVORITES가 서브쿼리의 최대 즐겨찾기 수와 동일한 레코드만 선택


## 문제 3
### 조건에 맞는 사원 정보 조회하기

```sql
WITH temp AS(
    SELECT 
        EMP_NO, SUM(SCORE) SCORE
    FROM 
        HR_GRADE
    GROUP BY 
        EMP_NO
)
SELECT 
    temp.SCORE SCORE, e.EMP_NO EMP_NO, EMP_NAME, POSITION, EMAIL
FROM 
    HR_EMPLOYEES AS e
JOIN 
    temp USING(EMP_NO)
WHERE 
    SCORE = (SELECT MAX(SCORE) FROM temp)
ORDER BY   
    SCORE DESC;
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image8.png)

> 배운 점

- `WITH temp`절은 `HR_GRADE` 테이블에서 사원별 평가 점수를 `SUM`으로 합산한 후, `GROUP BY`로 각 사원의 총 점수를 계산
- 서브쿼리의 경우 생성한 `temp` 테이블의 최대 SCORE을 찾고, 이를 기준으로 최고 점수를 받은 사원을 필터링