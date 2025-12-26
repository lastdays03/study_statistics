# 학습 계획: AI/LLM 엔지니어를 위한 실전 통계학 (Deep Theory Edition)

**Status**: 🔄 In Progress
**Goal**: LLM, RAG, 머신러닝 기초 학습을 위한 필수 통계 지식 습득 (이론과 실습의 완벽한 조화)
**Estimated Time**: 4주 (주당 6-8시간)

---

## 📋 개요 (Overview)
본 커리큘럼은 **"수학적 원리(Theory) -> 코드 구현(Practice) -> 실험(Experiment) -> 회고(Retrospective)"**의 4단계 엄격한 사이클을 따릅니다. 단순히 라이브러리를 쓰는 것을 넘어, **공식의 유도 과정과 통계적 함의**를 깊이 있게 이해하는 것을 목표로 합니다.

---

## 🚀 학습 세션 (Learning Sessions)

### Session 1: 데이터 문해력과 기술 통계 (The Foundation)
**Goal**: 데이터의 분포를 파악하고, 모수와 통계량의 차이, 그리고 자유도의 개념을 수학적으로 이해합니다.

#### 1. 🎯 Deliverables (결과물)
- [ ] **Integrated Notebook**: `notebooks/01_descriptive_stats.ipynb` (Theory + Manual Code + Experiments)
    - Part 1: Deep Theory (모집단/표본, 분산 공식 유도)
    - Part 2: Manual Implementation (평균/분산 직접 구현)
    - Part 3: Concepts & Visualization (기술 통계 시각화)
    - Part 4: Experiments (이상치, 샘플 크기 실험)

#### 2. 📐 Deep Theory (수학 및 기초 이론)
- **통계의 언어 (Notation)**:
    - 모집단($N, \mu, \sigma^2$) vs 표본($n, \bar{x}, s^2$)의 엄격한 구분.
    - 합의 기호 시그마($\sum$) 자유자재로 다루기.
- **중심 경향성(Central Tendency)과 퍼짐(Spread)**:
    - 산술 평균, 기하 평균, 조화 평균의 차이와 활용 사례.
    - 편차(Deviation)의 합은 왜 항상 0인가? ($\sum(x_i - \bar{x}) = 0$ 증명).
