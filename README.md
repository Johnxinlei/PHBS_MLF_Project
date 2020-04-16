# Predicting Bank Term Deposit Subscription

|     Name    | Student ID |
|-------------| ---------- | 
|[Chang Xinlei](https://github.com/Johnxinlei)| 1801212779 | 
|[Wang  Lu](https://github.com/wltll)| 1801212803 |
|[Huang Zongmin](https://github.com/dylanhzm)| 1801212785 |
|[Wang Lei](https://github.com/wlfengwuhen)| 1801212802 |
|[Sun Xiuwen](https://github.com/Sunlalaa)| 1801212801 |

## Introduction
Banking industry plays an important role in national economies. However, with the integration of global economy and innovation of financial instruments, traditional commercial banks are facing unprecedentedly fierce competition and high risk of losing customers. With the advent of the era of big data, the banks who can efficiently and effectively find, understand, and serve customers will take the lead in the fierce market competition. With the ability of analysis, prediction and insight of big data, we'd like to use machine learning method to predict results of bank marketing for certain types of customers and try to achieve precision marketing in the future.

Since term deposit is one major stable and credible financing source of banks, here we use data related to the marketing activities of Portuguese banking institutions to predict customers’ term deposit subscription behaviors and understand customers’ features to improve the effectiveness and accuracy of bank marketing. This forecast can help make a preliminary plan for future work of banks, and it also provides a reference for whether certain type of customers will subscribe to term deposits.

## Data Sources
   Created by: Paulo Cortez (Univ. Minho) and Sérgio Moro (ISCTE-IUL) @ 2012,  https://archive.ics.uci.edu/ml/datasets/Bank+Marketing.
   


## Data description:

* The data is related with direct marketing campaigns of a Portuguese banking institution. It contains 4521 observations along with 16 features about information of clients as shown below:

![](./data.png)
step1

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
  


