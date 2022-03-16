# DS Lab Evaluation
# Kaggle Challenge: IPL 2020 Player Performance 
#[Kaggle Challenge ](https://www.kaggle.com/c/ipl-2020-player-performance/overview)

## Shruty_101917187_3CSE8 

Documentation for IPL 2020 Player Performance. This is a Regression Problem. On whole I have used different models , trained them by using given IPL2008-19 training dataset and then on basis of that predicted the player performance index of each player who participated in 2020 IPL. [(Notebook Link)](https://www.kaggle.com/shrutykhullar/ds-ipl-prediction-shruty) [(Github Link)](https://github.com/Shruty-Khullar/DS_Evaluation-16-03-2022-/blob/main/Shruty_101917187_CSE8(DS_LabEval1).ipynb)
## STEPS FOLLOWED:
 1. Pre-processing 


	 a. [Columns Splitting](#columns-splitting)

	 b. [Joining Columns](#joining-columns)
   
    c. [Removing Null Values](#removing-null-values)

	 d. [Normalising columns](#normalising-columns)

 2. [Regression](#regression)



  	 a. Built-in LinearRegression
   
     b. Built-in SVR  
   
     c. Built-in Decision Tree Regressor 
     
     d. Built-in Random Forest Regressor 
     
     e. Built-in Ada Boost Regressor 
     
     f. Built-in Gradient Boosting Regressor
     

 3. [Validation Accuracy](#validation-accuracy)

 4. [Score](#Score)

---
### *Columns Spliting*
The dataset had id of form (match_id)\_(playername), which had to be splitted into seperate columns, so as to perform join operation with table data of IPL 2008-2019.


---
### *Joining of Columns*
The Joining operation was performed between training.csv and IPL2008-19.csv on match_id, because the data of player and match were in different tables.

---
### *Removing Null Values*
Checked for null values in columns. For dealing with null values I used dropna() method.

---
### *Normalising columns*
Used LabelEncoder for converting 'team1' and 'team2' column values into numerical values for futher use. 

---
### *Regression*

Used various Regression Models to get the best possible accuracy:

   ### *1. Linear-Regression*
   Trained Linear Regression model and obtained the RMSE: 31.634
   
   ### *2. SVR*
   One of the Non-linear regression model.SVR works on the principle of SVM . Given data points, it tries to find the curve. But since it is a regression algorithm instead of using the curve as a decision boundary it uses the curve to find the match between the vector and position of the curve.
   Trained the model and obtained the RMSE of 32.153
   
   ### *3. Decision Tree Regressor*
   Decision Tree is a decision-making tool that uses a flowchart-like tree structure or is a model of decisions and all of their possible results, including outcomes, input costs, and utility.
   Decision-tree algorithm falls under the category of supervised learning algorithms. It works for both continuous as well as categorical output variables.
   By using DecisionTreeRegressor the model gave RMSE of 31.812.
   
   
   ### *4. Random Forest Regressor*
   A Random Forest is an ensemble technique capable of performing both regression and classification tasks with the use of multiple decision trees and a technique called Bootstrap and Aggregation, commonly known as bagging.
   Here by using in-built RandomForestRegressor we get RMSE:31.803.
   
   ### *5. Ada Boost Regressor*
   The AdaBoost algorithm involves using very short (one-level) decision trees as weak learners that are added sequentially to the ensemble. Each subsequent model attempts to correct the predictions made by the model before it in the sequence. This is achieved by weighing the training dataset to put more focus on training examples on which prior models made prediction errors.
   Got RMSE of 33.054
   
   ### *6. Gradient Boosting Regressor*
   Gradient boosting is a machine learning technique used in regression and classification tasks, among others. It gives a prediction model in the form of an ensemble of weak prediction models, which are typically decision trees.
   This model gave RMSE 31.695
   
   Therefore, it is observed that LinearRegression Predicted the best possible result in this case.
---
### *Validation Accuracy*

| LinearRegression | SVR                  | DecisionTreeRegressor | RandomForestRegressor | Ada Boost Regressor | GradientBoostingRegressor |
|------------------|----------------------|-----------------------|-----------------------|---------------------|---------------------------|
| 31.634           | 32.153               | 31.812                | 31.803                | 33.054              | 31.695                    |

---

### *Score*
Got a score of 29.35.

---

### Rank is not available.
---

Code: [Notebook Link](https://www.kaggle.com/shrutykhullar/ds-ipl-prediction-shruty/edit)
