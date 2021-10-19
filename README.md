# EdgeDevice-Console Over Kubernetes
EdgeDevice admin console

Install steps:

1. install rancher local-path storage class for kubernetes:
   kubectl apply -f https://github.com/rancher/local-path-provisioner/blob/master/deploy/provisioner.yaml
2. install edge console :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/edge-localpath.yaml
3. install monitor module :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/monitoring.yml
4. install contour
   kubectl apply -f https://projectcontour.io/quickstart/contour.yaml  
5. config contour ingress:
  kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/ingress.yml
  
 Device geography map, all devices with satellite location can be found from the map. 
 
     a. Query device with name 
     b. Check device status by different color
     c. Check all autoevents throughput , or individual autoevent
    
  <img width="1894" alt="地理" src="https://user-images.githubusercontent.com/80612608/137683025-6dd89a46-660b-4b7e-874c-0e44f3cccd1e.png">
  
  Monitor autoevent:
  
  ![image](https://user-images.githubusercontent.com/80612608/137683450-26833a9a-7d88-446e-b0a0-6df5b400171c.png)

 Profile Manager: 
 
    a. Create ,delete ,update profile
    b. Check profile's resources ,device commands, and associated devcices
 
 <img width="1896" alt="profile" src="https://user-images.githubusercontent.com/80612608/137683546-8b37597b-6f1b-424c-9000-9c4b50e6e986.png">
 
 Device service :
 
     a. Check assocaited devices
     b. Bulk import and delete devices
     c. Supply dowanload and print function
 
 <img width="1883" alt="deviceservice" src="https://user-images.githubusercontent.com/80612608/137684000-dc0af605-7d0a-4013-b270-acb01906b3db.png">
 
 Device Dashboard:
 
 <img width="1901" alt="autoevent" src="https://user-images.githubusercontent.com/80612608/137684129-2f06f367-f9a4-417d-ba3a-d9a44f074a66.png">
 <img width="1890" alt="comamndmetrics" src="https://user-images.githubusercontent.com/80612608/137684153-29e96c89-1909-41f1-a27e-8a0c42de3eda.png">
 
 Scheduer Manager:
 <img width="1274" alt="scheduler" src="https://user-images.githubusercontent.com/80612608/137684768-63ac698a-2583-4049-8e57-96a902ab1b57.png">
 
 Rule Manager:
 
 <img width="1885" alt="rule" src="https://user-images.githubusercontent.com/80612608/137684819-e00cceb9-5d59-4624-8811-a95798d62e56.png">


  App service management:
![image](https://user-images.githubusercontent.com/80612608/137682898-3cd91b4f-8882-4b70-978f-8b898809a8c6.png)
