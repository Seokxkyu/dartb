# Third Study Week

- 20강: [파이와 도넛차트](#20강-파이와-도넛차트)

- 21강: [워드와 버블차트](#21강-워드와-버블차트)

- 22강: [이중축과 결합축](#22강-이중축과-결합축)

- 23강: [분산형 차트](#23강-분산형-차트)

- 24강: [히스토그램](#24강-히스토그램)

- 25강: [박스플롯](#25강-박스플롯)

- 26강: [영역차트](#26강-영역차트)

- 27강: [간트차트](#27강-간트차트)

- 28강: [필터](#28강-필터)

- 29강: [그룹](#29강-그룹)


- 문제1 : [문제1](#문제1)

- 문제2 : [문제2](#문제2)

- 참고자료 : [참고자료](#참고-자료)



## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://youtu.be/3ovkUe-TP1w?si=CRjj99Qm300unSWt)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=Qcl4l6p-gHM)      |
| 30~39강      | 🍽️      | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)       |
| 40~49강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 50~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |


<!-- 여기까진 그대로 둬 주세요-->
<!-- 이 안에 들어오는 텍스트는 주석입니다. -->

# Third Study Week

## 20강: 파이와 도넛차트
<!-- 파이와 도넛차트에 관해 배우게 된 점을 적어주세요 -->
 **파이차트**
 - 전체에 대한 비율 표시할 때 주로 사용
 - 표현 방식에서 파이차트 선택하고, 레이블 퀵 테이블 계산에서 구성 비율 선택하면 효과적
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-1.png)

> **🧞‍♀️ 도넛차트를 생성하는 법을 기록해주세요.**
> - **이중축 활용하기**
> - 기존의 파이차트에 작은 원을 하나 더 그려서 올려주는 방식
> - 열 선반 더블 클릭하여 '0' 입력하면 임의의 축 생성
> - 복사된 파이차트에서 기존의 레이블 및 마크 제거 
> - 마크의 크기 조정하여 양쪽 파이차트 크기 다르게 설정하고, 두 개의 분리된 파이차트 완성하고 이중축 설정

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-2.png)

## 21강: 워드와 버블차트
<!-- 워드와 버블차트에 관해 배우게 된 점을 적어주세요 -->
**버블차트**
- 수치적 데이터를 원의 크기로 표현하는 차트
- Ctrl키 누르고 국가/지역, 매출 필드 선택한 뒤, 표현 방식으로 버블차트 설정
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-3.png)

**워드 클라우드**
- 문서 내에서 등장하는 키워드가 얼마나 자주 등장하는지를 텍스트 크기로 표현하여 직관적으로 시각화할 수 있는 차트
- 국가/지역 필드 우클릭하여 크기 마크로 드래그 (카운트)
- 국가/지역 필드 레이블 마크로 드래그
- 마크에서 텍스트로 변경 
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-4.png)

## 22강: 이중축과 결합축
<!-- 이중축과 결합축에 관해 배우게 된 점을 적어주세요 -->
**이중축**
- 하나의 뷰어 안에서 축을 이중으로 사용하는 차트
- 마크를 각각에 축에 개별적으로 적용 가능
- 필드에 각각의 마크 창 있기 때문에 독립적으로 마크 수정 가능
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-5.png)

**결합축**
- 하나의 축을 공유하는 차트
- 축을 공유하는 측정값을 필요에 따라 추가할 수 있음
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-6.png)

## 23강: 분산형 차트
<!-- 분산형 차트에 관해 배우게 된 점을 적어주세요 -->
**분산형 차트**
- 파라미터 간의 상관관계 파악하는데 유용한 그래프
- 분석탭에서 추세선 분석을 통해 분포에 대한 추세 직선 그래프로 표현 가능
- 마크에서 색상 통해 해당 변수 표시할 수 있고, **세부정보** 활용하여 조정
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-7.png)

## 24강: 히스토그램
<!-- 히스토그램에 관해 배우게 된 점을 적어주세요 -->
**히스토그램**
- 분포 형태를 표시하는 차트
- **연속형** 측정값을 범위, 구간 차원으로 그룹화한다는 점에서 막대 그래프와 차이
- 차원 필드 없이, 측정값만으로 그래프 그릴 때 주로 사용하는 표현 방식
- 막대와 막대 사이 붙어있음

**생성 방법 1**
- 매출 필드 우클릭하여 `만들기` 통해서 구간 임의로 생성
- 생성된 매출(구간 차원) 필드 열 선반으로 드래그, 연속형으로 변경
- 매출 필드 행 선반으로 드래그
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-8.png)

**생성 방법 2**
- 구간 임의로 생성하지 않고, 표현방식 히스토그램으로 설정하여 생성
- 열 선반으로 드래그한 수익 필드 연속형 `구간 차원`으로 변경, 행 선반에 카운트(수익) 필드 생성
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image-9.png)

## 25강: 박스플롯
<!-- 박스플롯에 관해 배우게 된 점을 적어주세요 -->
**박스 플롯**
- 데이터의 분포 파악하는데 사용하는 그래프 
- 분포와 이상치 등을 한눈에 볼 수 있다는 장점 (1,2,3분위 수, 바깥울타리, 안쪽울타리)
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image10.png)

> **IQR**(Q3-Q1): 분포의 퍼짐을 표현하는 지표
> 울타리 범위 밖의 값: 이상치, 아웃라이어

- 표현 방식으로 `박스 플롯` 선택
- 고객별 매출로 시각화하기 위해서 고객 이름을 마크의 세부정보로 드래그
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image11.png)



## 26강: 영역차트
<!-- 영역차트에 관해 배우게 된 점을 적어주세요 -->
**영역차트**
- 영역과 축 사이의 공간이 색상으로 채워진 라인차트
- 연속형 데이터의 누계를 표현하는 데 사용
- 세그먼트 별 누계 매출 확인하기 위해 색상 마크에 세그먼트 드래그 하고, 표현방식 연속형 영역차트로 변경
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image12.png)


