![](UTA-DataScience-Logo.png)


# Binary Classification with a Tabular Kidney Stone Prediction Dataset

This repository is my work comparing the results of LinearRegression, DecisionTreeRegressor, and RandomForestRegressor models on predicting the likehood of a patient being afflicted with kidney stones based on 6 features of a urinalysis.
https://www.kaggle.com/datasets/vuppalaadithyasairam/kidney-stone-prediction-based-on-urine-analysis

## Overview


  * **What is the challenge?**  The goal of this Kaggle Challenge is ultimately to predict the probability that a patient is afflicted with kidney stones based on the results of a urinalysis test using 6 different metrics.
  * **The Approach** The approach in this repository formulates the problem as a classification task, using the sklearn models LinearRegression, DecisionTreeRegressor, and RandomForestRegressor. The 3 different models were compared and found that RandomForestRegressor was the best performer.
  * **Summary of the performance achieved** The 3 models performed as follows using R2 as the metric:: LinearRegression: 0.28; DecisionTreeRegressor: 0.26; RandomForestRegressor: 0.30.

## Summary of Workdone

Include only the sections that are relevant an appropriate.

### Data

* Data:
  * Type: For example
    * Input: medical images (1000x1000 pixel jpegs), CSV file: image filename -> diagnosis
    * Input: CSV file of features, output: signal/background flag in 1st column.
  * Size: How much data?
  * Instances (Train, Test, Validation Split): how many data points? Ex: 1000 patients for training, 200 for testing, none for validation

#### Preprocessing / Clean up

* Describe any manipulations you performed to the data.

#### Data Visualization

Show a few visualization of the data and say a few words about what you see.

### Problem Formulation

* Define:
  * Input / Output
  * Models
    * Describe the different models you tried and why.
  * Loss, Optimizer, other Hyperparameters.

### Training

* Describe the training:
  * How you trained: software and hardware.
  * How did training take.
  * Training curves (loss vs epoch for test/train).
  * How did you decide to stop training.
  * Any difficulties? How did you resolve them?

### Performance Comparison

* Clearly define the key performance metric(s).
* Show/compare results in one table.
* Show one (or few) visualization(s) of results, for example ROC curves.

### Conclusions

* State any conclusions you can infer from your work. Example: LSTM work better than GRU.

### Future Work

* What would be the next thing that you would try.
* What are some other studies that can be done starting from here.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

* Describe the directory structure, if any.
* List all relavent files and describe their role in the package.
* An example:
  * utils.py: various functions that are used in cleaning and visualizing data.
  * preprocess.ipynb: Takes input data in CSV and writes out data frame after cleanup.
  * visualization.ipynb: Creates various visualizations of the data.
  * models.py: Contains functions that build the various models.
  * training-model-1.ipynb: Trains the first model and saves model during training.
  * training-model-2.ipynb: Trains the second model and saves model during training.
  * training-model-3.ipynb: Trains the third model and saves model during training.
  * performance.ipynb: loads multiple trained models and compares results.
  * inference.ipynb: loads a trained model and applies it to test data to create kaggle submission.

* Note that all of these notebooks should contain enough text for someone to understand what is happening.

### Software Setup
* List all of the required packages.
* If not standard, provide or point to instruction for installing the packages.
* Describe how to install your package.

### Data

* Point to where they can download the data.
* Lead them through preprocessing steps, if necessary.

### Training

* Describe how to train the model

#### Performance Evaluation

* Describe how to run the performance evaluation.


## Citations

* Provide any references.


### The Problem:
This challenge was a binary classification of patients as either having, or not having kidney stones based on the 6 features of a urinalysis. This data was actually generated from a deep learning model trained on the "Kidney Stone Prediction based on Urine Analysis" dataset.
### The Discussion:
The data for this challence came in 2 files: a traing file and a testing file meant as the test set to be scored. The training file is only 414 different simulated patients over 6 different features of a urinalysis including:
- The specific gravity (gravity), 
- Ph (ph), 
- Osmolarity (osmo), 
- Conductivity (cond), 
- Concentration of urea (urea), and 
- The concentration of calcium in urine (calc). 

The goal of the submission was to predict the likelihood of each patient is afflicted with kidney stones. 
### The Process
I started by segregating this set into a set with kidney stones(target = 1), and a set without kidney stones (target = 0). Using this differentiation, some visualization showed a slight correlation betweensome of the features, but nothing very promenent. The original dataframe was then split into what would be used to train the models, and what would be used to test the models (~10% reserved for testing because of the relatively small sample size). Three algorithms were chosen to compare: LinearRegression, DecisionTreeRegressor, and RandomForestRegressor. Comparing the performance of all three models against each other, RandomForestRegressor turned out to perform the best.
