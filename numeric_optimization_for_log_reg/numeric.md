# Numeric optimization in logistic regression

## Team members:

1. Project manager - Adema
2. Technical writer - Daulet
3. Author of executable content - Meiram
4. Designer of interative plots - Amina
5. Designer of quizzes - Adilzhan

Link of the book [here](https://headsman-4899.github.io/Numeric_optimization_for_logistic_regression/intro.html)

## Overview of Numeric Optimization

Numeric optimization aims to find the minimum (or maximum) of a given function by iteratively adjusting its parameters. In the context of logistic regression, the goal is to minimize the cost function, which quantifies the difference between predicted probabilities and actual labels.

The logistic regression cost function, often expressed as the binary cross-entropy loss, is a convex function. This convexity allows numeric optimization algorithms to converge to a global minimum efficiently.

## Gradient Descent

Let $x_0$ - be the starting point of the gradient descent. Then we select each next point as follows:

$$ x_{k+1} = x_k - \alpha \nabla f(x_k), $$

where $\alpha$ – this is the step size (aka the learning rate). The general gradient descent algorithm is written very simply and elegantly:

```Python
x = normal(0, 1)                # you can try other types of initialization
repeat S times:                 # another variant: while abs(err) > tolerance
   h = grad_f(x)                # calculating the direction of descent
   x -= alpha * h               # updating the value at the point
```

There is a so-called steepest descent method: choose the step size so as to reduce the function as much as possible:

$$\alpha_k = \arg\min_{\alpha \geq 0} f(x_k - \alpha \nabla f(x_k)).$$

## Newton's Method

So, our task is to unconditionally optimize a smooth function

$$f(x) \to \min_{x \in \mathbb{R}^d}.$$

As with gradient descent optimization, we will look for the direction of functional reduction. But this time we will not use a linear approximation, but a quadratic one:

$$f(x + \Delta x) \approx f(x) + \langle \nabla f(x), \Delta x \rangle + \frac{1}{2}\langle \Delta x, B(x) \Delta x \rangle.$$

Taylor's formula tells us to take $B(x) = \nabla^2 f(x)$. By equating the gradient of this quadratic approximation to zero, we obtain the direction of descent for Newton's method:

$$\Delta x = [B(x)]^{-1} \nabla f(x).$$

Let 's denote $B_k = B(x_k), H_k = B_k^{-1}$. In this case, we can write down an iterative descent algorithm:

$$x_{k+1} = x_{k} - \alpha_k \cdot H_k \nabla f(x_k).$$

In the literature, the Newton method is called such a method at $\alpha_k = 1$, at a different step size $\alpha_k \in (0, 1)$, this method is called the damped Newton method.