
# Module 10 - Configure and run the build pipeline in Azure DevOps

## About
This module covers configuring a build pipeline and executing it, and finally renaming it to something meaningful.  It also covers stufy of the AML assets created, and artifact published which is input for the release pipeline.
<br><br>Dedicate 180 minutes for this module - to thoroughly understand and execute

## 1.0. Create a build pipeline in Azure DevOps

![dse2-0](../images/0001-create-build-pipeline-00.png)
<br>
<hr>
<br>

1) Select existing Azure Pipelines YAML as the base
![dse2-1](../images/0001-create-build-pipeline-01.png)
<br>
<hr>
<br>

2) Select the YAML file
![dse2-2](../images/0001-create-build-pipeline-02.png)
<br>
<hr>
<br>


3) Edit the YAML file to update it with your details
![dse2-4](../images/0001-create-build-pipeline-04.png)
<br>
<hr>
<br>


4) Save and run with commit to master branch
![dse2-5](../images/0001-create-build-pipeline-05.png)
<br>
<hr>
<br>


5) You should see the pipeline starting
![dse2-6](../images/0001-create-build-pipeline-06.png)
<br>
<hr>
<br>


6) Browse around; The pipeline takes 30 minutes to run.
![dse2-7](../images/0001-create-build-pipeline-07.png)
<br>
<hr>
<br>

7) Browse around...
![dse2-8](../images/0001-create-build-pipeline-08.png)
<br>
<hr>
<br>


8) Browse around...
![dse2-9](../images/0001-create-build-pipeline-09.png)
<br>
<hr>
<br>


9) Browse around...
![dse2-10](../images/0001-create-build-pipeline-10.png)
<br>
<hr>
<br>

10) Browse around...
![dse2-11](../images/0001-create-build-pipeline-11.png)
<br>
<hr>
<br>

11) Note the steps executing...
![dse2-12](../images/0001-create-build-pipeline-12.png)
<br>
<hr>
<br>

12) Verify if the transient compute got created...<br>
Note that it does not have "manual" keyword in it
![dse2-13](../images/0001-create-build-pipeline-13.png)
<br>
<hr>
<br>

13) Verify if the experiment got created...<br>
Note that it does not have "manual" keyword in it
![dse2-14](../images/0001-create-build-pipeline-14.png)
<br>
<hr>
<br>

14) Notice that there are multiple runs<br>

![dse2-15](../images/0001-create-build-pipeline-15.png)
<br>
<hr>
<br>

15) Run 1 for provisioninhg the training compute<br>

![dse2-16](../images/0001-create-build-pipeline-16.png)
<br>
<hr>
<br>

16) Here is run 2<br>
![dse2-17](../images/0001-create-build-pipeline-17.png)
<br>
<hr>
<br>

17) Run 2 is the build pipeline<br>
![dse2-18](../images/0001-create-build-pipeline-18.png)
<br>
<hr>
<br>

18) Here is run #3<br>
![dse2-19](../images/0001-create-build-pipeline-19.png)
<br>
<hr>
<br>


19) Its the model training step.  Click on the runID link..<br>
![dse2-20](../images/0001-create-build-pipeline-20.png)
<br>
<hr>
<br>


20) Click on the link to the training compute<br>
![dse2-21](../images/0001-create-build-pipeline-21.png)
<br>
<hr>
<br>


21) Fancy new AML UI that shows the transient compute state<br>
![dse2-22](../images/0001-create-build-pipeline-22.png)
<br>
<hr>
<br>


22) Observe the steps<br>
![dse2-23](../images/0001-create-build-pipeline-23.png)
<br>
<hr>
<br>


23) Look at the detailed log on the right.  MNot optimal for production, but great for learning MLOps.<br>
![dse2-24](../images/0001-create-build-pipeline-24.png)
<br>
<hr>
<br>


24) Where are we now?<br>
![dse2-25](../images/0001-create-build-pipeline-25.png)
<br>
<hr>
<br>


25) Inside containerize.py<br>
![dse2-26](../images/0001-create-build-pipeline-26.png)
<br>
<hr>
<br>

26) Determine if the model makes the cut to be deployed..<br>
![dse2-27](../images/0001-create-build-pipeline-27.png)
<br>
<hr>
<br>

