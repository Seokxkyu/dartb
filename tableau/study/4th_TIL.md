# Fourth Study Week

- 30강: [계층](#30-계층)

- 31강: [집합](#31-집합)

- 32강: [결합집합](#32-결합집합)

- 33강: [계산된 필드](#33-계산된-필드)

- 34강: [행수준계산](#34-행수준계산)

- 35강: [집계계산](#35-집계계산)

- 36강: [테이블계산](#36-테이블계산)

- 37강: [퀵테이블계산(1)](#37-퀵테이블계산1)

- 38강: [퀵테이블계산(2)](#38-퀵테이블계산2)

- [문제1](#문제-1)

- [문제2](#문제-2)

- [문제3](#문제-3)

## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)       |
| 30~38강      | ✅      | [링크](https://youtu.be/e6J0Ljd6h44?si=nhGbB7GsdOCqj15f)       |
| 39~49강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 50~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |

<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘의 스터디는 지니와 함께합니다.**


## 30. 계층

<!-- 계층 구조와 관련된 개념, 사용 방법 등을 적어주세요. -->
**계층**
- 뷰에서 데이터를 드릴 다운하여 값을 세부적으로 찾을 때 유용한 방법
- 위치 관련 필드를 Location으로 계층화하면, 주, 지방, 도시 순으로 데이터 활용 가능
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/계층.png)

## 31. 집합

<!-- 집합의 정의 및 활용 방법에 대해 알게 된 점을 적어주세요. -->
**집합**
- 사용자가 직접 어떤 조건을 설정하고, 그 조건을 기반으로 데이터를 구분하는 방법
- 특정 필드 위에서 우클릭하고, `만들기` 선택 `집합` 생성
- `상위` 탭 이용하면, 필드 기준 상위 n개 데이터 활용 가능
- 집합 조건 충족된 데이터 `IN`
- 남은 데이터는 `OUT`으로 묶어서 구분
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/집합.png)

## 32. 결합집합

<!-- 결합집합의 개념 및 사용 사례를 적어주세요. -->
**결합 집합**
- 두가지 조건 적용하여 집합 생성하고 싶은 경우 사용
- 각각의 조건을 먼저 생성하고 결합하여, `조건` 선택 (필요에 따라 교집합, 합집합, 차집합 선택)

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/결합집합1.png)

- 결합된 `집합` 필드의 모든 조건 동시에 적용 가능 함 (마크 탭의 색상 추가)
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/결합집합2.png)

## 33. 계산된 필드

<!-- 계산된 필드를 사용하는 방법과 예시를 적어주세요. -->
**계산된 필드**
- 데이터 원본에 있는 필드 활용하여 **새로운** 필드 만드는 기능
- 기존 데이터 이외에 계산해야 할 데이터가 추가로 필요한 경우, 직접 생성하여 사용 가능 (**함수** 기능 활용)


> **수익률(%)** 필드<br>
> = SUM(Profit) / SUM(Sales)

- 데이터 패널 통해서 생성
- `분석` 탭 활용하여 생성
- 사용하고자 하는 필드 우클릭하고, `만들기` 선택하여 `계산된 필드`

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/계산된필드.png)

## 34. 행수준계산

<!-- 행수준 계산의 의미와 적용 방법을 적어주세요. -->
1. 기본 계산
- 데이터 원본에 대한 `행 수준 계산` (각 레코드를 통한 계산), `집계 계산` (뷰에서 보이는 기준)

2. 테이블 계산

3. **LOD 표현식**
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/LOD표현식.png)

- 고객 이름 필드에서 고객 이름, 성 `SPLIT` 함수 사용하여 새로운 계산 필드 생성
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/SPLIT함수.png)

- `IF THEN ELSE` 함수 활용하여 매출이 0보다 큰 경우과 작은 경우를 분기하여 값 할당
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/IFTHENELSE함수.png)

- `DATEDIFF` 함수 활용하여 주문 일자와 배송 일자 사이 계산하여 데이터 활용 가능
- 해당 필드를 `측정값`에서 `차원`값으로 변경하여 사용 (중복된 id값으로 인한 계산 오류 방지 목적)

## 35. 집계계산

<!-- 집계계산의 정의 및 활용 사례에 대해 알게 된 점을 적어주세요. -->
**집계 계산**

- 현재 뷰에서 보이는 기준으로 계산하는 방식(필드 레벨에 따라)
- 특정 필드 우클릭 후, `기본 속성`을 `집계`로 변경
- 기본 생성된 필드의 경우, 마우스 우클릭 통해 집계 방식 변경 가능 (합계, 평균, 중앙값 등)
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/집계계산.png)


## 36. 테이블계산

<!-- 테이블 계산의 개념 및 사용 방법을 적어주세요. -->
**테이블 계산**

- 뷰에 보이는 내용 바탕으로 데이터 계산
- `계산된 필드 만들기`에서 `테이블 계산` 선택 후 새로운 `누적 매출` 필드 추가
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image19.png)
- 계산 방향 테이블 옆으로 자동 설정되어 있지만, 마우스 우클릭 `여러가지 계산 방향` 테이블 아래로 설정 가능
- `테이블 계산 편집` 옵션에서, 계산 방향 선택할 수 있고, 계산 옵션 추가 가능

- 현재 월과 전 월의 차이를 보여주는 `계산된 필드` 추가
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image20.png)
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image21.png)


## 37. 퀵테이블계산(1)

<!-- 퀵테이블 계산의 원리 및 예제에 대해 알게 된 점을 적어주세요. -->
**퀵테이블 계산**
- 뷰에서 보이는 내용을 바탕으로 데이터가 계산되어 적용되는데, 테이블 계산에서 가장 자주 쓰이는 테이블 계산 유형들을 클릭만으로 가능하도록 만들어 놓은 기능
    - **누계**: 집계한 값을 누적한 값

        ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image22.png)
    
    - **차이**: 측정값이 기준 값과 어느정도 차이가 나는지 구하는 계산 유형
    
        ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image23.png)
    
    - **비율 차이**: 측정값들 사이의 성장률 또는 % 차이를 표현
    
        ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image24.png)
    
    - **구성 비율**: 전체에서 각 항목들의 비중을 확인할 때 사용 (`다음을 사용하여 계산` 선택 후 `(패널) 아래로` 지정하면 지역별 구성 비율 확인 가능)
    
        ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image25.png)
    
    - **백분위수**: 전체에서 각 멤버들의 백분위 표시
    
        ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image26.png)


