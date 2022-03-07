# 코로나 백신과 영화 산업 상관관계 분석 및 시각화



### 주제 선정 이유

코로나 백신 접종이 시작됨에 따라 백신이 영화 산업에 미치는 영향 분석

### 프로젝트 개요

지역에 따라 백신 접종이 영화산업에 미치는 영향을 파악하기 위해 제 1도시(서울)와제 2도시(부산)의 데이터 분석 및 비교

### 프로젝트 기간 

2021.08.02~2021.08.24



### 프로젝트 진행 과정

(데이터 수집 --> 데이터 전처리 --> 데이터 시각화 -->  결론 및 한계점 )

<img src="https://raw.githubusercontent.com/DaeGyeongYi/03.vaccine_movie_project/main/picture/image-20210821152742009.png" alt="img"  />



1. 데이터 수집

​		(1)  KOBIS 데이터 수집

			- 데이터 명 : 지역별 영화 접유율
			- 제공 형태 : EXCEL 파일
			- 데이터 요약 : 지역별, 매출액, 관객수
			- 특이 사항 : Selenium을 통한 데이터 수집 자동화

​		![image](https://user-images.githubusercontent.com/98143525/156993442-cb90300b-d1e8-4580-b57d-aa6ff644f2fa.png) 



​		(2) 공공데이터 포털에서 오픈 API 활용

			- 데이터명 : 코로나 예방접종 통계 데이터 조회 서비스
			- 제공 형태 : 오픈 API 형태
			- 요약 : 지역명칭, 1차 및 2차 당일 통계, 누적통계

![image](https://user-images.githubusercontent.com/98143525/156993610-660dd1b7-1d0a-440d-80bb-a45af10cce32.png)

 

2. 데이터 전처리

 - 코로나 백신 접종 전/후의 매출액 결측치 처리
 - 데이터 수가 부족하여 결측치를 평균값으로 대체  

![image](https://user-images.githubusercontent.com/98143525/156993653-35855db3-a137-4359-a7ea-41a7f8dddaf8.png)

​	

3. 데이터 시각화

   (1) 코로나 백신 접종자 수 및 관객수 현황

   ![image](https://user-images.githubusercontent.com/98143525/156993770-92c0838e-3ee0-4d7f-91f3-a17c7f816b07.png)

   

   	(2) 서울 및 부산 2019년 대비 코로나 이후 매출액 비율

​			<img src="https://github.com/DaeGyeongYi/03.vaccine_movie_project/blob/main/picture/image-20210821153531255.png?raw=true" alt="image-20210821153531255.png" style="zoom:80%;" />

​		(3) 백신 접종 전/후 거리두기에 따른 매출액 비교

​		![image](https://user-images.githubusercontent.com/98143525/156993820-5f6f2b82-6d8a-41db-87f8-04bb7ee674a1.png)

​		                                                                          (서울)

​		![image-20210821152944920.png](https://github.com/DaeGyeongYi/03.vaccine_movie_project/blob/main/picture/image-20210821152944920.png?raw=true)

​		                                                                            (부산)

​		(5) 영화 매출액과 백신 접종률 종합 산점도(서울)

​			![image](https://user-images.githubusercontent.com/98143525/156993864-3d8cd3ad-e6a4-40ec-9ef3-e7a8af7333f0.png)

​		                                                                       (서울)



​		![image](https://user-images.githubusercontent.com/98143525/156993916-9d90f66b-164d-4838-a35a-e1c5f2b39548.png)

​                                                                                (부산)

​		(6) 상관계수 분석 및 시각화

![image](https://user-images.githubusercontent.com/98143525/156993963-84b0f8de-c587-4fe7-91d3-ac915e28338f.png)



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
