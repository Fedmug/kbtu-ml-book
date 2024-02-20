# Statistics

Различные типы распределений применяются в качестве теоретических моделей в задачах, связанных со случайностью и неопределённостью. Однако на практике далеко не всегда ясно, какое именно распределение моделирует имеющиеся в наличии данные. А если из каких-либо соображений тип распределения всё же установлен, то следующая задача — оценить параметры этого распределения, например, среднее и/или дисперсию в случае гауссовского распределения $\mathcal N(\mu, \sigma^2)$.

Подобными обратными по отношению к теории вероятностей задачами занимается **математическая статистика**. Типичный пример статистической задачи: по числовой выборке $X_1, \ldots, X_n$ оценить параметры распределения, из которого они были получены. Обычно предполагается, что выборка **i.i.d.** (**i**ndependent and **i**dentically **d**istributed), то есть представляет собой независимые реализации случайной величины с одним и тем же распределением. Параметр этого определения $\theta$ может быть числом или вектором; оценку этого параметра по выборке $X_1, \ldots, X_n$ обычно обозначают $\widehat \theta(X_1, \ldots, X_n)$ или просто $\widehat \theta$.

## Common statistics

**Statistic** is a function of sample $X_1, \ldots, X_n$. Here are some widely used statistics:

1. **Sample average**:

    $$
        \overline X_n = \frac 1n\sum\limits_{i=1}^n X_i.
    $$

2. **Sample variance**:

    $$
        \overline S_n = \frac 1n\sum\limits_{i=1}^n (X_i - \overline X_n)^2.
    $$

3. **Sample median** is the middle element of the rearranged sample

    $$
        X_{(1)} \leqslant X_{(2)} \leqslant \ldots \leqslant X_{(n)}.
    $$

    If $n$ is odd, $n=2m+1$, then the middle element is unique and 

    $$
    \mathrm{med}(X_1,\ldots, X_n) = X_{(m)}
    $$

    Otherwise, if $n=2m$, then median is taken as average of two middle elements:

    $$
    \mathrm{med}(X_1,\ldots, X_n) = \frac 12(X_{(m)}+ X_{(m+1)}).
    $$
