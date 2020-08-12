# Predict_Pneumonia
딥러닝(CNN)을 활용하여 흉부 X-Ray 이미지를 통해 폐렴 여부를 진단합니다.

## 데이터 소개
- 흉부 X-Ray 이미지 총 11793장.
- 총 4개의 질병 class를 진단합니다.
  - 정상 4255장
  - 박테리아성 폐렴 : 3755장
  - 바이러스성 폐렴 : 3455장
  - 코로나 : 328장
  ![classes](https://user-images.githubusercontent.com/37574274/89997891-bf0b1a80-dcc7-11ea-84c5-d457c71ecc0a.png)
- 데이터 출처
  - 아래 4개의 링크에서 이미지 파일이 중복되거나 폐 이미지가 아닌 경우를 제외하고 통합하였습니다. 
  - https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
  - https://www.kaggle.com/darshan1504/covid19-detection-xray-dataset
  - https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset
  - https://www.kaggle.com/tawsifurrahman/covid19-radiography-database
  - 전체 데이터에 대한 zip의 크기는 2.47GB 입니다.
  

## 결과
- 유명한 CNN 모델 중 가장 나은 정확도를 보여주었던 Xception 모델을 사용.
- Epoch 50 기준 test셋에 대한 accuracy : <span style="color:red">**90~98%**</span>
- 코로나에 대한 이미지의 수가 다른 질병에 비해 극히 적은데도, 좋은 예측 정확도를 보여주었습니다.
