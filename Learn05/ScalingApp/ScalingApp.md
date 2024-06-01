# Here we will learn a bit about Deployments and ReplicaSets

1) ReplicaSet: It ensures the desired number of pods are running or not, if the pod got killed there is some thing which 
   needs to be started automatically this is where (RS) plays a key role.
2) Service: It basically used for routing and loadbalancing for pods.
3) Deployments: ReplicaSets are being controlled by deployments
4) In Openshift we have ReplicaSet and ReplicaContoller where (RS) is controlled by Deployment and (RC) is controlled by Depolyment configs
5) In Kubernetes (D) defines deployment how something should be deployed. In almost all cases you will have Service, Pod, Deployment and ReplicaSet in place where openshift will create for you.

# Here we will exercise the Deployment and Scaling our APP in Developer Sandbox

   we will be using the below commands in the terminal to get Deployment(D) and ReplicaSet(RS)
  
   # To get deployment
   		oc get deployment 
   # To get ReplicaSet
      	oc get rs
        
<img width="590" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/db5759b0-483e-4143-b9ce-8fb84e9a1582">
<img width="557" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/c4d1f72e-4106-4d14-8b97-60b470b2b71b">

# Now we will scale our app
 		oc scale --replicas=2 deployment/parksmap
![image](https://github.com/sreeav6/RedHatOpenshift/assets/139438620/b99f5364-5e29-4461-a8c8-e81ea1dcbbe0)
# Now obeserve the ReplicaSet(RS) 
 		oc get rs
![image](https://github.com/sreeav6/RedHatOpenshift/assets/139438620/151cbc6c-bf6f-4d19-82f4-4b028ffb9b0a)
# Now observe the pods
   		oc get pods
![image](https://github.com/sreeav6/RedHatOpenshift/assets/139438620/1d985979-501b-4c21-b4a9-ef71bd3192af)
# Now examine the service by describing
	oc describe svc (svc-name)
 <img width="438" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/166f660b-9bac-472d-b4d1-104b539c6692">
 
# Now in the service Enpoints we will get where openshift will automatically maps endpoints to the service
   oc get endpoints (svc-name)
   
<img width="430" alt="image" src="https://github.com/sreeav6/RedHatOpenshift/assets/139438620/e67678fe-f365-4b52-9746-031e7dc30d94">

   




