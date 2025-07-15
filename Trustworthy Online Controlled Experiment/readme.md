# A/B Testing Process with Optimum Sample Size Calculation

## 📈 Project Overview

![A/B Testing Overview](https://github.com/user-attachments/assets/24de73e6-517e-4293-bb34-bae0703a351f)

This project showcases a complete A/B testing pipeline to evaluate the impact of a new feature on user behavior, specifically changes in Click-Through Rate (CTR). From calculating the optimal sample size to conducting statistical hypothesis testing, the project demonstrates how experimentation can guide product decisions.

---

## 📊 Project Objectives

* Design a statistically sound A/B testing framework
* Calculate optimal sample size using statistical power
* Simulate real-world control and treatment group data
* Conduct hypothesis testing using a two-proportion Z-test
* Drive a business decision backed by data

---

## 🔍 Problem Statement

A digital product team wants to evaluate whether a UI or feature change improves the user conversion rate. The team opts to use A/B testing rather than intuition to ensure measurable results.

---

## 📂 Dataset Description

* **Activity\_pretest.csv**: 31-day user activity logs (`userid`, `dt`, `activity_level`) to calculate Daily Active Users (DAU).
* **Ctr\_pretest.csv**: Historical CTR data to establish a pre-test baseline.
* **Activity\_all.csv**: Tracks user activity across control and treatment groups.
* **Assignments.csv**: Group assignment data for 8,807 users.
* **Ctr\_all.csv**: Post-test CTR data across both groups.

---

## 🧪 A/B Testing Workflow

### 1. Pre-Test Metrics Calculation

* **DAU** calculated for users with `activity_level > 0`.
* CTR baseline calculated as **33.0%** with a standard deviation of **1.73%**.

### 2. Minimum Detectable Effect (MDE)

* Chosen MDE: **2%** to represent a meaningful uplift beyond baseline noise.

### 3. Sample Size Calculation

* Confidence Level: 95%
* Power: 80%
* MDE: 2%
* Result: **1,356 users per group**

### 4. Randomized Assignment

* Randomized users into Control (A) and Treatment (B).

### 5. Hypothesis Testing

* **Null Hypothesis (H0)**: No difference in conversion rates.
* **Alternative Hypothesis (H1)**: Treatment conversion rate is higher.
* Test: **Two-Proportion Z-Test**
* **p-value**: **0.0021** (statistically significant)

---

## 📊 Project Output

* Visuals:

  * DAU trend
  * CTR baseline distribution
  * Sample size calculator result

* Result:

  * Treatment group showed **3% higher CTR**.
  * Statistically significant improvement confirmed via hypothesis test.

![DAU Trend](https://github.com/user-attachments/assets/08f5c67e-e86c-4834-96e3-92fd5f1c6d5a)
![CTR Distribution](https://github.com/user-attachments/assets/636970ce-a235-43f2-9adf-3ec544acc622)

---

## 📈 Data Storytelling

> “The A/B test showed a **3% uplift** in conversion rate for the treatment group. The test met all statistical thresholds for reliability, confirming the new feature positively impacted user behavior.”

---

## 🧠 Decision-Making

* **Decision**: Roll out the change to all users.
* **Why?**:

  * Statistically significant result (p = 0.0021)
  * Required sample size and power met
  * Meaningful and positive uplift in conversion

---

## 🌍 Project Impact

* Reinforced **data-driven decision-making**
* Reduced **subjective bias** in feature releases
* Built a **repeatable experimentation framework**
* Delivered **measurable insights** for product improvements

---

## 💼 Business Recommendations

1. **Institutionalize A/B Testing**

   * Adopt testing for all major feature releases.
2. **Pre-Test Sample Size Calculation**

   * Ensure statistical power in every experiment.
3. **Track Guardrail Metrics**

   * Include bounce rate, session length, etc., during live tests.
4. **Maintain Experiment Logs**

   * Build internal knowledge around testing outcomes.
5. **Use Phased Rollouts**

   * Start with 10–20% exposure to reduce risks before full release.

---
