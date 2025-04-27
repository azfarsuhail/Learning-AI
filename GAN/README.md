# MNIST GAN - PyTorch Implementation

This project implements a simple Generative Adversarial Network (GAN) trained on the MNIST dataset of handwritten digits using PyTorch.

## Overview

The GAN consists of:
- **Generator**: Takes random noise as input and generates fake MNIST-style images.
- **Discriminator**: Takes images (real or fake) and outputs a probability of the image being real.

The two networks are trained simultaneously: the generator tries to fool the discriminator, and the discriminator tries to correctly classify real vs. fake images.

## Project Structure

- **Imports and Setup**: Install and import necessary libraries (PyTorch, torchvision, matplotlib).
- **Device Setup**: Automatically uses GPU if available.
- **Hyperparameters**: Latent size, hidden layer size, batch size, number of epochs, learning rate.
- **Data Preparation**: Load and normalize MNIST dataset.
- **Model Definitions**:
  - `Generator`: Fully connected network using ReLU activations and Tanh output.
  - `Discriminator`: Fully connected network using LeakyReLU activations and Sigmoid output.
- **Loss and Optimizers**: Binary Cross-Entropy loss and Adam optimizer.
- **Training Loop**: Alternately update the discriminator and generator.
- **Visualization**: Generated images are saved periodically to monitor progress.

## Requirements

- Python 3.7+
- PyTorch
- torchvision
- matplotlib

Install dependencies (if needed):

```bash
pip install torch torchvision matplotlib
```

## How to Run

1. Clone the repository or download the notebook.
2. Install the required Python packages.
3. Run the notebook step-by-step.
4. Generated images will be displayed/saved during training.

## Results

- You can expect generated MNIST digits after a few training epochs.
- Losses for the generator and discriminator are plotted to visualize training stability.