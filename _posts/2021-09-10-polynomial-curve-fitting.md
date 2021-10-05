---
layout: post-no-feature
title: "Polynomial Curve Fitting"
comments: true
category: articles
---
Polynomial Curve Fitting is an example of Regression, a supervised machine learning algorithm.
- __End Goal of Curve Fitting__: We observe a real-valued input variable,  𝑥 , and we intend to predict the target variable,  𝑡 . Polynomial Curve fitting is a generalized term; curve fitting with various input variables,  𝑥 ,  𝑦 , and many more.

We will see curve fitting on a synthetic dataset.

For the synthetic dataset, we will generate the data points from a function  sin2𝜋𝑥  with some random normal noise included.


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

where,

M = order of the polynomial

𝑤0,𝑤1,...,𝑤𝑀 = polynomial coefficients (denoted by vector,  v )

Remember:  𝑦(𝑥,𝑤)  is non linear function of  𝑥  but the linear function of coefficients,  𝑤 . Functions which are linear in terms of unknown parameters are called linear models.
__Determinine the unknown parameters,  w__

The value of the coefficients is found by fitting the polynomial to the training dataset. For this, we minimize the error function that calculates the misfit between function  𝑦(𝑥,𝑤)  and the training data points. One of the widely used error functions is the Sum of the Squares of the Errors (SSE).

<figure>
	<img src="/images/1_5.png">
	<figcaption></figcaption>
</figure>

1/2  has a convenience, which we will see in later chapters. SSE is a non-negative quantity and we wish to choose unknown parameters, w to make SSE minimum. The error function is quadratic so its first derivative for coefficients, w will be a linear equation with w as unknown. So, we can solve for the unique values of w, which we will denote by w∗ since this set of parameters minimize the error function's value and the resulting curve is given by 𝑦(𝑥,𝑤∗).


__Determine the order of the polynomial,  M__

Now, we need to find  M  for the curve.  M  is the order of the polynomial and selection of the order of the polynomial comes under a broad topic, Model Comparison or Model Selection.
- With  M=0
<figure>
	<img src="/images/1_6.png">
	<figcaption></figcaption>
</figure>

For the elucidation, we will see how the unique value for  w  is found out with  M=0 , since it is easiest among all possible valued of  M  to calculate manually. For  M=0 , the coefficient(unknown parameter) is denoted by  𝑤0 , so we wil find  𝑤0  now.

The Error function fully expanded seems like:

<figure>
	<img src="/images/1_7.png">
	<figcaption></figcaption>
</figure>

```
from sympy import *
w_0 = Symbol('w_0')
E = .5 * ((w_0 - 1.76405235)**2 + (w_0 - 1.04294482)**2+ (w_0 - 1.96354574)**2+ (w_0 - 3.1069186)**2+ 
        (w_0 - 2.20957813)**2+ (w_0 + 1.31929802)**2+ (w_0 - 0.08406301)**2+ (w_0 + 1.13616496)**2+ 
        (w_0 + 0.74600646)**2+ (w_0 - 0.4105985)**2) 
```

Now, we compute the first derivative of  E(𝑤0)  with respect to  𝑤0  and solve it for  𝑤0 . Mathematically:

<figure>
	<img src="/images/1_10.png">
	<figcaption></figcaption>
</figure>


In case, we choose higher  M , we would have more more unknown parameters, to state there would be  M+1 , unknown parameters and we would find all the unknown parameters by simply taking the partial derivative of the error function w.r.t to all the unknown parameters.


```
## Calculate the partial derivative w.r.t w_0
Eprime = E.diff(w_0)

## See the output
print(Eprime)
```
Output: 10.0*w_0 - 7.38023171

```
## Solve the linear equation of Eprime by equating to 0.
w_0 = solve(Eprime)
print(w_0)
```
Output: [0.738023171000000]

So, now this is the value for  𝑤0  to minimize the error function. Let's plot this line on the original data points set.


𝑦=0.739

```
plt.scatter(x, t)
plt.show()
```

