> **Deep Fake 영상 판별 모델 개발[팀]**

**‘’꼼꼼한 EDA를 통해 97.27%의 Deep Fake 영상 판별 달성’’**

### [목적]

- 7000개의 Deep Fake 영상 데이터를 활용해 3000개 영상의 Deep Fake 적용 여부 판단 알고리즘 구현

### [인원]

- 4명 - 백엔드 1명, AI 엔지니어 2명, AI전공 학부생 1명

### [역할]

- Xception,  EfficientNet모델을 활용한 Deep Fake 영상 판별 알고리즘 구현
- EfficientNet 대비 약 10% 향상된 결과를 보인 Xception 모델 선택
- EDA를 통해 훈련 데이터 중 Deep Fake 영상에서 Face swap이 Facial Expression보다 많이 적용됨 확인
- Real 영상과 Fake 영상의 평균 프레임 길이가  약 4배 정도 차이남을 확인하고 훈련 이미지의 Data balancing, Augmentation 수행
- Training 이미지 중 Face 부분이 두드러지는 이미지가 많아 MTCNN을 사용해 중심 보정 및 얼굴 부분을 Crop 해 새롭게 전처리
- 구축한 데이터를 이용해 Xception모델 Fine-Tuning한 결과 97.27%의 Deep Fake 영상 분류 정확도 달성

### [사용 기술]

- 언어: Python
- 프레임워크: Keras, Tensorflow
- 라이브러리: cv2, MTCNN, Scikit-learn, Pandas
- 서버: Elice Cloud
- 개발 환경: NVIDIA A100, VRAM 16G 컴퓨터 4대

### [성과]

- 국방부, 과학기술정보통신부 주관 [2023 국방AI경진대회 후원기업상 수상(리더보드 6등)](https://maicon.kr/%eb%9f%b0%ed%83%80%ec%9e%84%ec%97%90%eb%9f%ac/)
