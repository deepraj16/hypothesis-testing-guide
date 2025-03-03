# Laboratory Sample Analysis - Hypothesis Testing

## Overview
This repository contains a hypothesis testing analysis to determine whether there is a significant difference in the sample results from multiple laboratories. The goal is to analyze variations in sample measurements and assess if they are statistically significant.

## Objective
- To compare the sample means from different laboratories using statistical hypothesis testing.
- To apply **ANOVA (Analysis of Variance)** to check for significant differences among multiple sample groups.

## Hypothesis Formulation
- **Null Hypothesis (H₀):** There is **no significant difference** in the means of the sample results from different laboratories.
- **Alternative Hypothesis (H₁):** At least one laboratory's sample mean is significantly different from the others.

## Methods & Tools
- **Statistical Test Used:** One-Way ANOVA
- **Programming Language:** Python
- **Libraries Used:**
  - `pandas` (for data manipulation)
  - `numpy` (for numerical computations)
  - `scipy.stats` (for hypothesis testing)
  - `matplotlib & seaborn` (for visualization)

## Dataset
The dataset contains sample measurements from different laboratories:
- **Lab 1** (Column: `Lab 1`)
- **Lab 2** (Column: `Lab 2`)
- **Lab 3** (Column: `Lab 3`)
- **Lab 4** (Column: `Lab 4`)

## Analysis & Implementation
To perform the hypothesis test, run the following Python script:
```python
import pandas as pd
import scipy.stats as stats

# Load data
data = pd.read_csv("Laboratories.csv")

# Perform One-Way ANOVA test
f_stat, p_value = stats.f_oneway(data["Lab 1"], data["Lab 2"], data["Lab 3"], data["Lab 4"])

# Print results
print(f"F-Statistic: {f_stat}, P-Value: {p_value}")

# Interpretation
if p_value < 0.05:
    print("Reject the Null Hypothesis: There is a significant difference in sample means across laboratories.")
else:
    print("Fail to Reject the Null Hypothesis: No significant difference in sample means across laboratories.")
```

## Results & Interpretation
- **If p-value < 0.05**: Reject H₀ (At least one laboratory’s sample mean is significantly different).
- **If p-value ≥ 0.05**: Fail to reject H₀ (No significant difference in sample means across laboratories).

## Conclusion
The conclusion of the hypothesis test will be based on the computed p-value, helping to determine whether there are inconsistencies in sample results among laboratories.

## License
This project is open-source and available for educational purposes.

---
Feel free to contribute or suggest improvements! 🚀
