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

# Examining the pod

Finally if you want to know the details once it is deployed click on the runtime icon in the right side you will be seen the details of the pod.
<img width="966" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/ec3206ff-f8a9-4c5e-a9bf-5262245ba90e">

There is another way to check your pod swtich your account from Developer to Administrator and once you are in Administrator
in the left pane click on the workloads under select pods.
<img width="953" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/67c96bdf-afce-4051-9de4-17785c98e678">

Infact you can open terminal in the openshift only and examine the pods by running the below commands.
            oc get pods
<img width="955" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/443627f2-f3d4-41d7-ac62-86ac6bf05a5f">
If you want to examine even more you can check with the below command
            oc get pod (podname) -o yaml
If you want to check all the details,Metrics, YAML, Environment, Logs, Events, Terminal.  You can click on the pod name which will open with all theses details you can check one by one of these ones.

# Exaplained about the services as well in the mentioned doc please refer that how services play a important role.

    > The service maps to a set of pods is via system of Labels and Selectors
    > Services are assigned to a fixed IP address and many ports and porotocols can be mapped
    > Services receives a unique IP address upon creation, Service IPs are fixed and never change for the life of service
    > To view service  < oc get services >
    > Labels are just key/value pairs. Any Pod in this Project that has a Label that matches the Selector will be associated 
      with the Service. 
    > To see in detail oc describe service ( service name )
    