## 27강: 간트차트
<!-- 간트차트에 관해 배우게 된 점을 적어주세요 -->
**간트차트**
- 시간 경과에 따른 기간 시각화하는데 사용
- 제품 범주별 배송 기간을 배송 형태로 구분해서 간트차트로 시각화
- `분석`탭의 `계산된 필드 만들기` 사용하여 배송기간 필드 생성
- 마크 창에서 표현 방식 `간트 차트`로 변경
- 마크 창의 배송기간 필드 우클릭하여 측정값 `합계`에서 `평균`으로 변경
` 고객 이름 필드 필터로 가져와 특정 고객 데이터 필터링
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image13.png)


## 28강: 필터
<!-- 필터에 관해 배우게 된 점을 적어주세요 -->
**필터**
- 뷰, 쿼리 속도, 데이터 용량 측면에서 필터 핸들링에 따라 성능 차이 많이 나기 떄문에 필터링 중요
- 태블로는 `추출`, `데이터원본`, `컨텍스트`, `차원`, `측정값`, `필터` 순으로 동작

1. **데이터 원본 필터**
- 작업을 위한 데이터 중 일부만 워크 스페이스에 불러올 떄 사용
2. **컨텍스트 필터**
- 필터 중 상위 필터
- 태블로는 각 필터가 다른 필터에 관계 없이 모든 행에 액세스하도록 작동하는데, 컨텍스트 필터 지정하면 다른 필터가 컨텍스트 필터에 종속되어 작동
- 필드 색상 회색으로 변경되고, 필터 선반 맨 위에 정렬
- **기술 범주의 매출 상위 10개 항목 파악하는 법**
    - `범주`필터 컨텍스트에 추가
    - `매출 상위` 필터가 `범주`필터에 종속적으로 적용
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image14.png)

3. **차원 필터**
- `와일드카드`: 해당 단어를 포함하는 필드, 일정 문자나 숫자로 시작하고 끝나는 필드, 일치하는 필드 선택 
- `조건`: 필드에 조건을 걸어 데이터 가져올 수 있는데, 필드명과 필터링할 측정값 선택하고, 부호 조건 선택
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image15.png)


## 29강: 그룹
<!-- 그룹에 관해 배우게 된 점을 적어주세요 -->
> 데이터를 표시하는 방법에는 `그룹`, `계층`, `집합`이 있음

**그룹 생성 1**
- 뷰에서 그룹을 만드는 방법
- 뷰에서 해당 회사 제품 드래그하면 해당 제품들 선택, 우클릭하여 `그룹` 선택하면, 데이터필드에 그룹 생성
- 자동으로 마크 카드에 `제품 이름` 필드 놓여져 그룹이 색상으로 구분

**그룹 생성2**
- 항목별로 묶을 필드를 선택해 만드는 방법
- `제품 이름` 클릭에서 마우스 우클릭해 `만들기`, `그룹` 선택
- 기존 열 선반의 제품이름 필드를 생성된 `그룹` 제품이름 필드로 변경
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image16.png)

## 문제 1.

```js
유정이는 superstore 데이터셋에서 '주문' 테이블을 보고 있습니다.
1) 국가/지역 - 시/도- 도시 의 계층을 생성했습니다. 계층 이름은 '위치'로 설정하겠습니다.
2) 날짜의 데이터 타입을 '날짜'로 바꾸었습니다.

