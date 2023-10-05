# Setup Workstation

## Docker
Ensure Docker is installed on your machine. You can donwload and install Docker from it's [official website.](https://docs.docker.com/desktop/?_gl=1*k6dyed*_ga*MTc3OTY4ODk5MS4xNjkyMTIwNjM5*_ga_XJWPQMJYHQ*MTY5NjQ3NDg4Ni4xNS4xLjE2OTY0NzQ5MDQuNDIuMC4w)

## Kubectl
`kubectl` is the command-line tool for interacting with Kubernetes clusters. Install it using one of the following methods based on your OS:

### For Windows:
````shell
$ choco install kubernetes-cli
````

### For Mac (using Homebrew)
```shell
$ brew install kubectl
```

### For Linux (using package manager):

#### For Debia/Ubuntu
```shell
$ sudo apt-get update && sudo apt-get install -y kubectl
```

#### For CentOS/RHEL:
```shell
$ sudo yum install -y kubectl
```