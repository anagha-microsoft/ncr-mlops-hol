# Module 6 - The base experiment + Azure Machine Learning integration (Not Devops yet)

## About
This module covers review of a model training experiment with Azure ML integration. The notebook, 02-ml-ops-training.ipynb, referenced in the module is a sample you can use to show a Data Scientist how to leverage AML Service for transient training compute provisioning, model training, and registering the trained model into AML model registry. Section 8 of the notebook will be leveraged as a .py script in the DevOps pipeline.

## 1.0. Launch the notebook...
Launch 02-ml-ops-training.ipynb.  You can get to it in your Jupyter environment, you uploaded it in a previous module.

![dse2-1](../images/0001-ds-aml-00-1.png)
<br>
<hr>
<br>

![dse2-2](../images/0001-ds-aml-00-2.png)
<br>
<hr>
<br>

![dse2-3](../images/0001-ds-aml-00-3.png)
<br>
<hr>
<br>

## 2.0. Launch the notebook and update the environment variables with your details

![dse2-4](../images/0001-ds-aml-01.png)
<br>
<hr>
<br>

## 3.0. Load necessary packages

![dse2-5](../images/0001-ds-aml-02.png)
<br>
<hr>
<br>

## 4.0. Connect to your Azure Machine Learning workspace and authenticate

![dse2-6-1](../images/0001-ds-aml-03.1.png)
<br>
<hr>
<br>

Capture the device authn code, and click on the link.
![dse2-6-2](../images/0001-ds-aml-03.2.png)
<br>
<hr>
<br>

Enter your code
![dse2-6-3](../images/0001-ds-aml-03.3.png)
<br>
<hr>
<br>

Select your user name/subscription and authenticate yourself..
![dse2-6-4](../images/0001-ds-aml-03.4.png)
<br>
<hr>
<br>

Close the page..
![dse2-6-5](../images/0001-ds-aml-03.5.png)
<br>
<hr>
<br>

## 5.0. Instantiate an experiment in your notebook; Cross reference its creation in your AML workspace - experiments
In Jupyter, execute this cell..<br>
![dse2-4-1](../images/0001-ds-aml-04-1.png)
<br>
<hr>
<br>

Switch to the portal and look at "Experiments" in your AML workspace; You should see the experiment you created.
![dse2-4-2](../images/0001-ds-aml-04-2.png)
<br>
<hr>
<br>


## 6.0. Configure a project directory and see the same created in Jupyter home page
In Jupyter, execute this cell..<br>
![dse2-5-1](../images/0001-ds-aml-05-1.png)
<br>
<hr>
<br>

Switch to the Jupyter home page see the directory you created.
![dse2-5-2](../images/0001-ds-aml-05-2.png)
<br>
<hr>
<br>

## Next steps
Move to the next module -> data scientist trials continued, this time, with AML integration.




