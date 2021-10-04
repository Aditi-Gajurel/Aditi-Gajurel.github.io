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

Let's see if it comes or not.

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
	<figcaption></figcaption>
</figure>


