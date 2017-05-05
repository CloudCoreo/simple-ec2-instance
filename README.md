simple-ec2-instance
============================



## Description
This composite creates a simple AWS Linux server instance via an Autoscaling Group


## Hierarchy
![composite inheritance hierarchy](https://raw.githubusercontent.com/CloudCoreo/simple-ec2-instance/master/images/hierarchy.png "composite inheritance hierarchy")



## Required variables with no default

### `SERVER_KEYPAIR`:
  * description: the name of the keypair to launch server with


## Required variables with default

### `AUTOSCALING_GROUP_MAXIMUM`:
  * description: Maximum number of instances the autoscale group will launch
  * default: 1

### `AUTOSCALING_GROUP_MINIMUM`:
  * description: Minimum number of instances the autoscale group will launch
  * default: 1

### `VPC_NAME`:
  * description: The name of the VPC that this server is to be created in
  * default: test-vpc

### `VPC_OCTETS`:
  * description: the /16 net of the VPC to look for - i.e 10.11.0.0
  * default: 10.11.0.0


### `REGION`:
  * description: 
  * default: PLAN::region


### `PUBLIC_ROUTE_NAME`:
  * description: 
  * default: test-public-route

### `PUBLIC_SUBNET_NAME`:
  * description: The name of the public subnet you want to create your server in
  * default: test-public-subnet

### `PUBLIC_SUBNET_NUM_ZONES`:
  * description: How many public subnets to create
  * default: 3

### `VPC_CIDR`:
  * description: The CIDR to match to locate the VPC that this server is to be created in
  * default: 10.11.0.0/16

### `SERVER_NAME`:
  * description: the name of the server
  * default: simple-server


### `SERVER_INGRESS_PORTS`:
  * description: Ports to open up in the server security group
  * default: 50, 16

### `SERVER_INGRESS_CIDRS`:
  * description: 
  * default: 0.0.0.0/0

### `SERVER_SIZE`:
  * description: the size of the server to launch
  * default: t2.micro


### `TIMEZONE`:
  * description: the timezone the servers should come up in
  * default: America/Los_Angeles


## Optional variables with default

### `SERVER_UPGRADE_TRIGGER`:
  * description: A String used to trigger upgrades of ec2 instances. If specified, CloudCoreo will not roll instances unless this value changes.
  * default: initial



## Optional variables with no default

### `SUFFIX`:
  * description: when used will use the value to suffix the names of all converged objects

### `DATADOG_KEY`:
  * description: If you have a datadog key, enter it here and we will install the agent

## Tags
1. Servers
1. AWS Linux


## Categories
1. Servers



## Diagram
![diagram](https://raw.githubusercontent.com/CloudCoreo/simple-ec2-instance/master/images/diagram.png "diagram")


## Icon
![icon](https://raw.githubusercontent.com/CloudCoreo/simple-ec2-instance/master/images/icon.png "icon")

