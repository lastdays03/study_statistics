# 학습 계획: 함수 매핑 심화 (Manual vs Library)

**Goal**: 수동으로 구현한 수식들이 실제 라이브러리(Numpy, Pandas, Scipy, Sklearn)의 **어떤 함수**와 매핑되는지 명확히 연결합니다.

---

## 🔍 Gap Analysis & Action Items

학습자료를 전체적으로 검토한 결과, 아래 항목들에 대한 **"Library Mapping"**이 추가되면 좋습니다.

### Session 0: Math Basics
| Concept | Manual | Library Replacement |
| :--- | :--- | :--- |
| **Sigmoid** | `1 / (1 + math.exp(-x))` | `scipy.special.expit(x)` |
| **Softmax** | `exp(x) / sum(exp(x))` | `scipy.special.softmax(x)` |
| **Gradient** | `(f(x+h) - f(x)) / h` | `scipy.misc.derivative` or `np.gradient` |

### Session 1: Descriptive Stats
| Concept | Manual | Library Replacement |
| :--- | :--- | :--- |
| **Mode (최빈값)** | `Counter(data).most_common(1)` | `scipy.stats.mode` or `df.mode()` |
| **Skewness (왜도)** | (수식 복잡함) | `df.skew()` or `scipy.stats.skew` |
| **Kurtosis (첨도)** | (수식 복잡함) | `df.kurt()` or `scipy.stats.kurtosis` |

### Session 2: Probability
| Concept | Manual | Library Replacement |
| :--- | :--- | :--- |
| **N-gram Count** | `calc_bigram_prob` (Loop) | `sklearn.feature_extraction.text.CountVectorizer(ngram=2)` |
| **Combinations** | Factorial formula | `math.comb` or `scipy.special.comb` |

### Session 3: Correlation & Regression
| Concept | Manual | Library Replacement |
| :--- | :--- | :--- |
| **Gradient Descent** | `w = w - lr * grad` (Loop) | `sklearn.linear_model.SGDRegressor` (실제 GD 사용) |
| **OLS (Exact Sol)** | `inv(X.T @ X) @ X.T @ y` | `sklearn.linear_model.LinearRegression` (Uses SVD/OLS) |
| **Cosine using Dot** | `dot / (norm * norm)` | `scipy.spatial.distance.cosine` (Note: returns distance ($1-Sim$)) |

---

## 🛠 Execution Plan

1.  **Session 0 업데이트**: Sigmoid, Softmax, Log (np.log vs math.log) 비교 추가.
2.  **Session 1 업데이트**: Pandas의 왜도(`skew`), 첨도(`kurt`) 함수 소개 (정규성 검정용).
3.  **Session 3 업데이트**: `LinearRegression`과 `SGDRegressor`의 차이점(해석적 해 vs 수치적 최적화) 설명 추가.

## 📝 Deliverables
- [ ] Update `notebooks/00_math_basics.ipynb`
- [ ] Update `notebooks/01_descriptive_stats.ipynb`
- [ ] Update `notebooks/02_probability_distribution.ipynb`
- [ ] Update `notebooks/03_correlation_regression.ipynb`
