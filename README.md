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
  
![image](https://user-images.githubusercontent.com/80612608/137682898-3cd91b4f-8882-4b70-978f-8b898809a8c6.png)
