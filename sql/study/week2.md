## 문제 1
### 우리 플랫폼에 정착한 판매자 1

```sql
SELECT 
    seller_id, 
    COUNT(DISTINCT order_id) AS orders
FROM 
    olist_order_items_dataset
GROUP BY 
    seller_id
HAVING 
    orders >= 100
ORDER BY 
    orders DESC;
```
![image](https://github.com/user-attachments/assets/eb800d3c-23f2-4cd4-b90e-8c883e676072)

> 배운 점

`HAVING orders >= 100`은 판매자가 처리한 주문 수가 100건 이상인 판매자만 필터링 가능

`WHERE 절`과 다르게 집계 함수가 계산된 후의 결과에 조건을 적용


## 문제 2
### 몇 분이서 오셨어요?

```sql
SELECT *
FROM tips
WHERE MOD(size, 2) = 1;
```
![image](https://github.com/user-attachments/assets/d553c7e5-722c-4b15-8691-fa11668808ee)

> 배운 점

`MOD` 함수는 나머지 연산자로, 두 수를 나눴을 때 나머지를 반환

## 문제 3
### 최고의 근무일을 찾아라

```sql
SELECT 
    day, 
    ROUND(SUM(tip), 3) AS tip_daily
FROM 
    tips
GROUP BY 
    day
ORDER BY 
    tip_daily DESC
LIMIT 1;
```
![image](https://github.com/user-attachments/assets/bf177402-300d-4fdf-84bd-454ba8e9f532)

> 배운 점

집계 함수 `SUM(tip)`은 각 요일별로 모든 팁의 합계를 계산

`LIMIT 1`으로 상위 1개 결과 출력
