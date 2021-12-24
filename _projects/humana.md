---
layout: page
title: Predicting Vaccine Hesitancy
description: Built predictive model and user segmentation. Won first place of Humana-Mays Analytics Competition.
img: assets/img/humana.png
importance: 2
category: work
---
## Team
Georgia Tech   

Jia Shi, Siyan Cai, Sam Pang, Manqiu Liu

See details [here](https://www.isye.gatech.edu/news/master-science-analytics-team-wins-humana-mays-healthcare-analytics-case-competition) :stars:

## Method

**Data Preprocessing**   

 - Data type transformation
 - Missing data imputation

**Feature encoding**   

 - binary labels
 - categorical to dummy
 - ordinal trend variable transformation

**Feature Engineering**   

 - External data: regional vaccination rate and social vulnerability index
 - Binning for Age
 - Combining variables: based on feature category and meaning

**Feature Selection**  

 - XGBoost
 - Gini Importance
 - Random Forest with entropy

**Model Building**  

2 stage process with train, validation, test and 6 model comparison

 - Logistic Regression
 - Random Forest
 - Neural Networks
 - GBDT
 - LightGBM
 - XGBoost

**Final Model**  

 - Fine-tuned XGBoost Classifier with Randomized Search
 - Test AUC: 0.6839
 - 90% precision rate for hesitant class
 - Disparity Score: 0.99



