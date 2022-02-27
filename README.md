# Future Ready Talent- Project
## Adult income prediction using Azure Machine Learning Studio (Classic)

***Project Description***
Using freely available datasets from UCI Machine learning repository on Adult census, I have tried to create a Machine Learning Model, that will predict how much is the income of a dataset. Using independent features like race, sex, age, capital loss, hours-per-week, native country, and others, I bionomically categories any individual if he falls above >=50k income pool, or <50k income pool. I do pre-processing on the available open dataset, do feature engineering, transform the label datatype, and use Decision Tree classifier to train the model. The final result is deployed as web service, that gives an API to perform GET requests and eventually infer from the model.

***Problem Statement/Opportunity***
Often, financial institutions need to categorize their customers based on their income, however, generic features like age, work-sector, education, are not enough to predict their income. The Adult Census dataset available in UCI ML repository, uses 14 features to predict an individual's income, thus helping in binomial classification of individuals based on their income. The result is useful in accurate service recommendation. Individuals with >= 50k income fall in medium wage income and thus can be segmented to respective promotional services, while those with < 50k income, can be provided with low cost services. Those above >=50k income are eligible for expensive offers and promotional memberships for clubs, credit cards, etc. while those with income <50k, shall be targeted with more budget constrained offers. The categorization can also help in predicting the life-style of the individual.

The project is done in 6 steps:
> Introduction
> Dataset cleaning and Pre-processing
> Accounting for class imbalance
> Training the ML model-  Two-Class Boosted Decision tree; Hyper parameter tuning
> Scoring and Evaluating the models
> Publishing the trained model as a Web Service

The aim of this project is to build an end-to-end Machine Learning (ML here after) project using the Azure Machine Learning Studio Visual interface which is a no-code platform.

### Dataset discussion:
[Dataset](https://github.com/Sarthak-Goel/Adult-Income-Prediction-AzureMLStudio/blob/main/Adult%20Census%20Income%20Binary%20Classification%20dataset.csv)
- The dataset to be used is *Adult Census Dataset*, which is freely available in Dataset section of Azure ML Studio portal.
This a benchmark dataset, which is also available in UCI Machine Learning 
- *Problems with the dataset*
The dataset has a major class imbalance problem. This can lead to imbalanced results. Also, for many features the datatype is string while some are inconsistent. ALl this requires feature engineering, as it is necessary to convert it to categorical data.
- *Data Cleaning & Pre-Processing*
Firstly, we need to fill in the missing values.
I fill the missing values with 0.
fnlwgt column means 'final weight'. It signifieis the number of people that this particular individual represent in the population. This column isn't of much help, so we are going to get rid of this coulmn. Similarly, the education column is not of much importance, and therefore, we'll get rid of that as well.
Using the edit metadata tool, we convert columns to catagorical label from string features.
Removing columns, will reduce the cluttering in our dashboard and model.

### Aim: 
- The aim of this project is to check if an adult has income exceeding 50k per year based on the census data.

### Algorithm Used:
- For the following project, I have used the Decision Tree (Booster) algorithm to create and train the model.

### Delivery
- The model is available as an azure model web service. This exposes an API to perform a GET request for using the interface.

---

