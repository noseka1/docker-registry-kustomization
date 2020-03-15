# Kustomization for Installing Docker Registry on OpenShift

This repository contains kustomization for installing [Docker Registry](https://github.com/docker/distribution) on OpenShift using the official [Distribution](https://github.com/docker/distribution-library-image/tree/0b6ea3ba50b65563600a717f07db4cfa6f18f957) container image.

To deploy Docker Registry on OpenShift:

```
$ oc apply --kustomize docker-registry/base
```
