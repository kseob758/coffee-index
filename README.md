# 커피 지수(coffee index)
<br>
<p align="center">
  <img src="https://github.com/kseob758/coffee-index/assets/125840318/bfac0a85-1af2-4fdc-a4c8-522db8a711dc" width=850>
</p>

### 주제
- 서울시 카페 프랜차이즈 매장 수를 이용하여 경제 지표 만들기
- 카페 매장의 분포만으로도 서울 “지역(구)별 구매력”을 평가, 비교 가능
- 각 지역(구)의 물가수준을 간접적으로 가늠해볼 수 있는 수단
<br>

### 브랜드 선정
- 2023년 01월 커피전문점 프랜차이즈 브랜드평판 상위 기준으로 브랜드 선정
- 가격 내림차순으로 정렬

| 브랜드 | 아메리카노 가격 <br>(원/ml) |
|:---:|:---:|
| 커피빈 | 14.08 |
| 폴바셋 | 13.05 |
| 할리스 | 12.71 |
| 스타벅스<br>투썸플레이스<br>엔제리너스 | 12.67 |
| 파스쿠찌 | 11.68 |
| 이디야 | 8.33 |
| 빽다방 | 3.75 |
| 메가커피<br> 컴포즈커피 | 2.64 |
<br>

### 데이터 수집
- 카페 매장 데이터 각 브랜드별로 BeautifulSoup, Selenium 등을 사용하여 수집
- 서울시 경제, 인구, 사업체 등은 KOSIS에서 수집
  - 커피지수와의 상관분석, 회귀분석 등에 활용
<br>

### 두 가지 커피지수 설정
지수 설정시 중점 고려사항 : **단순히 총 매장의 개수가 많고 적음에 영향을 받지 않을 것**
1. **빅맥지수** 관점
- 빅맥지수(각 나라의 빅맥 가격을 미국 가격으로 나눈 것)에서 아이디어 발굴
- $커피지수1 = {지역구별\ 평균\ 1ml당\ 단가\over 전체\ 평균\ 1ml당\ 단가\}$
2. 자치구별 **브랜드 비율** 관점
- 브랜드별로 가격 편차가 크고, 각 브랜드별로 차지하고 있는 매장 비율이 다른 부분을 생각
- $커피지수2 =\ \sum{{해당\ 브랜드\ 매장 수\over 지역구별\ 전체\ 브랜드\ 매장수} \times 해당\ 브랜드\ 가중치}$
- 가중치는 원/ml를 기준으로 중위값이 1이 되도록 조정
<br>

### 자치구별 데이터 분석 및 두 커피지수 비교
- 총 부가가치
- 유동인구 및 생활인구
- 사업체 수 및 종사자 수
- 재정자립도
- 대규모 점포 수
- 공시지가
- 커피지수와의 상관관계
- 기타 분석
<br>

### 회귀 분석을 통한 최종 커피지수 선정
- 각 커피지수와 재정자립도, 총부가가치의 회귀분석
- 더 높은 설명력을 가지는 지수1을 최종 지수로 선정
- 유의한 설명력 : 약 66.9%
<br>

### 참고 사항
- [버거 지수](http://openlook.org/wp/does-lotteria-locate-different/)
- [스타벅스 지수](https://www.finder.com/starbucks-index)
- [빅맥 지수](https://ko.wikipedia.org/wiki/%EB%B9%85%EB%A7%A5_%EC%A7%80%EC%88%98)
