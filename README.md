# k8s-minecraft
Kubernetes definitions for Minecraft cluster

## Prerequisite

The declarations in this repository depend on Google Kubernetes Engine (GKE).
You need to be configured kubectl context in an proper manner.

## Dependency

* [itzg/minecraft-server](https://hub.docker.com/r/itzg/minecraft-server)

## Deploy

1. deploy `PersistentVolumeClaim`

```sh
$ kubectl apply -f pvc.yaml
```

1. deploy `StatefulSet`

```sh
$ kubectl apply -f server.yaml
```

1. deploy `Service`

```sh
$ kubectl apply -f service.yaml
```

## Configure minecraft servers

You can edit `config.yaml` and apply it to change the Minecraft server settings (serverProperty).
Please refere to [this document](https://docker-minecraft-server.readthedocs.io/en/latest/configuration/server-properties/) on the configuration options.
