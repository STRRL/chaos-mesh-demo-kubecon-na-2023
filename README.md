# Chaos Mesh Demo on KubeCOn NA 2023

This repo contains manifests which used on Chaos Mesh demo on KubeCon NA 2023.

Video: https://www.youtube.com/watch?v=j57F-c8zIuc

## Setup Kubernetes Cluster

Start minikube cluster

```bash
minikube start
```

Enable Kuberenetes Dashboard and Metrics Server

```bash
minikube addons enable dashboard
minikube addons enable metrics-server
```

Install Potato Head(https://github.com/podtato-head/podtato-head) as demo application

```bash
kubectl apply -f https://raw.githubusercontent.com/cncf/podtato-head/main/delivery/kubectl/manifest.yaml
```

Install Chaos Mesh

```bash
helm repo add chaos-mesh https://charts.chaos-mesh.org
helm install chaos-mesh chaos-mesh/chaos-mesh -n chaos-mesh --create-namespace
```

## Examples

### PodChaos pod-failure

### NetworkChaos network delay

### HTTPChaos replace http response
