#Release Notes
## Pravega operator Version v0.2.1

[Pravega]() is an open source distributed storage service implementing Streams. It offers Stream as the main primitive for the foundation of reliable storage systems: a high-performance, durable, elastic, and unlimited append-only byte stream with strict ordering and consistency.

We are announcing the first release of the Pravega Operator, the easiest and best way to deploy and manage Pravega cluster in Kubernetes. The Pravega operator manages Pravega clusters deployed to Kubernetes and automates tasks related to operating a Pravega cluster. The [Pravega Operator](https://github.com/pravega/pravega-operator) project is currently alpha. 

Pravega operator is built on top of a common set of Kubernetes APIs by providing great automation experience. The Pravega operator performs packaging, deploying and managing the Kubernetes application. The Pravega operator is developed using the operator framework (SDK).

Below is a summary of the issues addressed in the [v0.2.1 release]https://github.com/pravega/pravega-operator/releases/tag/0.2.1) of Pravega Operator. For full documentation of the release, a guide to [get started](), and information about the project, see the [Pravega website]() and [Pravega Operator Github Repository](). 
The documentation for the most recent release can be found at Pravega website.

# Important Reminders for Pravega version v0.2.1


## Supported Deployment
- Kubernetes 1.8+(https://kubernetes.io/blog/2017/09/kubernetes-18-security-workloads-and/)
      
## Supported Tier 2 Storage

Pravega requires a long term storage provider known as Tier 2 storage. The following Tier 2 storage providers are supported:

- **External HDFS** ( must support Append operation): Setup an HDFS storage cluster running HDFS version x.x+. The storage cluster is recommended to be run alongside Pravega on separate nodes.
- [Filesystem (NFS)](https://github.com/helm/charts/tree/master/stable/nfs-server-provisioner)
- [Google Filestore](https://github.com/pravega/pravega-operator#using-google-filestore-storage-as-tier-2)
- [DellEMC ECS](https://www.dellemc.com/sr-me/storage/ecs/index.htm#collapse)

## Supported External Connectivity

- **Zookeeper**:  An existing Apache Zookeeper 3.5 cluster. 

# Issues addressed in Pravega Operator version v0.2.1

Below is a summary of the issues addressed in the [V0.2.1 release](https://github.com/pravega/pravega-operator/releases/tag/0.2.1) of Pravega. For full documentation of the release, a guide to [get started](https://github.com/pravega/pravega-operator/blob/master/README.md), and information about the project, see the [Pravega website](http://pravega.io) and [Pravega OPerator Github Repository](https://github.com/pravega/pravega-operator). 

The [documentation](https://github.com/pravega/pravega-operator/blob/master/README.md) for the most recent release can be found at Pravega website.


## New feature

## Bug Fixes
[Issue 78:]() Clean up persistent volumes when deleting Pravega Cluster [#103]()
[Issue 97:]() Update to operator SDK v0.2.0 [#105]()
[Issue 82:]() Ability to scale Pravega Controller [#99]()
[Issue 61:]() Support external connectivity [#77]()
[Issue 95:]() Updated README.md [#95]()
[Issue 79:]() Ability to use non-default service accounts [#80]()
