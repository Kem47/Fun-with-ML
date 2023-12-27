# Neural Network at Different Levels

This project involves training the same neural network architecture using various methodologies. These methodologies are categorized based on the level of complexity required and the level of abstraction provided by the frameworks.

1. Tensorflow/Keras

    Keras offers a straightforward implementation of machine learning, placing it at level 1. The process involves building the architecture and running two steps: `model.compile()` and `model.fit()`. This simplicity allows for easy model training.

2. Pytorch out of the box

    Pytorch requires a more hands-on approach compared to Keras as it necessitates manual construction of the training loop. It's important to remember to use `.zero_grad()` and to run `loss.backward()`. The neural network architecture can be constructed from Pytorch's pre-built layers.

3. Pytorch with Autograd

    This level represents a more advanced usage of Pytorch. In many cases, there is a need for manual control or custom adjustments to the established methodologies. Pytorch's autograd feature is extremely beneficial in these scenarios.

4. Numpy

    This traditional approach to model construction predates ML frameworks. It involves manual processes, including backpropagation, and requires a thorough understanding of differentiation.

In each methodology, the same dataset - MNIST - is used, achieving consistent performance in terms of loss and accuracy.

This project demonstrates how the same model can be created using each methodology.

The ultimate goal of this project is to deconstruct the abstractions of ML frameworks and highlight the mathematical steps involved in training neural networks.

## Notes

- Default weight initialisations in pre-built layers are not the same in Keras and Pytorch. Therefore, manual weight initialisation of Glorot/Xavier Normal is performed. This is known to be a good choice of initialisation for tanh and sigmoid activations (which are used in this project).
- The architecture, learning rate, and other hyperparameters are kept simple, as the focus of this project is not on hyperparameter optimization.
- The MNIST data is obtained in the natural way for each framework and methodology.