# A/B-Testing-Project, E-commerce Conversion Optimization
## 📌 Overview
This project demonstrates how A/B testing can be applied to measure the impact of product or design changes on conversion rates.
The dataset comes from an e-commerce experiment where users were randomly assigned to:
         - **Control Group** → old website design
         - **Treatment Group** → new website design
The business goal is to evaluate whether the new design **improves conversion rates**.

## 🎯 Objectives
1. Define and test hypotheses for conversion improvement.
2. Explore and visualize the dataset.
3. Perform a two-proportion z-test to check statistical significance.
4. Compute confidence intervals for conversion rate differences.
5. Conduct power analysis to ensure the test is adequately powered.
6. Translate results into business insights & recommendations.

## 🗂️ Dataset
- **Columns:**
    - user_id → Unique identifier for users
    - timestamp → Date of visit
    - group → Control (old) or Treatment (new)
    - landing_page → Page version shown
    - converted → 1 if user converted, 0 otherwise
- **Source:** [Kaggle – E-commerce A/B Testing Dataset](https://www.kaggle.com/datasets/putdejudomthai/ecommerce-ab-testing-2022-dataset1?utm_source=chatgpt.com)

## 🔍 Methodology
1. **Data Cleaning**
     - Removed duplicates and missing values.
     - Checked balance between control & treatment groups.
2. **Exploratory Data Analysis (EDA)**
     - Conversion rates by group.
     - Distribution of users across groups.
     - Visual comparisons (bar plots, line trends).
3. **Statistical Testing**
     - **Null Hypothesis (H₀)**: Conversion rates are equal.
     - **Alternative Hypothesis (H₁)**: Conversion rates are different.
     -  Applied **two-proportion z-test** with α = 0.05.
     -  Calculated **95% confidence interval** for conversion difference.
4. **Power Analysis**
     - Checked statistical power (>0.8 preferred).
     - Ensured sample size was adequate for detecting meaningful effects.
  
## 📊 Results
     - Z-statistic: 1.19
     - P-value: 0.2323
     - 95% Confidence Interval for difference: [-0.0009, 0.0038]

## ✅ Interpretation
  - Since **p-value > 0.05**, we **fail to reject the null hypothesis**.
  -  The confidence interval for the difference includes 0, suggesting  **no statistically            significant improvement in conversion**.
  -  In other words, the new design did **not significantly outperform the old design**.
    
## 💡 Business Insights
  - The test suggests rolling out the new design may not yield higher conversions.
  - Further experiments could explore:
         - Segment-level testing (e.g., by device type, geography).
         - Alternative design changes or content personalization.
         - Running the test longer to collect more data.
    
## 🛠️ Tech Stack
  - **Python** (pandas, numpy, matplotlib, seaborn)
  - **Statsmodels** (proportions z-test, confidence intervals, power analysis)
  - **Google Collab** for analysis and storytelling
