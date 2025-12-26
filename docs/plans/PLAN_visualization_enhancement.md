# 학습 계획: 회귀 분석 시각화 강화 (Scatter & Regression Line)

**Goal**: 단순히 수치(상관계수)만 보는 것을 넘어, **산점도(Scatter Plot)**와 **회귀선(Regression Line)**을 통해 데이터의 패턴과 모델의 적합성(Fit)을 눈으로 확인하는 습관을 기릅니다.

---

## 🧐 Why Visualization Matters?

### 1. 앤스컴의 콰르텟 (Anscombe's Quartet)
- 평균, 분산, 상관계수까지 똑같은 4개의 데이터셋이 있습니다.
- 하지만 **그려보면(Plot)** 완전히 다른 모양입니다.
    - 선형적인 데이터
    - 곡선 데이터 (이차함수)
    - 이상치가 있는 데이터
- **Lesson**: "숫자만 믿지 마라. 반드시 그려봐라."

### 2. 회귀선 (Regression Line)의 의미
- 모델이 데이터를 얼마나 잘 설명하는지 보여주는 **추세선(Trend Line)**입니다.
- 데이터 포인트들이 회귀선 주변에 오밀조밀 모여있어야 예측 성능이 좋습니다.

---

## 🛠 Action Items

`notebooks/03_correlation_regression.ipynb`의 **Part 3 (Concepts & Practice)** 섹션에 시각화 파트를 대폭 강화합니다.

### 1. `seaborn.regplot` 도입
- 기존 `plt.scatter` + `plt.plot`은 코드가 깁니다.
- `sns.regplot(x, y)` 한 줄로 **산점도와 회귀선(천뢰구간 포함)**을 동시에 그립니다.

### 2. 잔차(Residual)의 시각적 이해
- 회귀선과 실제 데이터 점 사이의 **거리(Distance)**가 바로 에러(Error)임을 시각적으로 설명합니다.

### 3. 이상치(Outlier)의 영향 확인
- 이상치 하나가 회귀선의 기울기를 어떻게 망가뜨리는지 시각화로 체험합니다.

### 4. Correlation Analysis Deep Dive (상관분석 강화)
- **공분산(Covariance)의 한계**: "키(cm)와 몸무게(kg)의 공분산은 500인데, 키(m)로 바꾸면 5가 된다." -> **절대적인 크기 비교 불가**.
- **상관계수($r$)의 해석**:
    - **강도(Strength)**: $0.7$ 이상이면 강한 상관관계. $0$에 가까우면 관계 없음.
    - **방향(Direction)**: 양수(+)는 비례, 음수(-)는 반비례.
    - **함정(Pitfall)**: **"상관관계는 인과관계가 아니다 (Correlation $\ne$ Causation)."** (여름에 아이스크림 판매량과 익사 사고율이 같이 오르는 예시)

### 5. Heatmap 제대로 읽는 법
- **대칭성(Symmetry)**: 대각선을 기준으로 데칼코마니.
- **다중공선성(Multicollinearity)**: 설명변수(X)끼리 너무 빨갛다면(상관관계가 높다면) 모델에 안 좋다. (하나만 남겨야 함)

---

## 📝 Deliverables
- [ ] `notebooks/03_correlation_regression.ipynb` 업데이트 (시각화 섹션 추가).
