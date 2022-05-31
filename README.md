# SyriaTelCustChurn
Phase 3 Project: Flatiron School
# Overview

The goal of this project was to build a binary classifier to predict whether a customer would "soon" leave the telecommunications company, SyriaTel.

The current “churn” rate for SyriaTel is about 14%.

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

The decision tree model, with a recall score of 74%, was chosen for further analyses.


On the right side of the graph, the legend for feature value indicates that RED is HIGH feature value and BLUE is LOW feature value. On the y axis, the features are divided individually. The x axis ranks how significant the impact is.

***If the feature has a tail going to the right, it means that those values are causing an impact on model output, pushing customer churn from zero (not churning) to one (churn).***

# Findings and Reccomendation

Highest contributors of customer churn:
* Having an international plan
* Total number of day minutes
* High number of customer service calls
* Total number of evening minutes
* Lowest contributors of customer churn:

Number of Voicemail Messages
* Total international calls
* State
* Area code

It is evident that SyriaTel charges customers based on the number of minutes they use to make calls. The highest contributors of customer churn are factors that lead to a higher bill.


According to the data, the average charge per user is about $60. My recommendation would be for the company to charge a flat monthly fee to the demographic of customers who are charged $50 or less monthly and a higher tier plan for those who use their phones more.

The goal would be to reduce their churn rate to from 14% to 7% (about half of their current rate).
