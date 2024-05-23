# Credit-Card-Default-Prediction


## **Abstract:** 
 
We are all aware what is Credit card. It is type of payment card in which charges are made against a line of credit instead of the account holder's cash deposits. When someone uses a credit card to make a purchase, that person's account accrues a balance that must be paid off each month. Credit card default happens when you have become severely delinquent on your credit card payments. Missing credit card payments once or twice does not count as a default. A payment default occurs when you fail to pay the Minimum Amount Due on the credit card for a few consecutive months.

The provided dataset contains information about Gender, Amount of given credit, Education, Age, Repayment Status, Amount of Bill Statement, Amount of previous payment and the target is Default payment next month. This project is aimed at predicting the case of customers default payments in Taiwan.


## **1.Problem Statement**
 
We have given a dataset with the information in which the independent variables are Gender, Amount of given credit, Education, Age, Repayment Status, Amount of Bill Statement, Amount of previous payment and the Dependent variable is Default payment next month. The goal of the project is to predict the credit card default beforehand and to identify the potential customer base that can be offered various credit instruments so as to invite minimum default.
 
 We have given the following information in our dataset: 

•**ID**: Id of each client

•	**LIMIT_BAL:** Amount of the given credit in NT dollar

•	**SEX: Gender** (1 = male, 2 = female)

•	**EDUCATION**: (1 = graduate school, 2 = university, 3 = high school, 0,4,5,6 = others)

•	**MARRIAGE:** Marital status (0 = others, 1 = married, 2 = single, 3 = others)

•	**AGE:** Age is in years

•	**PAY_0**: Repayment status in September, 2005

•	**PAY_2:** Repayment status in August, 2005

•	**PAY_3:** Repayment status in July, 2005

•	**PAY_4:** Repayment status in June, 2005

•	**PAY_5**: Repayment status in May, 2005

•	**PAY_6**: Repayment status in April, 2005

•	**BILL_AMT1:** Amount of bill statement in September, 2005

•	**BILL_AMT2:** Amount of bill statement in August, 2005

•	**BILL_AMT3:** Amount of bill statement in July, 2005

•	**BILL_AMT4:** Amount of bill statement in June, 2005

•	**BILL_AMT5:** Amount of bill statement in May, 2005

•**BILL_AMT6** : Amount of bill statement in April, 2005

•	**PAY_AMT1**: Amount of previous payment in September, 2005

•	**PAY_AMT2:** Amount of previous payment in August, 2005

•	**PAY_AMT3:** Amount of previous payment in July, 2005

•	**PAY_AMT4:** Amount of previous payment in June, 2005

•	**PAY_AMT5**: Amount of previous payment in May, 2005

•	**PAY_AMT6:** Amount of previous payment in April, 2005

•	**default.payment.next.month:** Default payment (1=yes, 0=no)

## **2. Introduction**
We have given a dataset with the information in which the independent variables are Gender, Amount of given credit, Education, Age, Repayment Status, Amount of Bill Statement, Amount of previous payment and the Dependent variable is Default payment next month.
Our dataset has 30000 rows and 25 columns. The goal of the project is to predict the credit card default beforehand which could us to get basic understanding of our dataset, finding outliers, finding correlation between the data, perform Data visualization, models implementation and finally getting conclusion. 

## **3. Steps Involved**

●**Data Summary**

After loading the dataset we performed this step to understand the data better in the dataset and creating various graphical representations to get some conclusion from it.
This step is an important method for getting a grasp on the meaning of the content of a large collection of data. It basically simplify data for better understanding of our dataset. 

•**Data Preprocessing**

First we check for missing values thankfully there are no null values in our dataset then we rename some column name for ease of understanding. 

•**Identify relationships in dataset** 

Correlation matrix measures the statistical relationship between two different variables. Correlation evaluates the direction as well as strength of a relationship between continuous variables. Correlation coefficient can range from -1 to +1, which signifies strong negative to strong positive relation between the variables


●**Encoding of categorical columns**

We used One Hot Encoding to produce binary integers of 0 and 1 to encode our categorical features because categorical features that are in string format cannot be understood by the machine and needs to be converted to numerical format.

●**Exploratory Data Analysis** 

After loading the dataset we performed this method by comparing our target variable that is default payment next month with other independent variables. This process helped us figuring out various aspects and relationships among the target and the independent variables. It gave us a better idea of which feature behaves in which manner compared to the target variable. With the help of Exploratory data analysis we analyzed the categorical as well as numerical features in the dataset.

•**Feature Selection**

There are 25 columns in this dataset and the target variable is default payment next month. We drop the column ‘ID’ and the target variable and save the rest 23 as predictor features These predictor variables include categorical variable such as sex,  age ,Education, Marital status along with numerical features such as payment status , Credit limit, bill amount ,etc

## **Models implemented**

**1.Logistic Regression** -
Logistic Regression is actually a classification algorithm that was given the name regression due to the fact that the mathematical formulation is very similar to linear regression.
The function used in Logistic Regression is sigmoid function or the logistic function given by:
		f(x)= 1/1+e ^(-x)


**2.Random Forest Classifier** -
Random Forest is a bagging type of Decision Tree Algorithm that creates a number of decision trees from a randomly selected subset of the training set, collects the labels from these subsets and then averages the final prediction depending on the most number of times a label has been predicted out of all.

## **Model performance**

Model can be evaluated by various metrics such as:
1.	**Confusion Matrix**- The confusion matrix is a table that summarizes how successful the classification models at predicting examples belonging to various classes. One axis of the confusion matrix is the label that the model predicted, and the other axis is the actual label.
2.	**Precision/Recall-**
Precision is the ratio of correct positive predictions to the overall number of positive predictions : TP/TP+FP
      **Recall** is the ratio of correct positive predictions to the overall number of positive 
      examples in the set: TP/FN+TP          
3.	**Accuracy**-  Accuracy is given by the number of correctly classified examples divided by the total number of classified examples. In terms of the confusion Matrix, it is given by: TP+TN/TP+TN+FP+FN
4.	**Area under ROC Curve(AUC**)- ROC curves use a combination of the true positive rate (the proportion of positive examples predicted correctly, defined exactly as recall) and false positive rate (the proportion of negative examples predicted incorrectly) to build up a summary picture of the classification performance.

## **Conclusion**
1.	Starting with loading the data so far we have done EDA , null values treatment, encoding of categorical columns, Outliers detection and removing and then model building.
2.	 Logistic Regression having Recall, F1-score equals 78%, 73% resp and Random forest Classifier having Recall, F1-score values equals 85%, 83%resp.
3.	The best accuracy is obtained for the Random forest than Logistic Regression.
4.	If the balance of recall and precision is the most important metric, then Random Forest is the ideal model. Since Random Forest has slightly lower recall but much higher precision than Logistic Regression, I would recommend Random Forest.

