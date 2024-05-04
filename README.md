# Masters Degree - Thesis
## Topic
Empirical Asset Pricing via Random Forest

## Degree
Master of Science Quantitative Finance

## Institute
Institute for Quantitative Business and Economics Research,
Christian Albrechts Universität zu Kiel

Email: stu213387@mail.uni-kiel.de

## Reviewed by:
* 1- Primary Review: Prof. Dr. Alexander Klos - https://www.qber.uni-kiel.de/de/team/alexander-klos
* 2- Secondary Review: Prof. Dr. Stefan Reitz - https://www.qber.uni-kiel.de/de/team/stefan-reitz

# Table of Contents

- [List of Tables](#list-of-tables)
- [List of Figures](#list-of-figures)
- [1 Introduction](#1-introduction)
  - [1.1 Previous Research](#11-previous-research)
    - [1.1.1 CAPM Beta](#111-capm-beta)
    - [1.1.2 Earnings-to-Price Ratio (E/P)](#112-earnings-to-price-ratio-ep)
    - [1.1.3 Size / Market Value of Equity (ME)](#113-size--market-value-of-equity-me)
    - [1.1.4 Combination of Size and Book-to-Market Equity BE/ME](#114-combination-of-size-and-book-to-market-equity-beme)
    - [1.1.5 Momentum](#115-momentum)
    - [1.1.6 94-Factors](#116-94-factors)
  - [1.2 The Importance of Machine Learning on Asset Pricing](#12-the-importance-of-machine-learning-on-asset-pricing)
- [2 Methodology](#2-methodology)
  - [2.1 Preliminary Concepts of Machine Learning](#21-preliminary-concepts-of-machine-learning)
    - [2.1.1 Definition of Machine Learning](#211-definition-of-machine-learning)
    - [2.1.2 Definition of Statistical Learning](#212-definition-of-statistical-learning)
    - [2.1.3 Supervised vs. Unsupervised Learning](#213-supervised-vs-unsupervised-learning)
    - [2.1.4 Regression vs. Classification](#214-regression-vs-classification)
    - [2.1.5 Resampling Methods](#215-resampling-methods)
  - [2.2 Tree-Based Methods](#22-tree-based-methods)
    - [2.2.1 Regression Trees](#221-regression-trees)
    - [2.2.2 Bagging or Bootstrap Aggregation](#222-bagging-or-bootstrap-aggregation)
    - [2.2.3 Random Forest](#223-random-forest)
- [3 Empirical Study of US Equities](#3-empirical-study-of-us-equities)
  - [3.1 Data Overview](#31-data-overview)
  - [3.2 Model Specification](#32-model-specification)
  - [3.3 Sample Splitting and Tuning via Validation](#33-sample-splitting-and-tuning-via-validation)
  - [3.4 Main Findings](#34-main-findings)
  - [3.5 Return Prediction for Individual Stocks](#35-return-prediction-for-individual-stocks)
    - [3.5.1 Data Modification](#351-data-modification)
    - [3.5.2 Sample Splitting, Estimation Procedure, and Hyperparameter Tuning](#352-sample-splitting-estimation-procedure-and-hyperparameter-tuning)
    - [3.5.3 Model Evaluation](#353-model-evaluation)
    - [3.5.4 Stocks Return Predictions](#354-stocks-return-predictions)
- [4 Conclusion](#4-conclusion)
- [References](#references)
- [Appendix A](#appendix-a)
  - [A.1 Proof for Bagging of Numerical Predictions](#a1-proof-for-bagging-of-numerical-predictions)
  - [A.2 Proof of the Variance Reduction Equation 17](#a2-proof-of-the-variance-reduction-equation-17)
- [Appendix B](#appendix-b)
  - [B.1 Details of the 94 Stock-Level Characteristics](#b1-details-of-the-94-stock-level-characteristics)
  - [B.2 Characteristics Importance by each ML Model in Gu et al. (2020)](#b2-characteristics-importance-by-each-ml-model-in-gu-et-al-2020)
- [Appendix C](#appendix-c)
  - [C.1 Data Pre-Processing](#c1-data-pre-processing)
    - [C.1.1 Filtration](#c11-filtration)
    - [C.1.2 Return Calculation](#c12-return-calculation)
    - [C.1.3 Sample Splitting](#c13-sample-splitting)
  - [C.2 Hyperparameter Tuning via H2O](#c2-hyperparameter-tuning-via-h2o)
  - [C.3 Model Evaluation/Prediction](#c3-model-evaluationprediction)
  - [C.4 Return Prediction for Microsoft and Apple Inc.](#c4-return-prediction-for-microsoft-and-apple-inc)
 
  # Conclusion
  This paper identifies the best 20 stock-level characteristics out of 94 features
examined by Gu et al. (2020) that have explanatory power in explaining the
excess returns exhibited by the US stock market. It also aims to implement
the Random Forest model that incorporates these characteristics to predict the
individual’s stock returns.
Asset pricing applications bring challenges due to a low signal-to-noise ratio.
Machine Learning algorithms, especially Random Forest, can predict returns
based on the signal; thus, leading to better measurement. The Success of
Random Forest based on a significant out-of-sample R-squared ratio brings
hope for optimal portfolio decisions.
