코로나 백신과 영화 산업 상관관계 분석 및 시각화



주제 선정 이유

코로나 백신 접종이 시작됨에 따라 백신이 영화 산업에 미치는 영향 분석

프로젝트 개요

지역에 따라 백신 접종이 영화산업에 미치는 영향을 파악하기 위해 제 1도시(서울)와제 2도시(부산)의 데이터 분석 및 비교

프로젝트 기간 

2021.08.02~2021.08.24



프로젝트 진행 과정

(데이터 수집 --> 데이터 전처리 --> 데이터 시각화 -->  결론 및 한계점 )

<img src="https://raw.githubusercontent.com/DaeGyeongYi/03.vaccine_movie_project/main/picture/image-20210821152742009.png" alt="img"  />



1. 데이터 수집

​		(1)  KOBIS 데이터 수집

			- 데이터 명 : 지역별 영화 접유율
			- 제공 형태 : EXCEL 파일
			- 데이터 요약 : 지역별, 매출액, 관객수
			- 특이 사항 : Selenium을 통한 데이터 수집 자동화

​		![image-20220307160903735](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307160903735.png) 



​		(2) 공공데이터 포털에서 오픈 API 활용

			- 데이터명 : 코로나 예방접종 통계 데이터 조회 서비스
			- 제공 형태 : 오픈 API 형태
			- 요약 : 지역명칭, 1차 및 2차 당일 통계, 누적통계

<img src="C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307160924216.png" alt="image-20220307160924216"  />

 

2. 데이터 전처리

 - 코로나 백신 접종 전/후의 매출액 결측치 처리
 - 데이터 수가 부족하여 결측치를 평균값으로 대체  

![image-20220307162016461](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307162016461.png)

​	

3. 데이터 시각화

   (1) 코로나 백신 접종자 수 및 관객수 현황

   <img src="C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307162559797.png" alt="image-20220307162559797" style="zoom:150%;" />

   

   	(2) 서울 및 부산 2019년 대비 코로나 이후 매출액 비율

​			<img src="https://github.com/DaeGyeongYi/03.vaccine_movie_project/blob/main/picture/image-20210821153531255.png?raw=true" alt="image-20210821153531255.png" style="zoom:80%;" />

​		(3) 백신 접종 전/후 거리두기에 따른 매출액 비교

​		![image-20220307162843175](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307162843175.png)

​		                                                                          (서울)

​		![image-20210821152944920.png](https://github.com/DaeGyeongYi/03.vaccine_movie_project/blob/main/picture/image-20210821152944920.png?raw=true)

​		                                                                            (부산)

​		(5) 영화 매출액과 백신 접종률 종합 산점도(서울)

​			![image-20220307163151766](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307163151766.png)

​		                                                                       (서울)



​		![image-20220307163248873](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307163248873.png)

​                                                                                (부산)

​		(6) 상관계수 분석 및 시각화

![image-20220307163511568](C:\Users\82104\AppData\Roaming\Typora\typora-user-images\image-20220307163511568.png)



4. 결론 및 한계점

   (1) 결론

	- 코로나 백신과 영화 매출액에는 상관관계가 존재
	- 누적 접종률이 주간 접종률 보다 강한 상관관계를 가진다
	- 백신과 영화 매출액의 상관관계는 지역별 차이가 존재
	- 백신 접종률이 증가하면 영화 산업에 경제적 효과가 있을 것 같다

​		(2) 한계점 및 개선 방안

   - 지역별 차이에 대한 표본이 부산 한 곳이므로, 이를 명확하게 확인 할 수 없었다

      --> 서울과 부산을 제외한 타 지역의 데이터 분석이 필요하다

   - 코로나에 둔감하게 된 사람들의 심리가 반영되지 못 했다

     --> 설문 자료 및 여론조사 관련 추가 데이터 수집 필요하다

   - 거리 두기를 고려 하다 보니 계절성을 고려하고, 적절한 크기의 표본을 선정하는데 어려웠다

     --> 접종 이후의 데이터가 많아진다면 분석의 정확도를 높일 수 있을 것 같다
