# Module 13 - Execute and end to end run

## About
This module covers cleaning up your workspace, editing the code, and committing to master -> this triggers an end to end, build to release pipeline.  This will help us ensure everything works as expected from a continuous deployment perspective.  Lets do this lab twice and observe how the release pipeline differs the second time around in the logs.
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

Check the Azure portal - AML workspace to ensure you see the AML assets getting provisioned/created/registered

## 4.0. Monitor the release pipeline through completion (30-40 minutes - take a power nap/break)
