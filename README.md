# H&M-Customer-Prediction
* 프로젝트 주제: H&M 고객 이탈 예측 분석
* 프로젝트 목적: 고객 이탈 예측 하여 충성 고객 증대 위한 방법 제시 - 고객 이탈 예측을 통해 기업의 고객 유출 예측 하고 고객 생애 가치(CLV) 증대 마케팅 전략 제시
* 프로젝트 기간: 2023.09 - 2023.10

# 데이터 소개
![image](https://github.com/forkgmltnr/HM-Customer-Prediction/assets/61262393/930615f9-1660-4856-b916-011110bc2692)
* 2018년 9월부터 2020년 9월까지 H&M 기업 온라인& 오프라인 매장 데이터 대략 2400만 개 row존재(sample_submission 딥러닝 이미지 데이터 제외)

# 고객 구매 이력 추가(purchase_diff)
![image](https://github.com/forkgmltnr/HM-Customer-Prediction/assets/61262393/8b8aa612-4036-4a8b-ac08-470acb8dff6e)
* 고객의 이탈 기준 정립하기 위해 H&M 고객 구매 일자 데이터와 고객 고유 번호 데이터 사용하여 고객 구매 이력 데이터 추가하여 기존 데이터의 고객 이탈 비율 확인 
* puchase_diff 컬럼은 고객 구매 이력 데이터


# 고객 구매 이력 데이터 기준 정립
![image](https://github.com/forkgmltnr/HM-Customer-Prediction/assets/61262393/18a1884b-7254-4657-a28f-f7e016bc56f1)
* 위에서 추가한 고객 구매 이력 데이터를 boxplot 사용하여 고객의 구매 주기를 등급화
* 1일 이상 118일 이하 -> 이탈도1(Very Good) 긍정
* 119일 이상 238일 이하 -> 이탈도2(Fine) 보통
* 239일 이상 365일 이하 -> 이탈도3(Danger) 위험
* 365일 이상 -> 이탈도 4(Leave) 고위


# 구매 이력 분포 확인
![image](https://github.com/forkgmltnr/HM-Customer-Prediction/assets/61262393/02e5f4c5-3930-4e7a-a8b1-c4e6ea558177)
* 총 이용 고객 데이터 1236431개(123만)
* 긍정 지표 Very Good& Fine 비율 51.7% 차지
* 부정 지표 Danger& Leave 비율 47.4% 차지


# 고객 이탈 예측에 사용할 데이터프레임 재구성
![image](https://github.com/forkgmltnr/HM-Customer-Prediction/assets/61262393/8913df6c-bd16-407f-9565-54168815f960)
* 월 별 구매 횟수 추가
 * 각 고객의 월별 구매 횟수 카운트하여 고객 이탈 예측에 사용할 입력 데이터 추가
* 
