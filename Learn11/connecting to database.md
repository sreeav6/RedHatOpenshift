Here we will work with Database
-----
1) Usually our nationalparks application(backend) has to store location information to this we require database to store the data so we will using MongoDb here.
2) We will make nationalparks application(backend) as a map visualization tool so that parkamap application (frontend) will discovery automatically using openshift discovery mechanism. So that the map will be displayed accordingly.
3) You can get visualization of both 1 and 2 points in the below image.
![image](https://github.com/user-attachments/assets/2c60b16b-4ed8-47af-9f36-ce49807f0fa1)
                    **Image Source: RedHat OpenShift**

Here we will see about Background Storage
-----
1) Most useful applications are "stateful" or "dynamic" in some way, and this is usually achieved with a database or other data storage.
2) In this lab we are going to add MongoDB to our nationalparks application and then rewire it to talk to the database using environment variables via a secret.

Exercise: Deploy MongoDB
-----
1) First we need to create four key/value pairs which are called secrets in kubernetes which are used to store the database related configuration and credentials before deploy of mongodb.
2) In the Developer perspective, choose Secrets in the left navigation menu, then click the Create button in the upper right and select Key/value secret.Like below image.
![image](https://github.com/user-attachments/assets/a561f79a-fb75-445f-b20f-ccb2ded2505d)

3) In the dialog, fill in the entries shown below, by adding four key/value pairs in total.

Secret Name → mongodb-credentials

key: admin-usr | value: admin

key: admin-pwd | value: secret

key: app-usr | value: parksapp

key: app-pwd | value: keepsafe

![image](https://github.com/user-attachments/assets/44009b04-c798-4324-9326-599b19ace71a)



   
