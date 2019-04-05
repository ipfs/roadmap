# IPFS Go Core Dev Team - Roadmap 2019

The Go IPFS Working Group is responsible for the development of the Go IPFS implementation and participating in the planning and development of IPFS in general. 

### Responsibilities include:
* Implement new features in the Go IPFS implementation
* Support Go IPFS, fixing bugs and improving stability and performance
* Develop specifications for new IPFS protocols and capabilities

## Current Projects
* go-ipfs
* IPLD
* gx
* Data Exchange/Transfer - improve performance of data transfer
* Data Management - improve ability of Go IPFS to manage large data sets
* Provider Strategies - improve efficiency of DHT use
* Commands Lib
* API
* Base32 CIDv1

## Major 2019 goals to achieve
1. Benchmarks for Go IPFS that measure IPFS behavior across data lifecycle for a broad set of inputs. 
2. ‘Indefinite’ refactors are complete; code is maintainable and understandable
3. Improve data transfer speed so that it is at least 0.8 times that of bittorrent/rsync, (whichever is faster) for a given set of peers and data
4. Support adding/getting/pinning large volumes of data efficiently. Go-IPFS can add (and provide) 10TB of small files (< 1MB each) at > 0.5 times the speed of a simple dd] copy. 
5. Make storing, looking up, and retrieving provider data in the DHT reliable and fast. 
6. Complete, documented, performant, stable APIs for interacting with a running Go IPFS node.

## Milestones

### 📦 Package managers

For the core implementation of IPFS to support package manager needs - go-ipfs needs to be fast, efficient and stable when handling and transferring large amounts of data. It also needs to understand and support the specific tooling and usability needs of the package manager community.

NOTE: “large files” = 10GB - 1TB, “many small files” = 10K-1M 1MB files. Benchmark goals refer to the speed of transferring data when already connected to IPFS nodes that have that data (not finding the data).

#### Understanding Package Manager needs
* `M (P0)`: The IPFS core team understands the needs of package management communities and engages their interest
   * Meet people from various package management communities -- both distros and language tooling -- and learn about their needs
   * Support interested package manager communities with DRIs
      * F-droid
      * Guix
      * Snapshots.debian.org ?
* `M (P0)`: We have understanding and documentation of what kind of scale (in terms of size at one time; and change in size over time) mirroring a package manager archive requires.
   * Ex: document how long mirroring npm into IPFS takes
   * Ex: VictorBjelkholm/arch-mirror also exists, let’s make sure we gather stats
* `M (P1)`: Develop documentation for what Package Distribution with IPFS should look like.
   * There is documentation and guidelines to help maintainers from existing package management communities learn about IPFS, explore common alternatives, and figure out what would work for their system
   * Document and highlight best practices for dealing with the common hurdles in moving to immutable-first: e.g. “save packages in a merkle tree; build a package index merkle tree; use IPNS to handle updates of the tip of package index tree”.
* `M (P1)`: There is a way to prioritize different peers to optimize network utilization
   * Bitswap peer prioritization supports pinning local / responsive peers 

#### Supporting Package Manager speed and scalability needs
* Q1 - `M (P0)`: Awesome go-ipfs benchmark test suite exists comparing ipfs performance and transfer size relative to bittorrent
* Q2 - `M (P0)`: Expand benchmark test suite to compare relative to rsync, http, cp, dd
* `M (P0)`: Go-IPFS bitswap (or equivalent) can transfer large files from many peers at 0.8 times the speed of BitTorrent. 
   * Q1 - Bitswap session improvements that improve transfer efficiency by reducing duplicate blocks and efficiently fetching related data from many peers simultaneously. 
   * Graphsync selector implementation that can understand non-overlapping subsets of data to select from multiple hosts and the driver that can build up graphsync requests for many peers to maximize efficiency and throughput. 
* `M (P0)`: Go-IPFS can transfer many small files at 0.8 times the speed of rsync (for single peers) or BitTorrent (for many peers)
   * Bitswap session improvements
   * Graph Exchange that can route requests efficiently
   * Q1 - Graphsync makes accessing files in large directories log(n) faster
   * Q1 - Flexible provider strategies
* `M (P1)`: Go-IPFS can transfer large files from a single peer at 0.8 times the speed of HTTP. 
   * Q1 - Flexible provider strategies to use the DHT efficiently (and therefore not slow IPFS down while adding/fetching files) while still preserving the reachability of data. 
