

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

8) You are still in the process of configuring a trigger
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

11) Rename pipeline to something meaningful
![dse2-11](../images/0001-release-11.png)
<br>
<hr>
<br>

12) Click on "Tasks", then on "Agent job" and configure agent specs as shown in screenshot
![dse2-12](../images/0001-release-12.png)
<br>
<hr>
<br>

13) Ensure artifact config is as shown
![dse2-13](../images/0001-release-13.png)
<br>
<hr>
<br>

14) Save
![dse2-14](../images/0001-release-14.png)
<br>
<hr>
<br>

15) Add a task to the "Agent job" by clicking on the "+"
![dse2-15](../images/0001-release-15.png)
<br>
<hr>
<br>

16) Add a "Use Python task"
![dse2-16](../images/0001-release-16.png)
<br>
<hr>
<br>

17) Configure as shown below - name it "Install Python 3.6", complete the rest of the configuration
![dse2-17](../images/0001-release-17.png)
<br>
<hr>
<br>

18) Save
![dse2-18](../images/0001-release-18.png)
<br>
<hr>
<br>

19) Add another agent job task
![dse2-19](../images/0001-release-19.png)
<br>
<hr>
<br>

20) Select "bash" this time
![dse2-20](../images/0001-release-20.png)
<br>
<hr>
<br>

21) Click on "Add"
![dse2-21](../images/0001-release-21.png)
<br>
<hr>
<br>

22) Name it "Install dependencies on agent", and select script path by clicking on ellipsis
![dse2-22](../images/0001-release-22.png)
<br>
<hr>
<br>

23) Navigate to the agent-dependencies.sh
![dse2-23](../images/0001-release-23.png)
<br>
<hr>
<br>

24) Configure script path
![dse2-24](../images/0001-release-24.png)
<br>
<hr>
<br>

25) Save
![dse2-25](../images/0001-release-25.png)
<br>
<hr>
<br>

26) Add yet another task
![dse2-26](../images/0001-release-26.png)
<br>
<hr>
<br>

27) Select "Azure CLI"
![dse2-29](../images/0001-release-29.png)
<br>
<hr>
<br>

28) You should see an Azure CLI task
![dse2-30](../images/0001-release-30.png)
<br>
<hr>
<br>

29) Lets configure it
![dse2-31](../images/0001-release-31.png)
<br>
<hr>
<br>

30) Type in, in the "Inline script text area" -

```python scripts-operationalize/deploy-rest-service.py --service_name $(service_name) --aks_name $(aks_name) --aks_region $(aks_region) --description $(description)```
 

![dse2-27](../images/0001-release-27.png)
<br>
<hr>
<br>

31) Select directory from artifact
![dse2-32](../images/0001-release-32.png)
<br>
<hr>
<br>

32) What it should look like
![dse2-35](../images/0001-release-35.png)
<br>
<hr>
<br>

33) Save
![dse2-34](../images/0001-release-34.png)
<br>
<hr>
<br>

34) Now lets switch to variables
![dse2-36](../images/0001-release-36.png)
<br>
<hr>
<br>

35) Lets add pipeline variables
![dse2-37](../images/0001-release-37.png)
<br>
<hr>
<br>

36) Key in the following variables exactly as shown below as key-value pair, including any quotes:<br>
aks_name        chdinf01<br>
aks_region      eastus2<br>
description     "Coronary Heart Disease Prediction REST Service"<br>
service_name    chd-predictor-service<br>
   
![dse2-38](../images/0001-release-38.png)
<br>
<hr>
<br>

38) 
![dse2-39](../images/0001-release-39.png)
<br>
<hr>
<br>

39) 
![dse2-40](../images/0001-release-40.png)
<br>
<hr>
<br>

40) 
![dse2-41](../images/0001-release-41.png)
<br>
<hr>
<br>

41) 
![dse2-42](../images/0001-release-42.png)
<br>
<hr>
<br>

42) 
![dse2-43](../images/0001-release-43.png)
<br>
<hr>
<br>

43) 
![dse2-44](../images/0001-release-44.png)
<br>
<hr>
<br>

40) 
![dse2-45](../images/0001-release-45.png)
<br>
<hr>
<br>

40) 
![dse2-46](../images/0001-release-46.png)
<br>
<hr>
<br>

40) 
![dse2-47](../images/0001-release-47.png)
<br>
<hr>
<br>

40) 
![dse2-48](../images/0001-release-48.png)
<br>
<hr>
<br>

40) 
![dse2-49](../images/0001-release-49.png)
<br>
<hr>
<br>

40) 
![dse2-50](../images/0001-release-50.png)
<br>
<hr>
<br>

40) 
![dse2-51](../images/0001-release-51.png)
<br>
<hr>
<br>

40) 
![dse2-52](../images/0001-release-52.png)
<br>
<hr>
<br>

40) 
![dse2-53](../images/0001-release-53.png)
<br>
<hr>
<br>

40) 
![dse2-54](../images/0001-release-54.png)
<br>
<hr>
<br>

40) 
![dse2-55](../images/0001-release-55.png)
<br>
<hr>
<br>

40) 
![dse2-56](../images/0001-release-56.png)
<br>
<hr>
<br>

40) 
![dse2-57](../images/0001-release-57.png)
<br>
<hr>
<br>

40) 
![dse2-58](../images/0001-release-58.png)
<br>
<hr>
<br>



## Recap
Its a wrap for this module.  You now know how to (1) ..

## Next steps
Move to the next module -> this covers testing the REST service operationalized as part of the release pipeline, manually, in a Jupyter notebook
