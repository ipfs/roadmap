# IPFS Cluster Working Group 2019 Roadmap
 
The IPFS Cluster WG implements the IPFS Cluster product. IPFS Cluster facilitates the orchestration of multiple IPFS daemons, as well as collaboration maintaining IPFS pinsets and datasets.

**Current Projects:**
- IPFS Cluster
- Pinbots
- Cluster infra
- Support decentralized data stewardship
- IPFS Storage for partners

## 🚀 Major 2019 goals to achieve

- IPFS Cluster facilitates the ingestion and replication of package repositories to IPFS
- IPFS Cluster is the goto team for experience and expertise handling large files
- IPFS Cluster facilitates distribution of content large IPFS datastores among different organizations and users
- IPFS Cluster enables the creation of collaborative IPFS content networks
- Cluster provides managed IPFS storage for select partners that need them
- IPFS Cluster takes a key role in the IPFS Conf

## 💎 Milestones

### Package Managers

- `M (P0)`: IPFS Cluster can be used to shard large repositories among multiple IPFS daemons
  - Go-ipfs supports pinning strategies
  - IPFS Cluster supports sharding https://github.com/ipfs/ipfs-cluster/issues/496
- `M (P0)`: IPFS Cluster understands the requirements for package managers infrastructure and can become an useful layer on top of IPFS
  - Attend the reproducible builds summits
  - Produce a document that show how exactly IPFS cluster can help ipfs-based package managers
  - Scaling and federation
  - Spec out enterprise support requirements
- `M (P1)`: IPFS Cluster is used to manage at least one package repository of some kind
  - Collaborative clusters need to be ready possibly (depends on previous)
  - Redirect registry.js.ipfs.io to use IPFS Cluster rather than just one IPFS node

### Large Files

- `M (P1)`: IPFS Cluster team is a key participant for data-together efforts creating and storing archives
  - We need to start joining their meetings
  - Support any actual efforts with our tech
- `M (P0)`: At least two organizations run a “federated” IPFS Cluster
  - Federated clusters is a defined usecase
  - We have figured out how to do this
  - Permissions in endpoints
  - Cluster API IPFS Connector
Advanced allocators, priority allocators, compositionable allocators

### Decentralized Web

- `M (P0)`: We run some topic networks like “cat pictures” or “tweets” and > 10 followers help pinning content for them
  - “Collaborative pinsets” (crdt+pubsub+trusted pinners) works
  - Super easy initialization of cluster configuration for this
  - We have an official website for this

### Support User

- `M (P1)`: Cluster provides managed IPFS storage for select partners that need them and this takes less than 2h time to 1 engineer.
  - We can setup new clusters on AWS very easily
  - AWS deployment and docs
  - We know how much it costs to do this
  - We have a document outlining which partners are the best fit to do this

### Strategic Projects

- `M (P1)`: We run at least four talks at IPFS Conf: IPFS Cluster 101, IPFS Cluster to back up your personal content, Federating IPFS Clouds with IPFS Cluster, IPFS Cluster for cloud administrators, IPFS Internals
  - Create all these talks
  - Make sure we participate in IPFS Conf preparation and push the project to be prominent
- `M (P0)`: We need to have figured out very clear product description of Cluster and cover all the features they need
  - Collaborative pinsets
  - Federation

## Timeline

- Q1
- Q2
- Q3
- Q4
