**A/B Testing Case Study – Discount Banner Experiment**

This case study evaluates whether a redesigned discount banner (Variant B) leads to a meaningful uplift in conversion rate, revenue, and user spending behavior compared to the existing banner (Variant A).

# Project Summary

**Goal:**
Determine whether Variant B should replace Variant A by measuring impact on:

Conversion Rate (primary KPI)

Average Order Value (Secondary KPI)

Outcome:
Variant B shows a statistically significant +11.6% relative uplift in conversion rate and a ~₹450 increase per 1,000 sessions, with no negative effect on order value.
→ Recommended for rollout.

## 1. Problem Statement

The Growth team needs to assess whether updating the discount banner will increase completed purchases.
This project simulates and analyzes 50,000 user sessions to demonstrate a full A/B testing workflow for analytics roles

## 2. Dataset Overview

Each row represents a user session:
Column	Description
variant	A (control) or B (treatment)
ordered	1 if purchase completed
order_value	Order amount if purchased (else 0)

Data is generated using:

Bernoulli/Binomial for conversions

Lognormal distribution for order values (realistic, right-skewed)

Total sessions: 50,000 (balanced across variants)

## 3. Methodology
**Exploratory Analysis**

Conversion rate comparison

Revenue-per-session comparison

AOV distribution visualizations

Outlier & skew analysis

Frequentist Statistical Testing

Two-proportion Z-test for conversion

Wilson Confidence Intervals

Mann-Whitney U test for skewed AOV

Bootstrap CI for mean differences

Bayesian Inference

Beta-Binomial posterior simulation

Probability that Variant B > Variant A

Power & Sample Size Analysis

MDE calculation

Required sample per arm

Achieved test power

Business Uplift Estimation

Revenue-per-session uplift

Expected gain per 1,000 sessions

## 4. Results
Conversion Rate
| Variant | Conversion | Wilson CI    |
| ------- | ---------- | ------------ |
| A       | 11.57%     | 11.18–11.97% |
| B       | 12.91%     | 12.50–13.33% |


*Absolute Lift: +1.34 pp*
*Relative Lift: +11.6%*

**Z-test p-value: 4.8 × 10⁻⁶ → significant**

AOV Among Converters

Distributions similar across variants
Mann-Whitney U: significant but small effect
AOV is not the main driver of conversion uplift
Revenue Impact

Estimated uplift: +₹458 per 1,000 sessions

Bayesian View

P(B > A) ≈ 1.00
→ High level of confidence in Variant B.

# 5. Interpretation & Insights

The new banner increases the likelihood of purchasing.
Statistical power is strong (≈93%), making results reliable.

# 6. Recommendation

Roll out Variant B using a phased rollout (10–20%)

# 7. Tech Stack

Python, Pandas, NumPy
SciPy, Statsmodels
Matplotlib, Seaborn
Bootstrap resampling
Bayesian inference (Beta distribution)

