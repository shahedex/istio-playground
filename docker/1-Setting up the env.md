# Install istio and its dependencies for docker

## Add current user to docker group

```bash
$ sudo usermod -aG docker user_x
```

## Install docker-compose and make it executable

```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
```

## Pre-configure kubectl for pilot

```bash
$ kubectl config set-context istio --cluster=istio
$ kubectl config set-cluster istio --server=http://localhost:8080
$ kubectl config use-context istio
```

## Create a DOCKER_GATEWAY environment variable

```bash
$ export DOCKER_GATEWAY=172.28.0.1:
```
