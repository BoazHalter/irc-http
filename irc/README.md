# IRC helm chart

```
$ helm install irc
```

### Run with Helm on top of Kubernetes




Parameter | Description | Default
--- | --- | ---
`replicaCount`| Set the Number Statefullsets launched| `5`
`image.repository`|| aws#.dkr.ecr.us-east-1.amazonaws.com/irc-http
`image.pullPolicy`||IfNotPresent
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
`service.type`|| ClusterIP
`service.port`|| 3000
`service.name1`|| johnny 
`service.type`|| ClusterIP
`service.port`|| 6667
`service.name2`|| joey
`ingress.enabled`|| false
`ingress.annotations` ||{}
`ingress.kubernetes.io/ingress.class`|| nginx
`ingress.kubernetes.io/tls-acme`|| "true"
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
