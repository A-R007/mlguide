---
{"dg-publish":true,"permalink":"/machine-learning/lecture-2/bias-variance/","dgPassFrontmatter":true}
---

#### Bias
- Bias is the expectation of the difference between the estimate and the true value.
- Bias values of complex models tend to be lesser than simpler models.
- $Bias(\hat{f(x0)}) = \mathbb{E}[\hat{f(x0)}] - f(x0)$
#### Variance
- Variance is the inconsistency or variability of the model's performance when applied to different data sets.
- Variance values of complex models tend to be higher than simpler models.
- ${Variance} = \mathbb{E}\left[(\hat{f}(x0) - \mathbb{E}[\hat{f}(x0)])^2\right]$
#### Trade-Off
- Reducible error is composed of variance and squared bias of the model.
- Flexibility of a model impacts both its bias and variance.
- The expectation of the squared error is given by $E \left( y_0 - \hat{f}(x_0) \right)^2$.
- This can be decomposed as $E(Y - \hat{Y})^2 = E[f(X) + \epsilon - \hat{f}(X)]^2$.
- Further simplifying this:
	 $E[f(X) + \epsilon - \hat{f}(X)]^2 = \underbrace{[f(X) - \hat{f}(X)]^2}_{\text{Reducible}} + \underbrace{\text{Var}(\epsilon)}_{\\text{Irreducible}}$
- In order to minimize the expected test error rate, we need to select a Machine Learning method that simultaneously achieves low variance and low bias.
	- Negative correlation between variance and bias of model.
	- ML model's flexibility has direct impact on its Variance & Bias.

![Pasted image 20240715150911.png](/img/user/Pasted%20image%2020240715150911.png)
