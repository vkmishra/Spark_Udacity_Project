# Spark_Udacity_Project
## Spark Project Overview

**Sparkify** is a digital music service similar to [**Netease** **Cloud** **Music**]( https://music.163.com/ ) or [**QQ Music**](https://y.qq.com). Many of the users stream their favorite songs in Sparkify service everyday, either using free tier that places advertisements in between the songs, or using the premium subscription model where they stream music as free, but pay a monthly flat rate. User can upgrade, downgrade or cancel their service at anytime.  

This is a `Customer Churn Prediction Problem` , 
So, our job is deep mining the customers' data and implement appropriate model to predict customer churn as follow steps:

- Clean data: fill the nan values , correct the data types, drop the outliers.
- EDA: exploratory data to look features' distributions and correlation with key label (churn).
- Feature engineering: extract and found customer-features and customer-behavior-features; Implement standscaler on numerical features.
- Train and measure models:  I choose logistic regression, linear svm classifier, decision tree and random forest classifier to train a baseline model and tuning a better model from best of them. It is worth mentioning that this data is unbalanced because of less churn customers, so we choose `f1 score`  as a metrics to measure models' performance.

## Installation

- Python 3.6
- PySpark ML
- Jupyter

## Results

The baseline of four machine learning methods: Logistic Regression, Linear SVC, Decision Tree Classifier and Random Forest Classifier. 

![u8Af6e.png](https://s2.ax1x.com/2019/09/29/u8Af6e.png)

Though the `LinearSVC` spent more training time, but it can get the highest f1 score 0.702. And the `LogisticRegression` has a medium training time and f1 score, maybe I can tuning it to get a higher 
score. So I'll choose `LinearSVC` and `LogisticRegression` to tuning, and the result is as follows:


Considering this is only a quit mini dataset and our purpose is scaling this up to the total 12G  dataset, so, the logistic regression is the best model from now on in this project.
