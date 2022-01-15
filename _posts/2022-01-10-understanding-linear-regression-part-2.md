---
title: Understanding Linear Regression [2/4]
layout: single
author_profile: true
read_time: true
categories: [Machine Learning]
excerpt : Work in Progress
---

__Ordinary Least Squares with Simple Linear Regression__
Since you have already been introduced to simple linear regression, we won't discuss the details here.

The simple linear regression model is:

<figure>
	<img src="/images/7_1.png">
	<figcaption></figcaption>
</figure>

where, we need to estimate the parameters, intercept(𝛽0) and slope(𝛽1).

Let's recall an Advertising dataset and simple linear regression performed on scatter plot of sales Vs. TV. With the help of Scikit-Learn, we were able to fit the best regression line among all the possibilities. Here is a snapshot:

<figure>
	<img src="/images/7_2.png">
	<figcaption></figcaption>
</figure>

The blue line is a simple linear regression line with output 𝐲 as sales and 𝐱 as TV. The residual or error, 𝜖 is the difference between the observed value, y𝑖, and predicted value, yhat . The observed value is the actual output data point, which is all red dots in the figure, and the predicted value is the point given by the blue regression line. Error for each output data point is shown by the vertical distance from the actual output data point to the predicted point on a regression line.

The predicted output value is:

<figure>
	<img src="/images/7_3.png">
	<figcaption></figcaption>
</figure>

The observed (actual) output value is:

<figure>
	<img src="/images/7_4.png">
	<figcaption></figcaption>
</figure>

Where  𝜖𝑖  is a random error, not a parameter. The error 𝜖𝑖 as (y-yhat) can either be positive or negative or even 0 sometimes. As we can see in the figure, vertical lines are on either side of the regression line. To avoid the cancellation of the error while summing errors, we square each error and sum them, called Residual Sum of Squares (RSS) or Sum of Squared Errors (SSE).

<figure>
	<img src="/images/7_5.png">
	<figcaption></figcaption>
</figure>

The summation is indexed from  1 to 𝑛, since we have 𝑛 samples. Sum of Squared Errors (SSE) is the function of  𝛽0 and 𝛽1 . We can also take it as Loss function. The main principle of Least Squares is that we should end up choosing intercept (𝛽0) and slope (𝛽1) such that the overall sum is minimum.

Thus, to estimate the parameters, we minimize the sum of squared error. Sum of Squared Errors (SSE) can also be written as:

<figure>
	<img src="/images/7_6.png">
	<figcaption></figcaption>
</figure>

yhat  is replaced with the simple linear regression model equation. Since we tend to minimize  SSE , it is also called an objective function. Since the objective function,  SSE  is a squared term, it is always positive. If we plot objective function, it would be a convex graph facing upwards.

<figure>
	<img src="/images/7_7.png">
	<figcaption></figcaption>
</figure>

