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


