# A/B Testing with Python

## 📌 Project Overview
This project demonstrates how to apply **A/B testing** and hypothesis testing in Python to evaluate the effectiveness of a marketing campaign using the `marketing_AB.csv` dataset. The goal is to determine whether the 'ad' group (exposed to the new campaign) performs significantly better than the 'psa' group (public service announcement).

---

## 🛠️ Tools & Libraries
- Python (pandas, numpy, scipy, matplotlib, seaborn)
- Jupyter Notebook (`marketing_ab_analysis.ipynb`)

---

## 📂 Dataset
The `marketing_AB.csv` dataset simulates user behavior in a marketing campaign, with columns like:
- `user id` – unique customer ID
- `test group` (renamed to `group`) – 'ad' (treatment) or 'psa' (control)
- `converted` – 1 if the user converted (purchase/click), 0 otherwise
- `total ads` – total ads seen by the user
- `most ads day` – day of the week when most ads were seen
- `most ads hour` – hour of the day when most ads were seen

---

## 🔑 Steps Performed (in `marketing_ab_analysis.ipynb`)
1. **Data Loading and Preprocessing**
   - Loaded `marketing_AB.csv`.
   - Renamed the 'test group' column to 'group'.
   - Converted the 'converted' column to integer type (0 or 1).

2. **Conversion Rate Calculation**
   - Computed conversion rates for 'ad' and 'psa' groups.

3. **Visualization**
   - Plotted conversion rates for each group using a bar chart.

4. **Hypothesis Testing**
   - Null Hypothesis (H0): No difference in conversion between 'ad' and 'psa' groups.
   - Alternative Hypothesis (H1): The 'ad' campaign has a different conversion rate than 'psa'.
   - Conducted a **two-sample t-test** to check statistical significance.

5. **Results**
   - 'ad' group conversion: 2.55%
   - 'psa' group conversion: 1.79%
   - T-statistic: 7.3704
   - P-value: 0.0000 (indicating statistical significance)


## ✅ Key Insights
- A/B testing confirms whether a change (UI, campaign, or feature) impacts conversions.
- In this case, the **'ad' marketing campaign significantly improved conversion rates** compared to the 'psa' group.
