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


## 7.0. Provision managed compute
In Jupyter, execute this cell..<br>
![dse2-6-1](../images/0001-ds-aml-06-1.png)
<br>
<hr>
<br>

Observe the status changing in the cell output..
![dse2-6-2](../images/0001-ds-aml-06-2.png)
<br>
<hr>
<br>

You should see the completion message
![dse2-6-3](../images/0001-ds-aml-06-3.png)
<br>
<hr>
<br>

Switch to the portal and ensure you see the compute provisioned...
![dse2-6-4](../images/0001-ds-aml-06-4.png)
<br>
<hr>
<br>

## 8.0. Create a docker based environment
In Jupyter, execute this cell..<br>
![dse2-7-1](../images/0001-ds-aml-07.png)
<br>
<hr>
<br>

## 9.0. Create the training script file
In Jupyter, execute this cell..<br>
![dse2-8-1](../images/0001-ds-aml-08.png)
<br>
<hr>
<br>

In Jupyter, execute this cell..<br>
![dse2-8-2](../images/0001-ds-aml-09.png)
<br>
<hr>
<br>

## 10.0. Launch the experiment and check the execution details both in Jupyter cell output as well as the AML workspace in the portal
In Jupyter, execute this cell..<br>
![dse2-10-1](../images/0001-ds-aml-10-1.png)
<br>
<hr>
<br>


![dse2-10-2](../images/0001-ds-aml-10-2.png)
<br>
<hr>
<br>

You should see the experiment is running...
![dse2-10-3](../images/0001-ds-aml-10-3.png)
<br>
<hr>
<br>

You should see the output in Jupyter...
![dse2-10-4](../images/0001-ds-aml-10-4.png)
<br>
<hr>
<br>

## 11.0. Poll for experiment completion, and validate in Jupyter home page for creation of model 
In Jupyter, execute this cell..<br>
![dse2-11-1](../images/0001-ds-aml-11-1.png)
<br>
<hr>
<br>

Poll...
![dse2-11-2](../images/0001-ds-aml-11-2.png)
<br>
<hr>
<br>

![dse2-11-3](../images/0001-ds-aml-11-3.png)
<br>
<hr>
<br>

Poll...
![dse2-11-4](../images/0001-ds-aml-11-4.png)
<br>
<hr>
<br>

You should see the model persisted, in yiur Jupyter home page in the specified directory
![dse2-11-5](../images/0001-ds-aml-11-5.png)
<br>
<hr>
<br>

## 12.0. Check experiment status
In Jupyter, execute this cell..<br>
![dse2-12-1](../images/0001-ds-aml-12-1.png)
<br>
<hr>
<br>

You should see output like below.
![dse2-12-2](../images/0001-ds-aml-12-2.png)
<br>
<hr>
<br>

## 13.0. Review of experiment as logged in AML
In Jupyter, execute this cell..<br>
![dse2-13-1](../images/0001-ds-aml-13-1.png)
<br>
<hr>
<br>

Click on the link
![dse2-13-2](../images/0001-ds-aml-13-2.png)
<br>
<hr>
<br>

Click on the run number...
![dse2-13-3](../images/0001-ds-aml-13-3.png)
<br>
<hr>
<br>

Out fancy new UI shows the compute state
![dse2-13-4](../images/0001-ds-aml-13-4.png)
<br>
<hr>
<br>

Other general details, back in the portal experience...
![dse2-13-5](../images/0001-ds-aml-13-5.png)
<br>
<hr>
<br>

The model output...
![dse2-13-6](../images/0001-ds-aml-13-6.png)
<br>
<hr>
<br>


The logs..
![dse2-13-7](../images/0001-ds-aml-13-7.png)
<br>
<hr>
<br>


A snapshot of the training script is persisted along with the experiment run details for history and ntraceability
![dse2-13-8](../images/0001-ds-aml-13-8.png)
<br>
<hr>
<br>


## Next steps
Move to the next module -> Azure DevOps.




