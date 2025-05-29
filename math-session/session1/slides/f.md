# **Algebra and Linear Algebra in AI and Trading: Predicting Stock Prices with AI**

---

## **Introduction: How AI Relies on Algebra**

In AI-driven trading, algebra and linear algebra form the backbone of predictive systems.

Imagine Alex, a data scientist at a hedge fund, using AI to predict Nvidia’s stock price based on news sentiment scores. Behind the scenes, linear and quadratic equations—the core of algebra—power these AI models, turning raw market data into actionable insights.

Alex’s goal: predict the percentage change in stock price (y) given a sentiment score (x). We’ll explore how he builds, tests, and applies both linear and quadratic models to navigate a volatile market.

---

## **Polished Core Lecture**

### **Step 1: Linear Models – The Foundation of AI Predictions**

AI often starts with a **linear model**, grounded in linear algebra:

$$
 y = m x + b
$$

* \$y\$: predicted stock price change
* \$x\$: sentiment score
* \$m\$: slope (learned by AI)
* \$b\$: intercept (adjusted by AI)

This is called **linear regression**—algorithms use linear algebra to fit the best line through data.

**Example:** if AI learns \$m=5\$, \$b=0\$, and \$x=0.8\$:

$$
 y = 5 \times 0.8 + 0 = 4\%
$$

**Activity 1:** Test AI’s Prediction: for \$x=0.6\$ in \$y=5x+0\$, predict \$y\$.
**Answer:** \$y=5\times0.6=3%\$

---

### **Step 2: Quadratic Models – Capturing Non-Linear Trends**

When sentiment triggers unpredictable swings, AI uses a **quadratic model**:

$$
 y = a x^2 + b x + c
$$

The \$x^2\$ term captures non-linear patterns—essential in volatile markets.

**Example:** if AI learns \$a=-2\$, \$b=5\$, \$c=1\$, and \$x=0.8\$:

$$
 y = -2(0.8)^2 + 5(0.8) + 1 = 3.72\%
$$

**Activity 2:** Why Quadratic?
Answer: the \$x^2\$ term bends the curve, catching big jumps or drops that a straight line misses.

---

### **Step 3: How AI Learns Using Linear Algebra in Python**

AI uses **least squares**, a matrix-based method, to learn coefficients from data.

```python
import numpy as np
from sklearn.linear_model import LinearRegression

# Data
X = np.array([0.3, -0.5, 0.8, 0.2, 0.7]).reshape(-1,1)
 y = np.array([1.2, -3.8, 4.1, 1.0, 4.0])

# Fit linear model\ nmodel = LinearRegression().fit(X, y)
 print(model.coef_, model.intercept_)
 print("Prediction for x=0.7:", model.predict([[0.7]]) )
```

**Activity 3:** Modify code to predict for \$x=0.4\$ (replace `[[0.7]]` with `[[0.4]]`, expect \~2.3%).

---

### **Step 4: AI Tests and Compares Models**

AI backtests both models on historical data:

* Calculate error metrics (MSE, MAE).
* Compare linear vs. quadratic.

**Activity 4:** Identify outlier in points (0.3,1.2),(-0.5,-3.8),(0.8,4.1),(-0.9,-10.0).
**Answer:** (-0.9,-10.0) — extreme drop challenging the model.

---

## **Detailed Data, Equations & Predictions**

### **Dataset**

| News Event                    | Sentiment (x) | Actual Change (y) |
| ----------------------------- | ------------: | ----------------: |
| Positive Apple Product Launch |           0.9 |               +5% |
| Negative CEO Resignation      |          -0.8 |               -6% |
| Neutral Fed Rate Decision     |           0.2 |               +1% |
| Strong U.S. Election Outcome  |           0.7 |               +4% |
| Economic Crisis Announced     |          -0.9 |              -10% |

The economic crisis point (-0.9, -10%) is an outlier, hinting at non-linear dynamics.

---

### **Linear Model Fit**

Using least squares on these five points produces:

$$
 y = 7.7 x - 1.4
$$

**Predictions:**

| Event             |    x | Actual y | Predicted y |
| ----------------- | ---: | -------: | ----------: |
| Apple Launch      |  0.9 |      +5% |       +5.5% |
| CEO Resignation   | -0.8 |      -6% |       -7.6% |
| Fed Rate Decision |  0.2 |      +1% |       +0.2% |
| Election Outcome  |  0.7 |      +4% |       +4.0% |
| Economic Crisis   | -0.9 |     -10% |       -8.3% |

* Underestimates extreme downturns.

**Activity:** Predict at x=-0.5: \$7.7(-0.5)-1.4=-5.25%\$.

---

### **Quadratic Model Fit**

Fitting a quadratic to key points yields:

$$
 y = -2.5 x^2 + 8.3 x - 0.6
$$

**Predictions:**

| Event             |    x | Actual y | Quadratic y |
| ----------------- | ---: | -------: | ----------: |
| Apple Launch      |  0.9 |      +5% |       +4.9% |
| CEO Resignation   | -0.8 |      -6% |       -8.8% |
| Fed Rate Decision |  0.2 |      +1% |       +1.1% |
| Election Outcome  |  0.7 |      +4% |       +4.0% |
| Economic Crisis   | -0.9 |     -10% |      -10.0% |

* Matches extremes but can overfit moderate negatives.

**Activity:** Explain how \$x^2\$ captures non-linearity at extremes.

---

## **Applying Models to New Sentiment**

For a hypothetical regulatory shock (x=-0.5):

* **Linear:** \$y=7.7(-0.5)-1.4=-5.25%\$
* **Quadratic:** \$y=-2.5(0.25)+8.3(-0.5)-0.6=-5.38%\$

Both suggest \~–5.3% drop, guiding Alex’s decision to reduce positions.

---

## **Conclusion & Next Steps**

**Key Takeaways:**

* **Linear models:** Simple, interpretable, good for moderate moves.
* **Quadratic models:** Handle volatility, capture extreme swings.

**Next Steps:**

1. Explore higher-degree polynomials or regularization (Ridge, Lasso).
2. Add features: volume, technical indicators, macro variables.
3. Deploy models in real-time trading pipelines with continuous backtesting.

---

*End of Comprehensive Lecture*

