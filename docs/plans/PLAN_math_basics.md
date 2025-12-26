# 학습 계획: Session 0 - 통계를 위한 파이썬 수학 (Math Survival Kit)

**Goal**: 복잡한 수식 기호에 겁먹지 않고, **"수식 = 파이썬 코드"**라는 관점을 장착합니다.
**Format**: 다른 세션과 동일하게 **Theory -> Implementation -> Concepts -> Experiment** 흐름의 통합 노트북으로 진행합니다.

---

## 📅 Roadmap (Integrated Notebook Structure)

### [Session 0: Math Basics](notebooks/00_math_basics.ipynb)

#### Part 1. 📐 Theory as Code: 기호와 대수
> "수학 기호를 코드로 번역합니다."
- **Notation Mapping**:
    - $\sum$ (Sigma) $\rightarrow$ `for` loop & `sum()`
    - $\prod$ (Pi) $\rightarrow$ `for` loop & `*=`
    - $x \in \mathbb{R}$ $\rightarrow$ `isinstance(x, float)`
- **Logarithm**:
    - 곱셈을 덧셈으로 바꾸는 `log`의 마법 ($\log(ab) = \log a + \log b$)을 코드로 확인.

#### Part 2. 💻 Manual Implementation: 미분과 최적화
> "미분은 '아주 조금 움직여보기'입니다."
- **Numerical Differentiation (수치 미분)**:
    - 극한($\lim_{h \to 0}$) 대신 아주 작은수 `h=1e-5`를 대입하여 기울기 구하기.
- **Gradient Descent**:
    - 이차함수 $y = x^2$의 최저점을 찾아가는 과정을 loop로 직접 구현.

#### Part 3. 📖 Concepts: 선형대수 (Linear Algebra)
> "데이터를 엑셀(행렬)에 담고 유사도(내적)를 잽니다."
- **Scalar, Vector, Matrix**: 파이썬 리스트와 `numpy` 배열의 차이.
- **Dot Product (내적)**:
    - `np.dot(a, b)`가 의미하는 것 = "얼마나 닮았니?" (유사도).
    - 두 벡터가 수직이면 내적은 0이다.

#### Part 4. 🧪 Experiment: 시각화로 보는 수학
- **Scenario**: 미분 계수 `h`의 크기에 따른 오차 변화.
    - `h`가 너무 크면? (부정확)
    - `h`가 너무 작으면? (부동소수점 에러)
    - 최적의 `h`를 실험으로 찾아보기.

---

## 🛠 Deliverables
- [ ] **Integrated Notebook**: `notebooks/00_math_basics.ipynb`
    - Part 1: Notation Mapping (Sigma, Pi, Log)
    - Part 2: Numerical Differentiation (Slope implementation)
    - Part 3: Linear Algebra Basics (Dot Product intuition)
    - Part 4: Experiment (Numerical Stability of Derivative)
