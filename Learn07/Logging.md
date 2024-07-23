# Here we will be seeing about Logging.

Openshift porvides a better visibility of application logs where we can view the pod logs directly from the console or from the command line. 

# Background container Logs

Openshift is constructed in a such a way that it expects all containers to log all information to STDOUT. In this way both regualr and error messages are captured via standardized docker mechanism. 

While you are exploring the Pod's logs you are going through the docker deamon to access the container logs, through openshifts API.

NOTE: Openshift is not against any other logging process, In some cases application will not send logs to STDOUT and it might be sending to various external systems.It might writes to various log information to various files. 

# Examining Logs

Once after you deploy the pod and once the pod is up and running. In the Developer Perspective, from Topology view, click the parksmap entry and then the Resources tab. You should see a View Logs link next to the Pod entry.

# We can audit logs from the command line too

In the openshift web console we have command line option as well there check with the below commands.

          oc get pods

  ![image](https://github.com/user-attachments/assets/ef78ddc8-9b60-49f3-b90c-18947726709d)

          oc logs (pod name)

  ![image](https://github.com/user-attachments/assets/3a81b858-097b-48ee-8fb4-68a8d971d530)

  


