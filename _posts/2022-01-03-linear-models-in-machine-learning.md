---
title: Understanding Linear Regression [1/4]
layout: single
author_profile: true
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

Now that we are warmed up, we will proceed towards building a strong understanding of the underlying mathematical concepts of linear regression. I assume, we are familiar with the basic knowledge on what linear regression is about. If not, here is the basic revisit of linear regression.

__Data__

Input:  𝑥  (i.e, measurements, covariates, features, independent variables)

Output:  𝑦  (i.e., response, dependent variable)

__Goal__

You need to find a regression function  𝑦 ≈ 𝑓(𝑥,𝛽) , where 𝛽 is the parameter to be estimated from observations.

For Simple Linear regression:  𝑦 = 𝛽_0 + 𝛽_1*𝑥 

For Multiple Linear regression:  𝑦 = 𝛽_0 + 𝛽_1*𝑥_1 + 𝛽_2*𝑥_2 + ... + 𝛽_𝑑*𝑥_𝑑, where 𝑑 is the number of features.

A regression method is linear if the prediction 𝑓 is a linear function of the unknown parameters 𝛽.

Linear regression finds several applications in our day to day life. Suppose, in a sales company; you need to maximize the sales; it is essential to know the weightage of each factor, such as advertisement, investment, recruitment to the sales. This is where you use linear regression. As such, we have numerous applications of linear regression.

While modeling linear regression, the standard estimation techniques make several assumptions about the predictor variables or input variables, response variable or output variable, and their relationship.

__Some Assumptions of Linear Regression__

Linear regression should be linear in parameters

The response variable,  𝑦  is the function of input variables,  𝑥 's and parameters,  𝛽 's. But the linearity condition is up to parameters. The output variable should be linear in terms of parameters, not necessarily in terms of input variables.

For example:

The equation below is linear in terms of both inputs and parameters, so hold the assumption.

𝑦 = 𝛽0 + 𝛽1𝑥 

Similarly, equation below is not linear in terms of inputs but linear in terms of parmaeters so it holds the assumption.

𝑦=𝛽0+𝛽1𝑥2 

Lastly, the equation below is linear in terms of input but is not linear in terms of parameters, so it violates the assumption and is not a linear regression model.

𝑦=𝛽0+𝛽21𝑥 

Error or residuals should have constant variance and no autocorrelation.

An essential assumption of the linear regression model is that the residuals or errors have the same variance for all data points. This is called the homoscedasticity. If this variance is not constant (i.e. dependent on input variables,  𝑥′ s), then the linear regression model has heteroscedastic errors and this condition of heteroscedasticity might result incorrect parameters.

