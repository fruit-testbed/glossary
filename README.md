FRuIT glossary
==============

We need to establish a shared vocabulary so we can talk about the
technical aspects of the project sensibly. Here is a first stab at
some terms we might want to standardise. Feel free to add/edit. This
glossary is formatted for emacs org-mode.

* behind a NAT
  An NATted entity is on a private network and does not have a
  globally reachable IP address. This entity can contact the outside
  world, but other entities cannot initiate contact with this entity. 


* configuration
  This happens to individual nodes. A node is configured
  by a script, which sets up the node's software stack, from the OS up
  to the application layer. The precise details of the script support
  are TBC. Configuration will be managed remotely. 


* deploy task
  A task is deployed on an provisioned entity of configured nodes


* entity
  Either a node, a micro-cluster or a federation.


* federation
  A set of logically connected nodes and/or micro-clusters, reachable
  via a single overlay network. A federation is a dynamic construct
  that is assembled to operate on a compute task, probably using some
  kind of message passing protocol.

* management
  The management software layer is the core of the FRuIT system. It
  supports all the user-facing activities i.e. provisioning,
  configuration, deployment, update and surrender. 
  The management layer is a lightweight dom0 (i.e. not virtualized)
  daemon that runs on each node of the FRuIT system. It responds to
  message style requests to perform appropriate on-node actions. (Are
  these requests SERF style broadcast messages?)


* micro-cluster
  A set of nodes connected on a LAN. At least one node in the
  micro-cluster is a controller node, with an outside internet
  connection and responsibility for orchestrating cluster
  configuration/management. Everything we have built so far
  (Iridis-Pi, Glasgow PiCloud) is a micro-cluster. 


* node
  Probably a single Raspberry Pi board or other single board
  computer. A node has at least one IP
  address, probably corresponding to a physical ethernet connection. A
  node runs a local operating system, most likely a Linux distro. A
  node has at least one CPU core.

* overlay network
  A virtual connection network, using some protocol (perhaps VPN or
  some p2p protocol) that is layered on top of a physical network
  (probably ethernet)



* provisioning
  An end-user requests some number of entities to be allocated, with the
  intention of deploying a task on them. Parameters for provisioning are
  to be determined. cf. AWS instance provisioning via a web interface or
  programmatic API.


* resource sharing 
  Using containerization, it should be possible to host multiple tasks
  on a single node. This idea of multi-tenancy or resource sharing is
  a key concept in as-a-service computing. We need to decide whether we
  can give someone 0.5 of a node, or similar. Can we federate at finer
  granularity than dedicated node-level? How quantized are our
  entities? So far, all our nodes have been dedicated to a single
  task --- FRuIT should explore how we can achieve more efficient
  resource sharing.


* surrender
  An entity that has been provisioned can be surrendered, which means
  it is no longer required by that user, and may be redeployed. cf. AWS
  instance termination. Individual nodes may be surrendered one-by-one,
  which means a user can gradually return a provisioned entity
  comprising multiple nodes.


* task
  Users want to run tasks on entities. Precise nature of task needs to
  to be confirmed. Something like a docker container? At the very
  least, a task must be a packaged executable with associated
  metadata. Execution of tasks is the main purpose of the FRuIT system we
  are building. Current tasks on our existing clusters include MPI
  programs, Hadoop jobs, sensor data collection and forwarding.


* unique features of our project
  - federation is a layer higher than standard datacenters.
  - Some of our entities are not globally reachable.
  - We want to do config/update etc in a p2p manner.
  - we run on lightweight nodes, ideally using renewable energy sources


* update
  Software on a configured node is replaced or upgraded by an update operation.
  This might befor security or functionality improvements.


* workflow
  As far as the end-user is concerned, the typical interaction
  sequence with FRuIT is : provision -> configure -> deploy -> update
  (?) -> surrender. This sequence should be supported/automated by our
  FRuIT system. Current state of the art for our testbeds is manual
  provisioning, centralized configuration and deployment, manual
  update and no surrender (other than power down).


