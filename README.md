# Awesome AI-Assisted Feature Engineering Leakage

A curated research repository on **Data Leakage Risks in AI-Assisted
Feature Engineering Pipelines**.

This repository collects scholarly research papers, datasets, tools,
GitHub implementations, tutorials, and verification resources related to
data leakage in machine learning and AI-assisted feature engineering.

The goal is to provide a structured and reusable research resource for
understanding, detecting, preventing, and evaluating data leakage in
automated and LLM-assisted feature engineering workflows.

---

## Contents

- [Overview](#overview)
- [Research Questions](#research-questions)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Research Papers](#research-papers)
  - [Survey and Review Papers](#survey-and-review-papers)
  - [Foundational Papers](#foundational-papers)
  - [Feature Engineering and AutoML](#feature-engineering-and-automl)
  - [Validation and Model Selection](#validation-and-model-selection)
  - [Recent Research](#recent-research)
  - [Applications and Evaluation](#applications-and-evaluation)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [Research Challenges](#research-challenges)
- [Leakage Prevention Principles](#leakage-prevention-principles)
- [Repository Structure](#repository-structure)
- [License](#license)

---

## Overview

Machine learning systems are increasingly developed as multi-stage
pipelines involving data collection, preprocessing, feature engineering,
feature selection, model training, validation, hyperparameter
optimization, evaluation, and deployment.

Feature engineering is an important stage because it determines how raw
data is transformed into representations used by machine-learning
models. Automated feature engineering and large language models (LLMs)
can reduce manual effort by generating transformations, aggregations,
interactions, and candidate features.

However, increased automation can also increase the risk of **data
leakage**.

Data leakage occurs when information that should not be available to the
model at prediction time influences feature construction, preprocessing,
feature selection, model selection, or evaluation. Leakage can result in
overly optimistic evaluation results and models that perform poorly on
genuinely unseen data.

This repository focuses particularly on leakage introduced or amplified
by AI-assisted feature engineering. Important leakage pathways include:

- Preprocessing leakage
- Target leakage
- Temporal leakage
- Aggregation leakage
- Target-encoding leakage
- Feature-selection leakage
- Validation and model-selection leakage
- Leakage caused by repeated AI-assisted feature search
- Leakage through LLM prompts and context
- Leakage caused by dependent or duplicated observations
- Inadequate feature provenance
- Incorrect prediction-time feature availability

The central principle of this repository is that leakage prevention
should be treated as a **pipeline-level property**, not simply a
property of the final machine-learning model.

---

## Research Questions

This repository is organized around the following questions:

1. What forms of data leakage commonly occur in feature-engineering
   pipelines?

2. How can AI-assisted feature engineering introduce or amplify leakage
   risks?

3. How can preprocessing and feature-generation pipelines be designed to
   prevent leakage?

4. How should temporal and group-aware validation be performed?

5. How can feature provenance be used to identify hidden dependencies?

6. How can LLM prompts and AI-assisted feature search be made
   leakage-aware?

7. How can automated systems detect leakage before model evaluation?

8. What research gaps remain in developing reliable and
   leakage-resistant AI-assisted feature engineering systems?

---

## AI-Assisted Research Paper

### Data Leakage Risks in AI-Assisted Feature Engineering Pipelines

This research paper investigates data leakage risks throughout
AI-assisted feature engineering workflows.

The paper examines leakage during:

- Data preprocessing
- Feature generation
- Target encoding
- Temporal aggregation
- Feature selection
- Iterative validation
- Model selection
- Prompt construction
- Automated feature search

It also discusses the interaction between LLM-based feature engineering
and conventional machine-learning pipelines.

The paper argues that every data-dependent operation that contributes to
feature generation or model selection must respect the intended
information boundary.

**Paper:**

[Read the AI-Assisted Research Paper](paper/AI_Assisted_Research_Paper.pdf)

---

## Citation Integrity Audit

The research references and claims were reviewed against scholarly,
publisher, and academic sources.

The audit documents the verification process and identifies
bibliographic entries that require correction or careful interpretation.

**Citation Integrity Audit:**

[View Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

---

# Research Papers

The repository contains a curated collection of research papers related
to data leakage, feature engineering, AutoML, validation, model
selection, and AI-assisted feature engineering.

The papers are organized into meaningful categories so that researchers
can understand the progression from classical leakage research to
modern AI-assisted feature engineering.

---

## Survey and Review Papers

### 1. Overview of Data Leakage Scenarios in Supervised Machine Learning

**Authors:** Sasse et al.  
**Year:** 2025

Provides a broad discussion of leakage scenarios in supervised machine
learning, including preprocessing, feature selection, model selection,
validation, temporal dependencies, and dependent observations.

[Paper / DOI](https://doi.org/10.1186/s40537-025-01193-8)

---

### 2. Data Leakage and the Reproducibility Crisis in Machine Learning

**Authors:** Kapoor & Narayanan  
**Year:** 2023

Examines how methodological problems such as leakage can contribute to
unreliable machine-learning results and reproducibility problems.

[Paper / DOI](https://doi.org/10.1016/j.patter.2023.100804)

---

### 3. Feature Selection and Extraction: A Review and Comparison

**Authors:** Khalid, Khalil & Nasreen  
**Year:** 2014

Reviews feature-selection and feature-extraction approaches and provides
background for understanding data-dependent feature-selection decisions.

[Paper / DOI](https://doi.org/10.1109/SAI.2014.6918213)

---

## Foundational Papers

### 4. Leakage in Data Mining: Formulation, Detection, and Avoidance

**Authors:** Kaufman, Rosset, Perlich & Stitelman  
**Year:** 2012

A foundational work defining data leakage and discussing its detection
and prevention in data-mining workflows.

[Paper / DOI](https://doi.org/10.1145/2382577.2382579)

---

### 5. On the Cross-Validation Bias Due to Hyperparameter Selection

**Authors:** Moscovich & Rosset  
**Year:** 2022

Studies bias introduced when cross-validation results are repeatedly used
for model and hyperparameter selection.

[Paper / DOI](https://doi.org/10.1111/rssb.12537)

---

### 6. Deep Feature Synthesis: Towards Automating Data Science Endeavors

**Authors:** Kanter & Veeramachaneni  
**Year:** 2015

Introduces Deep Feature Synthesis, an automated approach for constructing
features through transformations and aggregations.

[Paper / DOI](https://doi.org/10.1109/DSAA.2015.7344858)

---

### 7. Feature Engineering for Machine Learning

**Authors:** Zheng & Casari  
**Year:** 2018

Provides practical and conceptual background on feature engineering for
machine-learning systems.

[Publisher / Book](https://www.oreilly.com/library/view/feature-engineering-for/9781491953235/)

---

## Feature Engineering and AutoML

### 8. CAAFE: Context-Aware Automated Feature Engineering

**Authors:** Hollmann, Müller & Hutter  
**Year:** 2023

Explores the use of large language models for automated feature
engineering on tabular datasets.

[NeurIPS Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c2df4c35cdbee764ebb9e9d0acd5197-Abstract-Conference.html)

---

### 9. Automated Feature Engineering for Automated Machine Learning

**Authors:** de Winter et al.  
**Year:** 2025

Examines automated feature engineering as part of automated machine
learning workflows.

[Paper / DOI](https://doi.org/10.1016/j.knosys.2025.113671)

---

### 10. LLM-FE: Large Language Model-Based Feature Engineering

**Year:** 2026

Investigates LLM-based automated feature engineering and program-search
approaches for generating feature transformations.

[Paper / DOI](https://doi.org/10.48550/arXiv.2601.21060)

---

## Validation and Model Selection

### 11. On Over-fitting in Model Selection and Error Estimation

**Authors:** Cawley & Talbot  
**Year:** 2010

Demonstrates how model-selection procedures can overfit finite datasets
and produce optimistic estimates.

[Paper / DOI](https://doi.org/10.1016/j.patrec.2010.04.013)

---

### 12. A Selection Bias in Model Selection

**Authors:** Varma & Simon  
**Year:** 2006

Examines bias resulting from using the same cross-validation process for
model optimization and error estimation.

[Paper / DOI](https://doi.org/10.1186/1471-2105-7-91)

---

### 13. Hyperparameter Optimization

**Authors:** Feurer & Hutter  
**Year:** 2019

Provides background on automated hyperparameter optimization and its
relationship to machine-learning model-selection workflows.

[Paper / DOI](https://doi.org/10.1007/978-3-030-05318-5_1)

---

## Recent Research

### 14. Data Leakage Inflates Prediction Performance in Machine Learning

**Year:** 2024

Investigates how leakage can inflate predictive performance and produce
misleading conclusions.

[Paper / DOI](https://doi.org/10.1038/s41467-024-46150-w)

---

### 15. Multi-Level Diagnosis and Evaluation for Robust Tabular Feature
Engineering with Large Language Models

**Authors:** Lim & Yoon  
**Year:** 2025

Studies robustness and evaluation of LLM-generated features for tabular
machine-learning tasks.

[Paper / DOI](https://doi.org/10.18653/v1/2025.findings-emnlp.249)

---

### 16. Preventing Data Leakage in Classification via Integrated Machine
Learning Pipelines

**Authors:** Ichwani et al.  
**Year:** 2026

Examines leakage prevention through integrated preprocessing, feature
transformation, and hyperparameter-tuning pipelines.

[Paper / DOI](https://doi.org/10.52436/1.jutif.2026.7.1.5490)

---

## Applications and Evaluation

### 17. Hidden Stratification Causes Clinically Meaningful Failures in
Machine Learning for Medical Imaging

**Authors:** Oakden-Rayner, Dunnmon, Carneiro & Ré  
**Year:** 2020

Demonstrates how hidden structure in datasets can produce misleading
model evaluation results in medical imaging.

[Paper / DOI](https://doi.org/10.1145/3368555.3384468)

---

### 18. Principal Component Analysis

**Authors:** Abdi & Williams  
**Year:** 2010

Provides background on dimensionality reduction and PCA, which is
relevant to understanding data-dependent preprocessing and feature
transformation.

[Paper / DOI](https://doi.org/10.1002/wics.101)

---

### 19. Feature Selection: A Data Mining Perspective

**Authors:** Jain & Zongker  
**Year:** 1997

Provides foundational work on feature-selection methods and their role in
machine-learning pipelines.

[Paper / DOI](https://doi.org/10.1109/34.574797)

---

### 20. LLM-Guided Automated Feature Engineering for Time Series Data with
Temporal Leakage Control

**Year:** 2026

Investigates LLM-assisted feature engineering for time-series data with
specific attention to temporal leakage control.

[Paper / DOI](https://doi.org/10.3390/ai7070245)

---

# Datasets

Relevant datasets are documented separately with their source,
description, potential application, and link.

[View Datasets](datasets/datasets.md)

Datasets can be used to study:

- Data leakage
- Feature engineering
- Temporal feature construction
- Classification
- Feature selection
- Automated machine learning
- Validation strategies

---

# Tools and Libraries

The repository documents useful tools and libraries for developing and
evaluating feature-engineering pipelines.

[View Tools and Libraries](tools/tools.md)

Important tool categories include:

- Machine-learning pipelines
- Automated feature engineering
- Feature stores
- Data validation
- Experiment tracking
- Feature selection
- Model evaluation

---

# GitHub Implementations

This section contains existing open-source implementations relevant to
the research topic.

[View GitHub Implementations](implementations/implementations.md)

Repositories are evaluated using criteria including:

- Documentation quality
- Source-code availability
- Maintenance and activity
- Examples
- Reproducibility
- License
- Connection to research papers or projects

---

# Tutorials and Learning Resources

The repository also contains authoritative learning resources covering
data leakage, automated feature engineering, data validation, feature
stores, and machine-learning pipelines.

[View Tutorials and Learning Resources](resources/resources.md)

The collection includes:

1. scikit-learn documentation on common machine-learning pitfalls
2. Featuretools automated feature-engineering documentation
3. Feast point-in-time join documentation
4. MLflow experiment-tracking documentation
5. Great Expectations data-validation documentation

---

# Research Challenges

Several important challenges remain in developing reliable AI-assisted
feature-engineering systems.

## 1. Automated Leakage Detection

Future systems should automatically inspect feature dependencies,
timestamps, preprocessing operations, prompts, validation procedures,
and model-selection history.

## 2. Feature Provenance

AI-generated features should maintain information about:

- Source columns
- Transformation operations
- Timestamps
- Training folds
- Prompt versions
- LLM/model versions
- Generated code
- Evaluation data
- Feature-selection decisions

## 3. Causal Feature Validity

A feature that is predictive is not necessarily valid for deployment.
Future systems should consider whether a feature would legitimately be
available under the intended prediction scenario.

## 4. Leakage-Aware LLM Prompts

Prompts should explicitly define:

- Prediction time
- Allowed information
- Forbidden information
- Target availability
- Temporal constraints

## 5. Standardized Leakage Benchmarks

Future benchmarks could include controlled examples of:

- Preprocessing leakage
- Temporal leakage
- Target leakage
- Duplicate leakage
- Group leakage
- Target-encoding leakage
- Feature-selection leakage
- Validation-feedback leakage
- LLM prompt leakage

## 6. Human-AI Verification

A promising architecture is:

```text
Generation Agent
        ↓
Leakage Verification Agent
        ↓
Human Approval
        ↓
Model Training
