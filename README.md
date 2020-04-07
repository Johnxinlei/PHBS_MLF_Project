# Prediction of Bank Term Deposit Subscription

|     Name    | Student ID |
|-------------| ---------- | 
|[Chang Xinlei](https://github.com/Johnxinlei)| 1801212779 | 
|[Wang  Lu](https://github.com/wltll)| 1801212803 |
|[Huang Zongmin](https://github.com/dylanhzm)| 1801212785 |
|[Wang Lei](https://github.com/wlfengwuhen)| 1801212802 |
|[Sun Xiuwen](https://github.com/Sunlalaa)| 1801212801 |

## Data sources:
   Created by: Paulo Cortez (Univ. Minho) and Sérgio Moro (ISCTE-IUL) @ 2012,  https://archive.ics.uci.edu/ml/datasets/Bank+Marketing.
   
## Data description:

* The data is related with direct marketing campaigns of a Portuguese banking institution. It contains 4521 observations along with 16 attributes about information of clients.  

![](./data.png)

## Attribute information:

   Input variables:
   bank client data:
   
   - `age (numeric)`
   
   - `job` : type of job (categorical: "admin.","unknown","unemployed","management","housemaid","entrepreneur","student",
                                       "blue-collar","self-employed","retired","technician","services") 
                                       
   - `marital` : marital status (categorical: "married","divorced","single"; note: "divorced" means divorced or widowed)
   
   - `education` (categorical: "unknown","secondary","primary","tertiary")
   
   - `default`: has credit in default? (binary: "yes","no")
   
   - `balance`: average yearly balance, in euros (numeric) 
   
   - `housing`: has housing loan? (binary: "yes","no")
   
   - `loan`: has personal loan? (binary: "yes","no") related with the last contact of the current campaign:
       
   - `contact`: contact communication type (categorical: "unknown","telephone","cellular") 
   
   - `day`: last contact day of the month (numeric)
  
   - `month`: last contact month of year (categorical: "jan", "feb", "mar", ..., "nov", "dec")
  
   - `duration`: last contact duration, in seconds (numeric)
       other attributes:
       
   - `campaign`: number of contacts performed during this campaign and for this client (numeric, includes last contact)
   
   - `pdays`: number of days that passed by after the client was last contacted from a previous campaign (numeric, -1 means client was          not previously contacted)
  
   - `previous`: number of contacts performed before this campaign and for this client (numeric)
  
   - `poutcome`: outcome of the previous marketing campaign (categorical: "unknown","other","failure","success")
       Output variable (desired target):
       
   - `y`: has the client subscribed a term deposit? (binary: "yes","no")
  

