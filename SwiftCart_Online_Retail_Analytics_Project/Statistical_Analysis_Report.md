# SwiftCart Statistical Analysis Report

## Distribution
- Mean Amount: **₹682.07**
- Median Amount: **₹646.00**
- Standard deviation: **₹268.58**
- Skewness: **1.0529**
- Excess kurtosis: **1.7687**

## Hypothesis Test 1 — Channel vs Status
- H₀: Channel and Status are independent.
- H₁: Channel and Status are associated.
- Test: Chi-square test of independence.
- α = 0.05
- χ² = **10.13**
- p-value = **0.927479**
- Decision: **Do not reject H₀**

## Hypothesis Test 2 — Amount by Gender
- H₀: Mean Amount is equal for Women and Men.
- H₁: Mean Amount differs.
- Test: Welch's independent two-sample t-test.
- α = 0.05
- t = **-56.7371**
- p-value = **0**
- Decision: **Reject H₀**

## Hypothesis Test 3 — Amount by Category
- H₀: All category mean amounts are equal.
- H₁: At least one category mean differs.
- Test: One-way ANOVA.
- α = 0.05
- F = **2,881.4376**
- p-value = **0**
- Decision: **Reject H₀**

## 95% Confidence Interval
- Mean Amount: **₹682.07**
- 95% CI: **₹679.09 to ₹685.06**

The confidence interval estimates the population mean under standard sampling assumptions; it is not an interval containing 95% of individual transactions.
