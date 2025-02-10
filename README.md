# 제 1회 산학연계 공모전
## 매니저 매칭 여부 예측 AI 개발
<br/>

## Overview
![산학연계 img1](https://github.com/user-attachments/assets/b480cbb5-aebe-4484-b502-56155fc49a98)

## 1. 배경 & 목적

- 고객 밀착형 서비스의 특성상 고객의 서비스 요청에 적합한 서비스 제공자 즉, 매니저를 매칭하는 것은 고객 만족도뿐만 아니라 비즈니스 모델의 성공을 위한 중요한 과업
- '사용자의 서비스 요청사항'과 '고객 및 매니저 정보'를 활용하여 매니저 매칭 성공 여부(0/1)를 예측 할 수 있는 머신러닝 모델의 개발
- 평가 지표: AUC

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최: (주)플랫포머스
- 주관: 국민대학교 빅데이터경영통계전공 D&A
- 참가 대상: 전공 학부생
- 성과: 최우수상 수상(2위)

<br/>

## 3. 대회 기간

- 제출마감: 2021년 11월 23일
- 코드 평가 마감 및 최종순위 발표: 2021년 11월 29일

<br/>

## 4. 내용
- 사용자의 서비스 요청사항과 고객 및 매니저 정보 데이터를 통해 매니저 매칭 성공 여부를 예측하는 이진 분류 문제임.
- 매니저 관련 column들은 비정상적인 score로 인해 drop되었음.
- 다양한 범주형 변수를 그룹화, 조합을 통해 생성하였음.
- 고객가입일이나 접수일과 같은 날짜 정보들을 대상으로 세부 날짜정보로 subdivision하였음.
- 정규화, 피처 셀렉션을 거쳐서 최종적으로 피처를 선정하였음.
- ExtraTrees 모델을 base model로 Catboost 모델을 앙상블하여 최종 submission을 생성하였음.

<br/>

## 5. Process

### ch.1 Feature Engineering

-  EDA
- Group Features
- Date Features
- Combination Features

---

### ch.2 Preprocessing

- Manager Feature drop
- NAN processing
- One-hot Encoding
- Normalization
- Feature Selection

---

### ch.3 Modeling

- ExtraTrees(Default parameters)
- Catboost(Default parameters)
- Additional Eval metric(Average Precision)

---

### ch.4 Ensemble

- Weighted Ensemble
- ExtraTress 8 : Catboost 2

<br/>

## 6. 참고자료

[제1회 산학연계 공모전 사이트](https://www.kaggle.com/competitions/2021-daplatformers-final-round/overview)
