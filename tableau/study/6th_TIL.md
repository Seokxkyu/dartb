# Sixth Study Week


## Study Schedule
<br>

| 회차 | 강의 범위   | 강의 이수 여부 | 링크                                                                                                     |
|------|-------------|----------------|--------------------------------------------------------------------------------------------------------|
| 1    | 1~7강       | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)    |
| 2    | 8~17강      | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)    |
| 3    | 18~27강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)    |
| 4    | 28~37강     | ✅              | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)    |
| 5    | 38~47강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)    |
| 6    | 48~57강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)    |
| 7    | 58~67강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)    |
| 8    | 68~77강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)    |
| 9    | 78~85강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)     |
---

<br/>
<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘은 강의보다 실습과 대시보드 직접 만들기가 더 중요하니, 기록보다는 사고하며 강의를 들어주세요.**

## 48. 워크시트 서식(2)

<!-- 워크시트에 관해 본 강의에서 알게 된 점을 적어주세요 -->
- **테두리 서식** : 뷰에서 테이블, 패널, 셀 및 머리글을 둘러싸는 라인의 서식 설정
- **라인 서식** : 뷰에서 표시된 데이터의 축에 대한 라인의 모양 설정

> 테두리 서식의 행 구분선에서 행 수준에 따른 테두리 색상, 두께 설정 가능

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/61.png)
    
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/62.png)


> 라인 서식을 통해 분석 탭의 참조선 및 추세선의 색상, 두께 설정 가능하고, 생성된 그래프의 격자선, 0 기준선 설정 

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/63.png)

## 49강. 대시보드패널

<!-- 대시보드패널 강의에서 알게 된 점을 적어주세요. -->
### 대시보드 개체 추가
- **웹페이지 URL**
- **이미지 파일 및 경로**
- **텍스트**
- **시트** 

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/64.png)

## 50. 대시보드 구성방식

<!-- 알게 된 점을 적고, 아래 질문에 답해보세요 :) -->

> **🧞‍♀️ 부동과 바둑판식 방식을 차이를 중점으로 기술해보세요**
- **바둑판식** : 격자무늬 구조에 따라 개체 구성

    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/65.png)

- **부동** : 개체 자유롭게 배치할 수 있으며, 사용자가 원하는대로 개체를 Drag and Drop 하여 배치

    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/66.png)

> 대시보드 크기가 자주 변경되는 경우에 개체 추가하면, 바둑판식 사용 (개체가 유사한 형식 유지)

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/67.png)

> 부동 개체는 대시보드 크기가 자주 변경되지 않는 경우에 사용하는 것이 적합

## 51. 대시보드 컨테이너
### 컨테이너
- 대시보드 객체들과 워크시트들을 그룹화하고 구성할 수 있는 공간

### 종류
- **가로 컨테이너**: 내부의 개체들을 수평 공간으로 배열할 때 사용
- **세로 컨테이너**: 내부의 개체들을 수직 공간으로 배열할 때 사용

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/68.png)


## 52. 레이아웃 패널
### 레이아웃 탭
- 대시보드의 개체 속성 변경 가능
- `부동` 옵션 해제하면 본래 자리로 돌아가지 않으니 주의
- `위치와 크기` 옵션을 통해 개체의 위치와 크기를 픽셀 단위로 변경 가능

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/69.png)

- 테두리 옵션은 개체 테두리의 선 유형, 두께 및 색상 변경 가능
- `바깥쪽 여백` 옵션에서는 컨테이너의 모서리와 테두리 사이의 공간 변경 가능
- `안쪽 여백` 옵션에서는 선택된 개체 모서리와 테두리 사이의 공간 변경 가능

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/610.png)

### 항목 계층
- 대시보드에 있는 컨테이너와 개체 볼 수 있음
- `항목계층`에서 개체 클릭하면 대시보드에서는 선택된 개체 확인 가능

## 53. 필터 동작

<!-- 필터 동작에 대해 알게 된 점을 적어주세요 -->

## 54. 대시보드 하이라이터 동작

<!-- 하이라이터에 대해 알게 된 점을 적어주세요 -->


## 55. 대시보드 URL

<!-- URL에 대해 알게 된 점을 적어주세요 -->


## 56. 대시보드 시트에 이동 동작

<!-- 대시보드 시트에 이동에 대해 알게 된 점을 적어주세요!-->

## 57. 매개변수 변경 동작

<!-- 매개변수 변경 동작에 대해 알게 된 점을 적어주세요!-->

## 문제

오늘은 별도의 문제가 없습니다. 

![1](../study/img/3rd%20study/1688556627184.png)

![1](../study/img/3rd%20study/Global%20SuperStore%20Dashboard.png)

![2](../study/img/3rd%20study/images.jpeg)
![2](../study/img/3rd%20study/maxresdefault.jpg)

여러 대시보드를 참고하시어, superstore 데이터를 사용해 나만의 대시보드를 제작해주세요.

**단, 워크시트 3개 이상의 그래프를 표시해야 하며 각 시트 간 상호작용성 필터 or 하이라이트 동작은 꼭 추가되어야 합니다**

어떤 부분에 가중을 두었는지, 어떤 사용자 편의성을 고려하였는지에 대한 설명이 필요합니다.