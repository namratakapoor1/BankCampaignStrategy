# Bank_Marketing_Campaign
  Bank Marketing Campaign
 
 ## Problem Statement
 Analysis of a Bank Marketing Campaign and gather insights for marketing team stakeholders
 
 ## Business Use Case
There has been a revenue decline for a bank and they would like to know what actions to take. After investigation, they found out that the root cause is that their clients are not depositing as frequently as before. Knowing that term deposits allow banks to hold onto a deposit for a specific amount of time, so banks can invest in higher gain financial products to make a profit. In addition, banks also hold better chance to persuade term deposit clients into buying other products such as funds or insurance to further increase their revenues. As a result, the bank would like to identify existing clients that have higher chance to subscribe for a term deposit and focus marketing efforts on such clients.


## Data Science Problem Statement
Predict if the client will subscribe to a term deposit based on the analysis of the marketing campaigns the bank performed.


## Evaluation Metric
We will be using roc_auc_score for evaluation.

## Objective of this notebook
The main objective of this template is to walkthrough the entire working pipeline that can be followed during work.

We will be writing modular code in form of functions, the major advantages of this are:

* Functions are reusable and at a later stage, the same task can be performed again by just importing the function without explicitly having to write the same piece of code again.This can save a good amount of time at work places.
* So we should make sure to assemble all lines of code within a function.

## Understanding the dataset
### Data Set Information
The data is related to direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be subscribed ('yes') or not ('no') subscribed.

There are two datasets: train.csv with all examples (32950) and 21 inputs including the target feature, ordered by date (from May 2008 to November 2010), very close to the data analyzed in [Moro et al., 2014]

test.csv which is the test data that consists of 8238 observations and 20 features without the target feature

**Goal:-** The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

### Features
| Feature | Feature_Type | Description |
|------|------|------|
|   age  | numeric| age of a person |
|job    | Categorigol,nominal|type of job ('admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')|
|marital|categorical,nominal|marital status ('divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)|
|education|categorical,nominal|('basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')|
|default|categorical,nominal|has credit in default? ('no','yes','unknown')|
|housing|categorical,nominal|has housing loan? ('no','yes','unknown')|
|loan|categorical,nominal|has personal loan? ('no','yes','unknown')|
|contact|categorical,nominal|contact communication type ('cellular','telephone')|
|month|categorical,ordinal|last contact month of year ('jan', 'feb', 'mar', ..., 'nov', 'dec')|
|day_of_week|categorical,ordinal|last contact day of the week ('mon','tue','wed','thu','fri')|
|duration|numeric|last contact duration, in seconds . Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no')|
|campaign|numeric|number of contacts performed during this campaign and for this client (includes last contact)|
|pdays|numeric|number of days that passed by after the client was last contacted from a previous campaign (999 means client was not previously contacted)|
|previous|numeric|number of contacts performed before this campaign and for this client|
|poutcome|categorical,nominal|outcome of the previous marketing campaign ('failure','nonexistent','success')|
|emp.var.rate|numeric|employment variation rate - quarterly indicator|
|cons.price.idx|numeric|consumer price index - monthly indicator|
|cons.conf.idx|numeric|consumer confidence index - monthly indicator|
|euribor3m|numeric|euribor 3 month rate - daily indicator|
|nr.employed|numeric|number of employees - quarterly indicator|


## Target variable (desired output):
|Feature|Feature_Type|Description|
|------|------|------|
|y|binary|has the client subscribed a term deposit? ('yes','no')|

There are many **Classification algorithms** are present in machine learning, which are used for different classification applications. Some of the main classification algorithms are as follows-

* Logistic Regression
* DecisionTree Classifier
* RandomForest Classfier
* XGBClassifier
* GradientBoostingClassifier

The function we have written below takes the features, target and the classification model as the input parameters and internally splits them into training data and validation data. It then fits the classification model on the train data and then makes a prediction on the validation data and outputs the roc_auc_score and the roc_curve for this prediction.

**Note:** Please refer *Bank_Marketing_Campaign_Analysis_Notebook.ipynb* in the repository for Python code, Observations, Machine Learning models and other details.










 
