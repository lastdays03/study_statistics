# 📊 AI/LLM 엔지니어를 위한 실전 통계학 (Deep Theory Edition)

> **"라이브러리만 임포트하지 말고, 그 뒤에 있는 수학을 이해하세요."**

이 저장소는 **LLM, RAG, 머신러닝** 개발자를 위해 설계된 엄격한 독학 커리큘럼입니다. 단순한 API 호출을 넘어, 견고한 AI 시스템을 구축하고 평가하는 데 필요한 **수학적 기초**와 **통계적 직관**을 기르는 데 집중합니다.

---

## 🧠 학습 철학: "Deep Dive" 사이클

이 커리큘럼의 모든 세션은 **Study Planner Workflow**에 기반한 4단계 구조를 따릅니다:

1.  **📐 Deep Theory (이론)**:
    - 수학적 정의($\sum, \int, \partial$)의 정확한 이해.
    - 공식 유도 (예: 표본 분산은 왜 $n-1$로 나누는가?).
2.  **💻 Manual Implementation (구현)**:
    - Python 기본 기능이나 `numpy`만을 사용하여 통계 함수를 **밑바닥부터 구현**.
    - 원리를 완벽히 이해하기 전까지는 `scikit-learn`이나 `scipy` 사용 지양.
3.  **📖 Concepts & Insight (직관)**:
    - 수학적 개념을 실제 AI 문제(RAG 청킹, 토큰 분포 등)와 연결.
4.  **🧪 Experiment & Verify (실험)**:
    - 시뮬레이션을 통한 이론 검증 (예: 몬테카를로, 대수의 법칙).

---

## 📚 커리큘럼 로드맵

총 4개의 집중 세션으로 구성되며, 각 세션은 하나의 **통합 노트북(Integrated Notebook)**으로 제공됩니다.

### [Session 0: Math Basics (Survival Kit)](notebooks/00_math_basics.ipynb)
- **목표**: "수포자"를 위한 코드 기반 수학 입문.
- **핵심 주제**:
    - **Theory as Code**: $\sum, \prod$ 기호를 파이썬 `for`, `sum`으로 1:1 매핑.
    - **미분(Derivative)**: 공식을 외우지 않고 '수치 미분' 코드로 경사하강법 구현.
    - **선형대수**: 벡터 내적(=유사도)의 직관적 이해.

### [Session 1: 데이터 문해력과 기술 통계](notebooks/01_descriptive_stats.ipynb)
- **목표**: 통계의 언어와 데이터의 본질 이해.
- **핵심 주제**:
    - 모집단 vs 표본 표기법 ($N, \mu$ vs $n, \bar{x}$).
    - **자유도(Degrees of Freedom)**: 베셀 보정(Bessel's Correction, $n-1$)의 비밀.
    - 평균 vs 중앙값: RAG 문서 길이의 이상치(Outlier) 처리.

### [Session 2: 확률과 분포](notebooks/02_probability_distribution.ipynb)
- **목표**: 언어 모델(Language Model)의 확률적 본질 파악.
- **핵심 주제**:
    - **확률의 공리**: 집합론적 기초.
    - **베이즈 정리**: 증거를 통한 믿음의 갱신 (Prior -> Posterior).
    - **분포**: 정규분포, 로그 정규분포, **Zipf's Law** (텍스트의 멱법칙).
    - **몬테카를로 시뮬레이션**: 난수로 $\pi$ 추정하기.

### [Session 3: 상관관계와 회귀 분석](notebooks/03_correlation_regression.ipynb)
- **목표**: 기계가 관계를 "학습"하는 방법 이해.
- **핵심 주제**:
    - **공분산 & 상관계수**: 수식 유도 및 정규화.
    - **최소제곱법 (OLS)**: 미분을 통한 $w, b$ 최적해 도출.
    - **경사하강법 (Gradient Descent)**: 딥러닝의 핵심 알고리즘 직접 구현.

### [Session 4: 벡터와 평가](notebooks/04_vectors_evaluation.ipynb)
- **목표**: 고차원 공간의 기하학 마스터.
- **핵심 주제**:
    - **내적(Dot Product) & 코사인 유사도**: 기하학적 해석.
    - **평가지표**: Precision, Recall, F1-score (조화 평균을 쓰는 이유).
    - **차원의 저주**: 고차원에서 왜 기존 인덱싱이 실패하는가?

---

## 🚀 시작하기 (Getting Started)

### 필수 요구사항
- Python 3.8+
- Jupyter Notebook / Lab

### 설치 방법
1.  이 저장소를 클론합니다.
2.  의존성 라이브러리를 설치합니다:
    ```bash
    pip install -r requirements.txt
    ```

### 세션 실행
Jupyter Notebook 서버를 실행하고 Session 1을 엽니다:
```bash
jupyter notebook notebooks/01_descriptive_stats.ipynb
```

---

## 📂 프로젝트 구조

```
.
├── notebooks/          # 핵심: 통합 학습 노트북
│   ├── 00_math_basics.ipynb
│   ├── 00_math_basics_exercises.ipynb
│   ├── 01_descriptive_stats.ipynb
│   ├── 01_descriptive_stats_exercises.ipynb
│   └── ... (각 세션별 _exercises.ipynb 포함)
├── docs/
│   └── plans/          # 커리큘럼 설계 문서
├── references/         # 참고 자료 (Skill, Templates)
└── requirements.txt    # Python 의존성 목록
```

---

## 📝 라이선스
개인 학습용 자료입니다.
