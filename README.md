# medical_AI_final-project
Repository for medical_AI_final-project in fastcampus


## 의료 이미지 데이터셋을 이용하여 일반인 정상폐 vs. 폐렴 환자 폐 분류 Task
**1. 프로젝트 명** : 의료 이미지 데이터셋을 이용한 폐렴 진단

**2. 프로젝트 목표**
- 흉부 X-ray 이미지를 사용하여 폐렴을 진단하는 딥러닝 모델을 구축
- CNN(Convolutional Neural Networks) 모델을 활용하여 정상 및 폐렴 이미지를 분류하는 과제를 수행.
- PyTorch를 이용하여 딥러닝 아키텍쳐 구성

**3. 데이터셋**
- Chest X-ray Images (Pneumonia): 정상과 폐렴을 구분하는 흉부 X-ray 이미지 데이터셋
- 해당 데이터셋은 train/test/validation의 3개의 folder로 구성되어 있고, 각 카테고리 하위에는 폐렴 혹은 정상으로 구분되어 폴더로 구성. 5,863개의 x-ray가 JPEG형식으로 저장되어 있음(정상: 1,583, 폐렴: 4,273).
- 데이터셋의 이미지 퀄리티 조정을 위해 사전에 데이터셋 전체를 검사하여 읽을 수 없거나 저화질의 이미지들은 제거하였음.
- 해당 데이터는 광저우 여성 어린이 메디컬 센터에서 1세부터 5세까지의 소아 환자들을 대상으로 찍은 흉부 x-ray. 2명의 내과 전문의가 이미지에 대한 진단을 내리고, 이후 다른 한 명의 내과 의사가 평가를 진행하여 레이블 생성에 오류가 없도록 하였음.
- 캐글 데이터셋 다운로드 후 사용: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia


**4. 프로젝트 단계**
- 0) 필요한 라이브러리 install 및 import
- 1) 데이터 다운로드 및 EDA(Exploratory Data Analysis) 진행
- 2) 데이터 전처리, 정규화, Augmentation
- 3) 모델 설계: CNN 사용
- 4) 모델 컴파일
- 5) 모델 평가: 평가 metric으로 모델의 정확도 확인
- 6) 결과 분석: 샘플 추출 후, label과 prediction 비교
