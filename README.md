## 📊 A/B Testing Under Conflicting Metrics: Revenue-Driven Decision Making
### 🔍 Project Overview

This project evaluates a real-world product A/B experiment where a new landing page introduced conflicting signals:

Conversion rate showed minimal change

Average order value declined

Customer support tickets increased

The objective was not to optimize a single metric, but to determine whether the experiment should be shipped, partially rolled out, or rolled back, using business-first decision logic.

### 🎯 Business Question

Should the company ship the new landing page when conversion, revenue, and operational metrics disagree?

This mirrors real product analytics problems where metric conflicts and trade-offs drive decision-making.

### 🧠 Key Analytical Approach

Instead of relying on vanity metrics, the analysis followed a structured decision framework:

Experiment Hygiene

Verified randomization and group balance

Removed contaminated observations where treatment exposure did not match assignment

#### Metric Hierarchy

Conversion Rate → Behavioral signal (gatekeeper)

Average Order Value → Transaction quality

Net Revenue Per User (Primary Decision Metric)

### Descriptive Analysis & Visualization

Order value distributions

Support ticket pressure

### Early warning signals before hypothesis testing

### Segmentation Analysis

New vs returning users

Tested feasibility of partial rollout

Uncertainty & Risk Assessment

Bootstrap confidence intervals

### Effect size vs statistical significance

## Business risk framing

### 📈 Key Findings

Net Revenue Per User declined by ~17% in the treatment group

Average Order Value dropped by over 20%

Customer support tickets increased significantly across all user segments

#### Revenue decline was:

Consistent for both new and returning users

Statistically reliable (non-overlapping confidence intervals)

Practically significant from a business standpoint

## 🚫 Final Recommendation

Roll back the experiment.

Shipping the new landing page would expose the business to:

Sustained revenue loss per user

Increased operational and support costs

Elevated risk of long-term user dissatisfaction

The data does not support a partial rollout.

## 🛠️ Tools & Techniques

Python (Pandas, NumPy)

Data visualization (Matplotlib, Seaborn)

Bootstrap confidence intervals

A/B testing best practices

Product & business metric reasoning

## 📂 Repository Contents

A-B-Testing-Refactored.ipynb → End-to-end analysis notebook

ab_test_full_project_dataset.csv → Dataset used for analysis

## 💡 Why This Project Matters

This project emphasizes:

Decision-making under uncertainty

Metric trade-offs instead of single-metric optimization

Business impact over statistical novelty

It reflects how product analytics is practiced in real organizations—not textbook scenarios.

## 🧪 Disclaimer

Due to the lack of publicly available datasets combining experimentation, revenue, and support interactions, certain fields (e.g., order value and support tickets) were modeled using realistic assumptions to evaluate decision logic. This mirrors real-world constraints where analysts often work with incomplete data.

## 📌 Author Note

If you're a recruiter or interviewer, this project is best discussed as a decision case, not a modeling exercise.
