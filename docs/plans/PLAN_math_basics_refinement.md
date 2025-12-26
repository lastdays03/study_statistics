# 학습 계획: 수학 기초 재설계 (Refinement for Developers)

**Goal**: "고등학교 때 배웠지만 다 까먹은" 개발자를 위해 Session 0 노트북을 개편합니다.
**Concept**: "수학 책의 공식을 파이썬 코드로 다시 쓰는 'Code-First' 접근."
**Level**: 고등학교 수학(함수, 수열 등)은 들어봤으나, 미분/기하학은 낯선 상태를 가정.

---

## 📅 Refinement Principles

### 1. 🏫 Resurrecting Memories (기억 되살리기)
- "이거 교과서에서 봤던 $f(x)$죠? 파이썬에선 `def f(x):`입니다."
- 아주 유치한 비유보다는, **직관적인 물리/데이터 비유**를 사용합니다.

### 2. 💻 Code Translation (번역기 모드)
-수학 기호를 프로그래밍 패턴으로 1:1 매핑합니다.
- $\sum$ $\to$ `for` loop / `sum()`
- $\prod$ $\to$ `math.prod()`
- $f'(x)$ $\to$ `(f(x+h) - f(x)) / h`
- Vector $\to$ `Array` (List)

### 3. � Practical Intuition (실용적 직관)
- **미분**: "접선의 기울기" (학교) $\to$ "**변화율**, 조금 움직였을 때 얼마나 변하나?" (공학/최적화)
- **벡터**: "화살표" (학교) $\to$ "**데이터의 묶음** (Feature Vector)" (AI)
- **내적**: "공식" $\to$ "**유사도** 측정기" (추천 시스템)

---

## 🛠 Action Items

`notebooks/00_math_basics.ipynb`를 다음 구조로 재작성합니다.

### Part 1. 함수와 기호 (Function & Notation)
- **Concept**: 함수는 '입력을 출력으로 매핑(Mapping)'하는 것.
- **Translation**:
    - 수학: $f(x) = x^2 + 2x + 1$
    - 코드: `def f(x): return x**2 + 2*x + 1`
- **Sigma ($\sum$)**: 수열의 합. `for` 반복문과 `sum` 내장함수로 연결.
- **Logarithm ($\log$)**: 곱셈을 덧셈으로 바꾸는 마법.
    - **Concept**: 아주 큰 수나 아주 작은 수(확률)를 다루기 편하게 만듦.
    - **Code**: `math.log(a*b) == math.log(a) + math.log(b)`.
    - **Analogy**: "지진 강도(규모)"나 "데시벨"처럼, 너무 큰 범위를 압축해서 보는 안경.

### Part 2. 미분 (Calculus): 변화를 다루는 기술
- **Concept**: 평균 변화율 vs 순간 변화율.
- **Key Question**: "입력($x$)을 아주 살짝($h$) 바꿨을 때, 출력($y$)은 얼마나 민감하게 반응하는가?"
- **Code**: 극한($\lim$)을 구현할 수 없으므로, 아주 작은 수 `h=1e-4`를 대입하여 **수치 미분(Numerical Differentiation)** 구현.

### Part 3. 선형대수 (Linear Algebra): 데이터를 담는 그릇
- **Concept**: 다차원 데이터를 다루기 위한 언어.
- **Vector**: 크기와 방향을 가진 물리량 $\to$ 여러 속성을 가진 **데이터 포인트** (예: [키, 몸무게, 나이]).
- **Dot Product (내적)**: 
    - 기하학적 의미: 투영(Projection).
    - AI 의미: **닮음(Similarity)**. 두 벡터가 같은 방향일수록 값이 큼.
- **Matrix Multiplication (행렬 곱)**:
    - **Concept**: 데이터 변환기.
    - **Check**: 모양(Shape) 맞추기 게임. `(N, M) @ (M, K) -> (N, K)`. 이것만 알면 딥러닝 에러 90% 해결.

### Part 4. 실전 최적화 (Optimization)
- **Scenario**: 안개 낀 산에서 가장 낮은 곳으로 내려가기.
- **Algorithm**: **경사하강법 (Gradient Descent)**.
    - 미분값(기울기)을 구하고, 그 반대 방향으로 조금씩 이동.
    - 이것이 딥러닝 학습의 핵심 원리임을 강조.

---

## 📝 Deliverables
- [ ] `notebooks/00_math_basics.ipynb` 전면 수정 (고등학생~성인 개발자 눈높이).
