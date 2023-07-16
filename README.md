# Edge Device Console Over Kubernetes

 Edge Device Console is designed for industry edge cloud , a small and low cost tool easy to  manager industry edge devices.  Edge Device Dashboard can run on different platform(x86-amd64, arm,arm64), support winows, linux ,Mac OS.

## Key Features

- Cross platform, Edge Device Dashboard  can create edge cloud on amd64,arm64,arm device. 
- Edge Device Dashboard  support english and simple chinese language, according to browswer's language setting.
- Low cost,low carbon, small memory size(500Mi or above) and hard disk size.
- Simplify operations by UI dashboard.

## System module
  - device metadate, include device profile,device service, devices
  - scheduler
  - notification
  - rule engine
  - app service
  - dashboard

Install steps:

1. Setup kubernetes cluster,How to setup cluster refer https://kubernetes.io/docs/setup/, or download ecm to setup kubernetes cluster from https://github.com/edgego/ecm, ecm is more convenient to install kubernetes cluster.
2. install rancher local-path storage class for kubernetes https://kubernetes.io/docs/setup/
   kubectl apply -f https://github.com/rancher/local-path-provisioner/blob/master/deploy/provisioner.yaml
3. install edge console :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/edge-system-redis-localpath.yaml
4. install monitor module :
   kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/monitoring.yml
5. install contour
   kubectl apply -f https://projectcontour.io/quickstart/contour.yaml  
6. config contour ingress:
  kubectl apply -f https://github.com/edgego/edge-console/blob/main/scripts/ingress.yml

Alternative simple way to install:

1. download ecm from https://github.com/edgego/ecm/releases/tag/V1.1.0
2. get ssh key with command: ssh-keygen -t rsa 
3. Run with command line:
  create edge cloud:
     ecm_win-amd64.exe  -d create \
     --region edge cloud location \
     --cluster \
     --enable dashboard edge-redis\
     --name demo-test \
     --ssh-user root \
     --ssh-password ****** \
     --ssh-port 22 \
     --master-ips 192.168.1.151
     
     or 
     
     Run with ui:  ecm -d serve --bind-port 8080
     
     <img width="1152" alt="ddd1" src="https://user-images.githubusercontent.com/80612608/187816142-38e4f8df-e849-492e-9504-99b64bca8c9b.png">

 Device dashbaord Overview
     Edge device console easily manage all devices' metadata : profiles, device services , devices, application services. Online deploy and undeploy device services and application services.
  From device dashboard also check all devices' operating state and admin state.

   ![image](https://github.com/edgego/device-console/assets/80612608/217f48f7-33f5-4be8-950b-77a77801cf4e)
        
 From dashboard, all devices with satellite location can be found from the map. 
 
     -  Query device with name 
     -  Check device status by different color
     -  Check all autoevents throughput , or individual autoevent
    
 Monitor device's autoevent:
  
  ![image](https://github.com/edgego/device-console/assets/80612608/b90250f7-133b-4614-a775-85a116930bca)


  Deploy or undeploy device service online
  
 ![image](https://github.com/edgego/device-console/assets/80612608/4576c480-310a-479c-8774-e0e403d934c6)


Device center provide functions such as add device , delete device . update device , bulk import devcices ,test device and monitor device.

![image](https://github.com/edgego/device-console/assets/80612608/e0e26df3-742a-4235-9120-a05fa3bcc962)


Operate data streams  easily

![image](https://github.com/edgego/device-console/assets/80612608/aa9cd148-9bec-4559-939b-b5635ff9a632)

Define or update rule 

<img width="1870" alt="image" src="https://github.com/edgego/device-console/assets/80612608/f9fb5820-807c-4436-afda-5cd337f688b3">

App Service dashboard provide function to operate data with buildin functions and export data via http or mqtt.
![image](https://github.com/edgego/device-console/assets/80612608/395a051a-4220-4029-8028-7862032c833d)


