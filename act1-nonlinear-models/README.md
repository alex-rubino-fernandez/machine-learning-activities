# Activity 1: Nonlinear Models

## Objective

Understand how linear classification models can address nonlinear classification problems using kernel methods.

## Dataset Description

The synthetic dataset has the following characteristics:
- Two interleaving half-moon shapes (classes 0 and 1)
- A third class with Gaussian distribution (class 2)
- Overlap between all classes

## Exercises

The activity is developed in a Jupyter notebook and consists of the following exercises:

1. **Dataset generation and visualization** - Create a synthetic dataset with the described characteristics and visualize it.
2. **SVM with linear kernel** - Implement SVM with linear kernel, train the model, and perform hyperparameter tuning (C) using GridSearchCV.
3. **SVM with nonlinear kernels** - Repeat the training using nonlinear kernels (RBF, polynomial) with hyperparameter tuning (C, gamma, degree).
4. **Visualization and comparison** - Display decision boundaries for each model and compare performance using metrics (accuracy, classification report, confusion matrix).
5. **Discussion** - Analyze and compare the results obtained with and without the use of kernels.

## Files

- `gcd_aa2_act1_alex_rubino.ipynb` - Main Jupyter notebook (in Spanish)

## Language

The notebook is written in Spanish, as required by the course activity.

## Usage

This code is for educational purposes as part of the Machine Learning 2 course.
Feel free to explore and learn from it.
