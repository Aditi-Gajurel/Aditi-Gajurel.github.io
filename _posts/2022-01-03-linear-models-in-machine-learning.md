---
title: Linear Regression [1/4]
layout: single
author_profile: false
read_time: true
categories: [Machine Learning]
excerpt : Work in Progress

---

In the pool of machine learning algorithms, linear regression is the most often seen, used, and go-to supervised linear model. When I say this, what do I mean by linear model?

Linear models are the most basic, which explains their widespread use and appeal. If I were to sum up linear models in a single sentence, it would be a model in which features are combined linearly to produce an output.

For instance, suppose we wish to create a linear model that predicts a salary of an individual. In this case, let's take age of an individual, gender of an individual, and an employer as the inputs or features. The linear model would look like:

```
salary = w_0 + w_age*age + w_gender*gender + w_employer*employer

```

w_0 = a constant or a bias (take it as a base salary)

w_age =  a number that tells by what factor does age influences the salary.

w_gender = a number that tells by what factor does gender influences the salary.

w_employer = a number that tells by what factor does employer influences the salary.