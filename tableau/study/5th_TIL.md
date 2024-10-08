# Fifth Study Week

- 38강: [퀵테이블계산(2)](#38-퀵테이블계산2)

- 39강: [LOD](#39강-lod)

- 40강: [EXCLUDE](#40-lod-exclude)

- 41강: [INCLUDE](#41-lod-include)

- 42강 : [매개변수](#42-매개변수)

* (43강이 없어 패스합니다)
- 44강: [매개변수 실습](#44-매개변수-실습)

- 45강: [마크카드](#45-워크시트-마크카드)

- 46강: [서식계층](#46-서식-계층)

- 47강: [워크시트](#47-워크시트-서식)

- [문제1](#문제-1)

- [문제2](#문제-2)

- [문제3](#문제-3)

## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)       |
| 30~39강      | ✅      | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)       |
| 40~49강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 50~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |


<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘의 스터디는 지니와 함께합니다.**

## 38. 퀵테이블계산(2)

<!-- 이동평균, YTD 총계, 전년 대비 성장률, YTD 성장률 등 본 강의에서 알게 된 점을 적어주세요 -->
- **이동평균**
  
  이전의 값부터 현재까지 값에 대한 평균을 낼 때 사용 (주식 데이터에서 많이 사용)

  ![image](https://github.com/user-attachments/assets/e3be2a0e-7d1d-42a1-bee8-2e4a0e92848f)


- **YTD**

  특정 시점을 기준으로 해당 연도부터 그 시점까지 총계 (연도보다 하위 레벨 필드인 '분기', '월'이 있어야 사용 가능)

  각 년도 안에서 매출 합계가 누적되어 데이터가 표현
  
  ![image](https://github.com/user-attachments/assets/f9d2830f-7f23-4538-8723-cc1de3766181)


- **통합 성장률**

  ![image](https://github.com/user-attachments/assets/c4ddc836-c0bd-4425-9039-fc22c645fd8e)


- **YTD 성장률**

  ![image](https://github.com/user-attachments/assets/2d2b926f-b5db-4736-9a41-0e697ee61218)




## 39강. LOD

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적어주세요. -->
- **LOD**

  Level of Detail의 줄임말로, 뷰의 세부 수준 나타냄 

- **LOD 표현식**

  현재 뷰에는 영향을 받지 않고, 원하는 세부 수준에서 계산 수행할 수 있음 (계산할 수준을 세부적으로 제어 가능)

- **FIXED LOD**

  현재 뷰에 있는 차원과 상관 없이 계산된 필드에서 원하는 차원을 따라 계산

  ![image](https://github.com/user-attachments/assets/5ac7e484-2b92-4253-a93d-bd4205a16a09)

  **계산된 필드 만들기, 퀵 테이블 계산과 비교**
  
  ![image](https://github.com/user-attachments/assets/82004086-5997-4a8c-a97a-41baf979fb63)



## 40. LOD EXCLUDE

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->

- **EXCLUDE LOD**

  현재 뷰에서 특정 차원을 제외하여 계산할 때 사용

  > 액세서리 매출과 각 제품 별 매출의 차이 그래프로 표시
    
    ![image](https://github.com/user-attachments/assets/a98b8328-db29-4028-81da-132ff30fb9f4)


  **비교**
  - EXCLUDE 활용
    
    ![image](https://github.com/user-attachments/assets/a6d4425e-f7b2-4cf6-a19e-f6b5dd9a9c91)
    > "하위 범주"를 "제조 업체" 수준으로 나타내면 EXCLUDE 사용한 경우에만 값이 변경됨
    
  - FIXED 활용
 
    ![image](https://github.com/user-attachments/assets/84dea7d1-d967-4e87-bb45-d7fe9bacba61)
    
  
> **🧞‍♀️ FIXED와 EXCLUDE을 사용하는 경우의 차이가 무엇인가요?**

```
FIXED는 현재 뷰와 관계없이 특정 차원을 사용해 계산하기 때문에 필터의 영향을 받지 않지만, EXCLUDE는 뷰에 있는 차원을 따라 계산하기 때문에 관련 차원을 필터로 걸어보면 필터가 영향 받음
```

> **🧞‍♀️ 왜 ATTR 함수를 사용하나요?**

```
액세서리 매출과 각 제품별 매출의 차를 계산하기 위해서, 각 제품 매출에서 동일한 단일 값을 빼도록 특성 함수 사용
```


## 41. LOD INCLUDE

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->

- **INCLUDE LOD**

  현재 뷰에서 특정 차원을 추가하여 계산 (EXCLUDE 처럼 차원 필터를 통해 해당 값 변경할 수 있음)

  > 각 도시의 고객당 평균 매출 계산

    **분석 탭 총계 활용하여 도시별 매출 평균 반환**
      ![image](https://github.com/user-attachments/assets/e6726e5b-6859-42b5-8079-81600113276f)

    **주문 ID 차원을 포함하여 합계한 매출의 평균 반환 (INCLUDE 함수 활용)**
      ![image](https://github.com/user-attachments/assets/3f42421a-4974-4491-91a4-d55d190dd91d)

    **EXCLUDE 활용**
      ![image](https://github.com/user-attachments/assets/40ee3bf1-cb0d-4180-8b24-f6c3a3341165)


> **🧞‍♀️ 그렇다면 어떤 경우에 각 표현식을 사용하나요? 예시와 함께 적어보아요**


```
뷰에 표시되는 값이 차원이면, FIXED LOD 표현식만 사용 (차원과 측정값 반환)
INCLUDE, EXCLUDE LOD 표현식은 측정값만 반환
반환 값을 차원 필터의 영향을 받게 되는 경우 INCLUDE, EXCLUDE 표현식 사용 
```


## 42. 매개변수

<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->

- **매개변수**

  고정된 상수값이 아닌 동적인 값으로 변경하기 위해서 활용하는 기능

  계산선, 필터, 참조선과 함께 사용

  > 매개변수 만들기 (데이터 필드 사용)
  
    ![image](https://github.com/user-attachments/assets/f613add9-df47-4c87-8f42-af8126b24d04)

  > 필터 편집 (필드 기준 변경)

    ![image](https://github.com/user-attachments/assets/de834ed1-280d-42c9-8303-52302e56814a)

  > 결과

    ![image](https://github.com/user-attachments/assets/219fd602-22eb-4f6d-adfe-b8734060c7b1)


> **🧞‍♀️ 집합에도 매개변수를 적용할 수 있나요? 시도해봅시다**

  ![image](https://github.com/user-attachments/assets/59c25da2-974d-4403-8a4b-8d70ea7b1ba5)


## 44. 매개변수 실습
(43번 강의가 없어 패스합니다)

<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->

> 분석 탭 참조선 추가

  ![image](https://github.com/user-attachments/assets/3c17f513-795d-4324-974c-2653c370cadb)

    값 -> 새 매개변수 추가

> 계산 필드 추가 (해당 필드 색상 마크 적용)

  ![image](https://github.com/user-attachments/assets/65130875-08d5-4d77-b3a0-1f152b057f52)

  ![image](https://github.com/user-attachments/assets/c1c06a65-f431-4a9b-8117-350c0a1041e5)

> 참조 구간 설정 방법

 ![image](https://github.com/user-attachments/assets/eaff5b3b-61a8-48fd-8cf8-11e48b2cdb1f)

 ![image](https://github.com/user-attachments/assets/3fac908a-4751-49f0-a139-62c6ed9ca3fe)



## 45. 워크시트 마크카드

<!-- 마크카드에 대해 알게 된 점을 적어주세요 -->
![image](https://github.com/user-attachments/assets/7bcf53d3-65bb-4afe-9ec0-e2eb4824f341)

> 여러 개의 텍스트 레이블 적용 시 편집

  ![image](https://github.com/user-attachments/assets/beb2428c-f1d8-4b58-ac9d-200fdd369615)


## 46. 서식 계층

<!-- 서식계층에 대해 알게 된 점을 적어주세요 -->

계층마다 서식 지정할 수 있으며, 이전에 설정한 서식들을 전부 지워야 하는 경우에는, "서식" 탭 "워크시트 서식 지우기"

> 마크 카드에서 설정된 서식 그대로 표시

![image](https://github.com/user-attachments/assets/bbd7c693-9ed4-4188-9a98-730dd3993ede)



> **🧞‍♀️ 서식계층을 일반적인 것에서 구체적인 것 순서로 기입해보세요**


```
워크 시트 서식
행 / 열 서식 
특정 필드
필드 레이블
도구설명 / 제목 / 마크
```


## 47. 워크시트 서식

<!-- 워크시트 서식에 대해 알게 된 점을 적어주세요!-->



## 문제 리스트

### 문제 1.

다음은 Tableau의 다양한 계산을 사용할 수 있는 경우를 빈칸으로 두고 문제를 작성한 것입니다. 각 빈칸에 적합한 계산 유형을 채워보세요.

보기
> **누계, 차이, 비율 차이, 구성 비율, 순위, 백분위수, 이동 평균, YTD 총계, 통합 성장률, 전년 대비 성장률, YTD 성장률**

| 계산 유형               | 설명                                                                 | 사용 예시                                                                                          |
|-------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 누계           | 데이터의 누적 합계를 계산                                             | 한 기업이 월별 매출 데이터를 누적하여 연간 매출 추이를 보고 싶을 때 사용                                      |
| 차이            | 연속 데이터 포인트 간의 차이를 계산                                    | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감량을 분석하고 싶은 경우                                        |
| 비율 차이            | 연속 데이터 포인트 간의 비율 변화를 계산                               | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감률(%)을 분석하고 싶은 경우                                      |
| 구성 비            | 전체에서 각 데이터 포인트의 비율을 계산                                | 한 기업이 전체 매출에서 각 제품군이 차지하는 비율을 보고 싶을 때 사용                                           |
| 순위            | 데이터의 순위를 매깁니다                                              | 한 기업이 제품별 매출 데이터를 순위별로 정렬하여 상위 10개 제품을 분석하고 싶은 경우                              |
| 백분위            | 데이터의 백분위를 계산                                               | 한 기업이 고객별 구매 금액 데이터를 백분위수로 나누어 상위 25% 고객을 분석하고 싶은 경우                          |
| 이동평균            | 일정 기간의 평균을 계산                                               | 한 기업이 주간 매출 데이터에서 4주 이동 평균을 계산하여 트렌드를 분석하고 싶은 경우                              |
| YTD 총계            | 연초부터 현재까지의 총계를 계산                                      | 한 기업이 월별 매출 데이터를 연초부터 현재까지 누적하여 연간 매출 목표 달성 여부를 분석하고 싶은 경우             |
| 통합성장률            | 일정 기간 동안의 연평균 성장률을 계산                                  | 한 기업이 5년 간 매출 데이터를 바탕으로 연평균 성장률(CAGR)을 계산하고 싶은 경우                                  |
| 전년대비성장률            | 전년 동기간 대비 성장률을 계산                                        | 한 기업이 월별 매출 데이터에서 전년 동월 대비 매출 성장률을 분석하고 싶은 경우                                    |
| YTD 성장률            | 연초부터 현재까지의 성장률을 계산                                     | 한 기업이 올해 연초부터 현재까지의 매출이 전년 동기 대비 얼마나 성장했는지 분석하고 싶은 경우                     |

> 사용 예시를 참고하여 실제 경우처럼 생각하며 고민해보아요 :)

## 문제 2.

```
가장 많이 주문한 사람들은 물건 배송을 빨리 받았을까요?
조건을 준수하여 아래 이미지를 만들어봆시다.
1) 국가/지역별(이하 '나라'로 통칭), 범주별로 배송일자가 다를 수 있으니 먼저, 나라별/범주별로 평균 배송일자를 설정한 뒤,
2) 각 나라에서 가장 많이 주문한 사람의 이름을 첫 번째 열,
3) 그 사람이 주문한 제품 이름을 2번째 열,
4) 각 상품이 배송까지 걸린 날 수를 표현하고
5) 그리고 만약 배송이 각 나라/범주별 평균보다 빨랐다면 '빠름', 같다면 '평균', 느리다면 '느림' 으로 print 해주세요. 
```

![이미지주소](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/2nd%20study/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-08-13%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2010.12.36.png?raw=true)

<!-- 여기까지 오는 과정 중 알게 된 점을 기입하고, 결과는 시트 명을 본인 이름으로 바꾸어 표시해주세요.-->

> 규석 결과

  ![image](https://github.com/user-attachments/assets/b099c261-c72c-4780-844e-4b89c76ff0f2)


## 문제 3.

```
채원이는 태블로를 쓰실 수 없는 상사분께 보고하기 위한 대시보드를 만들고 싶어요. 

제품 중분류별로 구분하되 매개변수로써 수익, 매출, 수량을 입력하면 저절로 각각 지표에 해당하는 그래프로 바뀌도록 설계하고자 해요.

 어떤 값이 각 지표의 평균보다 낮은 값을 갖고 있다면 색깔을 주황색으로, 그것보다 높다면 파란색으로 표시하고 싶어요. 그 평균값은 각 지표별로 달라야 해요.
```
