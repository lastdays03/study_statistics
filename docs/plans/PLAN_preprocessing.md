# 학습 계획: 데이터 전처리 (Preprocessing & Scaling)

**Goal**: 데이터의 **단위(Scale)**가 다를 때 발생하는 문제를 이해하고, 이를 해결하는 **표준화(Standardization)**와 **정규화(Normalization)**를 학습합니다.
**Missing Gap**: 현재 노트북에는 평균과 분산은 있지만, 이를 이용해 데이터를 변환하는 Scaling 기법이 빠져 있습니다.

---

## 📅 Refinement Principles

### 1. 📏 Scale Matters (단위의 중요성)
- **Problem**: 키(cm)는 170인데, 시력(0.1~2.0)은 1.0이다. 숫자의 크기 차이 때문에 AI가 시력을 무시할 수 있다.
- **Solution**: 모든 데이터를 공평한 경기장(Scale)으로 불러오자.

### 2. 📊 Standardization vs Normalization
- **표준화 (Z-score)**: 평균을 0, 분산을 1로 맞춤. ($x \to \frac{x - \mu}{\sigma}$)
    - **Use Case**: 이상치(Outlier)가 있어도 덜 민감함, 대부분의 머신러닝 모델(선형회귀, 딥러닝)에 적합.
- **정규화 (Min-Max)**: 0과 1 사이로 압축. ($x \to \frac{x - min}{max - min}$)
    - **Use Case**: 이미지 픽셀(0~255) 처리, 거리 기반 알고리즘(KNN) 등 정확한 범위가 필요할 때.

---

## 🛠 Action Items

`notebooks/01_descriptive_stats.ipynb`의 **Part 2 (Manual Implementation)**와 **Part 3 (Practical Usage)** 사이에 새로운 섹션을 추가합니다.

### New Section: ⚖️ Preprocessing: 데이터의 눈높이 맞추기

#### 0. 편차 (Deviation): 기준으로부터의 거리
- $$ d = x - \mu $$
- 분산($s^2$)도, 표준편차($s$)도, 표준화($z$)도 모두 **'편차'**에서 시작합니다.
- 데이터가 평균보다 크면 양수(+), 작으면 음수(-)입니다.

#### 1. Z-score (Standardization) 직접 구현
- $$ z = \frac{x - \mu}{\sigma} $$
- 내 점수가 평균에서 얼마나 떨어져 있는가? (상대적 위치)

#### 2. Min-Max Scaling 직접 구현
- $$ x_{norm} = \frac{x - x_{min}}{x_{max} - x_{min}} $$
- 데이터를 % 퍼센트로 변환하는 느낌.

#### 3. 🚀 Practical Usage: `sklearn.preprocessing`
- `StandardScaler`
- `MinMaxScaler`
- 현업에서는 직접 계산하지 않고 이걸 쓴다.

---

## 📝 Deliverables
- [ ] `notebooks/01_descriptive_stats.ipynb` 업데이트.
