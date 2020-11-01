# cluster-overprovisioner


This chart provide a buffer for cluster autoscaling to allow overprovisioning of cluster nodes. This is desired when you have work loads that need to scale up quickly without waiting for the new cluster nodes to be created and join the cluster.

It works but creating a deployment that creates pods of a lower than default `PriorityClass`. These pods request resources from the cluster but don't actually consume any resources. These pods are then evicted allowing other normal pods are created while also triggering a scale-up by the [cluster-autoscaler](https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler).

# Steps to install helm chart

1. Clone the repository to local machine
```
$ git clone git@github.com:avedpathak/Overprovisioner.git
```
2. Navigate to the folder and use below command

```
$ Helm install <release_name> <directory path where helm chart has been cloned>
```

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Ajit Vedpathak | ajitvdpthk@gmail.com |  |

