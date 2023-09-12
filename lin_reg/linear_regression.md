# Linear regression

```{figure} https://www.mihaileric.com/static/linear_regression_joke-9400ea8c70e0500f1934f7a22c86bc68-b75a8.png
:align: center
```

Linear regression is a fundamental statistical and machine learning technique used for modeling the relationship between a dependent variable (target) and one or more independent variables (features). If we have $n$ training samples an $d$ features, they form a numeric dataset

```{math}
:label: dataset
\mathcal D = \{(\boldsymbol x_i, y_i)\}_{i=1}^n, \quad \boldsymbol x_i \in \mathbb R^d.
```

More precisely, the linear regression is called

- **simple linear regression** if $d=1$;
- **multiple linear regresion** if $d>1$;
- **multivariate linear regression** if the labels are vectors: $\boldsymbol y_i \in \mathbb R^m$, $m>1$.
