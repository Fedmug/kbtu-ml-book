# Probabilistic models

In probabilistic approach all quantities are considered as **random variables**. Each training sample $(\boldsymbol x, y)$ comes from a joint probability distribution with density $p(\boldsymbol x, y)$. If we are using some model of machine learning with parameters $\boldsymbol w$, then this density is conditioned on $\boldsymbol w$:

$$
    (\boldsymbol x, y) \sim p(\boldsymbol x, y\vert \boldsymbol w).
$$

The parametric family $p(\boldsymbol x, y\vert \boldsymbol w)$ is called a **probabilistic model** of a machine learning problem.

## Maximum likelihood estimation

The **likelihood** of the dataset
$\mathcal D = (\boldsymbol X, \boldsymbol y) = \{(\boldsymbol x_i, y_i)\}_{i=1}^n$ is

$$
    p(\boldsymbol y \vert \boldsymbol X, \boldsymbol w).
$$

If the samples $(\boldsymbol x_i, y_i)$ are i.i.d., then

$$
    p(\boldsymbol y \vert \boldsymbol X, \boldsymbol w) = \prod_{i=1}^n p(y_i \vert \boldsymbol x_i, \boldsymbol w).
$$

The optimal weights $\boldsymbol{\widehat w}$ maximize the likelihood, or, equivalently, log-likelihood:

```{math}
:label: log-likelihood-max
    \log p(\boldsymbol y \vert \boldsymbol X, \boldsymbol w) = \log\prod_{i=1}^n p(y_i \vert \boldsymbol x_i, \boldsymbol w) = \sum_{i=1}^n \log p(y_i \vert \boldsymbol x_i, \boldsymbol w) \to \max\limits_{\boldsymbol w}.
```

Alternatively, one can minimize **negative log-likelikelihood** (**NLL**):

$$
- \log p(\boldsymbol y \vert \boldsymbol X, \boldsymbol w) = -\sum_{i=1}^n \log p(y_i \vert \boldsymbol x_i, \boldsymbol w) \to \min\limits_{\boldsymbol w}.
$$

The optimal estimation of weights $\boldsymbol{\widehat w}$ maximizing log-likelihood {eq}`log-likelihood-max` is called **maximum likelihood estimation** (**MLE**).

## Bayesian approach

![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Thomas_Bayes.gif/274px-Thomas_Bayes.gif)

From {eq}`log-likelihood-max` we obtain a point estimation $\boldsymbol {\widehat w}_{\mathrm{MLE}}$. In Bayesian framework we estimate not points but distributions!

Assume that parameters $\boldsymbol w$ have **prior** distribution $p(\boldsymbol w)$. Observing the dataset $\mathcal D$, we can apply the Bayes formula and obtain **posterior** distribution

$$
    p(\boldsymbol w \vert \mathcal D) = \frac{p(\mathcal D \vert \boldsymbol w)p(\boldsymbol w)}{p(\mathcal D)}.
$$

**Maximum a posteriori estimation** (**MAP**) maximizes posterior distribution:

$$
    \boldsymbol{\widehat w}_{\mathrm{MAP}} = \arg\max\limits_{\boldsymbol w} p(\boldsymbol w \vert \mathcal D).
$$
