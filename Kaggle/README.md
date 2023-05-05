# Binary Classification with a Tabular Kidney Stone Prediction Dataset
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
