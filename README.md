# Autoencoder for Image Denoising

This project demonstrates an Autoencoder implemented in TensorFlow/Keras to remove noise from images. The model uses the MNIST dataset, with added noise for training and testing purposes.

## Table of Contents
- [Installation](#installation)
- [Dependencies](#dependencies)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Process](#training-process)
- [Evaluation and Visualization](#evaluation-and-visualization)
- [Acknowledgments](#acknowledgments)

---

## Installation

1. Clone the repository:
    bash
    git clone https://github.com/Adnan1902/Autoencoder_For_Noised_Images.git
    cd autoencoder-image-denoising
    

2. Set up a virtual environment (optional but recommended):
    bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    

3. Install the dependencies:
    bash
    pip install -r requirements.txt
    

---

## Dependencies

Here are the dependencies required for this project:

- *Python* >= 3.8
- *TensorFlow* >= 2.10
- *Matplotlib* >= 3.3

The required dependencies are listed in the requirements.txt file:
txt
tensorflow>=2.10
matplotlib>=3.3


---

## Dataset

This project uses the MNIST dataset of handwritten digits. The data is loaded, normalized, and reshaped to fit the input dimensions of the autoencoder. Noise is added to both the training and test images to simulate real-world scenarios.

---

## Model Architecture

The Autoencoder architecture consists of:

1. *Encoder:*
    - Convolutional layers with ReLU activation and max pooling to reduce spatial dimensions.

2. *Decoder:*
    - Convolutional layers with ReLU activation and upsampling to reconstruct the input image dimensions.
    - A final convolutional layer with sigmoid activation for pixel intensity values in the range [0, 1].

---

## Training Process

1. *Data Preprocessing:*
    - Normalize the pixel values to [0, 1].
    - Add random noise to the images.
    - Clip pixel values to ensure they remain within the [0, 1] range.

2. *Hyperparameters:*
    - Batch size: 128
    - Epochs: 10
    - Noise factor: 0.5

3. *Training:*
    - The model is trained using binary cross-entropy loss and the Adam optimizer.

---

## Evaluation and Visualization

After training, the autoencoder is evaluated on the noisy test images. The reconstructed images are visualized alongside the noisy inputs for comparison.
