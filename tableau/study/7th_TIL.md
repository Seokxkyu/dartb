# 7th Study Week

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
| 7    | 58~66강     | ✅             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)    |
| 8    | 67~77강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)    |
| 9    | 78~85강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)     |
---

<br/>

> **🧞‍♀️ 오늘은 강의보다 실습과 대시보드 직접 만들기가 더 중요하니, 기록보다는 사고하며 강의를 들어주세요.**

## 58. 집합값 변경

<!-- 집합값 변경 강의에서 알게 된 점을 적어주세요 -->
[하위범주 막대그래프]에 하위범주 클릭하고 [도구] 설명에 옵션 클릭하면 다른 대시보드로 이동 가능 구현

- 새로운 대시보드에 세로 컨테이너, 빈 페이지, `제품 막대그래프` 배치
- [대시보드]에 [동작] 클릭 후, [동작 추가]에 [집합 값 변경] 선택
- [대상 집합]에 [해당 집합] 선택
- [동작 실행 결과]에 [집합에 값 할당] 선택, [집합에서 모든 값 제거] 선택
- [집합 값 변경 동작] 추가하고, 대상 집합에 [제조 업체 집합] 선택

## 59. 스토리패널

<!-- 스토리패널 강의에서 알게 된 점을 적어주세요 -->
- 왼쪽의 스토리 패널과 오른쪽의 스토리 워크시트 페이지로 구성
```
스토리 워크시트 페이지: 각 시트를 추가함으로써 스토리 포인트 생성 가능 공간
스토리 포인트: 스토리 각각의 개별 시트
스토리 패널: 대시보드, 시트 및 텍스트 설명을 스토리 시트로 가져올 수 있음
스토리 툴바: 변경된 내용 되돌리기, 스토리 포인트에 대한 업데이트 적용, 삭제, 생성 가능
```
- [빈 페이지] 선택하여 새 스토리 포인트 추가
- [복제] 선택하여 현재 스토리 포인트를 다음 스토리 포인트의 시작점으로 사용 가능
- 스토리 툴바의 [새 이름으로 저장] 통해 현재까지 작업을 시작지점으로 지정하여 작업 진행 가능

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/71.png)

## 60. 스토리

<!-- 알게 된 점을 적고, 아래 질문에 답해보세요 :) -->
### 스토리
> 생성한 워크시트와 대시보드에 설명을 덧붙여 데이터를 설명하거나 정보를 전달하고, 의사결정에 도움을 주고 설득력 있는 사례를 구성하는 등의 기능을 구현하는 작업 가능

- 전체적으로 살펴보면 매출은 문제가 없으나, 수익이 적자가 발생하는 항목을 찾아내고, 그 항목 중에서 어떤 제품이 문제가 되는지 찾아내어 해결 방안을 생각할 수 있는 스토리

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/71.png)

## 61. 대시보드 탐색

<!-- 대시보드 탐색 강의에서 알게 된 점을 적어주세요 -->

### 탐색 버튼 활성화 하는 방법
- `막대 그래프 대시보드` 선택 후 [라인 차트 탐색] 버튼 더블 클릭
- `이동할 위치` [라인 차트 대시보드] 선택 후 [확인] 클릭
- 탐색 버튼 활성화되어 지정한 색상으로 변경 

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/72.png)

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/73.png)

## 62. 태블로 단추

<!-- 태블로 단추 강의에서 알게 된 점을 적어주세요 -->
- 그래프 선택 후 [기타옵션] 클릭
- [표시/숨기기 단추 추가] 선택하면, 부동의 형태로 X자 표시 단추 생성
- Alt 누른 상태로 X자 표시 단추 클릭하면, 해당 그래프 사라짐
- 부동 상태의 그래프 표시/숨기기 단추를 우클릭, [기타옵션] 클릭하여 부동 해제
- 부동 해제된 [표시/숨기기] 단추를 그래프 텍스트 오른쪽으로 이동

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/74.png)

- [표시/숨기기] 단추 선택한 뒤, 기타옵션 클릭하여 [편집단추] 클릭
- [표시하거나 숨길 대시보드 항목]으로 표시/숨기기 기능 적용시킬 항목 선택 가능
- 서식 변경 가능

![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/75.png)

## 63. 막대그래프 드릴다운

<!-- 막대그래프 드릴다운에 대해 알게 된 점을 적어주세요 -->

- 매개변수 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/76.png)
- 계산된 필드 (드릴다운) 생성
- [배송형태]가 [매개변수 Level 1]과 일치할 경우 [범주]로 드릴다운되고, 그렇지 않을 경우 [배송형태]로 돌아오는 필드
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/77.png)
- 매개변수 동작 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/78.png)

### 결과
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/79.png)


## 64. 트리맵 드릴다운

<!-- 트리맵 드릴다운에 대해 알게 된 점을 적어주세요 -->
- 트리맵에 드릴다운 구현하기 위해 집합 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/80.png)
- 계산된 필드 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/81.png)
- 워크시트 동작 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/82.png)

### 결과
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/83.png)


## 65. 파이 차트 드릴다운

<!-- 파이 차트 드릴다운에 대해 알게 된 점을 적어주세요 -->
- 드릴다운 구현하기 위한 집합 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/84.png)
- 계산된 필드 신규 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/85.png)
- [워크시트]에서 [동작] 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/86.png)

### 결과
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/87.png)


## 66. 지도 드릴다운

<!-- 지도 드릴다운에 대해 알게 된 점을 적어주세요 -->
- 생성된 [국가/지역] 집합에 대한 계산된 필드 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/88.png)
- [워크시트]에서 [동작] 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/89.png)
- 필터링을 위한 매개변수 생성
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/91.png)
- [매개변수 국가/지역]에 따라 True나 False 반환하는 계산된 필드 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/92.png)
- [워크시트]에서 [동작] 추가
    ![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/93.png)

### 결과
![images](https://github.com/Seokxkyu/dartb/blob/main/tableau/study/images/90.png)