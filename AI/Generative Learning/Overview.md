Training Data: Set of data
Observation: A data entry
Features: Data on each observation

Generative models need to be probabilistic (non deterministic, like calculating same operation), so they include some stochastic part. We need to define a probability of how the data set can be generated.

Difference with Discriminative models is that those are supervised learning (labeled) while generative are not (a form of unsupervised learning).

**Generative Model Framework**
We assume that the observations have been generated according to some unknown distribution, pdata. A generative model pmodel tries to mimic pdata. If we achieve this goal, we can sample from pmodel to generate observations that appear to have been drawn from pdata.

We are impressed by pmodel if: 
* Rule 1: It can generate examples that appear to have been drawn from pdata. 
* Rule 2: It can generate examples that are suitably different from the observations in X. In other words, the model shouldn’t simply reproduce things it has already seen.

Challenges:
* How does the model cope with the high degree of conditional dependence between features: We need to get some structure from data
* How does the model find one of the tiny proportion of satisfying possible generated observations among a high-dimensional sample space?