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

 
  Device service dashboard
  
  
<img width="1876" alt="a" src="https://user-images.githubusercontent.com/80612608/185780924-8af19103-fce1-4b2b-9514-f517d80123b5.png">
