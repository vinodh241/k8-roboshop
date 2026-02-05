# create a roboshop project with Kubernetes
=============================================

1. build the image

2. configure the image 

# K8's:
=======

1. create a namespace 
2. 

# mongodb:
==========
* create a deployment instead of pod 
* it will communicate other microservices so creating service and cluster IP 

* kubens roboshop   -- to activate custom roboshop 

# Install below commands:
-------------------------
* to activate the custom namespaces instead of default one 

kubens
https://github.com/ahmetb/kubectx

git clone https://github.com/ahmetb/kubectx /opt/kubectx
sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens

k9s
curl -sS https://webinstall.dev/k9s | bash

* take duplicate session and type k9s 
it will give a UI 

shift + ;  press 

* then see the options need to enter below commands everytime 


===
OR 
===

* you can set alias like AB="vinodh"

* alias ka="kubectl apply -f <manifest.yaml>"
* alias ks="kubectl get services"
* alias kp="kubectl get pods"

if you set alias no need to enter full command everytime just enter ka or kp as per above 



================================================================================