27) Registering container image<br>
![dse2-28](../images/0001-create-build-pipeline-28.png)
<br>
<hr>
<br>

28) Check on the portal AML workspace for impage registration<br>
![dse2-29](../images/0001-create-build-pipeline-29.png)
<br>
<hr>
<br>

29) Back in the main master build pipeline<br>
![dse2-30](../images/0001-create-build-pipeline-30.png)
<br>
<hr>
<br>

30) You should see an image, click on it<br>
![dse2-31](../images/0001-create-build-pipeline-31.png)
<br>
<hr>
<br>

31) Review the metadata<br>
![dse2-32](../images/0001-create-build-pipeline-32.png)
<br>
<hr>
<br>

32) Almost done<br>
![dse2-33](../images/0001-create-build-pipeline-33.png)
<br>
<hr>
<br>

33) Done<br>
![dse2-34](../images/0001-create-build-pipeline-34.png)
<br>
<hr>
<br>

34) Click on "Publish artifacts" - this is critical for the release pipeline<br>
![dse2-35](../images/0001-create-build-pipeline-35.png)
<br>
<hr>
<br>

35) Done<br>
![dse2-36](../images/0001-create-build-pipeline-36.png)
<br>
<hr>
<br>

## 2. Rename the pipeline to indicate it is the "Build" pipeline

36) Click on pipelines<br>
![dse2-37](../images/0001-create-build-pipeline-37.png)
<br>
<hr>
<br>


37) Rename<br>
![dse2-38](../images/0001-create-build-pipeline-38.png)
<br>
<hr>
<br>

## 3. Lets trigger a build and ensure it completes successfully

38) Note this line in the Build Master YAML - any change to git master branch will trigger build<br>
![dse2-39](../images/0001-create-build-pipeline-39.png)
<br>
<hr>
<br>

39) Edit the Readme.md to launch a build pipeline<br>
![dse2-40](../images/0001-create-build-pipeline-40.png)
<br>
<hr>
<br>

40) Commit to master<br>
![dse2-41](../images/0001-create-build-pipeline-41.png)
<br>
<hr>
<br>

41) ....<br>
![dse2-42](../images/0001-create-build-pipeline-42.png)
<br>
<hr>
<br>

42) Notice that it launched a job<br>
![dse2-43](../images/0001-create-build-pipeline-43.png)
<br>
<hr>
<br>

43) Give it 30 minutes - ensure it was successful<br>
![dse2-44](../images/0001-create-build-pipeline-44.png)
<br>
<hr>
<br>

44) Successful!!<br>
![dse2-45](../images/0001-create-build-pipeline-45.png)
<br>
<hr>
<br>

45) Total time<br>
![dse2-46](../images/0001-create-build-pipeline-46.png)
<br>
<hr>
<br>

## 4. The "build artifact"
The build artifact is published as part of the pipeline and it captures a snapshot of the code, training data and associated assets created.  It is tightly associated with an experiment run.  One component of it - a json file, forms the input for our release pipeline.  <br>

As a quick exercise, <br>
(1) Navigate in your git repo, and locate references to "artifact" <br>
(2) Locate the artifact of the first execution. download and browse through it<br>
(3) Review the json file and understand its contents<br>

1. Navigate to a recent run and click on it to get to the artifact
![dse3-1](../images/0001-artifact-01.png)
<br>
<hr>
<br>

2.
![dse3-2](../images/0001-artifact-02.png)
<br>
<hr>
<br>

3.
![dse3-3](../images/0001-artifact-03.png)
<br>
<hr>
<br>

4.
![dse3-4](../images/0001-artifact-04.png)
<br>
<hr>
<br>

5.
![dse3-5](../images/0001-artifact-05.png)
<br>
<hr>
<br>


## Recap
Its a wrap for this module.  You now know how to (1) navitgate in Azure DevOps, (2) and configure a "Build" pipeline that (3) provisions transient compute, (4) trains a model on the provisioned remote compute, (5) registers the model into AML model registry, and (6) creates a container image and (7) registers it into AML container registry. You also know (8) how to monitor the pipeline progress in Azure DevOps and (9) correlate to ML assets that become available in AML workspace on the portal from the pipeline execution; Finally (10) you understand what the published artifact is, how to locate it, how its tracked, and its function relative to the release pipeline

## Next steps
Move to the next module -> this covers building the release pipeline.
