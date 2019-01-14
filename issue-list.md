

# Release Notes: Pravega v0.4.0

- [Important Remainders for Pravega version v0.4.0](#important-remainders-for-pravega-version-v0-4-0)  
- [New features](#new-features)
- [Resolved Issues in Pravega version v0.4.0](#bug)
- [Upgrading to Pravega Version v0.4.0] 


# Important Remainders for Pravega version v0.4.0

The following prerequisites are required for running in production. This page describes the prerequisites and installation steps to deploy Pravega in a multi-node production environment. 

         
## Supported Tier 2 Storage

- **External HDFS**: Setup an HDFS storage cluster running HDFS version x.x+. The storage cluster is recommended to be run alongside Pravega on separate nodes.

- **AWS**: Have an AWS account and have Terraform installed. To install and download Terraform, follow the instructions here: https://www.terraform.io/downloads.html

## Supported External Connectivity

- **Zookeeper**:  Pravega requires Zookeeper x.x.x-x+. At least 3 Zookeeper nodes are recommended for a quorum. No special configuration is required for Zookeeper but it is recommended to use a dedicated cluster for Pravega. This specific version of Zookeeper can be downloaded from Apache at zookeeper-x.x.x-alpha.tar.gz.

## Bookkeeper

Pravega requires Bookkeeper x.x.0+. At least 3 Bookkeeper servers are recommended for a quorum. This specific version of Bookkeeper can be downloaded from Apache at bookkeeper-server-x.x.x-bin.tar.gz.

## Supported Deployment

- **Docker Swarm**: Docker Swarm can be used to quickly spin up a distributed Pravega cluster that can easily scale up and down. Unlike docker-compose, this is useful for more than just testing and development and will be suitable for production workloads in future.

- **Pravega Operator**: The Pravega operator  x.x.x manages Pravega clusters deployed to Kubernetes and automates tasks related to operating a Pravega cluster.


## Supported Stream Processing:

- **Flink connectors**:  The connectors currently require Apache Flink version x.x or newer. The latest release of these connectors are linked against Flink release x.x.x, which should be compatible with all Flink x.x.x versions.


# Issues addressed in Pravega version v0.4.0.

Below is a summary of the issues addressed in the [V0.4.0 release](https://github.com/pravega/pravega/releases) of Pravega. For full documentation of the release, a guide to [get started](), and information about the project, see the [Pravega website]() and [Pravega Github Repository](). 

The [documentation]() for the most recent release can be found at Pravega website.


## New Features
[Issue 291](https://github.com/pravega/pravega/issues/291): Add a byte oriented API per PDP-30 [PR-2978](https://github.com/pravega/pravega/pull/2978)

[Issue 2943](https://github.com/pravega/pravega/issues/2943): Controller metadata per stream scalability [PR-3033](https://github.com/pravega/pravega/pull/3033)

## Enhancement

[Issue 3096](https://github.com/pravega/pravega/issues/3096): Updating documentation with ZK TLS information. [PR-3102](https://github.com/pravega/pravega/pull/3102)
   

## Bug
[Issue 3122:](https://github.com/pravega/pravega/issues/3122) Bug in commit transaction workflow for a stream in sealing state (#3225)

[Issue 3224:](https://github.com/pravega/pravega/issues/3224) Moved initialization of metrics reporter to Controller main class. (#3226)

[Issue 3202:](https://github.com/pravega/pravega/issues/3202) Curator.close causes background curator calls to never complete (#3203)

[Issue 3131:](https://github.com/pravega/pravega/issues/3131) Controller shutdown is stuck for a long time during zk session expiry.  (#3143)

[Issue 3171:](https://github.com/pravega/pravega/issues/3171) Transaction commits metric not being reported (#3194)

[Issue 3138:](https://github.com/pravega/pravega/issues/3138) Use HOSTNAME envvar as metrics prefix (#3205)

[Issue 3173:](https://github.com/pravega/pravega/issues/3173) Prevent mis-routing of events (#3177)

[Issue 3108:](https://github.com/pravega/pravega/issues/3108)List all the scopes during listScopes call (#3110)

[Issue 3137:](https://github.com/pravega/pravega/issues/3137)Added prefix to StatsD reporter. (#3139)
  
[Issue-3137](https://github.com/pravega/pravega/issues/3137): Added prefix to StatsD reporter. [PR-3139](https://github.com/pravega/pravega/pull/3139)

[Issue 3144](https://github.com/pravega/pravega/issues/3144): Windows script text overwritten [PR-3145](https://github.com/pravega/pravega/pull/3145)

[Issue 3144](https://github.com/pravega/pravega/issues/3144): Windows script text overwritten (#3145)

[Issue 3082](https://github.com/pravega/pravega/issues/3082): HDFS misconfiguration in Docker Swarm deployment. (#3084)

[Issue 3048](https://github.com/pravega/pravega/issues/3048): Renamed ZKStreamTest to ZooKeeperStreamTest (#3050)

[Issue 2519](https://github.com/pravega/pravega/issues/2519): InProcPravegaCluster throws exception when keyFile is null (#2535)

[Issue 2944](https://github.com/pravega/pravega/issues/2944): ReadOnlySegmentContainer read retries (#3040)

[Issue 2987](https://github.com/pravega/pravega/issues/2987): Update Pravega base Docker images to Alpine (#2991)

[Issue 2399](https://github.com/pravega/pravega/issues/2399) : Create a custom classpath for Windows executable (#2452)

[Issue 3078](https://github.com/pravega/pravega/issues/3078): Fix Swarm-based system tests (#3087)

[Issue 3058](https://github.com/pravega/pravega/issues/3058): Additional unit tests for Controller Metadata Scalability work (#3061)

[Issue 3014](https://github.com/pravega/pravega/issues/3014): New system test for Byte Client (#3049)


## Security

[Issue-3108](https://github.com/pravega/pravega/issues/3108): List all the scopes during listScopes call [PR-3110](https://github.com/pravega/pravega/pull/3110)

## Release
[Issue 3055:]() Update Pravega version in r0.4 to 0.4.0 (#3056)

## Document Revision

[Issue 2966](https://github.com/pravega/pravega/issues/2966): Document fix pravegaconcepts doc (#3005)

[Issue 3009:]() Update streamcuts.md (#3019)

[Issue 3020:]() Update reader-group.md (#3021)

## Performance

[Issue-2982]()  Performance observed with NFS as Tier 2 storage (Known Issue)


## Issues related with Pravega Operator for Pravega version v0.4.0
           
## Issue related with Pravega Flink connectors for Pravega version v0.4.0
   
   [Issue 3076:]() Bugfix for outstanding checkpoint count. (#3079)

