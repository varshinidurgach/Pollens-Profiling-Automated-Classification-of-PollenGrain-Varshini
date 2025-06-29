# Pollen-s-Profiling-Automated-Classification-of-Pollen-Grains
Pollen’s Profiling is an AI-based system that classifies pollen grains from microscope images using a multi-scale CNN and SRGAN deblurring. It automates expert analysis, achieving up to 97.7% accuracy, and is useful in allergy monitoring, environmental studies, and botanical research.
# CNN Model to Classify Pollen Grains based on user input


## Dataset:
The dataset used for this project is Pollen Grain Image Classification Dataset from Kaggle. The classification of pollen species and types is an important task in many areas like forensic palynology, archaeological palynology and melissopalynology. This is the first annotated image dataset for the Brazilian Savannah pollen types that can be used to train and test computer vision based automatic pollen classifiers. 

The dataset has a total of 805 pollen grain images (.jpg files) containing 23 classes of pollen grains. The entire file size of the dataset is 32.85 MB with images of around 300x300 resolution. It has a usability of 8.8 and gives a good accuracy with CNN’s.

[kaggle data set link](https://www.kaggle.com/andrewmvd/pollen-grain-image-classification)

![image](https://user-images.githubusercontent.com/79707690/111902840-5659fc80-8a65-11eb-96ad-3efa75d7bd7d.png)

(Images of the different pollen grain classes in this dataset)

**The original article for the dataset:**
Feature Extraction and Machine Learning for the Classification of Brazilian Savannah Pollen Grains
Gonçalves AB, Souza JS, Silva GGd, Cereda MP, Pott A, et al. (2016) Feature Extraction and Machine Learning for the Classification of Brazilian Savannah Pollen Grains. PLOS ONE 11(6): e0157044.
https://doi.org/10.1371/journal.pone.0157044

## The model:
This is a deep learning model which solves a classification problem with respect to the above dataset. Steps involved in making the model: Data Exploration, Pre-processing, Data Augmentation,  Training (with Early Stopping), Predication
**Modules used : tensorflow, matplotlib, numpy , Pillow, scikit-learn, cv2, collections, os and random.**


## Model architecture:

Pretrained InceptionV3 + -->Dense layer/hidden layer (500)--> Dense layer/hidden layer (150)--> Output layer 
[Link to the training colab notebook]( https://colab.research.google.com/drive/1AsJm0SrCK4ciDfRnT3dZnLyawY_qcx7B)
The python file contains the code to run the trained model(iofinal.py).

# Note: 
To run the Python program on your computer, make sure to:

Download the trained model and dataset using the links provided in the links_to_model&dataset.md file.

Install all the required Python modules listed below.

Update the file paths for the model and dataset in the Python code as per the instructions in the links_to_model&dataset.md file.


### Exception:
There is an exception for the pollen grain pairs qualea-faramea,myrcia-arecaceae and matayba-eucalipto. The model predicts the first pollen grain type for both the types in the pair. Eg: for the first pair qualea-faramea, when the input is qualea the model predicts qualea but when the input is faramea the model still predicts it as qualea.
