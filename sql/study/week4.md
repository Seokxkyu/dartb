## 문제 1
### ROOT 아이템 구하기

```sql
SELECT 
    I.ITEM_ID, 
    I.ITEM_NAME
FROM 
    ITEM_INFO I
JOIN 
    ITEM_TREE T 
ON 
    I.ITEM_ID = T.ITEM_ID
WHERE 
    T.PARENT_ITEM_ID IS NULL
ORDER BY 
    I.ITEM_ID ASC;

```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image5.png)


> 배운 점
- `ITEM_INFO`와 `ITEM_TREE` 테이블을 결합할 때 동일한 `ITME_ID`가 있는 행만 반환하는 형태의 `JOIN` 사용
- 부모 아이템이 없는 루트 아이템 찾기 위하여 `ITEM_TREE` 테이블에서 `PARENT_ITEM_ID`가 NULL인 항목 필터링


## 문제 2
### 노선별 평균 역 사이 거리 조회하기

```sql
SELECT 
    ROUTE, 
    CONCAT(ROUND(SUM(D_BETWEEN_DIST),1),'km') AS TOTAL_DISTANCE, 
    CONCAT(ROUND(AVG(D_BETWEEN_DIST),2),'km') AS AVERAGE_DISTANCE
FROM 
    SUBWAY_DISTANCE
GROUP BY 
    ROUTE
ORDER BY 
    SUM(D_BETWEEN_DIST) DESC;
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image4.png)

> 배운 점
- 역 간 거리의 총 합계를 계산하여 소수점 반올림하고, 계산된 총 누계 거리(정수 타입)에 'km' 단위를 추가하기 위하여 `CONCAT` 함수를 사용.
- 해당 노선의 평균 역 간 거리를 계산하여 소수점 반올림하고, 계산된 평균 거리(정수 타입)에 'km' 단위를 추가하기 위하여 `CONCAT` 함수를 사용.
- 총 누계거리를 기준으로 내림 차순 정렬하기 위하여 `DESC` 활용


## 문제 3
### 헤비 유저가 소유한 장소

```sql
SELECT 
    ID, NAME, HOST_ID
FROM 
    PLACES
WHERE 
    HOST_ID IN(
        SELECT HOST_ID
        FROM PLACES
        GROUP BY HOST_ID
        HAVING COUNT(ID) >= 2
    )
ORDER BY 
    ID
;
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image3.png)

> 배운 점

- `WHERE 절`에서 서브쿼리를 사용하여 ID의 합계가 2 이상인 HOST_ID만 필터링하는 방법
- `HOST_ID`를 기준으로 `GROUP BY` 사용하여 ID 별로 몇 개의 `PLACES`를 등록하였는지 조회