코로나 시기의 도시별 매출 top10을 확인하고자
1) 배송 날짜가 코로나시기인 2021년, 2022년에 해당하는 데이터를 필터링했고
2) 위치 계층을 행으로 설정해 펼쳐두었습니다.
이때, 매출의 합계가 TOP 10인 도시들만을 보았습니다.
```

![image-2.png](https://github.com/yousrchive/tableau/blob/main/study/img/1st%20study/image-4.png?raw=true)

```
겉보기에는 전체 10개로, 잘 나온 결과처럼 보입니다. 그러나 유정이는 치명적인 실수를 저질렀습니다.
오늘 배운 '컨텍스트 필터'의 내용을 고려하여 올바른 풀이 및 결과를 구해주세요.
```

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image17.png)

```
유정아 내가 알려줄게, 2021년과 2022년에 해당하는 데이터에 대한 필터링이 매출 합계 TOP 10 조건 필터링보다 우선하여 종속 적용되어야 하므로, 배송년도 필터를 컨텍스트 필터로 지정해야 하면 문제를 해결할 수 있을 것 같아. 
```
<!-- DArt-B superstore가 아닌 개인 superstore 파일을 사용했다면 값이 다르게 표시될 수 있습니다.-->

## 문제 2.

```js
태영이는 관심이 있는 제품사들이 있습니다. '제품 이름' 필드에서 '삼성'으로 시작하는 제품들을 'Samsung group'으로, 'Apple'으로 시작하는 제품들을 'Apple group'으로, 'Canon'으로 시작하는 제품들을 'Canon group'으로, 'HP'로 시작하는 제품들을 'HP group', 'Logitech'으로 시작하는 제품들을 'Logitech group'으로 그룹화해서 보려고 합니다. 나머지는 기타로 설정해주세요. 이 그룹화를 명명하는 필드는 'Product Name Group'으로 설정해주세요.

(이때, 드래그보다는 멤버 찾기 > 시작 문자 설정하여 모두 찾아 한번에 그룹화해 확인해보세요.)
```

![group](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/3rd%20study/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-09-18%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.33.47.png?raw=true)

```js
해당 그룹별로 어떤 국가/지역이 주문을 많이 차지하는지를 보고자 합니다. 매출액보다는 주문량을 보고 싶으므로, 주문Id의 카운트로 계산하겠습니다.

기타를 제외하고 지정한 5개의 그룹 하위 목들만을 이용해 아래와 같이 지역별 누적 막대그래프를 그려봐주세요.
```

![image](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/3rd%20study/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-09-18%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.37.55.png?raw=true)


![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/image18.png)

```
태영아 내가 알려줄게, 기업 별 주문량을 막대 그래프로 표현하고 싶고, 특히 각 기업의 국가별 주문량을 색상으로 표시하고 싶다면 아래 순서를 따르면 돼.
1. 생성된 Product Group Name 필드를 필터 선반으로 가져와 기타를 제외한 나머지 5개 그룹을 필터링 해
2. 카운트(주문) 필드를 열 선반으로 드래그 하고, Product Group Name 필드를 행 선반으로 드래그 해
3. 국가 별 주문량을 확인하기 위하여 국가/지역 필드를 마크 창의 색상으로 드래그 해
완성이야~
```