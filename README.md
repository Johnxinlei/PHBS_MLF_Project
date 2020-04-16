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

* The data is related with direct marketing campaigns of a Portuguese banking institution. It contains 41188 observations along with 16 features about information of clients as shown below:
![](./data.png)

2.1: Drop the observations which contains missingvalue, then our observations count changes to 30488

2.2: Calculate the count and the subscribe percentage of each variable and plot for category variable

2.3: Plot the histogram of each variable for category variables for category variable

2.4: Calculate the correaltion of each variable

2.5: Balance the data (Becuase for the explained variable y, the counts of "yes" and "no" are 3859 and 26629 ,which means the data is very inbalanced)

2.6: Use "One-Hot Encoding" to divide one category variable with multiple value into several dummy variables

## 3.Model trainning 
3.1 Applying PCA to the balanced data 
![](./pca.png) 
![](./distribution.png)
3.2 Using first 2 PCA to train the logistic regresssion, SVM,KNN and decision tree.
![](./lr.png) 
![](./svm.png) 
![](./knn.png)
## 4.CV and evaluation
4.1 CV and learning curves

4.2 Evaluation Metrics

4.3 ROC 

## 5.Conclusion and possible improvements
5.1 Conclusion

5.2 Possible improvements

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
  


