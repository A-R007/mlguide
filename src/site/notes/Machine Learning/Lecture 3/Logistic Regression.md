---
{"dg-publish":true,"permalink":"/machine-learning/lecture-3/logistic-regression/","dgPassFrontmatter":true}
---

- A supervised ***classification technique*** that models the conditional probability of an observation belonging to a certain class.
- Logistic regression is used in various fields like social sciences, medicine, and engineering.
	- Relationship between two variables is linear.
	- Logistic function, too large and too small values $\rightarrow$ $[0,1]$.

### Logistic Regression Formula

The logistic regression model is used to model the probability of a binary outcome. The formula for the logistic regression model is:

# $P(Y=1|X) = \frac{1}{1 + e^{-(\beta_0 + \beta_1X_1 + \beta_2X_2 + \cdots + \beta_nX_n)}}$

Where:
- $P(Y=1|X)$ is the probability that the dependent variable $Y$ equals $1$ given the independent variables $X$.
- $\beta_0$ is the intercept.
- $\beta_1, \beta_2, \ldots, \beta_n$ are the coefficients of the independent variables $X_1, X_2, \ldots, X_n$

The logit function (log-odds) is given by:

# $\text{logit}(P) = \ln\left(\frac{P}{1-P}\right) = \beta_0 + \beta_1X_1 + \beta_2X_2 + \cdots + \beta_nX_n$

Where:
- $\text{logit}(P)$ is the natural logarithm of the odds of $P$.

### Likelihood and Log-Likelihood Functions for Logistic Regression

#### Likelihood Function

- The likelihood function estimates model parameters based on observed data.
- It is applicable when modeling binary outcomes in logistic regression.
- The likelihood function for logistic regression, given a set of $n$observations, is:

## $L(\beta) = \prod_{i=1}^n P(Y_i|X_i)^{Y_i} \left(1 - P(Y_i|X_i)\right)^{1 - Y_i}$

Where:
## $P(Y_i|X_i) = \frac{1}{1 + e^{-(\beta_0 + \beta_1X_{i1} + \beta_2X_{i2} + \cdots + \beta_nX_{in})}}$

- $Y_i$ is the observed value of the dependent variable for the $i$-th observation.
- $X_i$ is the vector of independent variables for the $i$-th observation.
- $\beta$ represents the vector of coefficients.

#### Log-Likelihood Function

- Log transformation simplifies product calculations to sum calculations.
- Maximum Likelihood Estimation technique is used in logistic regression for fitting.
- The log-likelihood function is the natural logarithm of the likelihood function. It is given by:

## $\ell(\beta) = \sum_{i=1}^n \left[ Y_i \ln(P(Y_i|X_i)) + (1 - Y_i) \ln(1 - P(Y_i|X_i)) \right]$

Where:
## $P(Y_i|X_i) = \frac{1}{1 + e^{-(\beta_0 + \beta_1X_{i1} + \beta_2X_{i2} + \cdots + \beta_nX_{in})}}$

- $Y_i$ is the observed value of the dependent variable for the $i$-th observation.
- $X_i$ is the vector of independent variables for the $i$-th observation.
- $\beta$ represents the vector of coefficients.
---
## Maximum Likelihood Estimation (MLE)

Estimation technique used to estimate parameters or coefficients for many machine learning models ($Eg:$ Logistic Regression).

![Pasted image 20240718162258.png](/img/user/Machine%20Learning/Lecture%203/Pasted%20image%2020240718162258.png)

### Steps:
- Define Likelihood Function.
- Write Log-like Function.
- Find Maximum of Log-like Function.
- Estimate the Parameters.
- Check model Fit.
- Make Predictions and Evaluate.

### Pros
- Simple Model.
- Low Variance.
- Low Bias.
- Provides Probability.
### Cons
- Unable to model non-linear relationship.
- Unstable when classes are well separable.
- Unstable when there are more than 2 classes.
---