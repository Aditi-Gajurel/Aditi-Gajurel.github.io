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

Multiple linear regression involves more than one input variable, so it is impossible to individually derive a solution for each regression coefficient for each input variable. In a sophisticated regression problem dimension (𝑑 ) can range to very higher values.

So, how do we estimate all regression coefficients?

From multiple linear regresssion model, we have:

<figure>
	<img src="/images/8_3.png">
	<figcaption></figcaption>
</figure>

We have 𝑛 set of observations. So we can write:

<figure>
	<img src="/images/8_4.png">
	<figcaption></figcaption>
</figure>

Xnd  is the 𝑛th observation for  𝑑th feature or input variable. These 𝑛 set of equations can be written in matrix form as:

<figure>
	<img src="/images/8_5.png">
	<figcaption></figcaption>
</figure>

Using mathematical notations, we can write as:

<figure>
	<img src="/images/8_6.png">
	<figcaption></figcaption>
</figure>

𝐲 is a n×1 column matrix where each element is the observed value of output variable. Similarly, 𝐗 is n×(d+1)  matrix. An extra dimension is due to the inclusion of 1′𝑠 in the first column. You can interpret the first column, including 1′s as being multiplied against 𝛽0. There are (d+1) unknown parameters, d regression coefficients for each of the input variables and 1 extra for the intercept, 𝛽0 .So 𝜷 is (d+1)×1 column matrix.






