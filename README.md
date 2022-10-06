# kubernetes exercise

[TOC]



## Introduction

This repository is to collate and investigate [Kubernetes](https://kubernetes.io/), to get familiar with the API, to investigate alternatives for generating [Cloud Foundry](https://www.cloudfoundry.org/) projects into the K8s platform, or some other alternative, like AWS copilot.

![Image result for k8s](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTOMHGXegGxDtiO50L0c7JZyAW9O3AK8Mbl0vBu_W279Q&s)

Kubernetes (also known as k8s or “kube”) is **an open source container orchestration platform that automates many of the manual processes involved in deploying, managing, and scaling containerized applications**. Get an introduction to enterprise Kubernetes.

## Why Kubernetes?

There’s a revolution going on. Actually, three revolutions: 

1. The first revolution is the creation of the **cloud**. 
2. The second is the dawn of **DevOps**. 
3. The third revolution is the coming of **containers**. 

Together, these three waves of change are creating a new software world: the cloud native world. The operating system for this world is called ***Kubernetes***.

Kubernets supports:

1. Automated rollouts and rollbacks
2. Service discovery and load balancing
3. Storage orchestration
4. Secret and configuration management
5. Automatic bin packing
6. Batch execution
7. IPv4/IPv6 dual-stack
8. Horizontal scaling
9. Self-healing
10. Designed for extensibility

**Popularity** is a good choice for developers as they like learning stuff that will be marketable and reward time spent.

![Which orchestrator are you using in production?](./images/popular-choice.png)

**Business people** like a reduction in costs, and so if this has the potential to be cheaper and more reliable, it will be easier to convince adding this to the radar.

![image-20221006235731359](./images/cost-fact.png)

## Getting started

- Install kubectl
  - [Linux](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux)
  - [macOS](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos)
  - [Windows](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows)
- Install [**Minikube**](https://minikube.sigs.k8s.io/docs/start/) if you want to run this locally and play for free

![Minikube](./images/minikube-start.png)

```bash
# Mac OS e.g.
brew install kubernetes-cli
# Learn locally
alias kubectl="minikube kubectl --"
brew install minikube
minikube start
# Deploy applications
kubectl create deployment hello-minikube --image=docker.io/nginx:1.23
kubectl expose deployment hello-minikube --type=NodePort --port=80
# Show dashboard and see below for output
minikube dashboard
```

![image-20221007091228205](./images/minikube-dashboard.png)

![image-20221007091403227](./images/hello-minikube.png)

Get the service by `minikube service hello-minikube`

![Run the service through minikube](./images/minikube-service.png)

![Nginx service](./images/nginx.png)

# References

- https://blog.thewiz.net/understanding-kubernetes-developers-guide
