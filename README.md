# Find-Scaler-Model
## Goal
* Compare the performance(accuracy) of the following classification models against the same dataset.
* Used classification
  - Decision tree (using entropy)
  - Decision tree (using Gini index)
  - Logistic regression
  - Support vector machine
 
## find_Scaler_Model
* Parameters:
    - X: array-like of shape
      - Training Vector
    - y: array-like of shape
      - Target relative to X for classfication
      
* Returns:
    - result_list: list
      - Returns a list that contains result of various combination of scalers, models,and model hyper parameters.
      
* Main function contains 5 sub functions: 
  - do_scaling, find_DecisionTree_gini, find_DecisionTree_entropy, find_SVC, find_LogisticRegression

* Brief description about sub functions:
  - Our main function first calls do_scaling function. do_scaling function returns a dictonary that contains scaler as a key and scaled dataframe as a value. Our team also added "None" key to the dictonary to test with non-scaled data. Then our main function calls find_DecisionTree_gini, find_DecisionTree_entropy, find_SVC, find_LogisticRegression. Each function returns a list that contains score, parameter, model of the result of each GridSearchCv. Using that results, our function can sort the result and returns the sorted result. Then we can use the best model to actually validate the model using test dataset.

* code for find_Scaler_Model sub functions:
  - do_scaling function
  - find_DecisionTree_gini function
  - find_DecisionTree_entropy function
  - find_SVC function
  - find_LogisticRegression funciton
 
## Requirements
* Mount google drive
* Libraries
    - StandardScaler
    - RobustScaler
    - MinMaxScaler
    - MaxAbsScaler
    - DecisionTreeClassifier
    - LogisticRegression
    - SVC
    - GridSearchCV
    - train_test_split
    - pandas
    - numpy
* Dataset
  - breast-cancer-wisconsin(url : https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/)
  - columns
    - Simple code number
    - Clump Thickness
    - Uniformity of Cell Size
    - Uniformity of Cell Shape
    - Marginal Adhesion
    - Single Epithelial Cell Size
    - Bare Nuclei
    - Bland Chromatin
    - Normal Nucleoli
    - Mitoses
    - Class
