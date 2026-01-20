# Iris Flower Species Classification 🌀

## Project Overview
This project demonstrates a complete **multiclass classification pipeline** using the famous **Iris dataset**. The goal is to predict one of three Iris flower species (*setosa*, *versicolor*, *virginica*) based on four features: sepal length, sepal width, petal length, and petal width.

Two models are implemented and compared:
- **Logistic Regression** (One-vs-Rest)
- **Random Forest Classifier**
- **Support Vector Classifier**

The project includes data loading from CSV, preprocessing, model training, evaluation, and comprehensive visualizations.

## Dataset
- Source: UCI Machine Learning Repository (downloaded as `iris.csv`)
- 150 samples, 3 classes (balanced)
- Features: `sepal_length`, `sepal_width`, `petal_length`, `petal_width`
- Target: `species` (cleaned to remove "Iris-" prefix)


## Requirements

pandas
scikit-learn
matplotlib
seaborn
numpy