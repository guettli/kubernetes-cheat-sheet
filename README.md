# My Kubernetes Cheat Sheet

## Terminology

[Pod](https://kubernetes.io/docs/concepts/workloads/pods/): A Pod is a group of one or more containers, with shared storage/network resources,

[Node](https://kubernetes.io/docs/concepts/architecture/nodes/): Kubernetes runs your workload by placing containers into Pods to run on Nodes. A node may be a virtual or physical machine.

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

# Central Repo for. It contains most well known tools
helm repo add stable https://kubernetes-charts.storage.googleapis.com/

# Read requirements.yaml, downloads dependencies and stores them in the "charts" directory.
helm dependency update

helm install . --generate-name

```

