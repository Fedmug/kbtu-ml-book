<!-- #region -->
# Multilayer perceptron (MLP)

**Multilayer perceptron** (MLP) was originally introduced in {cite:p}`rosenblatt1958perceptron`. It is a simplest type of feedforward artificial neural network that consists of multiple layers of interconnected artificial neurons (perceptrons).

```{figure} https://miro.medium.com/v2/resize:fit:1400/1*ofVdu6L3BDbHyt1Ro8w07Q.png
:align: center
```

MLP consitsts of **neurons**, each neuron holds a number. In the picture above we can see an input layer of neurons $x_1, \ldots, x_n$ and one neuron $z$ of the output layer. To calculate $z$ one needs to apply $2$ operation:


* linear tranformation

$$
    y = \sum\limits_{i=1}^n w_i x_i + w_0 
$$

* activation function 

$$
    z = \psi(y), \quad \psi(y) = \mathbb I[y > 0].
$$

If we have several neurons $z_1, \ldots, z_m$ in the output layer, then the linear transformation between layers can be written as

```{math}
:label: linear-layer-coord
    z_j = \sum\limits_{i=1}^n w_{ij} x_i + b_j, \quad j = 1, \ldots, m.
```

```{admonition} Question
:class: important
Denote $\boldsymbol x^{\mathsf T} = (x_1, \ldots, x_n)$, $\boldsymbol z^{\mathsf T} = (z_1, \ldots, z_m)$,  $\boldsymbol W = (w_{ij})$. How to rewrite {eq}`linear-layer-coord` in matrix form?
```
<!-- #endregion -->
