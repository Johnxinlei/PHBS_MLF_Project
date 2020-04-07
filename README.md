# Prediction of Bank Term Deposit Subscription

|     Name    | Student ID |
|-------------| ---------- | 
|[Chang Xinlei](https://github.com/Johnxinlei)| 1801212779 | 
|[Wang  Lu](https://github.com/wltll)| 1801212803 |
|[Huang Zongmin](https://github.com/dylanhzm)| 1801212785 |
|[Wang Lei](https://github.com/wlfengwuhen)| 1801212802 |
|[Sun Xiuwen](https://github.com/Sunlalaa)| 1801212801 |

## Classification Goal
The classification goal is to predict if the client will subscribe a term deposit (variable y).

## Sources
   Created by: Paulo Cortez (Univ. Minho) and Sérgio Moro (ISCTE-IUL) @ 2012,  https://archive.ics.uci.edu/ml/datasets/Bank+Marketing.
   


## Data description:

* The data is related with direct marketing campaigns of a Portuguese banking institution. 
     The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, 
     in order to access if the product (bank term deposit) would be (or not) subscribed. 
* There are four datasets: 
  1) bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010)
  2) bank-additional.csv with 10% of the examples (4119), randomly selected from i, and 20 inputs.
  3) bank-full.csv with all examples and 17 inputs, ordered by date (older version of this dataset with less inputs).
  4) bank.csv with 10% of the examples and 17 inputs, randomly selected from iii (older version of this dataset with less inputs).
* The classification goal is to predict if the client will subscribe a term deposit (variable y).
![](./data.png)

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
  

