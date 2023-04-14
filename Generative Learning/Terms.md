**Sample Space**
The complete set of all values an observation *x* can take (combinations of all values from all features)

**Latent Space**
A more conceptual space where we have some features built from the sample space (low dimensionality)

**Probability Density Function**
Function that maps a point *x* on the sample space to a number between 0 and 1. The sum of the function over all the points on the sample space must equal 1.

**Parametric Modeling**
Family of density functions that can be described using a finite number of parameters $\theta$

**Likelihood**
$L(\theta|x)$ of a parameter set $\theta$ is a function that measures the plausability of $\theta$ given some observed point x

$L(\theta|x) = p_\theta(x)$ 

We have a whole dataset X and we can use log to estimate, so it's more efficient to compute:

$L(\theta|x) = \sum\limits_{x \in X} \log p_\theta(x)$ 

**MLE**
Maximum Likelihood Estimate is a technique that allows us to estimate the set of parameters $\theta$ of a density function that are most likely to explain some observed data X.

$\hat{\theta} = \underset{\theta}{\operatorname{arg max}}L(\theta|X)$

**Representation Learning**
Establishes the most relevant high-level features that describe how groups of pixels are displayed so that is it likely that any point in the latent space is the representation of a well-formed image
