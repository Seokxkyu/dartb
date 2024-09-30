# SQL Assignment Week 1


## 1. BigQuery 기초 지식
데이터베이스 : 데이터의 저장소<br>
테이블: 데이터가 저장된 공간<br>
저장된 데이터를 제품에서 사용

### OLTP
- Online Transaction Processing
- 거래를 하기 위해 사용되는 데이터베이스
- 보류, 중간 상태가 없음
- 데이터의 추가(INSERT), 변경(UPDATE) 많이 발생 
- SQL 사용해 데이터 추출할 수 있으나, 분석을 위해 만든 데이터베이스가 아니라 쿼리 속도가 느릴 수 있음

### SQL
- Structured Query Language
- 데이터베이스에서 데이터를 가지고 올 때 사용하는 언어
- 데이터베이스의 데이터를 관리하기 위해 설계된 특수 목적의 프로그래밍 언어

### OLAP
- OLTP로 데이터 분석을 하다가 속도, 기능 부족의 이슈로 OLAP 등장
- **OLAP**: Online Analytical Processing
> **데이터 웨어하우스**<br>
데이터를 한 곳에 모아서 저장<br>
여러곳에 저장된 데이터 예시 (Database, 웹, 파일 api 결과 등)

### BigQuery
Google Cloud의 OLAP + Data Warehouse

**장점**
1. 난이도<br>
SQL을 사용해 쉽게 데이터 추출 가능
2. 속도<br>
OLAP 도구이므로 속도가 빠름
3. Firebase, Google Analytics 4의 데이터를 쉽게 추출할 수 있음<br>
사용 기기, 위치, OS 버전, 이벤트 행동 획득 가능 (별도의 로깅 필요)
4. 데이터 웨어하우스를 사용하기 위해 서버 (컴퓨터)를 띄울 필요 없음<br>
구글에서 인프라 관리

### Big Query 사용하는 이유
- 회사에서 앱이나 웹에서 Firebase, Google Analytics 4를 활용할 경우
- 운영을 적은 비용으로 진행하기 위해 


## 2. BigQuery 환경 설정
### BigQuery의 환경 구성 요소
1. 프로젝트 (Project)
- 하나의 큰 컨물
- 하나의 프로젝트 내에 여러 데이터셋이 존재할 수 있음
- 목적에 맞는 형태로 특정 데이터만 프로젝트에 저장 

2. 데이터셋 (Dataset)
- 프로젝트에 있는 창고 (각 창고 공간에 데이터를 저장)
- 판매 데이터, 고객 데이터 등 별도의 데이터 저장할 수 있음
- 하나의 데이터셋에 다양한 테이블 존재할 수 있음

3. 테이블 (Table)
- 창고에 있는 선반
- 테이블 안에는 상품의 세부 정보가 저장
- 테이블 안에 행과 열로 이루어진 데이터들이 저장
- 스프레드 시트 형식


## 3. 데이터 활용 Overview
**데이터를 활용하는 과정**

![image](https://github.com/user-attachments/assets/67c89144-e930-483d-84ae-d794be96b819)

> 문제 정의<br>
**MECE**: 중복이 없고 상호배제적<br>
So What?, Why so?

> 지표 정의<br>
Metric


## 4. 저장된 데이터 확인하기
### SQL 쿼리를 작성하기 전에
- 데이터가 어떻게 저장되어 있는가?에 대해 생각해보기
- 어떤 데이터가 저장되어 있는가?
- 칼럼의 의미는 무엇인가?

> 데이터를 제대로 이해해야 올바른 데이터를 추출할 수 있음 (구체적인 정의를 항상 확인하면서 쿼리를 작성해야 함)

### 데이터가 저장되는 형태
**ERD**<br>
    데이터베이스 구조를 한눈에 알아보기 위해 사용
    ![image](https://github.com/user-attachments/assets/65e89355-2641-40ff-ae5b-198953803a1b)


**ERD 예시 - Pokemon**
![image](https://github.com/user-attachments/assets/ba33067d-c3d7-44be-ad33-291d2b521eed)

