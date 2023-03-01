# 제주도 도로 교통량 예측 AI 경진대회

![image](https://user-images.githubusercontent.com/114792430/222132514-a107d781-ae90-4db9-bf90-8c196a890742.png)

## Task

제주도 교통 정보로부터 target(평균 속도)를 예측하는 **Regression** task

## Dataset

* target(평균 속도)를 포함하여 22개의 feature로 구성
* 4,701,217개의 train data와 291,241개의 test data

변수명|변수|설명|
--|--|--|
0|   id|   아이디|
1|   base_date|날짜|
2|   day_of_week|   요일|
3|   base_hour|   시간대|
4|   lane_count|   차로수|
5|   road_rating|   도로등급|
6|   multi_linked|   중용구간 여부|
7|   connect_code|   연결로 코드|
8|   maximum_speed_limit|   최고속도제한|
9|   weight_restricted|   통과제한하중|
10|   height_restricted|   통과제한높이|
11|   road_type|   도로유형|
12|   start_latitude|   시작지점의 위도|
13|   start_longitude|   시작지점의 경도|
14|   start_turn_restricted|   시작 지점의 회전제한 유무|
15|   end_latitude|   도착지점의 위도|
16|   end_longitude|   도착지점의 경도|
17|   end_turn_restricted|   도작지점의 회전제한 유무|
18|   road_name|   도로명|
19|   start_node_name|   시작지점명|
20|   end_node_name|   도착지점명|
21|   vehicle_restricted|   통과제한차량|
22|   target|   평균속도(km)|

## 주요 전처리 point
* base_date를 이용한 파생변수 생성
* 관광객 수, 공휴일 여부 등 외부 데이터를 이용한 파생변수 생성
* 위도, 경도 데이터를 활용한 지리정보 파생변수 생성
* test data에는 존재하지 않는 이상치 처리
* 0/1 비율이 한쪽으로 치중된 변수의 처리

## model
Randomforest, LGBMRegressor, XGBRegressor 등 boosting model
