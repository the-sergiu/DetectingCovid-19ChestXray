# Detecting Covid-19 with Chest X-rays

## Description
The purpose of this project pretty straight-froward: to accurately predict Covid-19 in potential pacients, based on X-ray scans. This is a classification problem, where the available output labels are: ***NORMAL*, *Viral Pneumonia* or *Covid-19***.

Note: This Notebook is an academic representation of potential COVID-19 prediction, and will most likely not be sufficient in predicting true COVID-19 cases. Even so, it represents a good initial depiction of the process X-ray images should undergo in order to eventually be trained on a CNN.

## Dataset
The dataset used for training this specific model is found on Kaggle, at the following link:
https://www.kaggle.com/tawsifurrahman/covid19-radiography-database

## Installation Instructions
- Download Dataset
- Create environment with Python 3.7
- Run:
```
conda install pytorch==1.5.1 torchvision==0.6.1 cudatoolkit=10.2 -c pytorch
pip install matplotlib
```
- Place Notebook outside Dataset
- Rename:
```
COVID-19 Radiography Dataset -> Dataset

*Inside the Dataset*

Viral Pneumonia -> viral
Normal -> normal
COVID-19 -> covid
```
- The beginning functions should then create test datasets. If they don't work, create the test test manually, for each class. Then create a separate folder with the exact name as the training folder. In each class folder, cut and paste 30 images from the test dataset. These will be the validation images.

## Results Obtained
My model obtained an accuracy of 96%, by the end of a single epoch. That accuracy was measured on a test set, which was composed of: 30 normal X-ray scans, 30 viral pneumonia X-ray scans, and 30 COVID-19 X-ray scans.

## Room for improvement
Due to the fact that this Notebook is purely academic, I found the accuracy of 96% to be satisfactory. Nontheless, here are some things I would add if I wanted to obtain better results:

* More epochs - I obtained 96% accuracy with a single epoch. I am pretty sure that training for 2 epochs would drive my accuracy near 100%, but might also introduce overfitting.
* Dropout Regularization.
* Larger Network (Although Resnet18 did the job just fine, on this "small" dataset of 3000 images).