# Deploying an application in Kubernetes manually

## Creating a Kubernetes Cluster

### Setup KinD
Ensure KinD is installed on your machine. Follow the [website instructions](https://kind.sigs.k8s.io/docs/user/quick-start/) for your OS.

#### Deploy a cluster using KinD
```shell
$ kind create cluster --name bsides --config kind.yaml
```

#### Deploy ingress nginx controller
```shell
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml

$ kubectl wait --namespace ingress-nginx \
  --for=condition=ready pod \
  --selector=app.kubernetes.io/component=controller \
  --timeout=90s
```

## Let's deploying the WeatherApp

```shell
$ kubectl apply -f weatherapp/k8s/
```

```shell
$ kubectl wait --namespace default \
    --for=condition=ready pod \
    --selector=app=weatherapp \
    --timeout=90s
```