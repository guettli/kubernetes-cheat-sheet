# My Kubernetes Cheat Sheet

## Terminology

Ephemeral Container: A Container type that you can temporarily run inside a Pod. Custom (your) code usualy runs in ephemeral (stateless) containers.

Helm: The package manager for Kubernetes

Helm Chart: A package (like rpm/dpkg/msi)

Minikube: A tool for running Kubernetes locally.

[Node](https://kubernetes.io/docs/concepts/architecture/nodes/): Kubernetes runs your workload by placing containers into Pods to run on Nodes. A node may be a virtual or physical machine.

[Pod](https://kubernetes.io/docs/concepts/workloads/pods/): A Pod is a group of one or more containers, with shared storage/network resources,

Volume: A directory containing data, accessible to the containers in a Pod.


## Minikube

```
# This is a lightweight testing environment. No VM needed
minikube start --driver=docker

# Nice web based GUI
minikube dashboard

```

## kubectl

```
kubectl get pods

kubectl describe jobs

kubectl describe job JOB-ID

kubectl logs POD-ID

kubectl describe pod POD-ID

```

## Helm


```
# Central Repo. It contains most well known tools
helm repo add stable https://kubernetes-charts.storage.googleapis.com/

# Read requirements.yaml, downloads dependencies and stores them in the "charts" directory.
helm dependency update

helm install . --generate-name

```

