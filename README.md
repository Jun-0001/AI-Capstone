
# 🎨 AI_Capstone : Deep-Image-Colorization-Keras

> **Keras 및 딥러닝 기반의 흑백 이미지 자동 컬러 복원(Colorization) 프로젝트**

본 프로젝트는 흑백 이미지(Grayscale)를 입력받아 자연스러운 컬러 이미지로 변환하는 인공지능 모델을 구현한 기록입니다. 이미지의 밝기(L) 정보를 분석하여 색상(A, B) 정보를 예측하는 LAB 색 공간 변환 기법을 활용하였습니다.

---

## 🎯 프로젝트 목표 (Project Objectives)
- **자동 컬러링 구현:** 인공 신경망을 통해 흑백 이미지의 채색 과정을 자동화
- **LAB 색 공간 활용:** RGB 대신 밝기와 색상이 분리된 LAB 공간을 활용하여 학습 효율 극대화
- **특징 추출 최적화:** CNN(Convolutional Neural Networks)을 활용한 이미지 컨텍스트 이해 및 색상 매핑
- **결과 시각화:** 원본 흑백 이미지와 모델이 예측한 컬러 이미지를 비교 분석

## 🛠 기술 스택 (Tech Stack)

### **Deep Learning Framework**
- ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
- ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
- ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

---

## 📊 핵심 아키텍처 및 프로세스 (Key Process)

### 1. 데이터 전처리 (Image Preprocessing)
- **LAB Conversion:** 이미지의 `L` 채널(밝기)은 입력 데이터로, `a`, `b` 채널(색상)은 학습 타겟(Label)으로 설정.
- **Normalization:** 데이터 범위를 -1에서 1 사이로 정규화하여 학습 속도 및 안정성 향상.

### 2. 모델 구조 (Model Architecture)
- **Encoder-Decoder 구조:** 저차원에서 특징을 추출하고 고차원에서 색상을 복원하는 구조 채택.
- **Upsampling:** 낮은 해상도의 색상 맵을 원본 크기로 복원하기 위한 업샘플링 레이어 적용.

### 3. 학습 및 결과 (Training & Results)
- **Loss Function:** MSE(Mean Squared Error)를 활용하여 실제 색상과 예측 색상 간의 오차 최소화.
- **Inference:** 학습된 모델에 새로운 흑백 이미지를 투입하여 실시간 컬러 변환 수행.

---

## 📈 결과 및 자료 (Sample Results)
<img width="541" height="740" alt="image" src="https://github.com/user-attachments/assets/5ead3dce-a6bb-4bde-a1c1-48ed07c1f51d" />
![AI_Capstone_포스터](https://github.com/user-attachments/assets/d724aa67-8e1a-4b6a-b1ba-e8bd701e89c2)

---

## 📂 프로젝트 자산 (Project Assets)
- [📓 Image Colorization 메인 코드 (.ipynb)](./keras_colorization_final_sr_v1.ipynb)
- [📓 Image Colorization 최종 결과 코드 (.ipynb)](./prediction_for_new_test_set.ipynb)
- [📓 Image Colorization 성능 검토 코드 (.ipynb)](./prediction_for_validation_set.ipynb)
- *이미지 로드, LAB 변환, 모델 설계 및 학습 전 과정 포함*

---

## 📚 연구 및 이론 근거 (Technical Reference)
- *Colorful Image Colorization (ECCV, 2016) - 기초 이론 기반*
- *Learning Representations for Automatic Colorization (SIGGRAPH, 2016)*
