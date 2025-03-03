# Diameter of the Cutlet - Hypothesis Testing

## Overview
This repository contains a hypothesis testing analysis to determine whether there is a significant difference in the diameters of cutlets produced by two different manufacturing units (Unit A and Unit B).

## Objective
- To compare the mean diameters of cutlets from **Unit A** and **Unit B** using statistical hypothesis testing.
- To apply a **Two-Sample t-test** to assess if the observed differences are statistically significant.

## Hypothesis Formulation
- **Null Hypothesis (H₀):** There is **no significant difference** in the mean diameters of cutlets from Unit A and Unit B.
- **Alternative Hypothesis (H₁):** There **is a significant difference** in the mean diameters of cutlets from Unit A and Unit B.

## Methods & Tools
- **Statistical Test Used:** Two-Sample t-test
- **Programming Language:** Python
- **Libraries Used:**
  - `pandas` (for data manipulation)
  - `numpy` (for numerical computations)
  - `scipy.stats` (for hypothesis testing)
  - `matplotlib & seaborn` (for visualization)

## Dataset
The dataset contains diameter measurements of cutlets from two different production units:
- **Unit A** (Column: `Unit A`)
- **Unit B** (Column: `Unit B`)

## Analysis & Implementation
To perform the hypothesis test, run the following Python script:
```python
import pandas as pd
import scipy.stats as stats

# Load data
data = pd.read_csv("Cutlets.csv")

# Perform Two-Sample t-test
t_stat, p_value = stats.ttest_ind(data["Unit A"], data["Unit B"])

# Print results
print(f"T-Statistic: {t_stat}, P-Value: {p_value}")

# Interpretation
if p_value < 0.05:
    print("Reject the Null Hypothesis: There is a significant difference in cutlet diameters.")
else:
    print("Fail to Reject the Null Hypothesis: No significant difference in cutlet diameters.")
```

## Results & Interpretation
- **If p-value < 0.05**: Reject H₀ (There is a significant difference in cutlet diameters).
- **If p-value ≥ 0.05**: Fail to reject H₀ (No significant difference in cutlet diameters).

## Conclusion
The conclusion of the hypothesis test will be based on the computed p-value, helping to determine whether the production process affects cutlet size consistency.

## License
This project is open-source and available for educational purposes.

---
Feel free to contribute or suggest improvements! 🚀