## 38. 퀵테이블계산(2)

<!-- 이동평균, YTD 총계, 전년 대비 성장률, YTD 성장률 등 본 강의에서 알게 된 점을 적어주세요. -->
**퀵테이블 계산**
- **이동평균**: 이전의 값부터 현재까지 값에 대한 평균을 낼 때 사용하며, 주식 데이터에서 많이 활용
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image27.png)

- **YTD 총계(Year to Date)**: 특정 시점을 기준으로 해당 연도부터 그 시점가지의 총계. '연도'보다 하위레벨 필드인 '분기' 또는 '월'이 있어야 사용 가능
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image28.png)

- **전년 대비 성장률**: 같은 월을 기준으로 이전 연도 대비 얼마 정도 성장했는지를 살펴보는데 활용
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image29.png)

- **YTD 성장률**
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image30.png)


## 문제 1.

규석이는 이제껏 매출을 올리는 데에 힘썼었지만, 왠지 모르게 주머니에 들어오는 돈이 없어 속상합니다. 

그래서 매출이 상위 20곳에 속하지만, 수익률(%)이 마이너스인 시/도를 확인하려고 합니다.

> 수익률은 SUM([수익]) / SUM([매출])로 정의합니다.

어떤 집합을 만들었고, 어떤 결합을 하였는지를 중심으로 기술하고, 결과 자료를 첨부해주세요. 

(텍스트 표 형태이며, 색상으로 위 집합을 구분할 수 있게 만들어주세요.)

<!-- 아래 예시 이미지를 삭제하고, 직접 만든 시트 사진을 올려주세요. 시트의 이름은 본인 이름으로 기입해주세요-->


![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image31.png)

> 풀이 방법
1. `계산된 필드 만들기` 수익률(%) 필드 생성
2. `시/도` 필드 우클릭하여, 각각 매출이 상위 20곳인 시/도 집합, 수익률이 마이너스인 시/도 집합 생성
3. 수익률이 마이너스인 시/도 집합 마크 색상 창에 드래그
4. 생성된 두 개의 집합 결합하여 매출이 상위 20곳이면서 수익률이 마이너스인 시/도 결합 집합 생성


