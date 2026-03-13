# Microbiome-based BMI prediction using machine learning

This repository contains the code used in the master's thesis:

**"Comparative Evaluation of Machine Learning Models for BMI Prediction from Gut Microbiome Data"**

The project investigates how well body mass index (BMI) can be predicted from gut microbiome composition using different machine learning approaches. The models evaluated include linear regression with regularization (Lasso), gradient-boosted decision trees (XGBoost and CatBoost), and a transformer-based foundation model for tabular data (TabPFN).

The experiments compare model performance, examine the effect of training dataset size, and analyze feature importance across models.

---

## Dataset

The microbiome data were obtained from the **Metalog database**, which aggregates standardized human microbiome profiles together with curated metadata.  

Taxonomic profiles were generated using **MetaPhlAn4**, providing species-level relative abundance estimates for each sample.

The final dataset used in this study contains:

- **9,709 gut microbiome samples**
- **214 microbial species features**
- Metadata variables including **age, sex, and BMI**

Due to data licensing restrictions, the dataset itself is **not included in this repository**.

---

## Methods

The following models were evaluated:

- **Lasso regression** (baseline linear model with L1 regularization)
- **XGBoost** (gradient boosted decision trees)
- **CatBoost** (gradient boosting with symmetric trees)
- **TabPFN** (transformer-based foundation model for tabular data)

Microbiome features were transformed using **centered log-ratio (CLR)** transformation before model training.

Model performance was evaluated using:

- \(R^2\)
- RMSE
- MAE

---


## Running the code

Most analyses are implemented in **R**, with additional scripts in **Python** for running TabPFN.


## Reproducibility

All analyses were conducted using a fixed random seed to ensure reproducibility.  
Intermediate results, trained models, and generated plots are saved to disk during execution.

---

## References
[1] M. Kuhn et al., “Metalog: Curated and harmonised contextual data for global
metagenomics samples”, Nucleic Acids Research, vol. 54, no. D1, pp. D826–
D834, Oct. 2025, issn: 1362-4962. doi: 10 . 1093 / nar / gkaf1118. [Online].
Available: http://dx.doi.org/10.1093/nar/gkaf1118.

[2] R. Tibshirani, “Regression shrinkage and selection via the lasso”, Journal of
the Royal Statistical Society: Series B, vol. 58, no. 1, pp. 267–288, 1996.

[3] T. Chen and C. Guestrin, “Xgboost: A scalable tree boosting system”, in
Proceedings of the 22nd ACM SIGKDD International Conference on Knowl-
edge Discovery and Data Mining, Aug. 13, 2016, pp. 785–794. doi: 10.1145/
2939672.2939785. arXiv: 1603.02754[cs].

[4] L. Prokhorenkova, G. Gusev, A. Vorobev, A. V. Dorogush, and A. Gulin,
“Catboost: Unbiased boosting with categorical features”, in Advances in Neural
Information Processing Systems, vol. 31, Curran Associates, Inc., 2018.

[5] H.-J. Ye, S.-Y. Liu, and W.-L. Chao, A closer look at tabpfn v2: Understanding
its strengths and extending its capabilities, Jun. 11, 2025. doi: 10 . 48550 /
arXiv.2502.17361. arXiv: 2502.17361[cs].

## Author

Vilho Helenius  
University of Turku  
Master's thesis in Data Analytics
