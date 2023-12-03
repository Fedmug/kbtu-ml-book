# CNN

```{figure} https://miro.medium.com/v2/resize:fit:1400/0*IOvC3mgxzKBO502e.png
:align: center
```

One of the pioneering deep convolution neural networks (CNN) [AlexNet](https://proceedings.neurips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) won the [ImageNet Large Scale Visual Recognition Challenge](https://www.image-net.org/challenges/LSVRC/2012/index.php) (ILSVRC) in 2012. This event is now accepted as a key point of beginning of the deep learning era.

## CNN vs MLP

In CNN new kind of layers are introduced such as **convolution** and **pooling**. Why are they important for image processing?

An image in ImageNet collection usually has shape $224\times 224$, and it has three channels: red, green and blue. Hence, such image can be considered as a vector of size $224\times 224 \times 3 = 150528$.

````{admonition} Question
:class: important
Suppose that we are applying a linear layer to this vector, and the output has the same shape. How many parameters does such dense layer have?

```{admonition} Answer
:class: tip, dropdown
The matrix of weights will conatain

$$
224^2\times 224^2 \times 3^2 > 22 \text{ billion elements.}
$$

```
````

So, the number of parameters becomes too big. An MLP with so many parameters will train for a quite long time, and it could be easily overfitted. On the other hand, a convolution layer has much less parameters. For example, it the kernel size is $11$, number of input and output channels is $3$, then there are

$$
    11 \times 11 \times 3 \times 3 = 33^2 = 1089
$$

weights in the convolution layer.

## Advantages of convolutions

1. **Local Connectivity**. Convolutional layers have local connectivity, meaning each neuron is connected to a small local region of the input, enabling them to focus on local features and patterns.

2. **Parameter Sharing**. Convolutional layers use parameter sharing, where the same set of weights (filter) is applied to different parts of the input. This reduces the number of parameters, making the network more efficient and less prone to overfitting.

3. **Translation Invariance**. Convolutional layers inherently exhibit translation invariance, meaning they can recognize patterns regardless of their exact position in the input. This is particularly valuable for tasks like image recognition.

4. **Parameter Efficiency**. Convolutional layers are parameter-efficient compared to fully connected layers, especially when dealing with high-dimensional input data like images. This efficiency is crucial for training deep networks.

5. **Efficient GPU Implementation**. Convolutional operations can be highly parallelized, making them well-suited for efficient GPU implementation. This parallelization enhances the speed of both training and inference.
