# Building a CI/CD Pipeline with Tekton

## Installing Tekton Pipelines
```shell
$ kubectl apply --filename \
    https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

## Monitor installation
```shell
$ kubectl get pods --namespace tekton-pipelines --watch
```

## Install Tekton Triggers
```shell
$ kubectl apply -f \
    https://storage.googleapis.com/tekton-releases/triggers/latest/release.yaml
$ kubectl apply -f \
    https://storage.googleapis.com/tekton-releases/triggers/latest/interceptors.yaml
```

## Post message to event listener

```shell
$ curl --header "Content-Type: application/json" --request POST --data '{"username": "ar4mirez"}' http://localhost:63971/
```