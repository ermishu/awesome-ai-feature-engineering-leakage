# Tools and Libraries

This section lists tools and libraries that are relevant to studying
data leakage risks in AI-assisted feature engineering pipelines.

The selected tools support feature engineering, preprocessing,
validation, automated machine learning, experiment tracking, and
data-quality verification.

---

## 1. scikit-learn

**Purpose:**  
scikit-learn is a Python machine-learning library that provides tools
for preprocessing, feature selection, model training, cross-validation,
pipelines, and model evaluation.

**Why relevant:**  
scikit-learn is particularly useful for implementing leakage-aware
machine-learning pipelines. Its Pipeline and preprocessing utilities
help ensure that transformations such as scaling, encoding, and
imputation are fitted within the appropriate training-data boundary.

**Useful capabilities:**
- Preprocessing
- Feature selection
- Cross-validation
- Pipeline construction
- Model evaluation
- Train/test splitting

**Official link:**  
https://scikit-learn.org/

---

## 2. Featuretools

**Purpose:**  
Featuretools is an open-source framework for automated feature
engineering. It can automatically generate features from structured
and relational datasets.

**Why relevant:**  
Automated feature generation can introduce leakage if generated features
use information from outside the permitted prediction-time boundary.
Featuretools is therefore useful for studying how automated feature
engineering systems can be designed and evaluated for leakage risks.

**Useful capabilities:**
- Automated feature engineering
- Relational feature generation
- Aggregation features
- Transformation features
- Feature discovery

**Official link:**  
https://www.featuretools.com/

**Documentation:**  
https://docs.featuretools.com/

---

## 3. AutoGluon

**Purpose:**  
AutoGluon is an AutoML framework for building machine-learning models
with limited manual configuration. It supports tabular, multimodal,
and other machine-learning workflows.

**Why relevant:**  
AutoML systems can automatically perform preprocessing, feature
processing, model selection, and hyperparameter optimization. This
makes AutoGluon useful for investigating whether automated pipeline
components can unintentionally introduce data leakage.

**Useful capabilities:**
- Automated machine learning
- Tabular modeling
- Automated preprocessing
- Model selection
- Hyperparameter optimization

**Official link:**  
https://auto.gluon.ai/

---

## 4. MLflow

**Purpose:**  
MLflow is an open-source platform for managing machine-learning
experiments, models, datasets, and related metadata.

**Why relevant:**  
Tracking experiments and feature-engineering configurations can help
researchers identify changes in preprocessing, feature generation,
datasets, and validation procedures. This supports reproducibility
and auditing of leakage-prone machine-learning workflows.

**Useful capabilities:**
- Experiment tracking
- Dataset tracking
- Model tracking
- Metadata logging
- Reproducibility
- Model lifecycle management

**Official link:**  
https://mlflow.org/

---

## 5. Great Expectations

**Purpose:**  
Great Expectations is a data-quality and validation framework that
allows users to define and test expectations about datasets.

**Why relevant:**  
Data validation can help detect unexpected changes in datasets before
they enter a machine-learning pipeline. It can be incorporated into
leakage-aware workflows to check data properties and enforce quality
requirements.

**Useful capabilities:**
- Data validation
- Data-quality checks
- Schema validation
- Automated testing
- Pipeline data checks

**Official link:**  
https://greatexpectations.io/

---

## Tool Selection Summary

| Tool | Main Purpose | Relevance to Data Leakage |
|---|---|---|
| scikit-learn | ML pipelines and preprocessing | Prevents leakage through controlled transformations |
| Featuretools | Automated feature engineering | Useful for studying automated feature-generation leakage |
| AutoGluon | AutoML | Useful for examining leakage risks in automated pipelines |
| MLflow | Experiment tracking | Supports reproducibility and leakage auditing |
| Great Expectations | Data validation | Helps validate data entering ML pipelines |

---

## Recommended Usage in a Leakage-Aware Pipeline

A leakage-aware workflow can combine these tools as follows:

1. Use **Great Expectations** to validate incoming data.
2. Use **scikit-learn** pipelines to keep preprocessing inside the
   training workflow.
3. Use **Featuretools** for controlled automated feature generation.
4. Use **AutoGluon** to investigate automated model and feature
   processing.
5. Use **MLflow** to record datasets, experiments, features, and
   validation results.

The goal is to ensure that automated feature engineering and
machine-learning processes do not accidentally use information that
would be unavailable at prediction time.
