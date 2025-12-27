# Neural Network from Scratch: MNIST Digit Classifier

**A clean NumPy implementation of a two-layer neural network for MNIST digit classification, built from scratch without frameworks.**

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.21+-green.svg)](https://numpy.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Overview

This project demonstrates the fundamental building blocks of neural networks by implementing a two-layer digit classifier from scratch using only NumPy. It showcases forward and backward propagation, activation functions (ReLU and softmax), and gradient descent optimization—all without relying on deep learning frameworks like TensorFlow or PyTorch.

The implementation achieves approximately **90% accuracy** on the MNIST handwritten digit dataset.

## Problem & Approach

**Problem:** Classify handwritten digits (0-9) from the MNIST dataset using a custom neural network implementation.

**Approach:**
- Implements a two-layer neural network (one hidden layer with 64 neurons)
- Uses vectorized NumPy operations for computational efficiency
- Forward propagation with ReLU activation (hidden layer) and softmax (output layer)
- Backward propagation for gradient computation
- Cross-entropy loss function
- Gradient descent optimization for training

## Tech Stack

- **Python 3.x** - Programming language
- **NumPy** - Numerical computations and vectorized operations
- **scikit-learn** - MNIST dataset loading and preprocessing
- **Jupyter Notebook** - Interactive development and visualization

## Repository Structure

```
neural-network-practice-notebook/
├── mnist_classifier.ipynb    # Main implementation notebook
├── requirements.txt           # Python dependencies
├── README.md                  # This file
├── .gitignore                 # Git ignore patterns
├── project_identity.md        # Project identity documentation
├── report.md                  # Development and refactoring log
├── suggestion.txt             # Change suggestions ledger
└── suggestions_done.txt       # Applied changes ledger
```

## Setup & Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Install Dependencies

```bash
# Install required packages
pip install -r requirements.txt
```

This installs:
- `numpy>=1.21.0` - Core numerical operations
- `scikit-learn` - Dataset loading (via fetch_openml)
- `matplotlib>=3.3.0` - Visualization (optional, for future extensions)
- `jupyter>=1.0.0` - Notebook environment

## How to Run

### Option 1: Jupyter Notebook (Recommended)

1. Launch Jupyter Notebook:
```bash
jupyter notebook mnist_classifier.ipynb
```

2. Run cells sequentially from top to bottom:
   - **Cell 1:** Loads and preprocesses MNIST data
   - **Cell 2:** Defines the `TwoLayerNN` class with all methods
   - **Cell 3:** Trains the model and evaluates accuracy

### Option 2: JupyterLab

```bash
jupyter lab mnist_classifier.ipynb
```

### Expected Runtime
- Data loading: ~10-30 seconds (first run, downloads MNIST)
- Training (100 epochs): ~30-60 seconds
- Total: ~1-2 minutes

## Data

### Input Data
- **Dataset:** MNIST (Modified National Institute of Standards and Technology)
- **Source:** Automatically downloaded via `scikit-learn`'s `fetch_openml('mnist_784')`
- **Size:** 70,000 grayscale images (60,000 train, 10,000 test)
- **Format:** 28×28 pixels, flattened to 784-dimensional vectors
- **Preprocessing:** 
  - Normalized to [0, 1] range
  - Labels one-hot encoded (10 classes)
  - 80/20 train-test split (56,000 train, 14,000 test)

### No Manual Data Setup Required
The notebook automatically downloads and preprocesses the MNIST dataset on first run. An internet connection is required for the initial download (~15 MB).

## Outputs

### Training Outputs
- **Loss values** printed every 10 epochs
- Final training loss after 100 epochs

### Evaluation Metrics
- **Test Accuracy:** ~90% on 14,000 test samples
- Displayed at the end of the notebook

### Sample Output
```
Epoch 1/100, Loss: 2.3022
Epoch 11/100, Loss: 2.1493
Epoch 21/100, Loss: 1.2251
...
Epoch 100/100, Loss: 0.3415
Test Accuracy: 90.41%
```

## Implementation Details

### Network Architecture
- **Input Layer:** 784 neurons (28×28 flattened image)
- **Hidden Layer:** 64 neurons with ReLU activation
- **Output Layer:** 10 neurons with softmax activation (digit classes 0-9)

### Training Configuration
- **Epochs:** 100
- **Learning Rate:** 0.5
- **Batch Size:** Full batch (56,000 samples)
- **Loss Function:** Cross-entropy
- **Optimizer:** Vanilla gradient descent

### Key Methods
- `forward(X)` - Forward propagation
- `backward(X, y)` - Backpropagation and gradient computation
- `train(X, y, epochs, learning_rate)` - Training loop
- `predict(X)` - Class prediction

## Reproducibility

### Deterministic Results
To ensure reproducible results, the implementation uses:
- Fixed random seed in `train_test_split` (`random_state=42`)
- Consistent weight initialization

### Version Information
Tested with:
- Python 3.11.2
- NumPy 1.21.0+
- scikit-learn 1.0.0+

## Troubleshooting

### Common Issues

**1. Import Errors**
```bash
# Solution: Install missing dependencies
pip install -r requirements.txt
```

**2. MNIST Download Fails**
```
Error: Failed to fetch MNIST dataset
# Solutions:
- Check internet connection
- Try: pip install --upgrade scikit-learn
- Manual download: Use sklearn.datasets.fetch_openml with retry
```

**3. Memory Issues**
```
MemoryError during training
# Solutions:
- Reduce batch size (modify code to use mini-batches)
- Use a machine with more RAM (requires >4GB)
```

**4. Slow Training**
```
Training takes too long
# Solutions:
- Reduce epochs (e.g., 50 instead of 100)
- Reduce hidden layer size (e.g., 32 instead of 64)
- Training time is normal for CPU-only computation
```

**5. Lower Accuracy (<85%)**
- Check that data normalization is applied (X / 255.0)
- Verify learning rate is 0.5
- Ensure all 100 epochs complete
- Random initialization variance can cause ±2% accuracy difference

## Key Features

✅ **From-Scratch Implementation:** No PyTorch/TensorFlow—pure NumPy  
✅ **Educational:** Clear code with comments explaining each step  
✅ **Vectorized:** Efficient batch operations  
✅ **Complete Pipeline:** Data loading, training, evaluation  
✅ **Reproducible:** Fixed random seeds and documented setup  

## Future Enhancements (Not Implemented)

Potential improvements for learning:
- Mini-batch gradient descent
- Learning rate scheduling
- Additional hidden layers (deep networks)
- Different activation functions (e.g., Leaky ReLU, tanh)
- Regularization (L2, dropout)
- Visualization of learned weights and predictions
- Confusion matrix and per-class accuracy

## License

This project is available under the MIT License. See LICENSE file for details.

## Acknowledgments

- MNIST dataset: Yann LeCun, Corinna Cortes, and Christopher J.C. Burges
- Inspiration: Classic neural network educational implementations
