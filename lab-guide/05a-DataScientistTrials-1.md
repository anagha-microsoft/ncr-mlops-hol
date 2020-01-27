# Module 5a - The base experiment (without AML)

## About
This lab guide section covers review of a model training experiment - in one of the notebooks uploaded in the previous section.  The notebook details an entire experiment (model training).  The code is from my data scientist contact - Michael Kareev - formerly a customer contact<br>

## 1.0. About the dataset, framingham.csv
The dataset is framingham.csv, you downloaded it in section 2;  Its a popular Kaggle open dataset.<br>
https://www.kaggle.com/amanajmera1/framingham-heart-study-dataset

**Attributes/columns:** <br><br>
male: 0 = Female; 1 = Male<br>
age: Age at exam time<br>
education: 1 = Some High School; 2 = High School or GED; 3 = Some College or Vocational School; 4 = college<br>
currentSmoker: 0 = nonsmoker; 1 = smoker<br>
cigsPerDay: number of cigarettes smoked per day (estimated average)<br>
BPMeds: 0 = Not on Blood Pressure medications; 1 = Is on Blood Pressure medications<br>
prevalentStroke<br>
prevalentHyp<br>
diabetes: 0 = No; 1 = Yes<br>
totChol in mg/dL<br>
sysBP in mmHg<br>
diaBP in mmHg<br>
BMI: Body Mass Index calculated as: Weight (kg) / Height(meter-squared)<br>
heartRate: Beats/Min (Ventricular)<br>
glucose in mg/dL<br><br>

TenYearCHD - Did the person get heart disease in the 10 years study period? <br>
label; 0 = No for heart disease, 1 = Yes for heart disease;<br>

## 2.0. About the use case - Coronary Heart Disease Prediction
Given a set of attributes, predict whether a person is at risk of heart disease.

## 3.0. About the experiment
The data scientist first prepares the data/dfata engineers, then runs an ML algorithm to train the model.
The experiment is supervised learning, classification type, leveraging Scikit-Learn library.  Use case is Coronary Heart Disease Prediction with the famous Kaggle dataset - framingham.csv described above.

## 4.0. Why this notebook?
This notebook introduces the Jupyter notebook on Azure; Typically, a data scientist would run experiments here, and then collabnorate with the DevOps engineer for operationalizing the pipelines and the model as a REST service.  In the next module, you will learn how to take the code and integrate with Azure Machine Learning.<br>

## 5.0. Execute the notebook
1. Navigate to your Azure Machine Learning instance on the Azure portal
2. Click on "Compute" in the left navigation panel
3. Click on Jupyter service
4. Then click on the first notebook

The instructor will talk through how to use Jupyter notebook.<br>
The focus is not the ML experiment as much as how to integrate with Azure Machine Learning and Azure DevOps - bear this in mind.<br>

## 6.0. Notebook review - part 1 - load necessary packages

![dse1-1](../images/0001-run-experiment-01.png)
<br>
<hr>
<br>


![dse1-2](../images/0001-run-experiment-02.png)
<br>
<hr>
<br>


![dse1-3](../images/0001-run-experiment-03.png)
<br>
<hr>
<br>

![dse1-4](../images/0001-run-experiment-04.png)
<br>
<hr>
<br>

![dse1-5](../images/0001-run-experiment-05.png)
<br>
<hr>
<br>


![dse1-6](../images/0001-run-experiment-06.png)
<br>
<hr>
<br>


![dse1-7](../images/0001-run-experiment-07.png)
<br>
<hr>
<br>


![dse1-8](../images/0001-run-experiment-08.png)
<br>
<hr>
<br>


![dse1-9](../images/0001-run-experiment-09.png)
<br>
<hr>
<br>






## Next steps
Move to the next module -> data scientist trials with AML integration.




