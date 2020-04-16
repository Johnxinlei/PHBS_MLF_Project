# Predicting Bank Term Deposit Subscription

|     Name    | Student ID |
|-------------| ---------- | 
|[Chang Xinlei](https://github.com/Johnxinlei)| 1801212779 | 
|[Wang  Lu](https://github.com/wltll)| 1801212803 |
|[Huang Zongmin](https://github.com/dylanhzm)| 1801212785 |
|[Wang Lei](https://github.com/wlfengwuhen)| 1801212802 |
|[Sun Xiuwen](https://github.com/Sunlalaa)| 1801212801 |

## 1.Introduction
Banking industry plays an important role in national economies. However, with the integration of global economy and innovation of financial instruments, traditional commercial banks are facing unprecedentedly fierce competition and high risk of losing customers. With the advent of the era of big data, the banks who can efficiently and effectively find, understand, and serve customers will take the lead in the fierce market competition. With the ability of analysis, prediction and insight of big data, we'd like to use machine learning method to predict results of bank marketing for certain types of customers and try to achieve precision marketing in the future.

Since term deposit is one major stable and credible financing source of banks, here we use data related to the marketing activities of Portuguese banking institutions to predict customers’ term deposit subscription behaviors and understand customers’ features to improve the effectiveness and accuracy of bank marketing. This forecast can help make a preliminary plan for future work of banks, and it also provides a reference for whether certain type of customers will subscribe to term deposits.

   Data Sources
   Created by: Paulo Cortez (Univ. Minho) and Sérgio Moro (ISCTE-IUL) @ 2012,  https://archive.ics.uci.edu/ml/datasets/Bank+Marketing.
   
|   Features  |    Type    | Description |
|-------------| ---------- | ----------  |
|age| numeric |age| 
|job| categorical|type of job "married","divorced","single"; note: "divorced" means divorced or widowed |
|marital| categorical|marital status "married","divorced","single"; note: "divorced" means divorced or widowed |
|education| categorical| "unknown","secondary","primary","tertiary" |
|default| categorical|has credit in default?  binary: "yes","no"|
|housing| categorical|has housing loan? binary: "yes","no"|
|loan| categorical| has personal loan? binary: "yes","no" related with the last contact of the current campaign|
|contact| categorical| contact communication type "unknown","telephone","cellular" |
|day| numeric| last contact day of the month|
|month| numeric|last contact month of year |
|duration | numeric| last contact duration, in seconds|
|campaign| numeric| number of contacts performed during this campaign and for this client|
|pdays| numeric| number of days that passed by after the client was last contacted from a previous campaign |
|previous| numeric| number of contacts performed before this campaign and for this client|
|poutcome| categorical| outcome of the previous marketing campaign |
|emp.var.rate| numeric| employment variation rate - quarterly indicator|
|cons.price.idx| numeric| consumer price index - monthly indicator|
|cons.conf.idx| numeric| consumer price index - monthly indicator|
|euribor3m| numeric| euribor 3 month rate - daily indicator |
|nr.employed| numeric| number of employees - quarterly indicator|
|y| categorical| has the client subscribed a term deposit?binary: "yes","no"|


## 2.Data description and processing:

* The data is related with direct marketing campaigns of a Portuguese banking institution. It contains 41188 observations along with 21 features about information of clients as shown below:
![](./data.png)

2.1: Drop the observations which contains missing value, then our observations count changes to 30488

2.2: Calculate the coefficient of each variable

2.3: Balance the data (Becuase for the explained variable y, the counts of "yes" and "no" are 3859 and 26629 ,which means the data is very unbalanced)

2.4: Use "One-Hot Encoding" to divide one category variable with multiple value into several dummy variables

## 3.Model trainning 
3.1 Applying PCA to the balanced data after standardization

<img src="pca.png" width="400" height="250"/>
** After sliptting the original data into training set and test set, we apply standardization and PCA to the training set and transform the training set and test set. Then we can find that the explained variance ratio of the two largest conponents account is more than 90%, so we choose two components for our following work.

<img src="distribution.png" width="400" height="250"/>

3.2 Using first 2 PC to train the logistic regresssion, SVM,KNN and decision tree.

<img src="lr.png" width="400" height="250"/>
<img src="svm.png" width="400" height="250"/> 
<img src="knn.png" width="400" height="250"/>

## 4.CV and Model Evaluation
4.1 CV and learning curves

First, we optimize the hyperparameters of the model by grid research using 10-fold cross validation. 

Under LR method, the optimal value for C is 1, with which we can reach an accuracy of 0.7100.

Under Decision Tree method, the Gini index performs better for Classification error, and we limit the max depth to 10 to avoid overfitting, getting an optimal accuracy of 0.9046.

Under SVM, the optimal value for C is , for gamma is , with which we can get an accuracy of 


Then, to diagnose whether this model has a problem with overfitting or underfitting, we plot the learning curve of our model. As the figure shows, our model has small variance but relatively high bias, which may be our major challenge for model improvement. Also, we find that the accuracy is stable ahter the sample size reaches 10000, which suggests that a relative smaller sample size than current sample size (30488) will be enough for our model training and testing.

4.2 Evaluation Metrics

Next, we plot the confusion matrix of out model, from which we compute PRE as 73.6%, REC as 67.7% and F1 as 70.5%. Since we are aimed to find out the target clients who will subscribe term deposits, we care more about REC, which demonstrates the proportion of potential subscribers detected by the model. 67.7% of REC implies that among all the potential subscribers, our model can only detect 67.7% of them, which is acceptable but there is still much room for improvement.

4.3 ROC 

Finally, we plot the ROC curve of our model. The resulting ROC curve indicates that there is not much variance between the different folds, and the average ROC AUC is 0.77, which falls between a perfect score (1.0) and random guessing (0.5). This shows that our model performs quite well.

|   Model   |    Accuracy    | Description |
|-----------| -------------- | ----------  |
|age| numeric |age| 

## 5.Conclusion and possible improvements
5.1 Conclusion

We used LR, SVM and decision tree models to make predictions. The accuracy of the model prediction is as follows:

|     MODEL   | ACCURACY |
|-------------| ---------- | 
|LR|0.709|
|SVM|0.725|
|Decision tree|0.717|

Based on the above model, we use the Bagging algorithm to combine the above models, and the final prediction accuracy of the model is +++++.

5.2 Possible improvements

From the learning curve we can tell that our model can converge with a limited number of samples. And the fluctuation of model prediction accuracy is relatively small. However, the prediction accuracy is not good enough. We need to improve the model to increase accuracy.


## Attribute information:

   Input variables:
   * bank client data:
   
     `age (numeric)`
   
     `job` type of job (categorical: "admin.","unknown","unemployed","management","housemaid","entrepreneur","student",
                                       "blue-collar","self-employed","retired","technician","services") 
                                       
     `marital` marital status (categorical: "married","divorced","single"; note: "divorced" means divorced or widowed)
   
     `education` (categorical: "unknown","secondary","primary","tertiary")
   
     `default` has credit in default? (binary: "yes","no")
   
     `housing` has housing loan? (binary: "yes","no")
   
     `loan` has personal loan? (binary: "yes","no") related with the last contact of the current campaign:
       
     `contact` contact communication type (categorical: "unknown","telephone","cellular") 
   
     `day` last contact day of the month (numeric)
  
     `month` last contact month of year (categorical: "jan", "feb", "mar", ..., "nov", "dec")
  
     `duration` last contact duration, in seconds (numeric)
     
  * other attributes:
       
     `campaign` number of contacts performed during this campaign and for this client (numeric, includes last contact)
  
     `pdays` number of days that passed by after the client was last contacted from a previous campaign (numeric, -1 means client was                not previously contacted)
  
     `previous` number of contacts performed before this campaign and for this client (numeric)
  
     `poutcome`: outcome of the previous marketing campaign (categorical: "unknown","other","failure","success")
 
  * social and economic context attributes: 
  
     `emp.var.rate` employment variation rate - quarterly indicator (numeric)
  
     `cons.price.idx` consumer price index - monthly indicator (numeric)
     
     `cons.conf.idx` consumer confidence index - monthly indicator (numeric)
     
     `euribor3m` euribor 3 month rate - daily indicator (numeric)
     
     `nr.employed` number of employees - quarterly indicator (numeric)

  * Output variable (desired target):  
  
     `y` has the client subscribed a term deposit? (binary: "yes","no")
  


