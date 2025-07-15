# 📊 A/B Testing in Python: SEO/Digital Marketing Campaign Analysis

## 📃 Context / Table of Contents

* [📈 Project Overview](#-project-overview)
* [🎯 Project Goal](#-project-goal)
* [⚙️ Implementation Steps](#-implementation-steps)
* [📊 Results & Interpretation](#-results--interpretation)
* [💡 Real-World Applications](#-real-world-applications)
* [📄 Conclusion](#-conclusion)

---

## 📈 Project Overview

A/B testing is a statistical method used to compare two different groups and determine whether there is a significant difference between them. In this project, we analyze the performance metrics of two different SEO/Digital Marketing campaigns to identify which strategy is more effective.

---

## 🎯 Project Goal

The goal of this project is to evaluate the effectiveness of two different marketing campaigns (Group A and Group B) based on four key performance indicators (KPIs):

* **Impression**: Number of times the advertisement was viewed.
* **Click**: Number of times the advertisement was clicked.
* **Purchase**: Number of purchases made as a result of the campaign.
* **Earning**: Total revenue generated from purchases.

Using statistical hypothesis testing, we aim to determine if the differences in these metrics between the two campaigns are statistically significant.

---

## ⚙️ Implementation Steps

### Step 1: Importing the Dataset

* Loaded two Excel sheets representing Group A and Group B using `pandas.read_excel()`.

### Step 2: Data Preprocessing & Feature Engineering

* Created new feature **Earning per Purchase**.
* Added a **Group** column to distinguish A and B.

### Step 3: Exploratory Data Analysis (EDA)

* Summary statistics calculated.
* Histograms and boxplots visualized KPIs across both groups.

### Step 4: Testing Normality

* Used **Shapiro-Wilk Test** for each metric.
* p-value < 0.05 → not normally distributed.

### Step 5: Testing Homogeneity of Variance

* If data was normal, **Levene’s Test** would have been used.
* Not applicable as normality was not met.

### Step 6: Hypothesis Testing

* **Mann-Whitney U Test** applied as a non-parametric test.
* If p-value < 0.05, significant difference exists.

---

## 📊 Results & Interpretation

* Data is **not normally distributed** → Mann-Whitney U Test used.
* Results showed **statistically significant differences** in conversion.
* **Group B** performed better overall.

#### 📊 Statistical Summary:

* **Control Group Conversion Rate**: X%
* **Treatment Group Conversion Rate**: Y%
* **Z-score**: Z-value
* **P-value**: P-value
* **Conclusion**: \[Reject] Null Hypothesis

### 🔥 Business Recommendations

* Roll out the better-performing strategy (Group B).
* Monitor for sustained performance improvements.
* Consider segmenting users for more granular testing.

---

## 💡 Real-World Applications

1. **Digital Marketing Optimization**: Test landing pages, ad creatives, CTAs.
2. **E-commerce**: Evaluate pricing, product placements, or shipping models.
3. **User Experience (UX)**: Compare UI designs or page layouts.
4. **Medical Trials**: Compare treatment effectiveness.

### Example:

* **Group A**: Standard discount ads
* **Group B**: Personalized product recommendations
* Result: Group B yields higher purchase and earnings rates.

---

## 📄 Conclusion

This project demonstrates a complete A/B testing framework in Python using real-world marketing data.

Using rigorous statistical testing and careful analysis, we:

* Detected significant performance differences
* Identified the winning strategy
* Supported marketing decisions using data science methods

> This process enhances business confidence in decision-making and promotes data-driven growth.

---

## 🌍 Tags

`A/B Testing` `Hypothesis Testing` `Mann-Whitney U` `Digital Marketing` `Earning per Purchase` `Conversion Rate` `Python` `Campaign Analysis`

