# Project Identity

## Professional Identity

**Display Title:** Neural Network from Scratch: MNIST Digit Classifier

**Repo Slug:** neural-network-mnist-numpy

**Tagline:** A clean NumPy implementation of a two-layer neural network for MNIST digit classification, built from scratch without frameworks.

**GitHub Description:** Educational implementation of a two-layer neural network from scratch using NumPy. Demonstrates forward/backward propagation, ReLU/softmax activations, and gradient descent on the MNIST dataset, achieving ~90% accuracy.

**Primary Stack:** Python, NumPy, Jupyter Notebook

**Topics/Keywords:**
- machine-learning
- neural-network
- mnist
- numpy
- deep-learning
- classification
- from-scratch
- backpropagation
- gradient-descent
- jupyter-notebook

## Problem & Approach

**Problem Solved:** 
Demonstrates the fundamental building blocks of neural networks by implementing a digit classifier from scratch without using deep learning frameworks like TensorFlow or PyTorch.

**Approach:**
- Custom implementation of a two-layer (one hidden layer) neural network
- Uses vectorized NumPy operations for efficiency
- Implements forward propagation with ReLU and softmax activations
- Implements backward propagation for gradient computation
- Uses cross-entropy loss and gradient descent for training
- Trains on the MNIST dataset of handwritten digits

## Inputs & Outputs

**Inputs:**
- MNIST dataset (70,000 grayscale images of handwritten digits, 28x28 pixels)
- Loaded automatically via scikit-learn's fetch_openml
- Images are flattened to 784-dimensional vectors and normalized to [0, 1]

**Outputs:**
- Training progress (loss per epoch)
- Trained neural network model
- Test accuracy metrics (~90% on MNIST test set)
- Can predict digit classes for new images

