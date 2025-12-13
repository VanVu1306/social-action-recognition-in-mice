# Kaggle: Social Action Recognition in Mice

**Group:** VANGA
**Competition Year:** 2025
**Course:** Machine Learning - 2526I_INT3405E_1
**Members:**

| Student ID      | Name                 | Email              |
| ----------------| ---------------------| -------------------|
| 23021647        | Hoang Thi Thanh Nga  | 23021647@gmail.com |
| 23021747        | Vu Nhat Tuong Van    | 23021747@gmail.com |

This repository contains all **codes and Jupyter notebooks** developed during participation in the **Kaggle Social Action Recognition in Mice** competition. The notebooks are organized by submission version and reflect the iterative modeling and feature-engineering process.

---

## Leaderboard Results

### Public Leaderboard Performance

> **Best Public Score:** `0.420`  
> **Best Public Rank:** `927 / 1411`

| Submission ID  | Notebook                         | Public Score | Notes              |
| -------------- | -------------------------------- | ------------ | ------------------ |
| v1             | `mabe_xgboost_0362.ipynb`        | 0.362        | Initial Submission |
| v2             | `mabe_lightgbm_0163.ipynb`       | 0.163        |                    |
| v3             | `mabe_ensemble_ver1_0379.ipynb`  | 0.379        |                    |
| v4             | `mabe_ensemble_ver2_0341.ipynb`  | 0.341        |                    |
| v5             | `mabe_ensemble_ver3_0380.ipynb`  | 0.380        |                    |
| v6             | `mabe_ensemble_ver4_0390.ipynb`  | 0.390        |                    |
| v7             | `mabe_ensemble_ver5_0384.ipynb`  | 0.384        |                    |
| v8             | `mabe_ensemble_ver6_0393.ipynb`  | 0.393        |                    |
| v9             | `mabe_ensemble_ver7_0402.ipynb`  | 0.402        |                    |
| v10            | `mabe_ensemble_ver8_0404.ipynb`  | 0.404        |                    |
| v11            | `mabe_ensemble_ver9_0398.ipynb`  | 0.398        |                    |
| v12            | `mabe_ensemble_ver10_0420.ipynb` | 0.420        | Highest Submission |

Notes:

* Scores shown correspond to **public leaderboard** evaluations.
* Some notebooks were exploratory and not submitted.
* Ranking fluctuated as the leaderboard updated.

---

## Key Notebook-by-Notebook Improvemments

Each notebook represents a distinct iteration. Below summarizes **key updates compared to the previous submission**.

### Notebook v1 – XGBoost

* Initial data loading and preprocessing
* Basic feature extraction from tracked body parts
* 1 XGBoost as binary classifier for each action
* `GroupKFold` (3-fold) Cross-Validation
* Simple grid-searched threshold tuning

### Notebook v2 – LightGBM

**Changes from v1:**

* Experimenting LightGBM

**Impact:**

* Additional understanding and comparison between model choices

### Notebook v3 – Early Ensemble and Improving Data Generation

**Changes from v2:**

* Improving Data Generating pipeline (execution time decreased from 6hrs --> 40mins)
* Experimenting Ensemble with 1 XGBoost and 1 LightGBM
* Early implementation of `StratifiedSubsetClassifier` wrapper class
* Early implementation of adaptive/custom threshold map

**Impact:**

* Increment in public leaderboard score
* Understanding of ensemble strategy

### Notebook v4 – Experimenting Ensemble

**Changes from v3:**

* Increase sample sizes on each learners
* Adding more features

**Impact:**

* Understanding of ensemble strategy and runtime improvement

### Notebook v5 – Experimenting Ensemble

**Changes from v4:**

* Experimenting better choice of sample sizes on each learners
* Adding more features

**Impact:**

* Increment in public leaderboard score
* Understanding of ensemble strategy and runtime improvement

### Notebook v6 – Improving Features Engineering

**Changes from v5:**

* Early implementation of adaptive/custom windows map for each subset of data by using EDA
* Adding more features

**Impact:**

* Increment in public leaderboard score
* Better Feature Engineering results

### Notebook v7 – Improving Pipeline Design and Optimization

**Changes from v6:**

* Early implementation of smart sampling strategy
* Adding more features

**Impact:**

* Understanding of Pipeline Design and Optimization

### Notebook v8 – Milestone Improvement in Pipeline Design and Optimization

**Changes from v7:**

* Early implementation of min duration map for each action
* Improving smart sampling strategy with adaptivity by using EDA
* Additions in action-sequence predict generations
* Experimenting Ensemble with 1 XGBoost and 2 LightGBM

**Impact:**

* Increment in public leaderboard score
* Better Pipeline Design and Optimization results

### Notebook v9 – Improving Pipeline Design and Optimization

**Changes from v8:**

* Improving min duration map for each action by using EDA

**Impact:**

* Increment in public leaderboard score
* Better Pipeline Design and Optimization results

### Notebook v10 – Improving Pipeline Design and Optimization

**Changes from v9:**

* Improving action threshold map using Optuna

**Impact:**

* Increment in public leaderboard score
* Better Pipeline Design and Optimization results

### Notebook v11 – Experimenting Ensemble method

**Changes from v10:**

* Experimenting Ensemble with 1 XGBoost, 2 LightGBM and 1 CatBoost

**Impact:**

* Understanding of ensemble strategy

### Notebook v12 – Manual Pipeline Design and Optimization Tuning

**Changes from v11:**

* Experimenting different tuning strategy to find the most suitable parameters

**Impact:**

* Increment in public leaderboard score
* Better Pipeline Design and Optimization results

---

## References & Resources

### Competition & Dataset

* Kaggle Competition: *Social Action Recognition in Mice*
* MABe (Mouse Action Benchmark) dataset

### Code & Libraries

* Scikit-learn
* NumPy / Pandas
* Joblib
* xgboost, lightgbm, catboost
* PyTorch (working with GPU)

### Methods & Ideas Referenced

* Data Generation pipeline
* Choices of features in Features Engineering
* Adaptation of stratification in Training process
* Usage of gradient-boosted decision trees (GBDTs)

### External Resources

* Kaggle discussion threads
* Public notebooks within the competition community
  * [MABe V1 | Mouse Action Recognition](https://www.kaggle.com/code/analyticaobscura/mabe-v1-mouse-action-recognition/notebook): Main challenges competitors have to tackle
  * [MABe FPS-Aware Mode-Aware Thresholds v3](https://www.kaggle.com/code/bvproperty/mabe-fps-aware-mode-aware-thresholds-v3): Data Generation pipeline + Choices of features in Features Engineering
  * [MABe | LGB + XGB + CatBoost](https://www.kaggle.com/code/kerta27/mabe-lgb-xgb-catboost/notebook): Usage of gradient-boosted decision trees

> All external ideas were **re-implemented and adapted** within this repository. No code was copied verbatim.

---

## Repository Notes

* This repository is intended for **educational and reproducibility purposes**.
* Notebooks reflect an incremental research workflow rather than a single clean pipeline.
* Results may differ if re-run due to randomness and environment differences.