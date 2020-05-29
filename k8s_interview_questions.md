---
id: k8s_questions
title: kubernetes Interview k8s_questions
---

1. What is kubernetes?
* Kubernetes is container orchestration tool used to manage containers 

2. What is the diffrence between docker and kubernetes?
* Docker is used for building docker images and creating containers whereas kubenetes is used to manage containers

3. Tell three Similar softwares like kubernetes?
* Docker swarm
* Mesos
* DC/OS

4. What is the diffrence between kubernetes and docker swarm?
* Both are used for managing containers
* Docker swarm is not production ready
* Kubernetes is modular, flexibile and production ready

5. What is the difference between automation and orchestration?
* Automation is used for single task
* Orchestration is used for build a workflow

6. Explain kubernetes architecture
* Master
 *  kube-api server
 * scheduler
 * controler-manager
 * etcd
* Node
 * kubelet
 * kube-proxy
 * Container runtime (docker)

7. Image vs Container
* Docker image is a template which contains base os and application services and data
* Docker container is a copy of docker image with resources like cpu, memory, network and storage

6. Docker swarm vs docker compose?

7. Difference between bridge and overlay network

8. What is the difference between container and a vm

