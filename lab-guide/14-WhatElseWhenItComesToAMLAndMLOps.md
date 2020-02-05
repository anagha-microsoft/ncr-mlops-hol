
# Module 14 - What was missed?  How can we improve our pipelines?

## About
This module covers enhancements you can do to the code base to explore the full depth and breadth of Azure Machine Learning and MLOps. 

## Accessing data

Datastores can be used to access storage without having to hard code the information required to connect to these resources. Supported datastores are : blob, ADLS gen 2, Azure SQL, Azure PostgreSQL, Azure MySQL and Databricks File System (DBFS)

Datasets can be used to access the data inside the supported Datastores. Currently the two dataset types are tabular dataset and file dataset. Tabular data supports reading parquet, delimited files, sql, json etc. File datasets support multiple files or folders that you want to mount

More info here https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-register-datasets 

## Environments

One of the key pieces to getting MLOps to work is building and maintaining a consistent environment to train, test and deploy models. The Environments feature within AML Services enables the team to consistently deliver a fully reproducible model with all the artifacts used to build it.  https://docs.microsoft.com/en-us/azure/machine-learning/concept-environments 

## Estimators 

To ease the training and building of models across different frameworks and algorithms, a higher level abstraction is available in Azure ML. ML Estimator can be generic enough that any algorithm, compute target, framework can be run with the same code along with minor changes in configuration. This greatly enhances productivity and experimentation for data scientists https://docs.microsoft.com/en-us/azure/machine-learning/how-to-train-ml-models

## Model Interpretability

For end users of machine learning models, there is a need to understand the reason behind the predictions. The ability to explain what inputs contributed to a certain prediction is usually referred to as model explainability or interpretability. Popular open source tools like SHAP, LIME etc are used in delivering insights into the models. https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability-aml 

## Data Drift
In the context of machine learning, data drift is the change in the system that makes the data used in training no longer being relevant. It is one of the top reasons where model accuracy degrades over time, thus monitoring data drift helps detect model performance issues. In most scenarios this warrants a retraining of the model with more relevant data that may be newer and more representative of current behavior. The data drift feature in Azure ML service measures the following : data drift coefficient, data drift contributions by feature. 

https://docs.microsoft.com/en-us/azure/machine-learning/how-to-monitor-data-drift 
<br>


To be continued...page authored by Dr Thomas Abraham....
