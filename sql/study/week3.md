## 문제 1
### 조건에 맞는 사용자와 총 거래금액 조회하기

```sql
SELECT 
    u.USER_ID, 
    u.NICKNAME, 
    SUM(b.PRICE) AS TOTAL_SALES
FROM 
    USED_GOODS_BOARD AS b
JOIN 
    USED_GOODS_USER AS u
ON 
    b.WRITER_ID = u.USER_ID  
WHERE 
    b.STATUS = 'DONE'  
GROUP BY 
    u.USER_ID, u.NICKNAME  
HAVING 
    SUM(b.PRICE) >= 700000  
ORDER BY 
    TOTAL_SALES ASC;  
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image1.png)


> 배운 점

- `JOIN 절`에서 `USED_GOODS_BOARD` 테이블과 `USED_GOODS_USER` 테이블을 `WRITER_ID`와 `USER_ID`를 기준으로 연결

- `INNER JOIN`을 활용하면 두 테이블에서 일치하는 데이터가 있는 행만 결과에 표시 가능

- `HAVING 절`과 `WHERE 절`
    - 사용자의 총 거래 금액을 구하는 집계 함수 사용 목적
> - **WHERE 절**: 개별 행에 대한 조건을 필터링 (GROUP BY가 적용되기 전에 사용)
> - **HAVING 절**: 그룹화된 데이터에 대한 조건 필터링 (집계 함수(SUM, COUNT 등)를 사용한 결과에 대한 필터링 시 사용)


## 문제 2
### 업그레이드 할 수 없는 아이템 구하기

```sql
SELECT 
    i.ITEM_ID, 
    i.ITEM_NAME, 
    i.RARITY
FROM 
    ITEM_INFO i
LEFT JOIN 
    ITEM_TREE t
ON 
    i.ITEM_ID = t.PARENT_ITEM_ID
WHERE 
    t.PARENT_ITEM_ID IS NULL
ORDER BY 
    i.ITEM_ID DESC;
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image2.png)

> 배운 점

- `LEFT JOIN` 특성을 고려할 때, 왼쪽 테이블인 `ITEM_INFO`에는 존재하지만, JOIN 대상인 `ITEM_TREE`에 해당되는 자식 아이템 존재하지 않는 경우에는 NULL 값을 반환

## 문제 3
### 조건에 맞는 개발자 찾기

```sql
SELECT 
    d.ID, d.EMAIL, d.FIRST_NAME, d.LAST_NAME
FROM   
    DEVELOPERS AS d
WHERE EXISTS(SELECT 1
             FROM SKILLCODES AS s
             WHERE s.NAME IN ('Python', 'C#') AND
             d.SKILL_CODE & s.CODE = s.CODE )
ORDER BY ID
```
![image](https://github.com/Seokxkyu/dartb/blob/main/sql/study/images/image.png)

> 배운 점

- `WHERE 절`에서 서브쿼리를 사용하여 `SKILLCODES` 테이블에서 Python과 C#에 해당하는 스킬을 가진 개발자만을 선택하는 과정

- 비트 연산 (d.SKILL_CODE & s.CODE = s.CODE) 부분에서 연산자 `&`는 `DEVELOPERS` 테이블의 SKILL_CODE와 `SKILLCODES` 테이블의 CODE를 비교하여 모두 1로 True인 행만 반환