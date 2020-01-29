# Module 13 - Execute a continuous deployment (e2e run)

## About
This module covers cleaning up your workspace, editing the code, and committing to master -> this triggers an end to end, build to release pipeline.  This will help us ensure everything works as expected from a continuous deployment perspective.  Lets do this lab twice and observe how the release pipeline differs the second time around in the logs.<br>

For your pleasure, there are challenges at the end of the module.
<br><br>Dedicate 60-90 minutes for this module - to thoroughly understand and execute

## 1.0. Clean up resources in Azure ML workspace

1) Delete any prior deployment
![dse2-1](../images/0001-cd-cleanup-01.png)
<br>
<hr>
<br>

2) Delete any prior images
![dse2-2](../images/0001-cd-cleanup-02.png)
<br>
<hr>
<br>


3) Delete any prior models
![dse2-3](../images/0001-cd-cleanup-05.png)
<br>
<hr>
<br>


4) Delete any training compute (not manual)
![dse2-4](../images/0001-cd-cleanup-03.png)
<br>
<hr>
<br>


5) Delete any inference compute, wait till it shows complete deletion
![dse2-5](../images/0001-cd-cleanup-04.png)
<br>
<hr>
<br>


## 2.0. Modify code in your DevOps git and commit to master to trigger a build pipeline

1) Go to deploy-rest-service.py, line 188 and add two periods are the very end
![dse2-1](../images/0001-cd-test-01.png)
<br>
<hr>
<br>

![dse2-2](../images/0001-cd-test-02.png)
<br>
<hr>
<br>

## 3.0. Monitor the build pipeline through completion (30-40 minutes - take a power nap/break)
![dse2-3](../images/0001-cd-test-03.png)
<br>
<hr>
<br>


![dse2-4](../images/0001-cd-test-04.png)
<br>
<hr>
<br>


![dse2-5](../images/0001-cd-test-05.png)
<br>
<hr>
<br>

Build should complete successfully!
![dse2-6](../images/0001-cd-release-01.png)
<br>
<hr>
<br>


Check the Azure portal - AML workspace to ensure you see the AML assets getting provisioned/created/registered

## 4.0. Monitor the release pipeline through completion (30-40 minutes - take a power nap/break)

1) Release should start automatically!

![dsr2-2](../images/0001-cd-release-02.png)
<br>
<hr>
<br>

2) In progress...

![dsr2-3](../images/0001-cd-release-03.png)
<br>
<hr>
<br>

3) Deploy and test REST service...

![dse2-4](../images/0001-cd-release-04.png)
<br>
<hr>
<br>

4) Completion...

![dse2-5](../images/0001-cd-release-05.png)
<br>
<hr>
<br>

![dse2-6](../images/0001-cd-release-06.png)
<br>
<hr>
<br>

![dse2-7](../images/0001-cd-release-07.png)
<br>
<hr>
<br>

## 5.0. Run it again - from step 2
Discuss/explore what is different with the second run in this module.

## 6.0. Challenge - 1
In the script, deploy-rest-service.py, fix this piece of code that is commented out; You should be able to test the REST API as part of the script<br>

![dsc2-1](../images/0001-challenge-1.png)
<br>
<hr>
<br>

## 7.0. Challenge - 2
2) Navigate to Jupyter on the portal in your AML workspace, and run through the notebook, 04-ml-trials-model-telemetry.ipynb<br>
This enables telemetry and does some sample REST calls to collect some data for telemetry analysis

## 8.0. Challenge - 3
Run through this documentation and explore your model telemetry
https://docs.microsoft.com/en-us/azure/machine-learning/how-to-enable-data-collection

## Recap
In this module, you learned how modified code triggers a continuous build + release pipeline.  You noticed what happens from a REST service perspective with repeated runs.

## Next
This last module speakes to what else is available in AML and MLOps that was not included in the lab for scope management.  

