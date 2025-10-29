# image_reg-classification
# 📷 이미지 Classification vs Regression 정리

이미지를 활용한 딥러닝 문제는 크게 **Classification(분류)** 과 **Regression(회귀)** 으로 나뉜다.  
이 둘의 핵심 차이는 **예측 결과가 “종류인지(범주)” vs “숫자인지(연속값)”** 에 있다.

---

##  핵심 비교

| 구분 | Classification (분류) | Regression (회귀) |
|------|----------------------|-------------------|
| **출력 형태** | 라벨(label) → 카테고리 | 실수 값(continuous value) |
| **예측 결과** | “개 or 고양이” | “나이 23.7세” |
| **출력 개수** | 고정된 클래스 수 | 무한한 연속값 가능 |
| **대표 예시** | 얼굴 인식, 의료 영상 진단 | 나이 추정, 거리 추정 |
| **Loss 함수** | Cross Entropy Loss | MSE, MAE 등 |
| **평가 지표** | Accuracy, F1-score 등 | RMSE, R² 등 |

---

##  예시로 이해하기

| 상황 | Classification | Regression |
|------|----------------|-----------|
| 얼굴 사진 분석 | 남자 / 여자 | 나이 27.4세 |
| X-ray 이미지 | 정상 / 암 | 암 가능성 0.87 |
| 하늘 사진 | 맑음 / 흐림 / 비 | 구름 양 0.62 |
| 주차 거리 판단 | 앞차 / 없음 | 앞으로 1.3m |

---

##  딥러닝 구조 비교 (CNN 기반)

| 항목 | Classification | Regression |
|------|----------------|-----------|
| 마지막 레이어 | `Softmax`, `Sigmoid` 등 | `Linear` (값 그대로 출력) |
| 출력 차원 예시 | 2 (dog, cat) | 1 (예: 예측 나이) |
| Loss | CrossEntropyLoss | MSELoss |

---

##  한 줄 요약

> **Classification은 “무엇인지” 예측, Regression은 “얼마인지” 예측하는 문제이다.**

---

필요하면 여기서 **실제 CNN 코드 예제**도 이어서 추가해줄게. “코드도 작성해줘”라고 말해줘!