* `M (P1)`: Go-IPFS can add a directory of many small files at 50% the speed of a simple local hard drive copy (or dd) (10k x 1MB files)
   * Flexible provider strategies to limit the number of DHT provider advertisements we make
   * Q1 - Faster datastore (Badger or equivalent) that doesn’t slow down as the number of blocks stored grows large
   * GC improvements (transactions, speed)
* `M (P2)`: Data transferred over the network is no more than 1.2x the size of the data being transferred 
   * Bitswap session improvements to reduce duplicates
   * Graphsync

### 🤝 IPFS Contributors and Developers

Developers using IPFS can rely on go-ipfs as a platform on which to build their product, app, or ecosystem, and new contributors are well supported.

#### Contributors
* `M (P0)`: (all) Go-IPFS is approachable as a new contributor
   * Go-IPFS internals are well documented
   * Technical debt is paid off, all "indefinitely-in-progress" refactors are completed.
   * Cleanup/rethink abstraction layers with 20-20 hindsight.
   * Re-structure repos into reusable but not fragmented components.
* `Q1 - M (P0)`: (all) Go-IPFS is usable without gx
   * Fix the versions (make them all sub-0)
   * Add go.mod files to every package
   * Merge #5435.
* `M (P0)`: We have a stable core that people can add things to without breaking changes
   * UnixFS is stable and extensible
      * UnixFS v2 (with a good HAMT)
   * The DHT is extensible
      * Multi-DHT: https://github.com/ipfs/notes/issues/291#issuecomment-414495124
* `Q1 - M (P0)`: Have a solution for testing/benchmarking
   * Available for offline testing.
   * Reproducibility (across different platforms).
   * Provide realistic Internet/WAN simulations (with delays and dropped packets).
* `M (P1)`: Interfaces are future-proof enough for 1.0
   * CoreAPI
   * Plugins
   
#### Developers (Users)
* `M (P0)`: Provider lookups are efficient (<1 sec) in real-world network conditions (ex between physically distant peers)
* `M (P0)`: (all) Users can reliably transfer data between any two nodes.
   * Reliable NAT traversal (AutoNAT, relay, TURN, etc).
   * Connection manager doesn't kill useful connections.
   * Scalable content routing
   * Reliable DHT: unreliable nodes don't join the DHT.
* `M (P0)`: (dapps) ipfs:// and ipns:// work in web browsers
   * Base32 CIDs
   * Base32 IPNS or IPNS uses CIDs
* `M (P1)`: (all) Go-IPFS is approachable as a user/app developer
   * User documentation.
   * Well designed API interface
   * Well designed API transport
* `M (P1)`: (machine-learning/package managers) IPFS can handle (and transfer) large (>1M entries) sharded indexes (objects, directories)
   * Bitswap Improvements (sessions, prediction, etc)
   * UnixFS-V2 (better directory structure)
* `M (P1)`: Fast (< 3s), mutable name resolution (IPNS)
   * Reliable DHT.
   * QUIC (for fast connection establishment).
   * Better protocol negotiation (multistream-2.0)
   * Delegated Routing
* `M (P1)`: (Dapps) IPFS Realtime Story is as good as using a centralized service (e.g. Socket.io, Pusher, etc)
   * The API for doing secure (authenticated) broadcast updates exists 
* `M (P2)`: Go-ipfs can handle large datasets (>1TiB, >1M nodes)
   * Scalable content routing (providing)
   * DagSync (or at least better bitswap)
   * Reliable, performant datastore
* `M (P2)`: (all, Dapps) IPFS is pluggable and extensible (9/10 users don't need custom features)
   * The go-ipfs plugins system is expanded to support new datastores, exchanges, etc
   * Exchanges support multiple protocols (that diagram from hack week)
   * Multi-DHT (https://github.com/ipfs/notes/issues/291#issuecomment-414495124)
   * UnixFS-V2 is implemented
* `M (P3)`: (Dapps) IPFS can locally share data without a shared network
   * A bluetooth (or like) transport
* `M (P4)`: (anti-censorship) Our IPFS implementations are secure and don't leak sensitive information
   * Get a security audit
   * Implement the privacy preserving DHT (https://github.com/ipfs/notes/issues/291#issuecomment-396003860)
   * Add a download-only mode (avoid serving local data)
   * Investigate a privacy-preserving transport


## ⏳ Timeline

- Q1
- Q2
- Q3
- Q4

## ⁉️ Want to get involved?
- File an issue here with questions, or make a PR to suggest an alternate path or addition
- Want to help make this happen? [Open an issue on the Go IPFS Working Group repo!](https://github.com/ipfs/go-ipfs/issues)
