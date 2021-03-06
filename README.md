# Predict_Pneumonia
딥러닝(CNN)을 활용하여 흉부 X-Ray 이미지를 통해 질병(폐렴 및 코로나)을 진단합니다.

## 데이터 소개
- 흉부 X-Ray 이미지 총 11793장.
- 총 4개의 질병 class로 구성되어 있습니다.
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
  - 전체 데이터 크기 : 약 2.5GB
  
  - 한번에 다운받을 수 있도록 통합 데이터셋을 구축하였습니다 : https://www.kaggle.com/gibi13/pneumonia-covid19-image-dataset

## 모델 구현
- Xception 모델 사용. (loss='categorical_crossentropy', optimizer='adam')
- 모든 이미지의 크기를 (224, 224, 1)로 전처리
- train 데이터와 test 데이터는 매번 통합 데이터셋에서 랜덤으로 추출(split) → 따라서 결과(accuracy)가 매번 달라짐

## 결과
- Epoch 50 기준 최종 accuracy : <span style="color:red">**90~98%**</span><br/>
  ![train_graph](https://user-images.githubusercontent.com/37574274/92446497-dd920200-f1f0-11ea-8da5-860fa7abdf22.png)
- 특히, 코로나에 대한 이미지의 수가 다른 질병에 비해 크게 적은데도 좋은 예측 정확도를 보여주었습니다.
- Confusion Matrix
  <br/><img src="https://user-images.githubusercontent.com/37574274/91636158-54810b00-ea39-11ea-9d31-66636fc8b585.png" width="50%" height="50%" /><br/>
  ex) 정답이 박테리아성 폐렴인데, 바이러스 폐렴이라고 오진한 경우는 36건입니다.
