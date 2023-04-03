A linear model predicts a computed weighted sum of the input features plus a constant (bias)
* $\theta:$ Weights
* x: Features (n: length)

Normal Form: $$ y = \theta_0 + \theta_1x_1 + \theta_2x_2 + ... + \theta_nx_n $$
Vectorized Form:
$$y = \theta x$$
How do we train it? Training means setting its parameters so that the model best fits the training set. We need a measure of how well the model fits the training data.

**Perform Linear Regression**

```
from sklearn.linear_model import LinearRegression
lin_reg = LinearRegression()
lin_reg.fit(X, Y)
y_predict = lin_reg.predict(x_new)
```


`


