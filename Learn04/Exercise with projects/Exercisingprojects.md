# Here we will be doing our first Deployment exercise
First you need to login in to the developer sandbox given by the redhat and follow the steps in this url[https://redhat-scholars.github.io/openshift-starter-guides/rhs-openshift-starter-guides/4.11/parksmap-container-image.html#deploy_your_first_image]

Once you are in sandbox you make sure you are in Developer, from their click on Add-->Click on container image and once the field popup.
<img width="969" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/7b219195-2f85-4ae2-a833-381093a9e8e1">

    In the image filed name copy this <quay.io/openshiftroadshow/parksmap:latest> 
    In the run time icon you can leave default as openshift else you can choose according to your program language
    In the Application Name field <you provide input as "**workshop**"
    In the Name filed <you provide input as "**parksmap**"
    In the resource type select as "**Deployment from drop down**"
    Uncheck the *routecheck* tick 
    In Advance options we will be giving Labels for identification as defined in the doc
    Finally click on create

Everythig you will find in the above link in a detailed as a summary i have written for my understanding 
