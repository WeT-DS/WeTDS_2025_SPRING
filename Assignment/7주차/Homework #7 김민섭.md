## 7주차 머신러닝 과제

2023170864 김민섭

---

**1. 앙상블 학습**
앙상블 학습은 여러 예측 모델을 함께 사용해 단일 모델보다 정확도를 높이는 기법이다. 서로 다른 모델을 독립적으로 학습하거나 동일 모델에 다양한 샘플링 기법을 적용할 수 있다. 편향을 줄이는 부스팅과 분산을 줄이는 배깅으로 나뉘며, 배깅은 여러 모델 예측을 평균 또는 다수결로 합치고, 부스팅은 이전 모델의 오류를 보완하며 순차적으로 학습을 진행한다.

---

**2. 투표식 분류기**
투표식 분류기는 같은 데이터로 훈련된 여러 분류기의 결과를 합쳐 최종 클래스를 결정한다. 직접 투표 방식은 가장 많은 표를 얻은 클래스를 선택하고, 간접 투표 방식은 각 분류기가 출력한 확률을 평균 내어 가장 높은 확률을 가진 클래스를 고른다.

---

**3. 배깅과 페이스팅**
배깅은 원본 데이터를 복원 추출해 여러 동일 모델을 학습시키고, 분류는 다수결, 회귀는 평균으로 예측을 결정한다. 이로써 개별 모델 분산이 줄어들어 안정성이 높아진다. 페이스팅은 중복 없이 샘플을 추출해 모델을 학습하지만, 다양성이 배깅보다 낮아 분산 감소 효과가 작다.

---

**4. 랜덤 패치와 랜덤 서브스페이스**
랜덤 패치는 샘플과 특성을 모두 복원 추출해 학습에 사용하고, 랜덤 서브스페이스는 전체 샘플에서 특성만 무작위로 선택해 학습한다. 두 방법 모두 모델 간 상관관계를 낮춰 분산을 줄이며, 고차원 데이터에 특히 유리하다.

---

**5. 랜덤 포레스트**
랜덤 포레스트는 배깅과 랜덤 서브스페이스를 결합해 여러 결정트리를 앙상블한 모델이다. 각 트리는 무작위로 선택된 샘플과 특성만 사용해 분기 규칙을 학습하며, 최종 예측은 다수결(분류)이나 평균(회귀)으로 결정된다. 이를 통해 단일 트리에 비해 분산이 크게 줄고 과적합 위험이 낮아진다. 또한 특성 중요도를 계산해 변수 기여도를 파악할 수 있어 모델 해석에 유용하다.

---

**6. 부스팅**
부스팅은 여러 약한 학습기를 순차적으로 학습시켜 예측 오류를 보완하는 기법이다. 에이다부스트와 그레디언트 부스팅이 대표적이며, 후자는 이전 모델의 잔차를 학습해 성능을 개선한다. 학습률과 조기 종료 같은 규제 기법으로 과적합을 완화할 수 있고, XGBoost는 트리 복잡도를 비용 함수에 포함해 빠르고 효율적인 학습을 지원한다.

---
