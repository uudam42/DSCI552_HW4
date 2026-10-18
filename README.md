# DSCI 552 Homework 4

Time series classification on the UCI Activity Recognition (AReM) data set (binary and multi-class), plus ISLR exercises 4.8.3 and 4.8.7.

## Structure

```
.
├── data/
│   └── AReM/
│       ├── bending1/ ... walking/      # 7 activity folders, 88 instances
│       ├── bendingType.pdf
│       └── sensorsPlacement.pdf
├── notebook/
│   └── Agudanmu_Danmu_HW4.ipynb
└── requirements.txt
```

## How to run

```bash
pip install -r requirements.txt
cd notebook
jupyter notebook Agudanmu_Danmu_HW4.ipynb
```

The notebook reads the data with the relative path `../data/AReM/`, so it should be run from the `notebook/` folder. The Homework 3 code needed here (loading/cleaning the raw files, the train/test split and time-domain feature extraction) is included at the top of the notebook, so it runs on its own.

Running all cells takes a few minutes, mostly the cross-validation over the number of pieces `l` in 2(a)iii and 2(c).

## Contents

- **Problem 1** — HW3 feature extraction code, extended to break each series into `l` pieces.
- **Problem 2(a)** — Logistic regression for bending vs. other: scatter plots, choosing `(l, p)` with stratified 5-fold CV and recursive feature elimination (right vs. wrong way), confusion matrix, ROC/AUC, coefficients and p-values, test results, separation, case-control sampling.
- **Problem 2(b)** — L1-penalized logistic regression, compared with RFE / p-values.
- **Problem 2(c)** — 7-class classification with L1-penalized multinomial regression, Gaussian Naïve Bayes and Multinomial Naïve Bayes (confusion matrices and one-vs-rest ROC).
- **Problems 3 and 4** — ISLR 4.8.3 and 4.8.7.
