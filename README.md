# Edge Device Console Over Kubernetes
Edge Device admin console

Install steps:

1. Setup kubernetes cluster,How to setup cluster refer https://kubernetes.io/docs/setup/
2. install rancher local-path storage class for kubernetes https://kubernetes.io/docs/setup/
   kubectl apply -f https://github.com/rancher/local-path-provisioner/blob/master/deploy/provisioner.yaml
3. install edge console :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/edge-localpath.yaml
4. install monitor module :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/monitoring.yml
5. install contour
   kubectl apply -f https://projectcontour.io/quickstart/contour.yaml  
6. config contour ingress:
  kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/ingress.yml
7. import autoevent(autoevent.json) and command(command.json) dashboard from dir scripts to grafana.
  
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
     
    ![image](https://user-images.githubusercontent.com/80612608/185780795-097dde5c-8ef1-4200-92a1-3e0a640606e8.png)

 Device Dashboard:
     
     a. Query ,Create ,Update, Delete device
     b. Create , Delete ,Monitor Autoevent
     c. Define device protocol
     d. Monitor command
 
