Project: Try Again — Did Marketing Actually Cause the Conversion?

=================================
## Marketing Incrementality Analysis
=================================
### Business Problem
A streaming platform launched a multi-channel acquisition campaign during April 2024.

The objective of this project was to determine whether advertising exposure generated incremental subscription conversions beyond what would have occurred naturally.

Goal:
Measure whether a streaming acquisition campaign drove incremental conversions using a holdout testing framework.

Business Question:
Did the campaign create additional subscriptions, or would those users have subscribed anyway?

Scope:
This project focuses only on campaign-driven conversions, not retention, engagement, LTV, or post-signup behavior.

==============================
## Analytical Approach 
==============================

## Analytical Approach

The analysis followed a marketing science framework:

1. Build a user-level analytical dataset combining customer attributes, advertising exposure, and subscription outcomes.
2. Compare conversion rates between exposed and non-exposed users.
3. Estimate incremental lift and incremental conversions.
4. Test statistical significance using a two-proportion z-test.
5. Evaluate treatment-control balance to identify potential selection bias.
6. Adjust for observable differences using logistic regression.
7. Assess whether advertising remained a significant predictor of conversion after controlling for user characteristics.


=============================
## Key Findings
=============================

## Key Findings

### Conversion Rate Comparison

* Exposed Users: 14.84%
* Non-Exposed Users: 14.45%

Observed lift:

* Absolute Lift: +0.39 percentage points
* Relative Lift: +2.7%
* Estimated Incremental Conversions: 38

#### Statistical Significance

A one-sided two-proportion z-test was conducted to evaluate whether exposed users converted at a higher rate than non-exposed users.

* Z-statistic: 0.85
* P-value: 0.197

The observed lift was not statistically significant at the 95% confidence level.

#### Treatment-Control Balance

Balance checks revealed that exposed users differed from control users prior to campaign exposure.

Compared to the control group, exposed users exhibited:

* Higher prior subscriber rates
* Higher prior trial rates
* Higher historical engagement scores

These differences suggest potential selection bias.

#### Logistic Regression Adjustment

A logistic regression model controlling for prior subscriber status, prior trial status, historical engagement, age, and region found no statistically significant relationship between advertising exposure and conversion.

Exposure Coefficient: 0.032

Exposure P-value: 0.398

After adjustment, there remained insufficient evidence to conclude that advertising exposure caused incremental subscription growth.

=============================
## Limitations
=============================

This analysis relies on observational data rather than a randomized holdout design.

Although regression adjustment was used to control for observable differences between users, unobserved confounding factors may still influence results.

Future analyses could improve causal confidence through:

- Randomized holdout testing
- Geo-based experiments
- Propensity score matching
- Difference-in-differences methodologies


=============================
## Skills Demonstrated
=============================

- SQL-style dimensional modeling
- Fact table construction
- Exploratory Data Analysis (EDA)
- Marketing Measurement
- Incrementality Analysis
- Statistical Hypothesis Testing
- Logistic Regression
- Causal Inference Fundamentals
- Python (Pandas, NumPy, Statsmodels)
- Business Communication

=============================
## What Changed My Mind
=============================

Initial conversion rate comparisons suggested advertising may have increased conversions. However, after evaluating statistical significance and treatment-control balance, the evidence for a causal advertising effect weakened considerably. This project reinforced the importance of validating assumptions before drawing conclusions from observed lift.