- **자유도(Degrees of Freedom)**:
    - 표본분산($s^2$) 계산 시 $n$이 아닌 $n-1$로 나누는 이유 (Bessel's Correction) 직관적/수식적 이해.

#### 3. 💻 Python Practice (구현)
- **밑바닥부터 구현하기**:
    - `sum()`, `len()`만 사용하여 `my_mean()`, `my_variance()` 함수 만들기.
    - `numpy.var(ddof=1)`과 내 결과 비교하기.
- **시각화**:
    - 히스토그램 해석: Skewness(왜도)와 Kurtosis(첨도)가 분포의 모양에 미치는 영향 확인.

#### 4. 🧪 Experiment & Verify
- **Scenario**: 데이터가 10개일 때 $n$으로 나눈 분산과 $n-1$로 나눈 분산 중, 어느 것이 모분산 $\sigma^2$에 더 가까운가? (시뮬레이션 검증)

#### 5. 📝 Retrospective

---

### Session 2: 확률과 분포 (Frequency & Bayesian)
**Goal**: 확률의 공리부터 시작하여, 조건부 확률과 베이즈 정리를 통해 LLM의 작동 원리를 파악합니다.

#### 1. 🎯 Deliverables
- [ ] **Integrated Notebook**: `notebooks/02_probability_distribution.ipynb`
    - Part 1: Deep Theory (확률 공리, 조건부 확률, 베이즈 정리 유도)
    - Part 2: Manual Implementation (몬테카를로 시뮬레이션, Bigram 확률 직접 계산)
    - Part 3: Concepts & Practice (분포 시각화, Zipf's Law)
    - Part 4: Experiment (몬티 홀 문제 검증)

#### 2. 📐 Deep Theory
- **확률의 기초 (Set Theory & Axioms)**:
    - 표본 공간($\Omega$), 사건($E$), 합집합($\cup$), 교집합($\cap$).
    - 확률의 3가지 공리 (Kolmogorov axioms).
- **조건부 확률과 독립**:
    - $P(A|B) = \frac{P(A \cap B)}{P(B)}$ 의 직관적 이해 (표본 공간의 축소).
    - 독립사건의 정의 ($P(A \cap B) = P(A)P(B)$).
- **확률 변수와 분포**:
    - 이산(Discrete) vs 연속(Continuous).
    - PDF(확률밀도함수)와 CDF(누적분포함수)의 관계 (미분과 적분).
    - **Zipf's Law**: 멱법칙(Power Law) 분포의 수식적 특징 ($P(x) \propto x^{-\alpha}$).

#### 3. 💻 Python Practice
- **확률 계산**:
    - 텍스트 코퍼스에서 단어의 등장 확률, 조건부 확률($P(\text{word}|\text{previous})$) 계산.
- **분포 그리기**:
    - 정규분포, 로그 정규분포, 파레토 분포(Zipf) 생성 및 비교.

#### 4. 🧪 Experiment & Verify
- **Scenario**: 몬티 홀 문제(Monty Hall Problem)를 시뮬레이션으로 검증한다. 내 직관과 조건부 확률 계산이 일치하는가?

#### 5. 📝 Retrospective

---

### Session 3: 상관과 회귀 (Relationships & Learning)
**Goal**: 변수 간의 선형 관계를 수치화하고, 오차를 최소화하는 파라미터를 미분으로 찾아봅니다.

#### 1. 🎯 Deliverables
- [ ] **Integrated Notebook**: `notebooks/03_correlation_regression.ipynb`
    - Part 1: Deep Theory (공분산/상관계수 수식, OLS 미분 과정)
    - Part 2: Manual Implementation (경사하강법으로 회귀선 찾기)
    - Part 3: Concepts & Practice (상관 분석 Heatmap, Scikit-learn 활용)
    - Part 4: Experiment (노이즈와 회귀 파라미터 변화 실험)

#### 2. 📐 Deep Theory
- **공분산(Covariance)과 상관계수(Correlation)**:
    - 공분산의 한계와 상관계수($r$)로의 정규화 과정 ($Cov(X,Y) / (\sigma_x \sigma_y)$).
    - 상관관계 $\neq$ 인과관계 (Spurious Correlation).
- **선형 회귀와 최소제곱법(OLS)**:
    - 손실 함수(Loss Function) 정의: $MSE = \frac{1}{n}\sum(y_i - (wx_i + b))^2$.
    - **Optimization 맛보기**: MSE를 $w$와 $b$로 편미분하여 최적해 찾기.

#### 3. 💻 Python Practice
- **상관 분석**:
    - 다양한 데이터셋의 Heatmap 그리기.
- **회귀 분석**:
    - `scikit-learn` 없이 파이썬으로 단순 선형 회귀 구현 (Normal Equation 활용).

#### 4. 🧪 Experiment & Verify
- **Scenario**: 데이터에 노이즈를 점점 많이 섞을수록 $w$와 $b$의 추정치는 어떻게 변하는가? 신뢰 구간(Confidence Interval)은 어떻게 넓어지는가?

#### 5. 📝 Retrospective

---

### Session 4: 벡터와 차원 (Linear Algebra & Evaluation)
**Goal**: 고차원 데이터를 다루기 위한 선형대수 기초(벡터, 내적)를 익히고 RAG 성능 평가에 적용합니다.

#### 1. 🎯 Deliverables
- [ ] **Integrated Notebook**: `notebooks/04_vectors_evaluation.ipynb`
    - Part 1: Deep Theory (벡터 내적의 기하학적 의미, 오차 행렬)
    - Part 2: Manual Implementation (코사인 유사도, F1-score 직접 구현)
    - Part 3: Concepts & Practice (행렬 연산, 랭킹 평가 지표)
    - Part 4: Experiment (차원의 저주 실험)

#### 2. 📐 Deep Theory
- **벡터와 공간**:
    - 벡터의 크기(Norm)와 방향.
    - **내적(Dot Product)**: $A \cdot B = |A||B|\cos\theta$. 내적이 곧 '유사도'인 이유.
- **평가 지표의 본질**:
    - Confusion Matrix의 4가지 요소 (TP, TN, FP, FN).
    - 조화 평균(Harmonic Mean): F1-score에서 산술 평균 대신 조화 평균을 쓰는 이유.

#### 3. 💻 Python Practice
- **행렬 연산**:
    - `numpy` 브로드캐스팅을 활용한 다수 문서 간 유사도 고속 계산.
- **평가**:
    - 검색 결과 랭킹 평가 지표 (MRR, NDCG) 개념 학습 및 간단 실습.

#### 4. 🧪 Experiment & Verify
- **Scenario**: 차원이 커질수록(예: 2차원 -> 1000차원) 무작위 두 벡터 사이의 거리는 어떻게 되는가? (모든 점들이 멀어진다 - 차원의 저주).

#### 5. 📝 Retrospective
