# Here we will see about Route in Openshift
The Service resource provides internal abstraction and load balancing in openshift environment, if any of the clients (such as users,systems,devices e.t.c)needs to access the application which is outside of the openshift,here openshift uses the concept of routing layer and the data object behind that is **ROUTE** 

By default openshift router(HAProxy) uses HTTP header of the incoming request to determine where to proxy the connection. 
You can optionally define the security such as TLS, for the ROUTE. If you want your **Services** and **Pods** needs to be accessed outside of the openshift you need to create a ROUTE.

# Let's Exexrcise the ROUTE In Openshift
Here you can create route in the openshift web console while creating deployment itself, here we are exercising the ROUTE using terminal.

# First let's examine whether route exists or not by using the below command
        
        oc get route
        
# Secondly we will creating the route by taking service name
        
        oc get svc (here you copy the Name of the Service)
        
# Finally we will be creating the Route
        
        oc create route edge <name of the route(any name)> <service name>
                
oc create route edge parkmap --service=parksmap
        
# Now we need to verify the route by using the below command
        
        oc get route

![image](https://github.com/sreeav6/RedHatOpenshift/assets/139438620/cdef3d09-5393-4232-a8a7-0fcbdda5d223)


You can also verify in the openshift web console as well by clicking pod-->Resources at the bottom you will find the Route by clicking on it you will be able to access your application.


        

