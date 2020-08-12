# Predict_Pneumonia
딥러닝(CNN)을 활용하여 흉부 X-Ray 이미지를 통해 폐렴 여부를 진단합니다.

## 데이터 소개
- 흉부 X-Ray 이미지 총 ??장.
- 총 4개의 질병 class를 진단합니다.
  - 정상 ??장
  - 박테리아성 폐렴 : ??장
  - 바이러스성 폐렴 : ??장
  - 코로나 : ??장
  
- (이미지)
- 출처
  - 아래 4개의 링크에서 이미지 파일이 중복되거나 폐 이미지가 아닌 경우를 제외하고 통합하였습니다. 
  - https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
  - https://www.kaggle.com/darshan1504/covid19-detection-xray-dataset
  - https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset
  - https://www.kaggle.com/tawsifurrahman/covid19-radiography-database
  

## 결과
- 유명한 CNN 모델 중 가장 나은 정확도를 보여주었던 Xception 모델을 사용.
- Epoch 50 기준 test셋에 대한 accuracy : 90~98%
- 코로나에 대한 이미지의 수가 다른 질병에 비해 극히 적은데도, 좋은 예측 정확도를 보여주었습니다.
