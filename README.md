# coffee index - README 계속 수정 필요
### 주제
커피 지수를 통해 어느 지역구의 구매력이 대한민국 전국 평균에 비해 저평가되었는지, 
고평가되었는지 등의 적정성을 평가할 때 유용한 지표가 될 수 있으며, 
커피만으로도 각 지역의 물가수준을 간접적으로 가늠해볼 수 있는 수단이 될 수 있다.
카페 프랜차이즈 매장 수를 이용하여 일종의 경제 지표 설정
서울 “지역별 구매력” 평가를 비교할 수 있는 경제 지표로 만들어 보면 어떨까? 

평균 커피 단가가 높다는 건 그만큼 경제력이 있는 사람들이 그 커피를 마시기 때문에 높은 단가가 유지 되는 것은 아닐까? 하는 관점
1. 빅맥지수 관점
2. 자치구별 브랜드 비율 관점
<aside>
🍔 **빅맥지수 ?**

$빅맥지수 = {각\ 나라의\ 빅맥가격 \over 미국의\ 빅맥가격}$

전세계 맥도날드 빅맥 가격 비교를 통한 각국 통화 가치 및 물가 수준 분석을 위한 지수

</aside>

### 브랜드 선정
- 브랜드평판 top10 + 엔제리너스(지역별 편차 감안)
순위|	|브랜드 명|	|1ml 당 원 
|(소수점 3 번째 자리에서 버림)|
1	커피빈	14.08원
2	폴바셋	13.05원
3	할리스	12.71원
4	스타벅스, 투썸플레이스, 
엔제리너스	12.67원
5	파스쿠찌	11.68원
6	이디야	8.33원
7	빽다방	3.75원
8	메가커피, 컴포즈커피	2.64원
### 데이터 수집
- 카페 매장은 각 카페별로, 기타 서울시 경제, 인구, 사업체 등은 KOSIS에서 수집
### 각종 시각화
- 많은 그래프, 차트 등
### 커피지수 도출
- 2개의 후보 중에서 최종 선정
- 커피지수와 재정자립도, 커피지수와 총부가가치의 회귀분석을 통해 1번 후보를 최종 지수로 선정
- 유의한 설명력을 가진 것으로 판단
