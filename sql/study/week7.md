**동물의 생물 종, 이름, 성별 및 중성화 여부를 아이디 순으로 조회하는 SQL문을 작성합니다.**

이때, 이름이 없는 동물의 이름은 ‘No name’으로 합니다.

**문제1. IFNULL()으로 해결**

```sql
// IfNULL() 함수 문법을 익히고 사용하여 해결해주세요.
SELECT 
    ANIMAL_TYPE,
    IFNULL(NAME, 'No name') AS NAME,
    SEX_UPON_INTAKE
FROM
    ANIMAL_INS 
ORDER BY
    ANIMAL_ID
```

같은 문제를, CASE WHEN 문법을 사용하여 해결해주세요

**문제2. CASE WHEN으로 해결**

```sql
//CASE WHEN 문법을 익히고 사용하여 해결해주세요.
SELECT 
    ANIMAL_TYPE,
    CASE WHEN NAME IS NULL THEN 'No name' ELSE NAME END AS NAME,
    SEX_UPON_INTAKE
FROM
    ANIMAL_INS 
ORDER BY
    ANIMAL_ID
```

**-중성화 여부 파악하기**

[](https://school.programmers.co.kr/learn/courses/30/lessons/59409#qna)

**문제 3. 문제를 풀어주세요 (힌트: IF, LIKE를 사용할 수 있습니다)**

```sql
SELECT 
    ANIMAL_ID,
    NAME,
    IF(SEX_UPON_INTAKE LIKE '%Neutered%' OR SEX_UPON_INTAKE LIKE '%Spayed%', 'O', 'X') AS '중성화'
FROM 
    ANIMAL_INS
ORDER BY 
    ANIMAL_ID;
```

**문제 4. 아래는 QnA에 올라온 질문입니다. 왜 풀이가 틀렸는지 답해주세요.**

```sql
IF 함수에서 조건을 작성할 때 논리연산자 OR 조건문의 각 부분을 명확히 작성하지 않았음

if (sex_upon_intake like '%Neutered%' or '%Spayed%', 'O' , 'X') as '중성화'

대신

IF(SEX_UPON_INTAKE LIKE '%Neutered%' OR SEX_UPON_INTAKE LIKE '%Spayed%', 'O', 'X') AS '중성화'

구문을 사용해야 함
```