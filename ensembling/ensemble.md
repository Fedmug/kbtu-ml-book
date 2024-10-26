# Ensembling

**Ensembling** in machine learning refers to the technique of combining multiple models to improve overall performance, accuracy, and robustness compared to using a single model. The idea is that individual models may make different errors, and by aggregating their predictions, the overall prediction can become more accurate.

## Bagging (Bootstrap Aggregating)

```{figure} https://payload-cms.code-b.dev/media/Bagging.png
:align: center
```

Multiple instances of the same model are trained on different subsets of the training data (usually created by random sampling with replacement).

## Boosting

```{figure} https://miro.medium.com/v2/resize:fit:1050/1*4XuD6oRrgVqtaSwH-cu6SA.png
:align: center
```

Models are trained sequentially, where each new model tries to correct the errors of the previous ones. This leads to an improvement in performance as weaker models are gradually refined.

## Stacking

```{figure} https://miro.medium.com/v2/resize:fit:1050/1*DM1DhgvG3UCEZTF-Ev5Q-A.png
:align: center
```

In stacking, multiple models are trained, and then their predictions are used as input to another model (often called a "meta-model") which makes the final prediction.

## Voting

```{figure} https://www.researchgate.net/publication/338409197/figure/fig3/AS:844344101711875@1578318729741/Ensemble-Learning-or-Voting-Classifier-Architecture.png
:align: center
```

Simple ensembling method where multiple models make predictions, and the final prediction is made based on majority voting (for classification tasks) or averaging (for regression tasks).
