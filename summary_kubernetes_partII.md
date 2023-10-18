# Summary of CCOE Sharing Session 2 - Kubernetes Part 2

## Table of Contents

1. Differences between Containerization and Virtualizations
2. What is Kubernetes?
3. Kubernetes Cluster
4. What is Pods?
5. Replica Sets


### Differences between Containerization and Virtualization

Application can be deployed using a container or virtual machine. So, let's define the similarities and differences about containerization and virtualization!

The architecture:
![Containerization vs Virtualization](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/bltb6200bc085503718/5e1f209a63d1b6503160c6d5/containers-vs-virtual-machines.jpg)

**Similarities:**
Both containerization and virtualization can be used to deploying application, and they both isolated from the underlying hardware.

**Differences**
- Containerization (ex: Docker)
    + Every application that deployed inside the container is isolated BUT sharing the same kernel as other container on the same host.
    + Can be used to deploy microservices application.
    + Abstraction of application layer.
- Virtualization:
    + Everything running inside the Virtual Machine is independent of the host operating systems or hypervisor.
    + Every application in VM can be hosted in difference OS.
    + Simulation of the hardware level.

### What is Kubernetes?

- Kubernetes a.k.a k8s or "kube" is an open source container orchestration platform that automates many of the manual processes involved in deploying, managing, and scaling containerized applications.
[What is Kubernetes - Red Hat](https://www.redhat.com/en/topics/containers/what-is-kubernetes)


### What is Pods?

Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.

Assume that our web apps have been deployed in Docker, each pod is an instance of an application.

![Cluster](https://matthewpalmer.net/kubernetes-app-developer/articles/networking-overview.png)

Each cluster can have many node, and each node can have many pods. Here's the breakdown of the terminology:
1. Cluster: A Kubernetes cluster is a set of nodes that run containerized applications. It includes a control plane (usually one or more master nodes) and one or more worker nodes.
2. Node: A node, a.k.a a worker node or minion, is an individual machine within the cluster. Nodes are responsible for running containers and pods.
3. Pod: A pod is the smallest depoyable unit in Kubernetes. It can contain one or more containers that share the same network namespace, storage, and some other resources. Pods are scheduled to run on nodes in the cluster.

