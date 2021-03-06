# SyriaTelCustChurn
Phase 3 Project: Flatiron School
# Overview

The goal of this project was to build a binary classifier to predict whether a customer would "soon" leave the telecommunications company, SyriaTel. The term "churn" is used to describe a customer leaving.

According to the provided dataset, the current churn rate for SyriaTel is about 14%. A reasonable goal would be to reduce this rate to 7%-about half of the current total.

Using the provided dataset, the following questions were addressed:

* What features are the primary determinants of customer "churn"?
* Are there any predictable patterns?
* How can SyriaTel use these findings to implement cost-effective solutions?


## What is the *best metric* to use to maximize the reults?

SyriaTel would save the most money by prioritizing the retention of current customers over the aquisition of new customers.

In statistics, a type I error is a false-positive result, meaning that a null hypothesis is rejected when it is actually true. A  type II error is  a false-negative result, meaning that a null hypothesis is not rejected when it is actually false.

For this project, incorrectly classifying a false-negative (type II error) would be worse than incorrectly classifying a false-positive. A false negative would mean that the reality of a customer canceling would have been overlooked.

My goal was to **build a classifier that minimizes false negatives**.

# Building a Classifier

The following models were built and evaluated for recall:
* Logistic Regression
* K-Nearest Neighbors
* Decision Tree Model
* Bagged Trees
* Adaboost
* Gradient Boost
* XBoost

I ultimately decided to use my decision tree classifier for further analyses.

The decision tree had a recall score of 74%. In binary classification, “recall” is the ratio of true positives over the number of false negatives.

Recall took priority over precision because my goal is to minimize false negatives.


# Visualizing Results of Model Using SHAP

SHAPley Additive exPlanations is a tool that creates visualizations for a machine learning model. The resource I used to fit SHAP to my data can be found [HERE](https://anvilproject.org/guides/content/creating-links).

On the right side of the graph below, the legend indicates that RED is HIGH feature value and BLUE is LOW feature value. On the y axis, the features are divided individually. The x axis ranks how significant the impact is.

***If the feature has a tail going to the right, it means that those values are causing an impact on model output, pushing customer churn from zero (not churning) to one (churn).***

![](A06DC5AC-CC16-4DC8-9AE6-FEE83D16D5E9_4_5005_c.jpeg)


# Findings and Reccomendation

![](2A9755D0-3F4D-432A-8127-4B94D6F551E6.jpeg)

![](A237068E-ABA2-4E68-8C90-9F8EADB539E9.jpeg)

## Highest contributors of customer churn:
* Having an international plan
* Total number of day minutes
* High number of customer service calls
* Total number of evening minutes

## Lowest contributors of customer churn:
* Number of Voicemail Messages
* Total international calls
* State
* Area code

It is evident that SyriaTel charges customers based on the number of minutes they use to make calls. ALong with high customer service calls, the highest contributors of customer churn are factors that lead to a higher bill.

According to the data, the average charge per user is about $60. My recommendation would be for the company to charge a flat monthly fee to the demographic of customers who are charged $60 or less monthly. A higher tier plan could be offered to customers with higher phone use.

If SytriaTel can retain 247 more of the customers listed in this dataset, they would reach the goal of reducing thier churn rate from 14% to 7%. As thier business model improves, it would be wise to compare thier processes with thier competitors', and continue to evaluate thier churn rate with renewed persepective.
