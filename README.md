# Galaxy AI Contest
![image](https://user-images.githubusercontent.com/41675375/77989882-da017180-735a-11ea-8e1a-f388c46752aa.png)

### [월간 데이콘 2 천체 유형 분류 대회](https://dacon.io/competitions/official/235573/overview/)

Dacon에서 주최하는 월별 Competition의 일환으로 
[SDSS(Sloan Digital Sky Survey)](https://www.sdss.org/dr16/)에서 제공한 데이터를 가지고 천체의 유형을 분류하는 알고리즘 모델을 만드는 것이 목표 

## Team

- SukJin Lee
- HanBin Lee
- SeoYoung Ju

## Strategy

### ▶ Plan Design
<p align="center"><img src="https://user-images.githubusercontent.com/41675375/78154472-44a7cf80-7477-11ea-82f1-7f5165ab5ecf.png" width="700" height="350"></p>

### ▶ Tool
- Anaconda (python 3.7.4)
- Google Cloud Platform (NVIDIA GPU K80)

## Model

우선 이미지 데이터가 아닌 수치형 데이터를 대상으로 학습을 시키는 것이기에 Deep Learning보다 Machine Learning에 초점을 맞춰 모델을 선택했습니다. 그 중 높은 성능과 좋은 효율을 보이는 Boost 계열의 모델에 주목했습니다.  

LightGBM은 Bayesian Optimization을 통해, 나머지 boost모델은 Random Search(혹은 Grid)를 통해 parameter tuning을 진행했습니다.  

그 이후 최적의 모델을 가지고 Voting과 Stacking을 통해서도 학습을 진행했습니다.

[※ 참고논문](https://github.com/hanbinleejoy/galaxy-ai-contest/tree/master/src/_paper)

## Result & Improvements

### ▶ Result
최종: Final Stage 진출 / 리더보드 등록 기준 총 352팀 중 89등 기록(0.36718, logloss)  
[(Dacon 리더보드)](https://dacon.io/competitions/official/235573/leaderboard/)

### ▶ Improvements
- Data Handling과 Feature Engineering의 부족
- Parameter Tuning의 시간 부족
- AI Contest에 대한 경험 부족



