# IEEE Fraud Detection

[link](https://www.kaggle.com/competitions/ieee-fraud-detection/overview)

## Topic

### Why kaggle IEEE-fraud-detection?

데이터 분석을 혼자 공부하면서 생기는 난점 중 하나는, 
상당수의 학습용 데이터셋들은 미리 정제되어 있고, 데이터 크기도 크지 않은 경우가 많다는 점 이다. 
IEEE fraud detection의 train data는 약 60만개의 row, 400개 이상의 column 으로 이루어져 있고, 
실수값 뿐만 아니라 문자열 데이터도 포함 되어 있고, 결측치가 상당히 많다. 
또한, 대부분의 column들이 마스킹 되어 있어 실제 의미를 간접적으로 추론해야 한다. 

상기한 이유들 때문에 기존에 다루어 보았던 데이터들에 비해 전처리 및 분석 난이도가 높다보니 도전 욕구가 생겼다.

kaggle은 이미 종료된 대회도 late submission을 통해 점수 산출이 가능한데, 이를 통해 객관적인 위치를 파악할 수도 있다는 것도 장점이다.



### Goals

1달 정도의 시간을 투자하여 private score 기준 상위 30% 이내의 점수를 기록하는 걸 목표로 정했다.



### Exploratory Data Analysis

[analysis](/IEEE-fraud-detection/analysis.ipynb) 참조



### Modeling

기본적인 hyperparameter tuning만 거친 xgboost 단일모델을 사용하였다.

고득점을 위해서는 모델링에도 신경을 써야 하지만, 
모델링은 다른 데이터셋으로도 충분히 연습 할 수 있으며, 
이미 종료한 대회에 과도한 시간을 쏟는건 비효율적이라 생각하여 EDA 및 feature engineering 에 좀 더 초점을 맞추는 쪽으로 결정했다.

상세 내용은 [modeling](/IEEE-fraud-detection/modeling.ipynb) 참조



### Result

Highest Public Score: 0.950552 (상위 29.06%)

Highest Private Score: 0.924592 (상위 24.70%)


Public Score에 비해 Private Score 순위가 높게 나온건 참가자들이 overfitting된 모델을 많이 제출해서 인 것 같다.
