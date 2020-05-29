---
id: installing_k8s
title: Installing kubernetes using kubeadm
---


Step1: Install Docker

```
cat <<EOF > install-docker.sh
sudo apt-get update
sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
sudo apt-get update
sudo apt-get install -y docker-ce 
EOF
bash install-docker.sh

```

Step2: install kubelet kubeadm 
```
cat<<EOF > install-kubeadm.sh
sudo apt-get update && apt-get install -y apt-transport-https curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo echo  "deb https://apt.kubernetes.io/ kubernetes-xenial main" > /etc/apt/sources.list.d/kubernetes.list 
sudo apt-get update
sudo apt-get install -y kubelet kubeadm kubectl
sudo apt-mark hold kubelet kubeadm kubectl
EOF
sudo bash install-kubeadm.sh

```

Step3: Initilization
```
kubeadm init --pod-network-cidr 192.168.0.0/16 --apiserver-cert-extra-sans 3.234.215.25,madhu.com

```

To start using your cluster, you need to run the following as a regular user:
```
  mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config

```

Step4: Install calico for networking

```
kubectl apply -f https://docs.projectcalico.org/v3.14/manifests/calico.yaml

```

Step5: Joining nodes
Follow step1 and step2 and use kubeadm join command

ref: https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/
