Most common performance measure is RMSE for a regression model. We need to find the value of $\theta$ that minimizes RMSE. MSE is simpler to calculate than RMSE and leads to the same result.

MSE:
* m: Number of instances to measure MSE
* y: Labels
$$MSE(\theta) = MSE(X,h_\theta) = \frac1m \sum_{i=1}^m (\theta^Tx^i - y^i)^2 $$