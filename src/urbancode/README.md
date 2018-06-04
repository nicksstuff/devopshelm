![Node Red logo](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/6973d47ab769037fec3a6345552bb25a/offering_3a8369bb-d7b1-4425-bd13-0a01c88e5745.png)


#[UrbanCode Deploy](https://developer.ibm.com/urbancode/products/urbancode-deploy/)

UrbanCode Deploy is an application release automation solution that combines robust visibility, traceability and auditing capabilities. It allows you to seamlessly deploy to distributed data centers, cloud and virtualized environments—on demand or on a schedule. The plugin ecosystem eliminates scripting and helps build DevOps toolchains for complex applications.

IBM also provides a new bundled offering under a new consumption model that changes the way you can use and deploy DevOps software. The new offering helps simplify your planning for adoption and growth of critical IBM DevOps products. Read more in the solution brief below.


## Getting Help

More documentation can be found [here](https://developer.ibm.com/urbancode/documents/).


# Introduction

This chart deploys a single UrbanCode Deploy instance into an IBM Cloud private or other Kubernetes environment.

## Prerequisites

- Kubernetes 1.7 or greater, with beta APIs enabled

## Installing the Chart

To install the chart with the release name `nodered`:

```sh
helm install --name nodered DEVOPS/urbancode
```

> **Tip**: See all the resources deployed by the chart using `kubectl get all -l release= urbancode `

## Uninstalling the Chart

To uninstall/delete the `urbancode ` release:

```sh
helm delete urbancode
```

The command removes all the Kubernetes components associated with the chart, except any Persistent Volume Claims (PVCs).  This is the default behavior of Kubernetes, and ensures that valuable data is not deleted.  In order to delete the PVC use the following command:

```sh
kubectl delete pvc -l release= urbancode
```
# Version for UrbanCode Depoloy
tag: 6.2.7.1.960481



#Node Port
nodePort: 30123


## Configuration
The following table lists the configurable parameters of the `ibm-mqadvanced-server-dev` chart and their default values.

| Parameter                        | Description                                     | Default                                                    |
| -------------------------------- | ----------------------------------------------- | ---------------------------------------------------------- |
| `replicas`                        | Number of replicas for Agents  | `1`                                     |                                 |
| `serviceType`                        | Type for access  | `NodePort`                                     |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart.

> **Tip**: You can use the default [values.yaml](values.yaml)

## Persistence

The chart mounts NO [Persistent Volume](http://kubernetes.io/docs/user-guide/persistent-volumes/).

# Copyright

© Copyright Niklaus Hirt 2018
