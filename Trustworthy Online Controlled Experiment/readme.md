# A/B Testing Process with Optimum Sample Size Calculation

## 📌 Project Overview
This project showcases a full-cycle A/B testing analysis designed to assess the impact of a new feature on user behavior, specifically measuring changes in Click-Through Rate (CTR). By calculating the optimum sample size, establishing pre-test baselines, and running a simulated test, this project highlights the importance of data-driven experimentation in product decision-making.

## 📂 Dataset Description
### 1. `Activity_pretest.csv`
- Contains user-level activity logs over a 31-day period.
- Key columns: `userid`, `dt` (date), `activity_level`
- Used to calculate Daily Active Users (DAU) as a pre-test metric.

### 2. `Ctr_pretest.csv`
- Contains CTR statistics before launching the test.
- Used to calculate the baseline CTR mean and standard deviation.

## 🧪 A/B Testing Process
### 1. **Pre-Test Metrics Calculation**
- **Daily Active Users (DAU)** were computed by filtering users with `activity_level > 0`.
- Visualized DAU trends using Altair charts.
- **CTR Baseline**: Mean CTR was calculated as **33.0%** with a standard deviation of **1.73%**.

### 2. **Minimum Detectable Effect (MDE)**
- Chosen MDE: **2.0%**, slightly higher than baseline standard deviation.
- Ensures any observed difference is meaningful.

### 3. **Sample Size Calculation**
- Applied statistical formula for sample size calculation:
  - Confidence Level: 95%
  - Power: 80%
  - MDE: 2%
- Ensured both control and treatment groups meet the minimum required sample size.

### 4. **A/B Test Execution**
- Randomized user assignment into **Control (A)** and **Treatment (B)** groups.
- Simulated CTR outcomes for each group.
- Used hypothesis testing to determine statistical significance.

## 📊 Project Output
- Generated visualizations for:
  - Daily Active Users (DAU) trends
  - Pre-test CTR distribution
  - Sample size requirements
- Confirmed whether uplift in CTR was statistically significant through hypothesis testing.

## 💥 Project Impact
- Showcased the full lifecycle of an A/B test, from hypothesis to analysis.
- Provided a clear blueprint for future experiments using CTR as a primary metric.
- Reinforced the value of robust sample size planning to prevent misleading results.

## 💡 Business Recommendations
- Adopt A/B testing as a standard framework for validating product decisions.
- Incorporate CTR and DAU as core metrics in product analytics.
- Use dynamic dashboards to monitor test performance in real time.
- Ensure proper experiment design by calculating MDE and sample size before launching tests.

## 📁 Tools & Technologies Used
- **Python**: Data analysis and hypothesis testing
- **Pandas/Numpy**: Data manipulation
- **Altair**: Interactive visualizations
- **Statistical Methods**: Sample size calculation, significance testing

---

> ✅ This project is ideal for showcasing analytical rigor, business thinking, and statistical proficiency for data analyst or product analyst roles.


