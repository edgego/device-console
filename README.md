# edge-console
Edge admin console

Install steps:

1. install rancher local-path storage class for kubernetes:
   kubectl apply -f https://github.com/rancher/local-path-provisioner/blob/master/deploy/provisioner.yaml
2. install edge console :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/edge-localpath.yaml
3. install monitor module :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/monitoring.yml
4. install contour
   kubectl apply -f https://projectcontour.io/quickstart/contour.yaml  
5.config contour ingress:
  kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/ingress.yml
  
 Device geograpy dashboard 
  <img width="1894" alt="地理" src="https://user-images.githubusercontent.com/80612608/137683025-6dd89a46-660b-4b7e-874c-0e44f3cccd1e.png">
  
  Monitor autoevent:
  
  ![image](https://user-images.githubusercontent.com/80612608/137683450-26833a9a-7d88-446e-b0a0-6df5b400171c.png)

 Profile  Dashboard:
 
 <img width="1896" alt="profile" src="https://user-images.githubusercontent.com/80612608/137683546-8b37597b-6f1b-424c-9000-9c4b50e6e986.png">
 
 Device service dashboard:
 
 <img width="1883" alt="deviceservice" src="https://user-images.githubusercontent.com/80612608/137684000-dc0af605-7d0a-4013-b270-acb01906b3db.png">


  App service management:
![image](https://user-images.githubusercontent.com/80612608/137682898-3cd91b4f-8882-4b70-978f-8b898809a8c6.png)
