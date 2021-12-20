# descartes-underwriting-technical-test-mounier

The aim of this project is to implement a supervised machine learning algorithm in order to make a prediction on the dataset Auto Insurance based on the Kaggle competition:
<a> https://www.kaggle.com/c/auto-insurance-fall-2017</a>. The dataset contains insurance claim statics on the customers, and was downloaded from 
<a>https://github.com/descartes-underwriting/data-scientist-technical-test</a> and is made of two csv files :
- train_auto.csv : the dataset to train our machine learning algorithm
- test_auto.csv : the dataset on which we want to make a prediction

The target is `TARGET_FLAG`. Files `SHELL_AUTO` and `MEAN_AUTO` are ignored for this project.

This work is organised in 5 parts :
 - **II) Importing datasets** : we make the required imports and quickly analyse train and test sizes and target properties.
 - **III) Preprocessing** : we deal with some preprocessing issues such as fill missing values, encoding all numerical features as numbers, and harmonize notations of categorical features.
 - **IV) Exploratory data analysis** : we look into the distributions of feature values to discover patterns and get insights on each feature's predictive power. We also look at feature correlation.
 - **V) Model training** : first, we train a model on the whole dataset. As this gives unsatisfactory results, we downsample the dataset to get balanced target classes. We train three types of algorithms : Logistic Regression, Random Forest, Support Vector Machine (SVM). We use cross validation to compare their performances. We select the best model looking at accuracy and precision metrics.
 - **VI) Prediction on the test set** : we make the preprocessing transformations and the test set and predict target with selected model. The result is saved in a csv file named `test_predictions`.
