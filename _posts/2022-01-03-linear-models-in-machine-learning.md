---
title: Linear Models in Machine Learning
layout: single
author_profile: false
read_time: true
categories: [Machine Learning]
excerpt : Work in Progress

---

Linear models are the simplest, and that is the reason for its wide popularity and application. If I am to speak of a sentence on linear models, it would be, a model where we have linear combination of features to get an output. 

For example: We want to build a linear model which predicts the salary of an individual. In this case, let's take age of an individual, gender of an individual, and an employer as the inputs or features. The linear model would look like:

```
salary = w_0 + w_age*age + w_gender*gender + w_employer*employer

```

w_0 = a constant or a bias (take it as a base salary)

w_age =  a number that tells by what factor does age influences the salary.

w_gender = a number that tells by what factor does gender influences the salary.

w_employer = a number that tells by what factor does employer influences the salary.