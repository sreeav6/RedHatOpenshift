# Here we will learn to deploy Source to Image in OpenShift
In the previous labs we have learned that deploying pre exisiting image image. Now we will see how openshift builds container images using source code from existing repository. We will use Source to Image Project.

Source 2 Image is tool for building reproducible containers.
Note the whole is available in the reference link which I had shared in the begining and refer section called: National Parks Backend APP

OpenShift runs S2I process inside a special pod called a build pod and thus builds are subject to quotas, limits, resource scheduling and other ascepts of openshift

A full article of S2I is in this link: **https://docs.openshift.com/container-platform/4.11/openshift_images/create-images.html**

# Now we are exercising creating a backend application called National Parks Map

We are going to deploy the backend service using Python that will expose 2 main rest endpoints to visualizer application.The application will query for national parks information (including its coordinates) that is stored in a MongoDB database. This application will also provide an external access point, so that the API provided can be directly used by the end user.

The national parksmap which is backend to serve the data where frontend app will consume here we will use application code on Git server and we will be using the openshift web console to deploy this. OpenShift can work with any accessible Git repository. 

# Let's build it

In the Developer Perspective, click +Add in the left navigation, go to the Git Repository section and then choose From Git option.

The Import from Git workflow will guide you through the process of deploying your app based on a few selections.

Input this repo **https://github.com/openshift-roadshow/nationalparks-py.git**

OpenShift is intelligent enough to guess the code and you will now be asked to select an import strategy click on it.

<img width="833" alt="image" src="https://github.com/user-attachments/assets/064767f8-c2c7-4d00-b33a-9216563b6434">

You will be prompted with three options select Builder Image, After that u will be see the python builder image is automatically selected 

You need to input some fields as per this below doc

**https://redhat-scholars.github.io/openshift-starter-guides/rhs-openshift-starter-guides/4.11/nationalparks.html**

After inputing all fields click create and monitor the Builds where you can click Build Option in the left side 

<img width="956" alt="image" src="https://github.com/user-attachments/assets/36ffd6c8-6e93-41d4-982f-e1f5958ca33d">

Even you can see in the command line as well by typing this command known as (oc get builds)

![image](https://github.com/user-attachments/assets/f975fd63-7c15-46ab-a1db-ffaca952b0ed)

Even you can monitor the logs of this build like (oc logs -f build/{build-name})
I have just took only few lines of logs in the below screen shot

![image](https://github.com/user-attachments/assets/9b152199-8a1c-4b87-b4f6-0bfc09429c02)

After the build has completed and successfully:

The S2I process will push the resulting image to the internal OpenShift registry

The Deployment (D) will detect that the image has changed, and this will cause a new deployment to happen.

A ReplicaSet (RS) will be spawned for this new deployment.

The RS will detect no Pods are running and will cause one to be deployed, as our default replica count is just 1.

In the end, when issuing the oc get pods command, you will see that the build Pod has finished (exited) and that an application Pod is in a ready and running state

![image](https://github.com/user-attachments/assets/9273c503-a1c0-417e-9bea-eb58cd7269b0)

Even while creating the application we have created the route as well ( oc get route) this command will give the route, by accessing this route you will get some info

![image](https://github.com/user-attachments/assets/b60f4b84-095d-4032-befe-90993c685f5d)

Since this is a backend application it will not have web interface but can be used 















