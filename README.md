# Convolutional Autoencoder for Image Denoising
## AIM
To develop a convolutional autoencoder using PyTorch for removing noise from images.

## Problem Statement and Dataset
The objective is to train a model that can reconstruct clean images from noisy inputs.
The MNIST dataset is used, which consists of handwritten digit images (28×28 grayscale).
Artificial Gaussian noise is added to images to train the denoising model.

## Design Steps
### Step 1: Load Data
- Load MNIST dataset
- Convert images to tensor
- Use DataLoader for batching

### Step 2: Add Noise
- Add Gaussian noise using torch.randn_like()
- Clamp values between 0 and 1

### Step 3: Build Model
- Encoder: Conv layers + ReLU
- Decoder: ConvTranspose layers + Sigmoid

### Step 4: Initialize Model
- Loss: MSELoss
- Optimizer: Adam

### Step 5: Train Model
- Input: Noisy image
- Output: Clean image
- Update weights using backpropagation

### Step 6: Test & Visualize
- Test on new images
- Show Original, Noisy, and Denoised images

## RESULT
The convolutional autoencoder successfully learned to remove noise from MNIST images.
The denoised output images are significantly clearer than the noisy inputs and closely resemble the original images.
This demonstrates that the model effectively captures important image features and removes noise.
The convolutional autoencoder successfully learned to remove noise from MNIST images.
The denoised output images are significantly clearer than the noisy inputs and closely resemble the original images.
This demonstrates that the model effectively captures important image features and removes noise.
