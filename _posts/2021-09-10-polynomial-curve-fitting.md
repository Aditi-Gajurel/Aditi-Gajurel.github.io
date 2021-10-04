---
layout: post-no-feature
title: "Polynomial Curve Fitting"
comments: true
category: articles
---
Polynomial Curve Fitting is an example of Regression, a supervised machine learning algorithm.
- __End Goal of Curve Fitting__: We observe a real-valued input variable, __x__, and we intend to predict the target variable, __t__. Polynomial Curve fitting is a generalized term; curve fitting with various input variables, __x__, __y__, and many more.

We will see curve fitting on a synthetic dataset.

For the synthetic dataset, we will generate the data points from a function sin2pix with some random normal noise included.


```
## Imports
import warnings
import numpy as np
import matplotlib.pyplot as plt

## Set a seed
np.random.seed(0)

## Create Synthetic Dataset
x = np.linspace(0.0, 1.0, num=10)
t = (np.sin(2*np.pi*x)) + np.random.normal(0, 1, 10)

txt="Fig 1.1: Scatter plot of the observations with targets"
plt.scatter(x, t)
plt.xlabel("Observations, (x)")
plt.ylabel("Targets, (t)")
plt.title("Synthetic data points")
plt.show()
```
<figure>
	<img src="/images/1_1.png">
	<figcaption>Figure 1.1</figcaption>
</figure>

## In mathematical Notations

<figure>
	<img src="/images/1_2.png">
	<figcaption></figcaption>
</figure>

The scatter plot in Figure 1.1 possesses an underlying regularity which we want to learn. This is an intricate problem since we have a finite number of data set with noises embedded.

Now, let's consider a simple approach for curve fitting. Consider a polyomial function of the form:


<figure>
	<img src="/images/1_3.png">
	<figcaption></figcaption>
</figure>

<figure>
	<img src="/images/1_4.png">
	<figcaption></figcaption>
</figure>

__Determinine the unknown parameters,  w__

The value of the coefficients is found by fitting the polynomial to the training dataset. For this, we minimize the error function that calculates the misfit between function  𝑦(𝑥,𝑤)  and the training data points. One of the widely used error functions is the Sum of the Squares of the Errors (SSE).



