A linear model predicts a computed weighted sum of the input features plus a constant (bias)
* $\theta:$ Weights
* x: Features (n: length)

Normal Form: $$ y = \theta_0 + \theta_1x_1 + \theta_2x_2 + ... + \theta_nx_n $$
Vectorized Form:
$$y = \theta x$$
How do we train it? Training means setting its parameters so that the model best fits the training set. We need a measure of how well the model fits the training data.

**Error:** Most common performance measure is RMSE for a regression model. We need to find the value of $\theta$ that minimizes RMSE. MSE is simpler to calculate than RMSE and leads to the same result.

MSE:
* m: Number of instances to measure MSE
* y: Labels
$$MSE(\theta) = MSE(X,h_\theta) = \frac1m \sum_{i=1}^m (\theta^Tx^i - y^i)^2 $$
**Perform Linear Regression**

```
from sklearn.linear_model import LinearRegression
lin_reg = LinearRegression()
lin_reg.fit(X, Y)
y_predict = lin_reg.predict(x_new)
```


`


