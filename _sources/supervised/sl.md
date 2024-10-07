# Supervised learning

Supervised learning is the most commonly used type of machine learning. It involves training a model on labeled data, where the input data is paired with the correct output. The general pipeline of supervised learning:

- obtain a training **dataset** $\mathcal D = \{(\boldsymbol x_i, y_i)\}_{i=1}^n$ consisting of **samples** $\boldsymbol x_i$ paired with **labels** (or **targets**) $y_i$;

- build some **model** which makes predictions $\widehat y = f(\boldsymbol x)$ on each sample $\boldsymbol x$;

- choose a **loss function** $\mathcal L(\mathcal D) = \sum\limits_{i=1}^n \ell(f(\boldsymbol x_i), y_i)$ where $\ell(\widehat y, y)$ measures how good is the prediction $\widehat y = f(\boldsymbol x)$;

- minimize the loss function $\mathcal L(\mathcal D) \to \min$ to find the optimal model (this is called **fitting the model**).

After these steps the model is ready to make (hopefully, good enouch) predictions on new unseen data.

## Dataset

In supervised learning training **dataset** $\mathcal D = \{(\boldsymbol x_i, y_i)\}_{i=1}^n$ consists of

- training **samples** $\boldsymbol x_i$ which are usually vectors from a multidimensional space $\boldsymbol x_i \in \mathbb R^d$;

- **targets** (or **labels**) $y_i \in \mathcal Y$ paired with samples $\boldsymbol x_i$.

The elements of a training sample

$$
    \boldsymbol x^{\mathsf T} = (x_1, \ldots, x_d)
$$

are also called **features**. Thus, if $\boldsymbol x_i \in \mathbb R^d$, then dataset $\mathcal D$ has $d$ (numeric) features. All training samples

$$
    \boldsymbol x_i, \quad i = 1, \ldots, n,
$$

if written row by row, form the {ref}`feature matrix <feature-matrix>`.
