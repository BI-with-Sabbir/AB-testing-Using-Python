# A/B Testing Process with Optimum Sample Size Calculation

## 📌 Project Overview
![image](https://github.com/user-attachments/assets/24de73e6-517e-4293-bb34-bae0703a351f)

This project showcases a full-cycle A/B testing analysis designed to assess the impact of a new feature on user behavior, specifically measuring changes in Click-Through Rate (CTR). By calculating the optimum sample size, establishing pre-test baselines, and running a simulated test, this project highlights the importance of data-driven experimentation in product decision-making.


## 📌 Project Objectives

- Design a trustworthy A/B testing framework
- Calculate the optimal sample size based on statistical power
- Simulate real-world data for both control and treatment groups
- Apply a two-proportion Z-test to determine statistical significance
- Provide a data-driven decision and business recommendations

## 🔍 Problem Statement

A digital product company wants to assess whether a proposed product change (e.g., feature, UI improvement, or partnership) improves the user conversion rate. Instead of relying on intuition, the team uses A/B testing to validate the impact of the change with statistical rigor.




## 📂 Dataset Description
### 1. `Activity_pretest.csv`
- Contains user-level activity logs over a 31-day period.
- Key columns: `userid`, `dt` (date), `activity_level`
- Used to calculate Daily Active Users (DAU) as a pre-test metric.

### 2. `Ctr_pretest.csv`
- Contains CTR statistics before launching the test.
- Used to calculate the baseline CTR mean and standard deviation.

### 3. 'Activity_all.csv'
-Comparing Activity (activeness and activity_level) between the Groups.

### 4. 'Assignments.csv'
- We first need to randomly assign the test to 8,807 Users.
- We have the Assignment Data in the "Assignment.csv". We will load the dataset and inspect whether the assignment was done properly between the two groups.

### 5. 'Ctr_all.csv'
- Clear Increament between the groups after the test started
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

  ## 🧪 A/B Testing Workflow

### 1. Hypothesis Formulation
- **Null Hypothesis (H₀)**: There is no difference in conversion rates between control and treatment.
- **Alternative Hypothesis (H₁)**: The treatment group has a higher conversion rate.

### 2. Define Key Parameters
- **Baseline Conversion Rate**: 10%
- **Minimum Detectable Effect (MDE)**: 3%
- **Significance Level (α)**: 0.05
- **Power (1-β)**: 0.80

### 3. Sample Size Calculation
Using `statsmodels.stats.power` module:
- ✅ Minimum required sample size per group: **1,356**

### 4. Data Generation
Simulated data for:
- **Control Group**: 10% conversion
- **Treatment Group**: 13% conversion

### 5. Hypothesis Testing
- Test: Two-Proportion Z-Test
- **p-value**: 0.0021


## 📊 Project Output
- Generated visualizations for:
  - Daily Active Users (DAU) trends
![image](https://github.com/user-attachments/assets/08f5c67e-e86c-4834-96e3-92fd5f1c6d5a)
![image](https://github.com/user-attachments/assets/b06dfebf-e8a4-4fd0-876d-69e3ab5136f3)


  - Pre-test CTR distribution
![image](https://github.com/user-attachments/assets/636970ce-a235-43f2-9adf-3ec544acc622)

  - Sample size requirements
![image](https://github.com/user-attachments/assets/79da2051-ec54-4306-8dad-093c74b2d890)

- Confirmed whether uplift in CTR was statistically significant through hypothesis testing.

## 📈 Data Storytelling

> “The A/B test showed that the proposed change resulted in a 3% uplift in conversion rate, with strong statistical support (p = 0.0021). With over 1,350 users per group, the test was powered to detect even modest improvements. The data clearly justified rolling out the change to all users.”

---

## 🧠 Decision-Making

✔️ **Decision**: Roll out the proposed change to the entire user base.

**Justification:**
- Statistically significant uplift in conversion rate
- Minimum detectable effect achieved
- Sample size and power correctly calculated
- Strong evidence supports a positive business outcome

---

## 🌍 Project Impact

- ✅ Reinforced data-driven culture in product development
- ✅ Reduced risk of subjective decision-making
- ✅ Introduced robust experimental design principles
- ✅ Enabled measurable, repeatable results from testing

---

## 💼 Business Recommendations

1. **Adopt A/B Testing as a Standard Practice**  
   Integrate experimentation into every product change or partnership decision.

2. **Always Calculate Sample Size Beforehand**  
   Avoid underpowered tests that waste traffic and time.

3. **Monitor Guardrail Metrics**  
   In real scenarios, track bounce rate, session duration, etc.

4. **Document Experiment Results**  
   Maintain an experimentation logbook for internal learning and repeatability.

5. **Use a Gradual Rollout Strategy**  
   Start with 10–20% exposure and scale up as success is confirmed.

---



