# 학습 계획: 실전 라이브러리 활용 (Practical Ecosystem)

**Goal**: 이론 이해를 위해 직접 구현한("Manual Implementation") 방식과 달리, **실무에서 사용하는 효율적인 방법(Numpy/Pandas/Scikit-learn)**을 각 세션에 추가합니다.
**Concept**: "원리는 알았으니, 이제 도구를 쓰자." (Don't reinvent the wheel in production).

---

## 📅 Roadmap (Add-on Modules)

각 Notebook의 `Part 2. Manual Implementation`과 `Part 3. Concepts` 사이에 **`🚀 Practical Usage`** 섹션을 삽입합니다.

### Session 0: Math Basics
> "반복문 대신 벡터 연산(Vectorization)을 씁니다."
- **Numpy**: `np.sum()`, `np.prod()` (속도 비교), `np.dot()` (내적), `np.gradient()` (수치 미분 자동화).
- **Tip**: 왜 파이썬 `for`문보다 `numpy`가 수십 배 빠른가? (C언어 최적화 & SIMD).

### Session 1: Descriptive Stats
> "데이터프레임 한 줄 요약의 힘."
- **Pandas**: `df.describe()`, `df.mean()`, `df.var(ddof=1)`, `df.median()`.
- **Quantile**: `df.quantile([0.25, 0.75])`로 IQR 구하기.
- **Tip**: `ddof=1` (Pandas 기본) vs `ddof=0` (Numpy 기본) 차이 주의.

### Session 2: Probability
> "확률 분포 생성과 샘플링."
- **Numpy Random**: `np.random.normal()`, `np.random.choice()`.
- **Scipy Stats**: `scipy.stats.norm.pdf()` (확률밀도함수 값 구하기).

### Session 3: Regression
> "경사하강법을 직접 짤 필요 없습니다."
- **Pandas**: `df.corr()` (상관행렬 히트맵).
- **Scikit-Learn**: `LinearRegression.fit()`.
- **Tip**: `coef_` (기울기 $w$)와 `intercept_` (절편 $b$) 확인하기.

### Session 4: Vectors & Evaluation
> "평가 지표, 한 방에 계산하기."
- **Scikit-Learn Metrics**: `precision_score`, `recall_score`, `f1_score`.
- **Cosine Similarity**: `sklearn.metrics.pairwise.cosine_similarity` (행렬 연산 최적화).

---

## 🛠 Deliverables
- [ ] **Update Notebooks**: `00` ~ `04` 노트북 파일 수정.
    - 각 노트북에 `## 🚀 Practical Usage` 섹션 추가 및 예제 코드 삽입.
