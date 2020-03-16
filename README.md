# Kustomization for Installing Docker Registry on OpenShift

This repository contains kustomization for installing [Docker Registry](https://github.com/docker/distribution) on OpenShift using the official [Distribution](https://github.com/docker/distribution-library-image/tree/0b6ea3ba50b65563600a717f07db4cfa6f18f957) container image.

To deploy Docker Registry on OpenShift:

```
$ oc apply --kustomize docker-registry/base
```

Obtain the registry host name:

```
$ oc get route docker-registry \
    --namespace docker-registry \
    --output go-template \
    --template '{{.spec.host}}'
```

Log in into registry with username `registry` and password `9a5866dc0e500eea9b4f23bd99766053`:

```
$ podman login <your_registry_host_name>
```
