# 🧪 A/B Testing Process with Optimum Sample Size Calculation

## 🧭 Context / Table of Contents
- [📌 Project Overview](#-project-overview)
- [🎯 Project Objectives](#-project-objectives)
- [🔍 Problem Statement](#-problem-statement)
- [🗂️ Dataset Description](#-dataset-description)
- [🧪 A/B Testing Process](#-ab-testing-process)
- [📊 Project Output](#-project-output)
- [📈 Data Storytelling](#-data-storytelling)
- [🧠 Decision-Making](#-decision-making)
- [🌍 Project Impact](#-project-impact)
- [💼 Business Recommendations](#-business-recommendations)

---

## 📌 Project Overview

![Project Banner](https://github.com/user-attachments/assets/24de73e6-517e-4293-bb34-bae0703a351f)

This project demonstrates a complete A/B testing workflow to evaluate the impact of a new feature on user behavior (Click-Through Rate - CTR). It covers optimum sample size calculation, baseline metric setup, randomized group assignment, simulation, hypothesis testing, and final recommendations.

---

## 🎯 Project Objectives

- Design a statistically sound A/B testing framework.
- Calculate optimal sample size using confidence level, power, and MDE.
- Simulate test/control group data and CTR performance.
- Apply Two-Proportion Z-Test for result validation.
- Communicate outcomes and suggest business actions.

---

## 🔍 Problem Statement

A digital product team wants to evaluate whether a proposed change (UI/feature/offer) improves the conversion rate. Instead of deploying it blindly, they want to validate the effect through a rigorous A/B testing process.

---

## 🗂️ Dataset Description

| Dataset Name        | Purpose |
|---------------------|---------|
| `Activity_pretest.csv` | Logs user activity over 31 days to calculate DAU |
| `Ctr_pretest.csv`      | Provides baseline CTR mean and standard deviation |
| `Activity_all.csv`     | Tracks activity levels across test groups |
| `Assignments.csv`      | Records test/control group assignment for 8807 users |
| `Ctr_all.csv`          | Shows CTR values for both groups after rollout |

---

## 🧪 A/B Testing Process

### 📍 Step 1: Pre-Test Metrics
- Calculated **Daily Active Users (DAU)** from activity logs.
- Found baseline **CTR** = **33.0%**, SD = **1.73%**

### 📍 Step 2: Define Parameters
- Baseline CTR: **10%**
- Minimum Detectable Effect (MDE): **3%**
- Significance Level (α): **0.05**
- Power (1-β): **80%**

### 📍 Step 3: Sample Size Calculation
Used `statsmodels` to find that each group needs **at least 1,356 users**.

### 📍 Step 4: Simulate & Assign Data
- Simulated outcomes for:
  - **Control Group**: 10% CTR
  - **Treatment Group**: 13% CTR
- Randomly assigned users into groups.

### 📍 Step 5: Hypothesis Testing
- Applied **Two-Proportion Z-Test**
- **p-value = 0.0021** → Statistically significant

---

## 📊 Project Output

Visualizations included:
- 📈 Daily Active Users trend  
- 🎯 CTR distribution before & after test  
- 📊 Sample size calculator output  
- ✅ Significant uplift in Treatment group CTR

![DAU](https://github.com/user-attachments/assets/08f5c67e-e86c-4834-96e3-92fd5f1c6d5a)
![CTR](https://github.com/user-attachments/assets/636970ce-a235-43f2-9adf-3ec544acc622)
![Sample Size](https://github.com/user-attachments/assets/79da2051-ec54-4306-8dad-093c74b2d890)

---

## 📈 Data Storytelling

> “The A/B test showed a **3% uplift in CTR**, backed by a **p-value of 0.0021**. With 1,350+ users per group and proper power/MDE setup, this confirms the effectiveness of the change. The data supports a full rollout.”

---

## 🧠 Decision-Making

✔️ **Decision**: Roll out to 100% of users

**Why?**
- Statistically significant uplift
- Minimum required power and sample size achieved
- Business value confirmed

---

## 🌍 Project Impact

- ✅ Strengthened culture of data-driven product testing
- ✅ Reduced guesswork in feature releases
- ✅ Set a reusable testing framework for future launches

---

## 💼 Business Recommendations

1. **Standardize A/B Testing for All Feature Launches**
2. **Always Calculate Sample Size Before Running Tests**
3. **Track Guardrail Metrics (Bounce, Time-on-Page, etc.)**
4. **Document Learnings from Every Experiment**
5. **Use Controlled Rollouts (10–20% → 100%)**

---

## 🏷️ Tags

`A/B Testing` `Z-Test` `CTR Analysis` `Hypothesis Testing` `Product Analytics` `Experimentation` `Sample Size` `MDE` `Python` `statsmodels`

---
