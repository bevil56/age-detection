
# Age and Gender Prediction Using MLP, VGG16, and Custom CNN

This repository contains implementations of three different models for predicting age and gender from facial images: Multi-Layer Perceptron (MLP), VGG16, and Custom Convolutional Neural Network (Custom CNN). The models are trained and evaluated on the UTKFace dataset.

## Table of Contents
- [Dataset](#dataset)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Training the Models](#training-the-models)
- [Evaluation](#evaluation)
- [Results](#results)

## Dataset
The UTKFace dataset is used for training and evaluation. It contains over 20,000 images of faces with annotations for age and gender.

Download the dataset from Kaggle using the following link:
- [UTKFace Dataset](https://www.kaggle.com/jangedoo/utkface-new)

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/age-gender-prediction.git
   cd age-gender-prediction
   ```

2. Install the required packages:
   ```bash
   pip install numpy pandas matplotlib scikit-learn tensorflow keras opencv-python seaborn
   ```

## How to Run
### Setup and Data Preparation
1. Upload the `kaggle.json` file for Kaggle API authentication. This file can be obtained from your Kaggle account settings.
2. Download the UTKFace dataset:
   ```bash
   from google.colab import files

   uploaded = files.upload()

   !mkdir -p ~/.kaggle/ && mv kaggle.json ~/.kaggle/ && chmod 600 ~/.kaggle/kaggle.json
   !kaggle datasets download -d jangedoo/utkface-new
   !unzip utkface-new.zip
   ```

### Training the Models
1. **Multi-Layer Perceptron (MLP)**:
   ```python
   # MLP model training script
   python train_mlp.py
   ```

2. **VGG16**:
   ```python
   # VGG16 model training script
   python train_vgg16.py
   ```

3. **Custom CNN**:
   ```python
   # Custom CNN model training script
   python train_custom_cnn.py
   ```

### Evaluation
To evaluate the models, run the respective evaluation scripts:
```python
# Evaluate MLP model
python evaluate_mlp.py

# Evaluate VGG16 model
python evaluate_vgg16.py

# Evaluate Custom CNN model
python evaluate_custom_cnn.py
```

### Results
The results, including the training and validation loss curves, MAE curves, and sample predictions, will be saved in the `results/` directory. 

## Contributions
Feel free to contribute to this project by opening issues or submitting pull requests.
```
