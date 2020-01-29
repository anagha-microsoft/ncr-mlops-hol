

# Module 11 - Configure and run the release pipeline in Azure DevOps

## About
This module covers configuring a release pipeline and executing it.  It also covers study of the AML assets created as part of the pipeline execution.
<br><br>Dedicate 60-90 minutes for this module - to thoroughly understand and execute

## 1.0. Create a release pipeline in Azure DevOps

1) Create a new release pipeline by clicking on the button
![dse2-1](../images/0001-release-01.png)
<br>
<hr>
<br>

2) Click on "Empty job"
![dse2-2](../images/0001-release-02.png)
<br>
<hr>
<br>


3) Name the stage "Deploy REST Service & Test"
![dse2-3](../images/0001-release-03.png)
<br>
<hr>
<br>

4) We will add a build artifact
![dse2-4](../images/0001-release-04.png)
<br>
<hr>
<br>

5) Click on "Build" and fill in details
![dse2-5](../images/0001-release-05.png)
<br>
<hr>
<br>

6) Next we will configure a trigger for continuous deployment
![dse2-6](../images/0001-release-06.png)
<br>
<hr>
<br>

7) Complete the configuration as depicted
![dse2-7](../images/0001-release-07.png)
<br>
<hr>
<br>

8) 
![dse2-8](../images/0001-release-08.png)
<br>
<hr>
<br>

9) Save
![dse2-9](../images/0001-release-09.png)
<br>
<hr>
<br>

10) You should see a circle around the thunderbolt incon to reflect (visually) that its configured
![dse2-10](../images/0001-release-10.png)
<br>
<hr>
<br>

## Recap
Its a wrap for this module.  You now know how to (1) ..

## Next steps
Move to the next module -> this covers testing the REST service operationalized as part of the release pipeline, manually, in a Jupyter notebook
