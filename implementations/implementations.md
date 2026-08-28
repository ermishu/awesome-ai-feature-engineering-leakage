# GitHub Implementations

This section reviews existing GitHub implementations related to
data leakage, automated feature engineering, AI-assisted feature
engineering, feature stores, and leakage-aware machine-learning
pipelines.

The repositories were selected based on their relevance to the
research topic:

**Data Leakage Risks in AI-Assisted Feature Engineering Pipelines**

Each project is evaluated according to its purpose, implementation,
documentation, activity, examples, reproducibility, license, and
connection to the research literature.

---

## 1. LLM-FE

**Repository:**  
https://github.com/nikhilsab/llmfe

**Purpose:**  
LLM-FE is an automated feature-engineering system that uses large
language models as evolutionary optimizers for tabular data.

**What it implements:**  
The repository provides source code for an LLM-based feature-engineering
pipeline. It generates candidate features using an LLM and evaluates
the generated features on datasets.

**Why it is relevant:**  
LLM-FE is directly connected to this research topic because LLMs are
used to automatically generate and evaluate features. Such iterative
feature-generation systems create potential leakage risks if evaluation
data, future information, or target-derived information enters the
feature-generation process.

**Documentation quality:**  
The repository provides installation instructions, usage instructions,
evaluation instructions, and information about the required environment.

**Source-code availability:**  
The complete implementation is publicly available on GitHub.

**Examples:**  
The repository provides a shell script for running LLM-FE and an
evaluation notebook for testing generated features on datasets.

**Reproducibility:**  
The repository provides a requirements file and instructions for
creating a Conda environment. API configuration is also documented.

**Maintenance/activity:**  
The repository contains active project material and evaluation code.

**License:**  
MIT License.

**Connection to research:**  
The implementation directly corresponds to research on LLM-assisted
automated feature engineering and is particularly useful for studying
whether iterative LLM-based feature search can introduce data leakage.

**Research paper:**  
Nikhil Abhyankar, Parshin Shojaee, and Chandan K. Reddy,
"LLM-FE: Automated Feature Engineering for Tabular Data with LLMs as
Evolutionary Optimizers."

**Repository link:**  
https://github.com/nikhilsab/llmfe

---

## 2. CAAFE

**Repository:**  
https://github.com/noahho/CAAFE

**Purpose:**  
CAAFE provides a semi-automatic feature-engineering system that uses
large language models and dataset descriptions to generate features.

**What it implements:**  
The repository implements a CAAFE classifier that combines a base
machine-learning classifier with an LLM-based feature-engineering
process.

**Why it is relevant:**  
CAAFE is directly relevant to AI-assisted feature engineering.
The system generates new features and evaluates them iteratively.
This makes it useful for investigating the boundary between feature
generation and validation and for studying whether information from
validation or test data could influence the feature-search process.

**Documentation quality:**  
The README provides an overview, installation guidance, usage examples,
and information about the research paper on which the project is based.

**Source-code availability:**  
The implementation is publicly available on GitHub.

**Examples:**  
The repository provides Python usage examples showing how to create a
CAAFE classifier and fit it to training data.

**Reproducibility:**  
The repository provides implementation instructions and identifies the
base classifier and language-model configuration used by the system.

**Maintenance/activity:**  
The project has a public repository with source code and development
history.

**License:**  
Apache License 2.0.

**Connection to research:**  
CAAFE provides a concrete implementation of LLM-assisted feature
engineering and therefore serves as an important reference for
studying leakage risks in AI-driven feature generation.

**Research paper:**  
Noah Hollmann, Samuel Müller, and Frank Hutter,
"LLMs for Semi-Automated Data Science: Introducing CAAFE for
Context-Aware Automated Feature Engineering."

**Repository link:**  
https://github.com/noahho/CAAFE

---

## 3. Feast

**Repository:**  
https://github.com/feast-dev/feast

**Purpose:**  
Feast is an open-source feature store designed to manage features
consistently for machine-learning training and online inference.

**What it implements:**  
Feast provides offline and online feature stores, feature definitions,
feature retrieval, and feature-serving infrastructure.

**Why it is relevant:**  
Feast is particularly important for this research because it explicitly
addresses point-in-time correctness. Historical feature retrieval uses
timestamps so that future feature values are not accidentally included
in training data.

This directly addresses temporal leakage and future-information leakage.

**Documentation quality:**  
The project provides extensive documentation, quick-start material,
architecture documentation, use cases, and API documentation.

**Source-code availability:**  
The complete source code is publicly available.

**Examples:**  
The repository contains quick-start examples showing how to create
feature repositories, define features, retrieve historical features,
and serve features.

**Reproducibility:**  
The repository provides installation instructions, configuration
examples, documentation, and a structured development workflow.

**Maintenance/activity:**  
The project has an active public development history and ongoing
issues and pull requests.

**License:**  
Apache License 2.0.

