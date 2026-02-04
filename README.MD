# container Orchestrator :
--------------------------
* kubernetes : k8  --PAAS
 -----------------

 Auto scaling is easy, storage is outside of cluster, roll back and multiple deployment strategies are available in kubernetes. 
 Networking betweem containers is little easy in kubernetes

 # cluster:
 ================= 

terms:

* control plane
* worker nodes 

* data is not stored in clusters , stored outside of cluster ( volumes)
* we can configure n number of nodes 

  * A single master and mutliple nodes 

* Here we are writing manifest files 

* using terraform we can create culster 
* To interact with cluster using kubectl 

# Workstation:
 -----------

 1. install docker 
 2. Run aws configure 
 3. install eksctl for cluster creation ( we have mini kube , if it install system will slow)
 4. install kubectl for cluster intercation 

===================================================================================================================

*  Install eksctl and kubectl :
 ---------------------------

 aws configure
 ARCH=amd64
 PLATFORM=$(uname -s)_$ARCH
 curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"
 curl -sL "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_checksums.txt" | grep $PLATFORM | sha256sum --check
 tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz
 sudo install -m 0755 /tmp/eksctl /usr/local/bin && rm /tmp/eksctl
 eksctl version
 curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.34.2/2025-11-13/bin/linux/amd64/kubectl
 chmod +x ./kubectl
 sudo mv kubectl /usr/local/bin/kubectl
 kubectl version

=======================================================================================================================

# How to create a cluster :
-----------------------------

eksctl create cluster --config-file=eks.yaml 

* kubectl get nodes -- shows the worker nodes
* everything is called resources in kubernetes 












# ManageNode Group:
-----------------
No need to login aws instances and install , managenode component will take care everything 






# spot instances:
  --------------

on-demand -- whenever you required  you create instances , aws gaurntees you  to get instances 

spot -- aws data center have lot of resources 
 give for less cost 70-90 % discount --

# namespace:
  -------------

  * Isolated project space in kubernetes where you can create your workloads


syntax:
    apiVersion: v1  -- 
    kind: Namespace
    metadata:
      name: devlopment
      labels:
        project: roboshop
        environment: dev 