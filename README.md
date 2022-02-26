# Future Ready Talent- Project
## Adult income prediction using Azure Machine Learning Studio (Classic)

The project is done in 6 steps:
> Introduction
> Dataset cleaning and Pre-processing
> Accounting for class imbalance
> Training the ML model-  Two-Class Boosted Decision tree; Hyper parameter tuning
> Scoring and Evaluating the models
> Publishing the trained model as a Web Service

The aim of this project is to build an end-to-end Machine Learning (ML here after) project using the Azure Machine Learning Studio Visual interface which is a no-code platform.

### Dataset discussion:
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
