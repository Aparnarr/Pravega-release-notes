
# Important Reminders for Pravega version v0.4.0

The following prerequisites are required for running in production. This page describes the prerequisites and installation steps to deploy Pravega in a multi-node production environment. 

         
## Supported Tier 2 Storage

- **External HDFS**: Setup an HDFS storage cluster running HDFS version x.x+. The storage cluster is recommended to be run alongside Pravega on separate nodes.

- **AWS**: Have an AWS account and have Terraform installed. To install and download Terraform, follow the instructions here: https://www.terraform.io/downloads.html

## Supported External Connectivity

- Zookeeper:  Pravega requires Zookeeper x.x.x-x+. At least 3 Zookeeper nodes are recommended for a quorum. No special configuration is required for Zookeeper but it is recommended to use a dedicated cluster for Pravega. This specific version of Zookeeper can be downloaded from Apache at zookeeper-x.x.x-alpha.tar.gz.

## Bookkeeper

Pravega requires Bookkeeper x.x.0+. At least 3 Bookkeeper servers are recommended for a quorum. This specific version of Bookkeeper can be downloaded from Apache at bookkeeper-server-x.x.x-bin.tar.gz.

## Supported Deployment

- Docker Swarm: Docker Swarm can be used to quickly spin up a distributed Pravega cluster that can easily scale up and down. Unlike docker-compose, this is useful for more than just testing and development and will be suitable for production workloads in future.

- Pravega Operator: The Pravega operator  x.x.x manages Pravega clusters deployed to Kubernetes and automates tasks related to operating a Pravega cluster.


## Supported Stream Processing:

- Flink connectors:  The connectors currently require Apache Flink version x.x or newer. The latest release of these connectors are linked against Flink release x.x.x, which should be compatible with all Flink x.x.x versions.

