---
title: Understanding Linear Regression [3/4]
layout: single
author_profile: true
read_time: true
categories: [Machine Learning]
excerpt : Multiple Linear Regression
---
 
Now that you have estimated the parameters for simple linear regression with OLS let's do the same for multiple linear regression.

From L1 content, you have the idea of Multiple Linear Regression. Let's recall a bit. Multiple linear regression generalizes simple linear regression by allowing more than one input variable: 𝑥1,𝑥2,…,𝑥𝑑 . The goal of multiple linear regression is to find a relationship between the input variables and the output variable. This relationship is represented mathematically as follows:

<figure>
	<img src="/images/8_1.png">
	<figcaption></figcaption>
</figure>

𝛽1 through 𝛽𝑑 are the estimated regression coefficients for the independent variables  𝑥1  through  𝑥𝑑 . As in simple linear regression, the regression model to get actual output variable is:

<figure>
	<img src="/images/8_2.png">
	<figcaption></figcaption>
</figure>

𝜖 is the random error or residual, which reflects the difference between the actual output point and predicted output point.




