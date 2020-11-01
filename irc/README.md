# IRC helm chart

```
$ helm install irc
```

### Run with Helm on top of Kubernetes

## Prerequisites
  - Kubernetes 1.4+ with Beta APIs enabled

## Introduction

This chart deploy anumber of statefullsets containing irc client


## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm install --name my-release irc/
```

The command deploys irc on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following tables lists the configurable parameters of the chart and their default values.




Parameter | Description | Default
--- | --- | ---
`replicaCount`| Set the Number Statefullsets launched| `5`
`image.repository`|Docker registry addreess | aws#.dkr.ecr.us-east-1.amazonaws.com/irc-http
`image.pullPolicy`|in which case to pull the image |IfNotPresent
`image.tag`|| "latest"
`imagePullSecrets`|| []
`nameOverride`|| ""
`fullnameOverride` || ""
`serviceAccount.create`| Specifies whether a service account should be created| true
`serviceAccount.annotations`|Annotations to add to the service account| {}
`serviceAccount.name`|The name of the service account to use. If not set and create is true, a name is generated using the fullname template| ""  
`podAnnotations`|| {}
`podSecurityContext`|| {}
`podSecurityContext.fsGroup`|| 2000
`securityContext`|| {}
`securityContext.capabilities.drop`||- ALL
`securityContext.readOnlyRootFilesystem`|| true
`runAsNonRoot`|| true
`runAsUser`|| 1000
`service.type1`|| ClusterIP
`service.port1`|| 3000
`service.name1`|| johnny 
`service.type2`|| ClusterIP
`service.port2`|| 6667
`service.name2`|| joey
`ingress.enabled`|| false
`ingress.annotations` ||{}
`ingress.annotations.kubernetes.io/ingress.class`|| nginx
`ingress.annotations.kubernetes.io/tls-acme`|| "true"
`ingress.hosts.host|| chart-example.local
`ingress.hosts.paths`|| []
`ingress.tls`|| []
`ingress.tls.secretName`|| chart-example-tls
`ingress.tls.hosts`||- chart-example.local
`resources`|| {}
`resources.limits.cpu`|| 100m
`resources.limits.memory`|| 128Mi
`requests.cpu`|| 100m
`requests.memory`|| 128Mi
`autoscaling.enabled`|| false
`autoscaling.minReplicas`|| 1
`autoscaling.maxReplicas`|| 100
`autoscaling.targetCPUUtilizationPercentage`|| 80
`autoscaling.targetMemoryUtilizationPercentage`|| 80
`nodeSelector`|| {}
`tolerations`|| []
`affinity`|| {}
