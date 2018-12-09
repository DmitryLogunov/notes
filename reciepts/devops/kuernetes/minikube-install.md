## Links

 - https://kubernetes.io/docs/setup/minikube/
 - https://habr.com/company/flant/blog/333470/

## Steps

### Install  VirtualBox

 - Check the system support VM:

```
  cat /proc/cpuinfo | grep 'vmx\|svm'

```    
 
The output should not be empty

 - Install VirtualBox 

  https://pro-gram.ru/install-virtualbox-ubuntu.html

### Install Kubectl

```
  sudo apt-get update && sudo apt-get install -y apt-transport-https
  curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
  echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
  sudo apt-get update
  sudo apt-get install -y kubectl

```

### Install Minikube

 - Download & setup

```
  curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.30.0/minikube-linux-amd64 && chmod +x minikube && sudo cp minikube /usr/local/bin/ && rm minikube

```

 -  Start
 
 ```
  minikube start

 ```
  
  At the first run it will be downloaded ISO image of minikube and minikube will be configurated


### Check installation  

 - Output of 'minikube start' command:

```
  Starting local Kubernetes v1.10.0 cluster...
  Starting VM...
  Getting VM IP address...
  Moving files into cluster...
  Setting up certs...
  Connecting to cluster...
  Setting up kubeconfig...
  Starting cluster components...
  Kubectl is now configured to use the cluster.
  Loading cached images from config file.

``` 
 - Check kubectl version

 ```
  
  kubectl version

 ```  

 - Check kubernetes nodes and pods

```
  kubectl get nodes

  kubectl get pods --all-namespaces
   
```