## 문제 2.
선희는 주문 Id별로 주문에서 배송까지에 걸리는 날짜 일수가 궁금했습니다. 
그래서 주문 ID별로 주문에서 배송까지 걸리는 일자를 '배송까지 걸린 일수'라는 계산된 필드로 만들고, 이를 마크에 올린 후 확인해보았습니다. 
이때, 계산된 필드의 식은 'DATEDIFF' 함수를 이용하였습니다.

배송까지 걸린 일수 계산을 위한 DATEDIFF 함수 수식을 적어주세요.

```
DATEDIFF('day', [주문 날짜], [배송 날짜])
```

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image32.png)

그런데 위 그림처럼 '주문 날짜'와 '배송 날짜'를 함께 행에 올려 확인해보니, 주문날짜와 배송날짜의 차이가 '배송까지 걸린 일수'와 다릅니다.

ID-2021-11126을 보니, 11월 26일 배송에 11월 30일 배송이면 4일 차이인데, 12일이 걸렸다고 하네요. 왜 이런 문제가 생긴걸까요?

```
생성된 배송까지 걸린 일수 필드는 측정값이므로, 주문 Id가 중복되는 경우 잘못된 값을 반환할 수 있음
```

그리고 이를 해결하기 위해서는 어떻게 해야 할까요?

```
기존의 측정값(합계) 대신 차원값으로 변경하여 적용
```


## 문제 3.

다음은 Tableau의 다양한 계산을 사용할 수 있는 경우를 빈칸으로 두고 문제를 작성한 것입니다. 각 빈칸에 적합한 계산 유형을 채워보세요.

보기
> **누계, 차이, 비율 차이, 구성 비율, 순위, 백분위수, 이동 평균, YTD 총계, 통합 성장률, 전년 대비 성장률, YTD 성장률**

| 계산 유형               | 설명                                                                 | 사용 예시                                                                                          |
|-------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 누계           | 데이터의 누적 합계를 계산                                             | 한 기업이 월별 매출 데이터를 누적하여 연간 매출 추이를 보고 싶을 때 사용                                      |
| 차이            | 연속 데이터 포인트 간의 차이를 계산                                    | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감량을 분석하고 싶은 경우                                        |
| 비율 차이            | 연속 데이터 포인트 간의 비율 변화를 계산                               | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감률(%)을 분석하고 싶은 경우                                      |
| 구성 비율            | 전체에서 각 데이터 포인트의 비율을 계산                                | 한 기업이 전체 매출에서 각 제품군이 차지하는 비율을 보고 싶을 때 사용                                           |
| 순위            | 데이터의 순위를 매깁니다                                              | 한 기업이 제품별 매출 데이터를 순위별로 정렬하여 상위 10개 제품을 분석하고 싶은 경우                              |
| 백분위수            | 데이터의 백분위를 계산                                               | 한 기업이 고객별 구매 금액 데이터를 백분위수로 나누어 상위 25% 고객을 분석하고 싶은 경우                          |
| 이동 평균            | 일정 기간의 평균을 계산                                               | 한 기업이 주간 매출 데이터에서 4주 이동 평균을 계산하여 트렌드를 분석하고 싶은 경우                              |
| YTD 총계            | 연초부터 현재까지의 총계를 계산                                      | 한 기업이 월별 매출 데이터를 연초부터 현재까지 누적하여 연간 매출 목표 달성 여부를 분석하고 싶은 경우             |
| 통합 성장률            | 일정 기간 동안의 연평균 성장률을 계산                                  | 한 기업이 5년 간 매출 데이터를 바탕으로 연평균 성장률(CAGR)을 계산하고 싶은 경우                                  |
| 전년 대비 성장률            | 전년 동기간 대비 성장률을 계산                                        | 한 기업이 월별 매출 데이터에서 전년 동월 대비 매출 성장률을 분석하고 싶은 경우                                    |
| YTD 성장률            | 연초부터 현재까지의 성장률을 계산                                     | 한 기업이 올해 연초부터 현재까지의 매출이 전년 동기 대비 얼마나 성장했는지 분석하고 싶은 경우                     |

> 사용 예시를 참고하여 실제 경우처럼 생각하며 고민해보아요!
