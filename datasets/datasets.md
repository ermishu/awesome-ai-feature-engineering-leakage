# Relevant Datasets

This section provides datasets that can be used to study data leakage,
feature engineering, automated feature construction, temporal validation,
and trustworthy machine learning pipelines.

The datasets were selected because their structure allows researchers to
investigate realistic situations in which incorrectly constructed features,
preprocessing procedures, aggregation, or temporal information can cause
data leakage.

---

## 1. Default of Credit Card Clients

**Source:** UCI Machine Learning Repository

**Description:**  
The Default of Credit Card Clients dataset contains information about
30,000 credit card clients in Taiwan and is designed for binary
classification of default payments. The dataset contains 23 explanatory
features, including credit amount, demographic information, historical
repayment status, bill statements, and previous payments.

**Why it is relevant:**  
This dataset is particularly useful for studying temporal and feature
engineering leakage. Several variables represent monthly historical
information, so feature construction must respect the prediction time.
Researchers can investigate whether information from an inappropriate
time period is accidentally included when creating features.

**Possible research applications:**
- Temporal feature engineering
- Historical payment aggregation
- Target leakage investigation
- Train/test preprocessing
- Feature selection experiments
- Leakage-aware validation

**Dataset size:** 30,000 instances and 23 features

**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**DOI:** 10.24432/C55S3H

**Link:**  
https://archive.ics.uci.edu/dataset/350/default

**Citation:**  
Yeh, I. (2009). Default of Credit Card Clients [Dataset].
UCI Machine Learning Repository.
https://doi.org/10.24432/C55S3H

---

## 2. Online Retail

**Source:** UCI Machine Learning Repository

**Description:**  
The Online Retail dataset contains transactions from a UK-based
non-store online retailer between December 2010 and December 2011.
It contains 541,909 transactions and includes information such as
invoice number, product code, product description, quantity,
transaction date, unit price, customer ID, and country.

**Why it is relevant:**  
The dataset is useful for studying feature engineering involving
transaction histories and time-dependent information. Researchers can
construct customer-level features such as purchase frequency,
recency, monetary value, and rolling statistics while ensuring that
only information available before the prediction point is used.

**Possible research applications:**
- Temporal feature engineering
- Customer-level aggregation
- Rolling and cumulative features
- Time-aware train/test splitting
- Feature provenance
- Detection of future-information leakage
- Automated feature generation

**Dataset size:** 541,909 instances and 6 primary features listed by UCI

**Dataset characteristics:** Multivariate, sequential, and time-series

**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

**DOI:** 10.24432/C5BW33

**Link:**  
https://archive.ics.uci.edu/dataset/352/online-retail

**Citation:**  
Chen, D. (2015). Online Retail [Dataset].
UCI Machine Learning Repository.
https://doi.org/10.24432/C5BW33

---

## 3. Bank Marketing

**Source:** UCI Machine Learning Repository

**Description:**  
The Bank Marketing dataset contains information collected during
direct marketing campaigns of a Portuguese banking institution.
The classification task is to predict whether a client will subscribe
to a term deposit.

The dataset contains demographic, financial, contact, and campaign
related variables.

**Why it is relevant:**  
This dataset is useful for investigating target leakage and
post-outcome information. Some variables describe events that occur
during or as a consequence of a marketing contact. Researchers can
study whether features that would not be available at prediction time
are incorrectly included in a machine-learning pipeline.

**Possible research applications:**
- Target leakage
- Feature availability analysis
- Temporal feature engineering
- Train/test preprocessing
- Feature selection
- Leakage-aware model evaluation
- Automated feature engineering

**Dataset size:** Approximately 45,000 instances and 17 features

**Dataset characteristics:** Multivariate classification dataset

**Link:**  
https://archive.ics.uci.edu/dataset/222/bank%2Bmarketing

**Citation:**  
Moro, S., Cortez, P., & Rita, P. (2014).
A data-driven approach to predict the success of bank telemarketing.
Decision Support Systems, 62, 22–31.

---

## Dataset Selection Rationale

These three datasets were selected because they represent different
data structures and leakage risks:

| Dataset | Main Structure | Useful Leakage Scenario |
|---|---|---|
| Default of Credit Card Clients | Historical financial data | Temporal and target leakage |
| Online Retail | Transactional/time-series data | Future-information and aggregation leakage |
| Bank Marketing | Classification/campaign data | Target and post-outcome leakage |

Together, these datasets provide suitable test cases for studying
data leakage risks in AI-assisted feature engineering pipelines.

---

## Recommended Leakage-Aware Usage

When using these datasets, feature engineering should be performed
inside the appropriate training-data boundaries.

For example:

1. Split the data before learning preprocessing parameters.
2. Generate training features using only training information.
3. Avoid using future observations when creating historical features.
4. Fit encoders and imputers only on the training data.
5. Apply feature selection within the training procedure.
6. Use temporal or group-aware validation when appropriate.
7. Verify that every engineered feature would have been available
   at the prediction time.

These practices help prevent artificially inflated model performance
caused by information leakage.
