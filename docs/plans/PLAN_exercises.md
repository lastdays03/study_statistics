# 학습 계획: 실전 연습문제 (Practice Drills)

**Goal**: "눈으로 본 것"을 "내 손으로 짤 수 있는 것"으로 바꿉니다.
**Format**: 각 Session의 메인 노트북과 짝을 이루는 `_exercises.ipynb` 파일을 생성합니다.

---

## 📅 Roadmap (Exercise Notebooks)

### 구조 (Structure)
각 연습문제 노트북은 다음 3단계로 구성됩니다.

1.  **🧩 Concept Quiz (O/X 및 단답형)**
    - 이론적인 이해가 되었는지 확인합니다.
    - 예: "표본분산의 분모는 $n$인가 $n-1$인가?"
2.  **⌨️ Coding Drill (빈칸 채우기)**
    - 핵심 알고리즘의 뼈대를 주고 `TODO`를 채웁니다.
    - 예: `def my_variance(data): ... # TODO`
3.  **🔥 Challenge (응용 문제)**
    - 가이드 없이 처음부터 끝까지 구현해봅니다.
    - 예: "주어진 텍스트 파일에서 단어 빈도를 세고 Zipf 분포 그래프를 그리시오."

---

## 🛠 Deliverables

### [Session 0] `notebooks/00_math_basics_exercises.ipynb`
- $\sum$를 `for`문으로 바꾸는 연습.
- `h`값을 바꿔가며 미분 오차 줄이기 챌린지.
- 두 벡터가 가장 비슷한(내적이 큰) 쌍 찾기.

### [Session 1] `notebooks/01_descriptive_stats_exercises.ipynb`
- `numpy.var()` 안 쓰고 분산 구하기 (복습).
- 이상치(Outlier)를 제거했을 때와 안 했을 때의 평균 변화 관찰.

### [Session 2] `notebooks/02_probability_distribution_exercises.ipynb`
- 주사위 2개를 던져서 합이 7이 나올 확률 시뮬레이션.
- 어떤 문서에서 특정 단어가 나올 조건부 확률 계산 함수 작성.

### [Session 3] `notebooks/03_correlation_regression_exercises.ipynb`
- $y = 3x + 5$ 데이터를 만들고 경사하강법으로 3과 5 찾아내기.
- 상관계수가 0인데 관계가 있는 경우(2차 함수 등) 찾아보기.

### [Session 4] `notebooks/04_vectors_evaluation_exercises.ipynb`
- Precision, Recall 직접 계산 함수 만들기.
- 3차원 공간에서 가장 거리가 먼 두 점 찾기.

---

## ✅ Success Criteria
- [ ] 정답(Solution)은 노트북의 맨 아래에 'Hidden Cell' 혹은 별도 섹션으로 제공하여, 스스로 고민할 시간을 확보했는가?
- [ ] 메인 노트북을 보지 않고 풀 수 있는 수준인가?
