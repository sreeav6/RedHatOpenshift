# Here we will see how to connect to the container using remote shell session

1. OpenShift basically helps in establishing the remote shell session to the container with out run an ssh service inside each and every container.
2. In order to conncet to container use the below commands

   First get the pods using oc get pods command

       oc get pods
![image](https://github.com/user-attachments/assets/654927a1-8847-4441-9f89-a7a8fa838f94)

   Now you can establish a remote shell session into the pod by using the pod name:

      oc rsh (podname)
![image](https://github.com/user-attachments/assets/5b5e1a99-25d7-42c3-8ce7-78b215ec1ec5)

3. If you want to remote shell connection to the container using openshift web console
      Just click on the Topology view and click on the icon which will open the side details in the right side where we need to select the *Resources* one         and then click on the Pod name under Pods section which will navigate to the page where you can click on Terminal directly and you can able to enter         in to the container.
4. Now we will see few commands to execute remotely in a running container.

    To execute the command the desired command is present in the correct executable path.

    oc exec --help (Which will help to see and execute as per requirements)

    Here we want to see the application jar file in the container

       oc exec (pod name) -- ls -l /parksmap.jar
![image](https://github.com/user-attachments/assets/e0baaa35-0d5a-44ed-9a31-cf0cceb5b775)

    In order to check all the files under root (/) we can use oc rsh command as well
    
       oc rsh (pod name) ls -l /
![image](https://github.com/user-attachments/assets/2a1d8882-6b9e-48da-bcdd-866a1bf40101)

    oc rsh (pod name) whoami { you can experiment this }




    

      
