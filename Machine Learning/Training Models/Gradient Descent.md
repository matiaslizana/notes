Generic optimization algorithm to find optimal solutions to a wide range of problems.
Tweak parameters iteratively in order to minimize a cost function.

**Problems**
* Learning Rate small -> Slow Convergence
* Learning Rate big -> Non Convergence (or out of scope)
* Stucked in a local minimum or plateau (long line)

MSE cost function for a linear regression model is a convex function, and there is always only one global and local minimum.

**To converge easily**
* Features have similar scale
* As less features as possible

Repeat over a number of iterations:
$\theta$ = weights
$\mu$ = learning rate
$\triangle$ = gradient descent
$$ \theta_{next} = \theta - \mu \triangle_\theta MSE(\theta)$$

To calculate the number of iterations, we can set a threshold so it stops automatically when gradient is smaller than the trheshold (so it's not improving that much)