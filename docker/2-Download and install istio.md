# Download and install istio

## Download Istio and unpack it

```bash
$ wget https://github.com/istio/istio/releases/download/1.0.6/istio-1.0.6-linux.tar.gz
$ tar -xvf istio-1.0.6-linux.tar.gz
```

## Bring up istio's control plane

```bash
$ docker-compose -f ./istio-1.0.6/install/consul/istio.yaml up -d
```
If pilot hasn't started yet, run the istio.yaml file again.
