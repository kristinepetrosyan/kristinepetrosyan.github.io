---
layout: post
title:      "Handling missing data for Bank marketing dataset"
date:       2020-07-13 20:56:18 +0000
permalink:  handling_missing_data_for_bank_marketing_dataset
---


Last couple of months I was enhancing my knowledge in Data Science and here we go I just finished my third project.
For my project I chose famous dataset ‘Bank Marketing’ from UCI Machine Learning Repository. The aim of this project is to predict whether customer is subscribing bank deposit or no by applying several machine learning classification models. Of course I started with Data cleaning and againI have faced with handling the missing values. There are different approaches to this problem. Firstly, we should accept that there is no exact one way to deal with missing data. I have come across different solutions for data imputation depending on the kind of problem and it is difficult to provide a general solution.

In this blog, I will try to summarize the most commonly used methods and try to find a structural solution.
**Impute or Delete the Data**

Before we decide to remove or replace or impute the data, we have to understand the reason why data is missing.
Missing at Random : This means that the tendency for a data point to be missing is not related to the missing data, but it is related to some of the observed data.
Missing Completely at Random: The fact that a certain value is missing has nothing to do with its hypothetical value and with the values of other variables.
Missing not at Random: Possible reasons are that the missing value depends on the hypothetical value or missing value is dependent on some other variable’s value.
Above mentioned first two cases will allow safely remove the data with missing values depending upon their occurrences, but in the third case removing observations with missing values can produce a bias in the model. This means that we should be careful before removing anything.

In our example we have a dataset which consists of 21 columns and 41187 rows. The features of the data are:
1 — age (numeric)
2 — job : type of job (categorical: “admin.”,”blue-collar”,”entrepreneur”,”housemaid”,”management”,”retired”,”self-employed”,”services”,”student”,”technician”,”unemployed”,”unknown”)
3 — marital : marital status (categorical: “divorced”,”married”,”single”,”unknown”; note: “divorced” means divorced or widowed)
4 — education (categorical: “basic.4y”,”basic.6y”,”basic.9y”,”high.school”,”illiterate”,”professional.course”,”university.degree”,”unknown”)
5 — default: has credit in default? (categorical: “no”,”yes”,”unknown”)
6 — housing: has housing loan? (categorical: “no”,”yes”,”unknown”)
7 — loan: has personal loan? (categorical: “no”,”yes”,”unknown”)
8 — contact: contact communication type (categorical: “cellular”,”telephone”)
9 — month: last contact month of year (categorical: “jan”, “feb”, “mar”, …, “nov”, “dec”)
10 — day_of_week: last contact day of the week (categorical: “mon”,”tue”,”wed”,”thu”,”fri”)
11 — duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y=”no”). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
12 — campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13 — pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means clients was not previously contacted)
14 — previous: number of contacts performed before this campaign and for this client (numeric)
15 — poutcome: outcome of the previous marketing campaign (categorical: “failure”,”nonexistent”,”success”)
16 — emp.var.rate: employment variation rate — quarterly indicator (numeric)
17 — cons.price.idx: consumer price index — monthly indicator (numeric)
18 — cons.conf.idx: consumer confidence index — monthly indicator (numeric)
19 — euribor3m: euribor 3-month rate — daily indicator (numeric)
20 — nr.employed: number of employees — quarterly indicator (numeric)

We see that there are unknown values in features marital, education, default, housing and loan, which we may want to address:
![](https://medium.com/@kristinelpetrosyan/handling-missing-data-for-bank-marketing-dataset-8098385d489c)
marital married: The unknown values represent 0.2% of our dataset. We choose to replace the unknown values with the mode of the feature.

education university.degree: Although this is not a dominating feature we have a choice to keep it but we will impute using the k-Nearest Neighbors Imputer since 4% is unknown.
![](https://medium.com/@kristinelpetrosyan/handling-missing-data-for-bank-marketing-dataset-8098385d489c)

default no: 79% of the entries having value no. So we will replace the unknown values with no.
housing : Unknown data is 2.4% of the dataset. We will choose to impute using the k-Nearest Neighbors Imputer.
loan: 82% of the entries having value no and 2.4% of entries having value unknown. Based on difference we will replace the unknown values with no.
Hope I could help you.



