# Neural Network from Scratch: MNIST Digit Classifier

**A clean NumPy implementation of a two-layer neural network for MNIST digit classification, built from scratch without frameworks.**

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
neural-network-mnist-numpy/
├── mnist_classifier.ipynb    # Main implementation notebook
├── requirements.txt           # Python dependencies
├── README.md                  # This file
├── .gitignore                 # Git ignore patterns
└── LICENSE                    # MIT License
```

## Setup & Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Install Dependencies

```bash
pip install -r requirements.txt
```

## How to Run

1. Launch Jupyter Notebook:
```bash
jupyter notebook mnist_classifier.ipynb
```

2. Run cells sequentially from top to bottom

Expected runtime: ~1-2 minutes (including MNIST download on first run)

## Data

- **Dataset:** MNIST (Modified National Institute of Standards and Technology)
- **Source:** Automatically downloaded via `scikit-learn`'s `fetch_openml`
- **Size:** 70,000 grayscale images (60,000 train, 10,000 test)
- **Format:** 28×28 pixels, flattened to 784-dimensional vectors
- **Preprocessing:** Normalized to [0, 1] range, labels one-hot encoded

## Outputs

### Training Outputs
- Loss values printed every 10 epochs
- Final training loss after 100 epochs

### Evaluation Metrics
- Test Accuracy: ~90% on 14,000 test samples

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

## Reproducibility

To ensure reproducible results, the implementation uses:
- Fixed random seed in `train_test_split` (`random_state=42`)
- Consistent weight initialization

## Troubleshooting

**Import Errors:**
```bash
pip install -r requirements.txt
```

**MNIST Download Fails:**
- Check internet connection
- Try: `pip install --upgrade scikit-learn`

**Memory Issues:**
- Requires >4GB RAM for full batch training
- Consider mini-batch implementation if needed

## License

This project is available under the MIT License. See LICENSE file for details.

## Acknowledgments

- MNIST dataset: Yann LeCun, Corinna Cortes, and Christopher J.C. Burges
