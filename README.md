# Stock_Prediction

삼성전자의 주가를 다양한 방식으로 예측해보고자 합니다.
- ARIMA, SARIMA, Facebook Prophet부터
- RNN, LSTM, Transformer, TFT까지

Time Series Forecasting의 다양한 방법론들을 구현하고 실제 데이터에 실험해보고자 합니다.

--------------------------------------------------
### 1. 삼성전자 주식 가격 예측 with ARIMA, Prophet
ARIMA, Facebook Prophet 등 시계열 데이터의 주기성, 계절성을 바탕으로 예측을 진행하는 모델에 대해서 실험해보고자 하였다.

[ipynb 파일 바로보기 with Nbviewer](https://nbviewer.jupyter.org/github/jhbale11/DataScienceLab/blob/main/Dacon/%EC%82%BC%EC%84%B1%EC%A0%84%EC%9E%90%20%EC%A3%BC%EA%B0%80%20%EC%98%88%EC%B8%A1_ARIMA_PROPHET.ipynb)

--------------------------------------------------

### 2. 삼성전자 주식 가격 예측 with LSTM, Pytorch
pytorch를 사용하여 LSTM 모델을 구현하였으며, 구현한 모델을 바탕으로 삼성전자 주가를 예측하는 실험을 진행하였다.
하지만 딥러닝을 사용한 주가 예측 모델링의 치명적인 문제를 발견하였다.

**1) Non-Stationary Data**

**2) Volume, Nasdaq 증감률, Index Data와 함께 학습 필요**

**3) Overfitting 막기 위해 가격 예측이 아닌, Return 예측, 구매여부 예측하는 모델 필요**

이후 진행할 프로젝트에서는 이를 고려하여 진행하고자 한다.

----------------------------------------------------

### 3. 삼성전자 주식 가격 예측 with Facebook Prophet
Facebook Prophet을 사용하여 삼성전자 주가를 예측하는 실험을 진행하였다. 이전 Facebook Prophet을 진행했던 실험에 비해 Prophet의 구체적인 사용 방법과 Parameter의 의미도 함께 담아보았다. Change Point 시각화를 통해 삼성전자 주가의 Regime을 시각화해보았다.

-----------------------------------------------------

### 4. 삼성전자 주식 가격 예측 with Transformer
NLP분야 문제 해결을 위해 제안된 'Attention is All You Need(NIPS, 2017)'논문의 구조대로 Transformer를 구현하여 주가 예측 문제를 풀어보았다.Transformer Decoder가 좋지 못한 성능을 보여주었기에, FC Layer Decoder로 교체해서 학습을 진행하였고 그 결과를 확인하였다. 앞으로는
Time Series Regression 문제에 대해 Transformer Based Model을 구현하고 주가 데이터로 실험해볼 계획이다.
