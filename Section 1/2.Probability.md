## 1. Probability and Information Theory

Probability models uncertaintiy

3 sources of uncertainty

1. Inherent stochasticity in the system beind modeled
2. Incomplete observability of data
3. Incomplete modeling from generalization

When modeling systems, **Simple but unceratin rules >> Complex but certain rules**

Frequentist vs Bayesian Probability:

Frequentist only rely on observations, without prior information

Bayesians rely of prior information to construct probability

## 2. Random Variables

Random variables are variables that can take on any values.

They may be discrete or continuous.

## 3. Probability Distributions

A probability distribution is a description of how likely a set of random variables take each possible state.

Depending on the type of random variable, continuous or discrete, there are different ways to describe them

**Discrete variables can be decribed using a Probability Mass Function (PMF)**

**Continuous variables can be described using Probability Density Function (PDF)**

The total area under a PDF has a probability of 1

## 4. Marginal Probability

If we know the probability distribution of a set of random variables, we can get the probability distribution of just a **subset** of them. This is called the **marginal probability**

## 5. Conditional Probability

If we are interested in finding the probability of event `A` occuring **given** `B` has occured, this can be represented by the conditional probability equation `P(A|B)`.

This equation can be represented as `P(A|B) = P(A ^ B) / P(B)`

## 6. Chain Rule of Conditional Probability

`P(A ^ B ^ C) = P(A | B ^ C) * P(B ^ C)` -- `1`

`P(B ^ C) = P(B | C) * P(C)` -- `2`

`P(A ^ B ^ C) = P(A | B ^ C) * P(B | C) * P(C)` sub `2` into `1`

## 7. Independence and Conditional Independence

Two random variables `A` and `B` are independent if their probability distribution can be expressed as their products

`P(A ^ B) = P(A) * P(B)`

Two random variables `A` and `B` are **conditionally** independent given a variable `C` if they can be factorized

`P(A ^ B | C) = P(A | C) * P(B | C)`

## 8. Expectation, Variance, Covariance

The expectation of function `f(x)` w.r.t probability distribution `P(x)` is the average or mean value of `f` when `x` is sampled from `P`

Variance is a measure of how much each value of `x` varies in `P`. When variance is low, the values of `f(x)` is close to the expected value.

The square root of the variance is the **standard deviation**

Covariance tells us how much two variables are linearlly related to each other.

When Covariance is positive, it means that the two variables move together

When Covariance is negative, it means that the two variables move inversely

When the absolute value of Covariance is high, it means that the variables move together very closely.

**Correlation** is a scaled version of Covariance. Correlation also tells us if the variables moves together or inversely, but their values are bounded between `-1` and `1`. The values of correlation tell us the strength that these two features move together

If variables are independent, their covariance and correlation values are `0`

**Zero Covariance means two variables have no linear dependence. Independence means they have no linear and non-linear dependece (i.e. you can have zero covariance, but still be dependent in a non-linear relationship)**

## 9. Common Probability Distributions

- Bernoulli Distribution

   - Distribution over a single binary random variables

- Multinoulli Distribution

   - Distribution over a single discrete variable with `k` states where `k>2` and `k` is finite

- Gaussian Distribution

   - Distribution over real value numbers.
   - Central Limit Theorem (CLT) dictates that the sum of many independent random variables approximates a normal distribution

- Exponential and Laplace Distributions

   - In deep learning, we often want a sharp peak when `x=0`. This can be achieved using an exponential distribution

- Dirac Distribution and Empirical Distributions

   - In some cases, we wish to specify that all the mass in a probability distribution cluster around a single point
   - A Dirac Delta Function is defined such that it is zero valued everywhere except 0, yet integrates to 1
   
- Mixtures of Distributions
 
   - It is sometimes common to define probability distributions by combining other simpler distributions
   - Mixture Distribution is made up of several component distributions
   - A common and power mixture model is the Gaussian mixture model
    
## 10. Properties of Logistic Sigmoid and Softplus
 
The Logistic Sigmoid produces an S shape curve, which flattens out when the values of `x` are very positive are very negative.
 
The Softplus graph takes `max(0,x)`, which looks like a ReLU graph
 
## 11. Bayes Rule
 
`P(A | B) = (P(B | A) * P(A)) / P(B)`
 
## 12. Measure Theory
 
**Skipping**
 
## 13. Information Theory
 
Information theory quantifies how much information is present in a signal
 
Learning that an unlikely event has occurred is more informative than learning that a likely event has occurred
 
Likely events should have low information content, while unlikely contents should have higher information content. Independent events should have additive information.

The **Shannon Entropy** of a distribution is the expected amount of information in an event drawn from that distribution.

Distributions that are deterministic have low entropy value. Distributions that are uniform have high entropy values

When the distribution is continuous, the Shannon Entropy is know as the **Differential Entropy**

If we have two separate probability distributions `P(x)` and `Q(x)` over the same random variable `x`, we can measure how different the two distributions are using **Kullback-Leibler (KL) Divergence**

KL Divergence is non-negative, and `KL = 0` if `P(x) == Q(x)`

KL Divergence is non-symmetric `KL(P || Q) != KL(Q || P)`

## 14. Structured Probabilistic Models

A probability can be decomposed, and their individual probabilities be represented as nodes on a graph

`P(A ^ B ^ C) = P(A | B ^ C) * P(B | C) * P(C)`

Directed Graphs: Factorizations into conditional probabilities

Undirect Graphs: Factorized into functions
