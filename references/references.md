# Verified Research Papers

A curated collection of verified scholarly papers related to data leakage,
feature engineering, automated feature engineering, LLM-assisted feature
engineering, model validation, and leakage prevention.

The papers are organized by research subtopic and include bibliographic
information, a link to the original or authoritative source, and a brief
explanation of their relevance to this repository.

---

## 1. Data Leakage Fundamentals

### 1. Leakage in Data Mining: Formulation, Detection, and Avoidance

**Authors:** Shachar Kaufman, Saharon Rosset, Claudia Perlich, and Ronen Stitelman  
**Year:** 2012  
**Venue:** ACM Transactions on Knowledge Discovery from Data, 6(4), Article 15  
**DOI:** [10.1145/2382577.2382579](https://doi.org/10.1145/2382577.2382579)  
**Paper:** [ACM Digital Library](https://doi.org/10.1145/2382577.2382579)

**Relevance:** This foundational work defines data leakage in predictive
modeling and explains how information that should not be available at
prediction time can lead to overly optimistic model performance.

---

### 2. Overview of Leakage Scenarios in Supervised Machine Learning

**Authors:** L. Sasse, E. Nicolaisen-Sobesky, J. Dukart, S. B. Eickhoff,
M. Götz, S. Hamdan, V. Komeyer, A. Kulkarni, J. M. Lahnakoski,
B. C. Love, F. Raimondo, K. R. Patil, et al.  
**Year:** 2025  
**Venue:** Journal of Big Data, 12, Article 135  
**DOI:** [10.1186/s40537-025-01193-8](https://doi.org/10.1186/s40537-025-01193-8)  
**Paper:** [Springer Nature](https://link.springer.com/article/10.1186/s40537-025-01193-8)

**Relevance:** This survey provides a broad framework for leakage scenarios
in supervised machine learning, including preprocessing, feature selection,
validation, temporal dependencies, and model-selection leakage.

---

### 3. Leakage and the Reproducibility Crisis in Machine-Learning-Based Science

**Authors:** Sayash Kapoor and Arvind Narayanan  
**Year:** 2023  
**Venue:** Patterns, 4(9), 100804  
**DOI:** [10.1016/j.patter.2023.100804](https://doi.org/10.1016/j.patter.2023.100804)  
**Paper:** [Patterns / ScienceDirect](https://doi.org/10.1016/j.patter.2023.100804)

**Relevance:** This study examines the impact of leakage on reproducibility
across scientific fields and proposes a taxonomy and model-information
sheets for identifying leakage.

---

### 4. Don't Push the Button! Exploring Data Leakage Risks in Machine Learning and Transfer Learning

**Authors:** Andrea Apicella, Francesco Isgrò, and Roberto Prevete  
**Year:** 2024  
**Venue:** arXiv preprint  
**Paper:** [arXiv:2401.13796](https://arxiv.org/abs/2401.13796)

**Relevance:** This work examines how data leakage can arise when machine
learning systems are used without sufficient understanding of the underlying
workflow, including transfer-learning scenarios.

---

## 2. Preprocessing, Feature Selection, and Selection Bias

### 5. On Over-Fitting in Model Selection and Subsequent Selection Bias in Performance Evaluation

**Authors:** Gavin C. Cawley and Nicola L. C. Talbot  
**Year:** 2010  
**Venue:** Journal of Machine Learning Research, 11, 2079–2107  
**Paper:** [JMLR](https://www.jmlr.org/papers/v11/cawley10a.html)

**Relevance:** The paper demonstrates how repeated model-selection decisions
can overfit finite validation data and produce biased performance estimates,
which is directly relevant to iterative AI-assisted feature search.

---

### 6. Bias in Error Estimation When Using Cross-Validation for Model Selection

**Authors:** Sudhir Varma and Richard Simon  
**Year:** 2006  
**Venue:** BMC Bioinformatics, 7, Article 91  
**DOI:** [10.1186/1471-2105-7-91](https://doi.org/10.1186/1471-2105-7-91)  
**Paper:** [BMC Bioinformatics](https://pmc.ncbi.nlm.nih.gov/articles/PMC1397873/)

**Relevance:** This study shows that using cross-validation both for model
optimization and final error estimation can produce biased estimates,
supporting the need to separate model selection from final evaluation.

---

### 7. Consensus Features Nested Cross-Validation

**Authors:** Brett A. McKinney  
**Year:** 2020  
**Venue:** Bioinformatics, 36(10), 3093–3098  
**DOI:** [10.1093/bioinformatics/btaa046](https://doi.org/10.1093/bioinformatics/btaa046)  
**Paper:** [Oxford Academic](https://academic.oup.com/bioinformatics/article/36/10/3093/5716331)

**Relevance:** This work combines feature selection with nested
cross-validation and demonstrates how nested procedures can reduce
overfitting and improve feature-selection reliability.

---

### 8. Inflated Prediction Accuracy of Neuropsychiatric Biomarkers Caused by Data Leakage in Feature Selection

**Authors:** Miseon Shim, Seung-Hwan Lee, and Han-Jeong Hwang  
**Year:** 2021  
**Venue:** Scientific Reports, 11, Article 7980  
**DOI:** [10.1038/s41598-021-87157-3](https://doi.org/10.1038/s41598-021-87157-3)  
**Paper:** [Scientific Reports](https://www.nature.com/articles/s41598-021-87157-3)

**Relevance:** The study experimentally demonstrates that performing feature
selection outside the cross-validation procedure can substantially inflate
prediction accuracy.

---

### 9. Data Leakage Inflates Prediction Performance in Connectome-Based Machine Learning Models

**Authors:** Matthew Rosenblatt, Link Tejavibulya, Rongtao Jiang,
Stephanie Noble, and Dustin Scheinost  
**Year:** 2024  
**Venue:** Nature Communications  
**DOI:** [10.1038/s41467-024-46150-w](https://doi.org/10.1038/s41467-024-46150-w)  
**Paper:** [Nature Communications](https://www.nature.com/articles/s41467-024-46150-w)

**Relevance:** This study evaluates several leakage mechanisms and shows
that feature-selection leakage and repeated subjects can substantially
inflate predictive performance.

---

### 10. Guiding Questions to Avoid Data Leakage in Biological Machine Learning Applications

**Authors:** Judith Bernett, David B. Blumenthal, Dominik G. Grimm,
Florian Haselbeck, Roman Joeres, Olga V. Kalinina, et al.  
**Year:** 2024  
**Venue:** Nature Methods, 21, 1444–1453  
**Paper:** [Nature Methods](https://www.nature.com/articles/s41592-024-02362-y)

**Relevance:** This perspective provides practical questions for identifying
and preventing leakage in complex biological machine-learning workflows.

---

## 3. Automated Feature Engineering

### 11. Deep Feature Synthesis: Towards Automating Data Science Endeavors

**Authors:** James Max Kanter and Kalyan Veeramachaneni  
**Year:** 2015  
**Venue:** 2015 IEEE International Conference on Data Science and Advanced Analytics (DSAA)  
**DOI:** [10.1109/DSAA.2015.7344858](https://doi.org/10.1109/DSAA.2015.7344858)  
**Paper:** [IEEE DOI](https://doi.org/10.1109/DSAA.2015.7344858)

**Relevance:** This foundational paper introduces Deep Feature Synthesis,
an automated approach for generating features from relational data.
It provides important background for understanding automated feature
engineering systems.

---

### 12. ExploreKit: Automatic Feature Generation and Selection

**Authors:** Gilad Katz, Eui Chul Richard Shin, and Dawn Song  
**Year:** 2016  
**Venue:** 2016 IEEE International Conference on Data Mining (ICDM), 979–984  
**DOI:** [10.1109/ICDM.2016.0123](https://doi.org/10.1109/ICDM.2016.0123)  
**Paper:** [IEEE DOI](https://doi.org/10.1109/ICDM.2016.0123)

**Relevance:** ExploreKit automatically generates candidate features and
uses machine-learning-based feature selection to identify useful features,
making it directly relevant to automated feature-search pipelines.

---

### 13. Automating Feature Engineering

**Authors:** Udayan Khurana, Fatemeh Nargesian, Horst Samulowitz,
Elias Khalil, and Deepak Turaga  
**Year:** 2016  
**Venue:** NIPS 2016 Workshop on Artificial Intelligence for Data Science  
**Paper:** [Workshop Paper](https://workshops.inf.ed.ac.uk/nips2016-ai4datasci/papers/NIPS2016-AI4DataSci_paper_13.pdf)

**Relevance:** This work investigates automated feature engineering using
exploratory and learning techniques and provides background for automated
data-science pipelines.

---

### 14. One Button Machine for Automating Feature Engineering in Relational Databases

**Authors:** Hoang Thanh Lam, Johann-Michael Thiebaut, Mathieu Sinn,
Bei Chen, Tiep Mai, and Oznur Alkan  
**Year:** 2017  
**Venue:** arXiv preprint, arXiv:1706.00327  
**Paper:** [arXiv](https://arxiv.org/abs/1706.00327)

**Relevance:** OneBM automates feature discovery from relational databases,
including table joins and data transformations, demonstrating how
automation can increase the scale of feature generation.

---

### 15. AutoLearn — Automated Feature Generation and Selection

**Authors:** Ambika Kaul, Saket Maheshwary, and Vikram Pudi  
**Year:** 2017  
**Venue:** 2017 IEEE International Conference on Data Mining (ICDM), 217–226  
**DOI:** [10.1109/ICDM.2017.31](https://doi.org/10.1109/ICDM.2017.31)  
**Paper:** [IEEE DOI](https://doi.org/10.1109/ICDM.2017.31)

**Relevance:** AutoLearn automatically generates and selects features using
relationships between feature pairs, providing another example of
large-scale automated feature construction.

---

### 16. Automated Feature Engineering for Automated Machine Learning

**Authors:** Casper de Winter, Flavius Frasincar, Bart de Peuter,
Vladyslav Matsiiako, Enzo Ido, and Jasmijn Klinkhamer  
**Year:** 2025  
**Venue:** Knowledge-Based Systems, 321, Article 113671  
**DOI:** [10.1016/j.knosys.2025.113671](https://doi.org/10.1016/j.knosys.2025.113671)  
**Paper:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0950705125007178)

**Relevance:** This recent study investigates combining automated feature
engineering with AutoML and demonstrates the value of integrating the two
processes.

---

## 4. LLM-Assisted Feature Engineering

### 17. Large Language Models for Automated Data Science: Introducing CAAFE for Context-Aware Automated Feature Engineering

**Authors:** Noah Hollmann, Samuel Müller, and Frank Hutter  
**Year:** 2023  
**Venue:** arXiv preprint  
**Paper:** [arXiv:2305.03403](https://arxiv.org/abs/2305.03403)

**Relevance:** CAAFE uses LLMs to generate semantically meaningful features
from dataset descriptions and provides an important foundation for studying
LLM-assisted feature engineering and its potential leakage boundaries.

---

### 18. LLM-FE: Automated Feature Engineering for Tabular Data with LLMs as Evolutionary Optimizers

**Authors:** Nikhil Abhyankar, Parshin Shojaee, and Chandan K. Reddy  
**Year:** 2025  
**Venue:** Transactions on Machine Learning Research  
**Paper:** [arXiv:2503.14434](https://arxiv.org/abs/2503.14434)

**Relevance:** LLM-FE formulates feature engineering as an iterative program
search problem in which LLMs propose feature transformations and use
data-driven feedback to refine the search.

---

### 19. Human-LLM Collaborative Feature Engineering for Tabular Data

**Authors:** Zhuoyan Li, Aditya Bansal, Jinzhao Li, Shishuang He,
Zhuoran Lu, Mutian Zhang, Qin Liu, Yiwei Yang, Swati Jain, Ming Yin,
and Yunyao Li  
**Year:** 2026  
**Venue:** ICLR 2026  
**Paper:** [arXiv:2601.21060](https://arxiv.org/abs/2601.21060)

**Relevance:** This work introduces human–LLM collaboration for feature
engineering, separating feature proposal from feature selection and
incorporating human preference feedback.

---

### 20. Multi-level Diagnosis and Evaluation for Robust Tabular Feature Engineering with Large Language Models

**Authors:** Yebin Lim and Susik Yoon  
**Year:** 2025  
**Venue:** Findings of the Association for Computational Linguistics:
EMNLP 2025, 4630–4655  
**DOI:** [10.18653/v1/2025.findings-emnlp.249](https://doi.org/10.18653/v1/2025.findings-emnlp.249)  
**Paper:** [ACL Anthology](https://aclanthology.org/2025.findings-emnlp.249/)

**Relevance:** This paper studies the robustness of LLM-generated features
and develops a multi-level evaluation framework, making it relevant to
trustworthy and reliable AI-assisted feature engineering.

---

## Verification Note

The papers in this collection were checked against authoritative scholarly
sources such as publisher pages, DOI records, PubMed, conference proceedings,
arXiv, and academic repositories where appropriate.

The repository links to the papers rather than redistributing copyrighted
PDF files.
