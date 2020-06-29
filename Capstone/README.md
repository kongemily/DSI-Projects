# Capstone Project
#### Emily Kong
#### 29 June, 2020


## Problem Statement

The 80/20 rule has proven true for many businesses–only a small percentage of customers produce most of the revenue. As such, marketing teams are challenged to make appropriate investments in promotional strategies. For this project,we are challenged to analyze a Google Merchandise Store (also known as GStore, where Google swags are sold) customer dataset and identify the best model to predict the probability of the session being revenue-generating. 

The accuracy, f1 score and auc score from different machine-learning models will be compared and used to evaluate to find the best model for prediction.


## Executive Summary

**Exploratory Data Analysis**

From the exploratory data, there are 12 columns with more than 50% of missing values and of these 903,653 rows comprising of 714,167 of unique Visitor ID, only 1.4% of these customers are revenue generating and 1.3% of the rows generated revenue. 

19 columns had just 1 value which had to be dropped as it served to be of no value add. Based on the geoNetwork columns , we were able to see that most of the customer visits originated from the United States. Upon visiting the website, this is not surprising as the range of products available for the US market is much wider and ships out from US, meaning the shipping charges was lower whereas shipping to other parts of the world originates from the UK and charges in pounds. Revenue counts from US was the highest as well, meaning there were more visits which resulted in a transaction, followed by Canada. Other notable sources are chrome 


**Modelling**

Logistic Regression, Extra Trees and Gradient Boosting models are used to model the data. There is a heavy class-imbalance in the data, at 100:1 ratio of non-revenue generating against revenue generating sessions. Random UnderSampler was used to adjust for the imbalance using the sampling strategy of 1:20. 

Gradient Boosting has shown to be the best performing model at an overall accuracy of 96.7%,with f1 score and auc scores of 63% and 79% respectively. ROC-AUC score achieved 98% using this method

 
## Conclusions 

The results for the recall scores at approximately 60% is expectedly lower due to the highly imbalanced data and by using random undersampling: All of the training data points from the minority class (revenue generating) are used but instances are randomly removed from the majority training set till the desired balance is achieved which in this case the ratio applied was 1:20. One disadvantage of this approach is that some useful information might be lost from the majority class due to the undersampling. 


## Considerations 

One future consideration is to use undersampling methods in conjunction with an oversampling technique for the minority class, which may results in better performance than using oversampling or undersampling alone on the training dataset and to explore the Google Analytics Demo Account if there are further information which may serve to be more useful.





