EuroSAT Land Cover Classification using CNN with Residual Connections and Spatial Attention
Overview

This project implements a deep learning model for classifying satellite images from the EuroSAT dataset into 10 land-cover categories. A custom Convolutional Neural Network (CNN) with residual connections and a spatial attention mechanism is used to automatically learn important visual features from satellite imagery.

The model is trained and evaluated using TensorFlow/Keras in Google Colab and achieves approximately 95% test accuracy on the EuroSAT dataset.

Dataset

Dataset: EuroSAT RGB Dataset

The dataset contains satellite images belonging to the following classes:

AnnualCrop
Forest
HerbaceousVegetation
Highway
Industrial
Pasture
PermanentCrop
Residential
River
SeaLake

Images are automatically split into:

Training Set (70%)
Validation Set (20%)
Test Set (10%)
Features
Automated dataset download using Kaggle API
Data preprocessing and train/validation/test splitting
Image augmentation using ImageDataGenerator
Custom CNN architecture
Residual blocks for improved feature learning
Spatial attention mechanism for region-focused learning
Early stopping and learning rate scheduling
Classification report and confusion matrix evaluation
Grad-CAM visual explanations for model interpretability
Model Architecture

The model consists of:

Convolutional stem layer
Residual blocks
Spatial attention module
Global Average Pooling
Fully connected classification layer
Softmax output layer

Optimizer: Adam

Loss Function: Categorical Cross-Entropy

Evaluation Metric: Accuracy

Results
Metric	Value
Test Accuracy	95.19%
Test Loss	0.1354
Macro F1-Score	0.95
Weighted F1-Score	0.95
Per-Class Highlights
Forest: 99% F1-score
Residential: 99% F1-score
SeaLake: 99% F1-score
Industrial: 96% F1-score
Pasture: 95% F1-score
Explainable AI

Grad-CAM is used to visualize which regions of an image influence the model's predictions.

This helps verify that the model focuses on meaningful land-cover patterns rather than irrelevant image regions.

Technologies Used
Python
TensorFlow / Keras
NumPy
Matplotlib
OpenCV
Scikit-learn
Google Colab
Kaggle API
Project Structure
EuroSAT-LandCover-Classification/
│
├── EuroSAT_CNN_Attention.ipynb
├── training_history.json
├── README.md
└── model/
    └── eurosat_kaggle_best.keras
How to Run
Upload your kaggle.json file to Google Colab.
Run the notebook cells in order.
The dataset will be downloaded automatically.
The model will be trained and evaluated.
Grad-CAM visualizations and performance metrics will be generated.
Future Improvements
Experiment with transfer learning models such as MobileNetV2 or EfficientNet.
Use multispectral EuroSAT bands instead of RGB images.
Perform hyperparameter optimization.
Compare different attention mechanisms.
Deploy the model as a web application.