**Connection to research:**  
Feast provides a practical implementation of leakage-aware feature
retrieval. It is particularly relevant to the temporal leakage and
feature-generation pipeline risks discussed in this research.

**Important implementation concept:**  
Feast's historical feature retrieval uses event timestamps as upper
bounds for point-in-time joins so that future feature values do not
leak into training data.

**Repository link:**  
https://github.com/feast-dev/feast

---

## 4. OpenMLDB

**Repository:**  
https://github.com/4paradigm/OpenMLDB

**Purpose:**  
OpenMLDB is an open-source machine-learning database and feature
platform designed to produce consistent features for training and
inference.

**What it implements:**  
OpenMLDB provides feature engineering using SQL, time-series
processing, offline/online feature computation, and infrastructure
for consistent feature generation.

**Why it is relevant:**  
The project explicitly identifies data leakage and feature backfilling
as challenges in machine-learning feature engineering. It provides
mechanisms for producing consistent features across offline training
and online inference.

**Documentation quality:**  
The repository includes a README, architecture information,
quick-start instructions, use cases, roadmap, documentation, and
publications.

**Source-code availability:**  
The implementation is publicly available on GitHub.

**Examples:**  
The project provides quick-start instructions, feature definitions,
SQL examples, and documented use cases.

**Reproducibility:**  
The repository provides installation and usage documentation together
with example configurations and feature definitions.

**Maintenance/activity:**  
The project has an active open-source repository and a substantial
development history.

**License:**  
Apache License 2.0.

**Connection to research:**  
OpenMLDB is highly relevant to feature leakage because it focuses on
consistent feature computation between training and inference and
explicitly discusses data leakage and feature backfilling.

**Repository link:**  
https://github.com/4paradigm/OpenMLDB

---

## 5. Featuretools

**Repository:**  
https://github.com/alteryx/featuretools

**Purpose:**  
Featuretools is an open-source Python library for automated feature
engineering.

**What it implements:**  
Featuretools implements Deep Feature Synthesis and automatically
generates features from structured and relational datasets using
transformation and aggregation primitives.

**Why it is relevant:**  
Automated feature generation is one of the main areas of this research.
Automatically generated aggregation and transformation features can
introduce leakage when information from outside the allowed prediction
time is used.

Featuretools therefore provides a useful implementation for studying
how automated feature engineering should be controlled and evaluated.

**Documentation quality:**  
The repository provides installation instructions, documentation
references, examples, add-ons, and feature-engineering demonstrations.

**Source-code availability:**  
The complete source code is publicly available.

**Examples:**  
The README provides examples using Deep Feature Synthesis on timestamped
customer transactions.

**Reproducibility:**  
Installation instructions and example code are provided, making it
possible to reproduce basic feature-engineering workflows.

**Maintenance/activity:**  
The repository has an established open-source development history and
continues to receive updates.

**License:**  
BSD 3-Clause License.

**Connection to research:**  
Featuretools represents an important class of automated feature
engineering systems. It can be used as a baseline for studying
automated feature-generation leakage.

**Related research:**  
James Max Kanter and Kalyan Veeramachaneni,
"Deep Feature Synthesis: Towards Automating Data Science Endeavors."

**Repository link:**  
https://github.com/alteryx/featuretools

---

# Comparison of GitHub Implementations

| Project | Main Focus | Leakage Relevance | AI/Automation | Reproducibility |
|---|---|---|---|---|
| LLM-FE | LLM-based feature engineering | High | Very High | High |
| CAAFE | LLM-assisted feature engineering | High | Very High | High |
| Feast | Point-in-time feature retrieval | Very High | Medium | High |
| OpenMLDB | Consistent feature computation | Very High | Medium | High |
| Featuretools | Automated feature engineering | High | High | High |

---

# Overall Assessment

The five implementations represent complementary approaches to the
research problem.

**LLM-FE** and **CAAFE** demonstrate how large language models can
automate or assist feature engineering.

**Featuretools** demonstrates traditional automated feature generation
using transformation and aggregation primitives.

**Feast** and **OpenMLDB** address an important complementary problem:
ensuring that features used during training are temporally correct and
consistent with the features available during inference.

Together, these implementations provide practical examples for
studying the relationship between automated feature engineering and
data leakage.

---

# Relevance to the Research Topic

The implementations can be mapped to the major leakage risks discussed
in this research:

| Research Risk | Relevant Implementation |
|---|---|
| Automated feature-generation leakage | Featuretools, CAAFE, LLM-FE |
| Iterative feature-search leakage | CAAFE, LLM-FE |
| Temporal leakage | Feast, OpenMLDB |
| Future-information leakage | Feast, OpenMLDB |
| Aggregation leakage | Featuretools, Feast, OpenMLDB |
| Training/serving inconsistency | Feast, OpenMLDB |
| AI-assisted feature engineering | CAAFE, LLM-FE |

These projects can therefore be used as practical reference
implementations when designing and evaluating leakage-aware
AI-assisted feature engineering pipelines.
