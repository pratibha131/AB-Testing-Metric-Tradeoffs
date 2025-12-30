# 📊 A/B Testing Under Metric Tradeoffs: Revenue-Driven Product Decision
## 🚀 Project Overview

This project evaluates a product A/B experiment where a new landing page introduced conflicting performance signals:

Conversion rate showed minimal change

Average Order Value (AOV) declined

Customer Support Tickets increased

Instead of optimizing a single metric, the analysis focuses on decision-making under tradeoffs, using Net Revenue Per User (NRPU) as the primary business metric.

### The goal is to answer a real product question:

Should the company ship, partially roll out, or roll back the new landing page?

## 🎯 Business Context & Motivation

In real product teams, experiments often succeed on surface-level metrics (e.g., conversion) while silently damaging revenue or operations.

This project mirrors that reality by:

Prioritizing unit economics over vanity metrics

Incorporating operational cost signals (support tickets)

Making a binary business decision, not just reporting statistics

## 🧠 Analytical Framework

The analysis follows a structured, industry-aligned approach:

1️⃣ Experiment Validation

Verified group balance and randomization

Removed contaminated observations where treatment exposure did not match assignment

Ensured causal interpretability before analysis

2️⃣ Metric Hierarchy (Critical)

Metrics were evaluated in increasing order of business importance:

Conversion Rate → behavioral signal (gatekeeper)

Average Order Value (AOV) → transaction quality

Net Revenue Per User (NRPU) → primary decision metric

This avoids false positives caused by single-metric optimization.

## 📊 Exploratory & Descriptive Analysis

Initial EDA was used to surface early warning signals before hypothesis testing:

User distribution across experiment groups

Conversion behavior

Order value distributions

Support ticket pressure

This step prevents blind reliance on statistical tests.

## 📐 Hypothesis Definition

Primary Hypothesis (Business-Driven)

H₀ (Null): The new landing page does not improve Net Revenue Per User

H₁ (Alternative): The new landing page increases Net Revenue Per User

Secondary metrics (conversion rate, AOV) are evaluated to explain why NRPU changes.

## 🔬 Statistical Methodology

Descriptive statistics for behavioral diagnostics

Segmentation by new vs returning users

Bootstrap confidence intervals for NRPU to assess uncertainty

Effect size interpretation to distinguish statistical vs practical significance

The focus is on decision reliability, not p-value chasing.

## 📈 Key Results (Summary)
Metric	Control	Treatment	Impact

Conversion Rate	~12.04%	~11.88%	↓ Slight

Average Order Value	~119.8	~95.1	↓ ~21%

Net Revenue Per User	~18.82	~15.70	↓ ~16–17%

Support Tickets	Lower	Higher	↑ Operational risk

## Segmentation Insight

Revenue decline observed for both new and returning users

Support tickets increased across all segments

Partial rollout is not justified

Bootstrap confidence intervals for NRPU were non-overlapping, indicating the decline is statistically reliable and unlikely due to random noise.

## 📉 Visual Summary of Results

### Net Revenue Per User (Primary Decision Metric)
![NRPU Comparison](charts/nrpu_comparison.png)

### Order Value Distribution
![Order Value Distribution](charts/order_value_distribution.png)

### Customer Support Ticket Rate
![Support Tickets](charts/support_ticket_rate.png)


## 🚫 Final Recommendation
Decision: Roll Back the Experiment

Despite minimal change in conversion rate, the new landing page causes a material and reliable decline in net revenue per user, coupled with a significant increase in customer support burden.

Shipping the experiment would expose the business to:

Sustained revenue loss

Increased operational costs

Higher risk of user dissatisfaction and long-term churn

## Recommendation: Roll back the change and redesign the experience to address order-value dilution and user friction before re-testing.

📁 Repository Structure
AB-Testing-Metric-Tradeoffs/
├── README.md                         # Project overview & decision narrative

├── A-B-Testing_Final.ipynb           # Final, decision-focused analysis

├── ab_test_full_project_dataset.csv  # Dataset used for analysis

└── drafts/
    └── A-B-Testing.ipynb             # Exploratory analysis & iteration

## Notebook Guidance

Recruiters & reviewers: Focus on A-B-Testing_Final.ipynb

Draft notebook is included to demonstrate analytical iteration and learning

## ⚠️ Data Disclaimer

Due to the lack of public datasets combining experimentation, revenue, and support metrics, certain fields (e.g., order value and support tickets) were modeled using realistic assumptions.

The objective is to demonstrate analytical reasoning, metric tradeoff handling, and decision-making, which closely mirrors real-world constraints faced by product analysts.

## 💡 Why This Project Matters

This project demonstrates:

Decision-making under conflicting metrics

Revenue-first analytical thinking

Awareness of operational costs

Practical use of uncertainty and effect size

Willingness to reject a feature based on evidence
