

# Issues addressed in Pravega Version v0.4.0.

Below is a summary of the issues addressed in the [V0.4.0 release](https://github.com/pravega/pravega/releases) of Pravega. For full documentation of the release, a guide to [get started](), and information about the project, see the [Pravega website]() and [Pravega Github Repository]().
=======

# Release Notes: Pravega v0.4.0


- [Important Remainders for Pravega version v0.4.0](#important-remainders-for-pravega-version-v040)  
- [New features](#new-features)
- [Resolved Issues in Pravega version v0.4.0](#bug)
- [Upgrading to Pravega Version v0.4.0] 


# Important Remainders for Pravega version v0.4.0

The following prerequisites are required for running in production. This page describes the prerequisites and installation steps to deploy Pravega in a multi-node production environment. 

         
## Supported Tier 2 Storage


[Issue 3096](https://github.com/pravega/pravega/issues/3096): Updating documentation with ZK TLS information. [PR-3102](https://github.com/pravega/pravega/pull/3102)

=======
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

Below is a summary of the issues addressed in the [V0.4.0 Release](https://github.com/pravega/pravega/releases) of Pravega. For full documentation of the release, a guide to [get started](http://pravega.io/docs/latest/getting-started), and information about the project, see the [Pravega website](http://pravega.io) and [Pravega Github Repository](https://github.com/pravega/pravega). 

The [documentation](http://pravega.io/docs/latest/) for the most recent release can be found at Pravega website.
The highlights of the Pravega 0.4.0. release are:

- Over 125 issues have been fixed in this release
- A new byte API for ingesting unbounded streams (e.g., videos)
- Higher scalability per stream
- Updated Docker images to use an Alpine base to reduce image size


## New Features
[Issue 291](https://github.com/pravega/pravega/issues/291): Add a byte oriented API per PDP-30 [#2978](https://github.com/pravega/pravega/pull/2978)

[Issue 2943](https://github.com/pravega/pravega/issues/2943): Controller metadata per stream scalability [#3033](https://github.com/pravega/pravega/pull/3033)
  


## Bug


[Issue 3058](https://github.com/pravega/pravega/issues/3058): Additional unit tests for Controller Metadata Scalability [#3061](https://github.com/pravega/pravega/pull/3061)

[Issue 3082](https://github.com/pravega/pravega/issues/3082): HDFS misconfiguration in Docker Swarm deployment. [#3084](https://github.com/pravega/pravega/pull/3084)

[Issue 3076](https://github.com/pravega/pravega/issues/3076): Bugfix for outstanding checkpoint count. [#3079](https://github.com/pravega/pravega/pull/3079)

[Issue 3078](https://github.com/pravega/pravega/issues/3078): Fix Swarm-based system tests [#3087](https://github.com/pravega/pravega/pull/3087)

[Issue 3144](https://github.com/pravega/pravega/issues/3144): Windows script text overwritten [#3145](https://github.com/pravega/pravega/pull/3145)

[Issue 3137](https://github.com/pravega/pravega/issues/3137): Added prefix to StatsD reporter. [#3139](https://github.com/pravega/pravega/pull/3139) 

[Issue 3108](https://github.com/pravega/pravega/issues/3108): List all the scopes during listScopes call [#3110](https://github.com/pravega/pravega/pull/3110)

[Issue 3173](https://github.com/pravega/pravega/issues/3173): Prevent mis-routing of events [#3177](https://github.com/pravega/pravega/pull/3177)

[Issue 3138](https://github.com/pravega/pravega/issues/3138): Use HOSTNAME envvar as metrics prefix [#3205](https://github.com/pravega/pravega/pull/3205)

[Issue 3171](https://github.com/pravega/pravega/issues/3171): Transaction commits metric not being reported [#3194](https://github.com/pravega/pravega/pull/3194)

[Issue 3131](https://github.com/pravega/pravega/issues/3131): Controller shutdown is stuck for a long time during zk session expiry [#3143](https://github.com/pravega/pravega/pull/3143)

[Issue 3202](https://github.com/pravega/pravega/issues/3202): Curator.close causes background curator calls to never complete [#3203](https://github.com/pravega/pravega/pull/3203)

[Issue 3224](https://github.com/pravega/pravega/issues/3224): Moved initialization of metrics reporter to Controller main class [#3226](https://github.com/pravega/pravega/pull/3226)

[Issue 3122](https://github.com/pravega/pravega/issues/3122): Bug in commit transaction workflow for a stream in sealing state [#3225](https://github.com/pravega/pravega/pull/3225)

[Issue 3223](https://github.com/pravega/pravega/issues/3223): RetentionTest failure [#3303](https://github.com/pravega/pravega/pull/3303)

[Issue 3221](https://github.com/pravega/pravega/issues/3221): Fix Invalid Precondition check in SegmentInputStreamImpl [#3222](https://github.com/pravega/pravega/pull/3222)

[Issue 3326](https://github.com/pravega/pravega/issues/3326): Fix compilation issue in BoundedStreamReaderTest [#3327](https://github.com/pravega/pravega/pull/3327)

[Issue 3313](https://github.com/pravega/pravega/issues/3313): Add workaround for client blocking [#3335](https://github.com/pravega/pravega/pull/3335)

[Issue 3333](https://github.com/pravega/pravega/issues/3333): Tolerate partial set of segments in Position object. [#3336](https://github.com/pravega/pravega/pull/3336)

[Issue 2933](https://github.com/pravega/pravega/issues/2933): (SegmentStore) testEndToEndWithFencing fixes [#3294](https://github.com/pravega/pravega/pull/3294)

[Issue 3304](https://github.com/pravega/pravega/issues/3304): Check correctness of event sequences with a shared map across readers [#3315](https://github.com/pravega/pravega/pull/3315)

[Issue 3310](https://github.com/pravega/pravega/issues/3310): Execute waitForTxnsToComplete before stopping readers. Removed useless boolean from parent class. [#3314](https://github.com/pravega/pravega/pull/3314)


## Release
[Issue 3055](https://github.com/pravega/pravega/issues/3055): Update Pravega version in r0.4 to 0.4.0 [#3056](https://github.com/pravega/pravega/pull/3056)

## Document Revision
[Issue 3096](https://github.com/pravega/pravega/issues/3096): Updating documentation with ZK TLS information. [#3102](https://github.com/pravega/pravega/pull/3102)

[Issue 3136](https://github.com/pravega/pravega/issues/3136): Merge fixes from master to r0.4 for release v0.4.0 (Documentation) [#3298](https://github.com/pravega/pravega/pull/3298)

[Issue 3305](https://github.com/pravega/pravega/issues/3305): Wire-protocol.md included [#3306](https://github.com/pravega/pravega/pull/3306)


# Issues related with Pravega Operator for Pravega version v0.4.0

# Issue related with Pravega Flink connectors for Pravega version v0.4.0
=======
## Issues related with Pravega Operator for Pravega version v0.4.0
           
## Issue related with Pravega Flink connectors for Pravega version v0.4.0
   
   [Issue 3076](https://github.com/pravega/pravega/issues/3076): Bugfix for outstanding checkpoint count. [#3079](https://github.com/pravega/pravega/pull/3079)


   [Issue 3076:]() Bugfix for outstanding checkpoint count. (#3079)
