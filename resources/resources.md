# Tutorials and Learning Resources

This section contains authoritative tutorials and learning resources
related to data leakage, feature engineering, automated feature
engineering, feature stores, data validation, and machine-learning
pipelines.

The resources were selected from official documentation and are intended
to support practical understanding of the risks discussed in this
research.

---

## 1. scikit-learn — Common Pitfalls and Recommended Practices

**Purpose:**  
This official scikit-learn guide explains common machine-learning
mistakes, including inconsistent preprocessing and data leakage.

**What it teaches:**  
The resource explains how leakage can occur during preprocessing and
provides recommended practices for avoiding it. It also discusses the
use of pipelines to keep preprocessing and model fitting consistent.

**Why relevant:**  
Data preprocessing leakage is one of the central risks in the research
topic. This guide provides a practical foundation for building
leakage-aware machine-learning pipelines.

**Link:**  
https://scikit-learn.org/stable/common_pitfalls.html

**Official documentation:**  
https://scikit-learn.org/stable/user_guide.html

---

## 2. Featuretools — Deep Feature Synthesis Tutorial

**Purpose:**  
This official Featuretools tutorial introduces Deep Feature Synthesis
(DFS), an automated method for generating features from relational and
temporal data.

**What it teaches:**  
The tutorial demonstrates how to prepare an EntitySet and automatically
generate features using Featuretools.

**Why relevant:**  
Automated feature generation is a major component of this research.
Understanding DFS helps explain how automatically generated aggregation
and transformation features can create leakage risks when the feature
generation process is not restricted to information available at
prediction time.

**Link:**  
https://docs.featuretools.com/en/latest/getting_started/afe.html

**Official documentation:**  
https://docs.featuretools.com/en/latest/

---

## 3. Feast — Point-in-Time Joins

**Purpose:**  
This official Feast guide explains how to create point-in-time-correct
feature joins for machine-learning training data.

**What it teaches:**  
The tutorial explains how feature values are joined according to the
timestamp of an entity event. Feast scans backward from the event time
to obtain feature values that were available at that point in time.

**Why relevant:**  
This resource is directly related to temporal and future-information
leakage. It demonstrates a practical method for preventing future feature
values from leaking into model-training data.

**Link:**  
https://docs.feast.dev/getting-started/concepts/point-in-time-joins

**Additional quickstart:**  
https://docs.feast.dev/getting-started

---

## 4. MLflow — Tracking Quickstart

**Purpose:**  
The official MLflow Tracking Quickstart introduces experiment tracking
for machine-learning workflows.

**What it teaches:**  
The tutorial demonstrates how to log parameters, metrics, and models
and how to inspect tracked experiments.

**Why relevant:**  
Tracking preprocessing configurations, feature-engineering experiments,
datasets, models, and evaluation results can improve reproducibility
and make it easier to audit machine-learning experiments for leakage.

**Link:**  
https://mlflow.org/docs/latest/ml/getting-started/quickstart/

**Tutorials and examples:**  
https://mlflow.org/docs/latest/ml/tutorials-and-examples

---

## 5. Great Expectations — Try GX Core

**Purpose:**  
This official Great Expectations tutorial introduces data validation
using Expectations and validation workflows.

**What it teaches:**  
The tutorial demonstrates how to connect data, define Expectations,
validate data, and review validation results.

**Why relevant:**  
Data validation can be used as a quality-control stage before feature
engineering and model training. Validation rules can help identify
unexpected data changes, schema problems, duplicates, and other issues
that could compromise a machine-learning pipeline.

**Link:**  
https://docs.greatexpectations.io/docs/core/introduction/try_gx/

**Official documentation:**  
https://docs.greatexpectations.io/docs/core/introduction/

---

# Additional Learning Resources

## scikit-learn — Data Leakage During Preprocessing

**Purpose:**  
Provides a focused explanation of preprocessing leakage.

**Why relevant:**  
It explains why preprocessing statistics should not be learned from
test data and shows how to avoid this problem using appropriate
machine-learning workflows.

**Link:**  
https://scikit-learn.org/stable/common_pitfalls.html#data-leakage

---

## Feast — Quickstart

**Purpose:**  
Provides a practical introduction to building a feature store and
generating training data.

**Why relevant:**  
The quickstart demonstrates feature retrieval and point-in-time
correctness, which are important mechanisms for preventing future
feature values from leaking into training data.

**Link:**  
https://docs.feast.dev/getting-started

---

## Featuretools — Feature Engineering for Time Series Problems

**Purpose:**  
Provides guidance for using Featuretools with temporal data.

**Why relevant:**  
Time-dependent feature engineering requires careful handling of
cutoff times and historical information. This resource is useful for
understanding how temporal feature engineering should be structured.

**Link:**  
https://docs.featuretools.com/en/stable/guides/guides_index.html

---

# Resource Selection Summary

| Resource | Main Topic | Connection to Research |
|---|---|---|
| scikit-learn Common Pitfalls | Data leakage | Preprocessing and pipeline leakage |
| Featuretools DFS | Automated feature engineering | Automated feature-generation leakage |
| Feast Point-in-Time Joins | Temporal feature retrieval | Future-information leakage |
| MLflow Tracking | Experiment tracking | Reproducibility and auditing |
| Great Expectations | Data validation | Data-quality and pipeline validation |

---

# How These Resources Support the Research

These resources collectively provide practical guidance for building
safer feature-engineering pipelines.

**scikit-learn** provides guidance for preventing preprocessing leakage.

**Featuretools** demonstrates automated feature generation.

**Feast** provides point-in-time feature retrieval to prevent future
information from entering training data.

**MLflow** supports experiment tracking and reproducibility.

**Great Expectations** provides data validation mechanisms that can be
used to check data before it enters downstream machine-learning
pipelines.

Together, these resources complement the research discussion of
preprocessing leakage, automated feature generation, temporal leakage,
validation, reproducibility, and trustworthy AI-assisted
feature engineering.
