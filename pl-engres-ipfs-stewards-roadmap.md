# PL EngRes IPFS Stewards Roadmap (DRAFT)

## What is this document?
This is PL EngRes IPFS Stewards' stakeholder roadmap.  (You can learn more about the team [here](https://pl-strflt.notion.site/Kubo-go-ipfs-4a484aeeaa974dcf918027c300426c05).)  This document doesn't live in the [ipfs/kubo](https://github.com/ipfs/kubo) repo because per the team description above the team's area of ownership is larger than Kubo.  The team is often involved in discussions, decisions, and efforts that affect the wider IPFS ecosystem, and Kubo is used to give traction to and validate ideas.  We want to ensure the wider IPFS community knows the team's plans.
This document is not:
1. A roadmap for the IPFS project as a whole.
2. A detailed engineering plan for all of our ongoing initiatives.  The day-to-day shows up in the [Kubo GitHub Project Board](https://www.notion.so/pl-strflt/Kubo-GitHub-Project-Board-c68f9192e48e4e9eba185fa697bf0570).

## Themes

We’re defining a set of themes which help us think about how we are investing our engineering resources towards a few key strategies. In any given window of time, strategic priorities will dictate the relative amount of investment we make towards each theme. As time goes on, the themes will shift; some themes may get de-prioritized or dropped entirely as new ones come in. Some themes, however, may always be relevant. We try to keep between 3 to 5 themes total. 

### Theme 1: Ubiquitous Clients/Implementations
    
To increase usage of the IPFS protocol across the board, we need there to be a rich array of clients supporting many possible use-cases on many possible platforms. We do this by:

- Being the primary contributors/maintainers of one or more high-quality, off-the-shelf reference IPFS host implementation(s)
- Finding opportunities to unblock/accelerate new implementations being developed by other projects/organizations
- Helping guide the extensions to core protocols necessary to support new client design patterns (e.g., Thin Clients)

### Theme 2: Content Routing Innovation

Content routing will continue to be amongst the most critical areas for innovation to extend the reach of IPFS to all the data on the planet and to support low latency application scenarios. We will advance the state of IPFS Content Routing by:

- Ensuring the protocols and implementations support the flexibility for teams and organizations across the ecosystem to experiment with and commit to diverse content routing approaches
- Directly driving innovation in content routing technology into the core reference implementations of IPFS

### Theme 3: Privacy

Privacy is at the heart of Web3, and IPFS must hold an incredibly high privacy bar. We will continue to invest in protocols and implementations to ensure user privacy is always honored.

### Theme 4: Engineering Excellence

As an engineering team supporting a large amount of code in open source projects which now has some years behind it, there is always going to be engineering debt. But beyond debt, we want to continue to invest thoughtfully in ways that can increase the efficiency and effectiveness of our engineers.

### Theme 5: Rich Application Support

Future investment focus area we will flesh out more. Should include:

- Enhancing support for data mutability and addressing issues in current implementations/protocols
- Being able to make data available through IPFS without re-encoding/re-writing
	
## Legend

- Legend

⚫ Not Started

🟢 In progress - on track

🟡 At risk

🔴 Blocked

🔵 Done
	
## Roadmap
### 2022-10
#### 🟢 Reframe support in IPFS Gateways
Theme: Content Routing Innovation

Reframe is enabled on the ipfs.io gateway, hitting cid.contact in parallel to query the DHT to determine providers for a CID.

Tracking issue: https://github.com/ipfs/kubo/issues/9150

Done:

- Reframe is enabled on the [ipfs.io](http://ipfs.io/) gateway, hitting Store The Index in parallel to querying the DHT to determine providers for a CID.
- Above uses cache-friendly mechanisms like HTTP GET and DAG CBOR in URLs

### 2022-12
#### 🟢 Spec for content routing selection
Theme: Content Routing Innovation

Evolve IPFS specs to define mechanisms for content routing selection and defaults. There is a clear community-reviewed spec for how an implementation like Kubo would use indexers by default without hardcoding it into Kubo's default configuration.

Shared effort with Bedrock and other IPFS implementers.

Done: Accepted spec (IPIP process) to define how IPFS implementations can bootstrap content routing selection/defaults. 

#### 🟢 Enable verifiable retrieval on the ipfs.io gateway
Theme: Ubiquitous Clients

Specification for gateway-verifiable retrieval and implementation in Kubo gateway code.

One major remaining issue is signed IPNS records. We will need to update IPFS specs to define how this works: https://github.com/ipfs/specs/issues/320

Another issue: There is also perf. problem of  multiple round-trips when requesting deep sub paths like `/ipfs/cid/sub/dir/some/file.jpg` → requires 5 requests (1CAR with file.jpg and 4 blocks, one  for each dir level) 

Done:

- Update IPFS specs to define protocol changes to enable verifiable retrieval in all cases
- Update (Kubo) Gateway code to address known deficiencies so that we can properly support verifiable retrieval from light clients

#### ⚫ DHT Double Hashing Support
Theme: Privacy

Define and deliver support for double hashing in Kubo DHT nodes to enhance IPFS privacy.

Shared effort with Probelab. Steward work needs to be better understood and estimated to have higher confidence on the date.

Why: Double Hashing ensures that user requests for content on the network cannot be tracked, ensuring user privacy.

In partnership with ProbeLab: [Double Hashing for Privacy](https://www.notion.so/Double-Hashing-for-Privacy-ff44e3156ce040579289996fec9af609) 

Also partnership with LibP2P

Done: 

- finalized design for double hashing on content requests to the DHT
- Update IPFS specs
- double hashing support for DHT lookups implemented in Kubo

### 2023-Q1
#### ⚫ libipfs
Theme: Ubiquitous Clients

Core Kubo functionality is refactored into a library used both by Kubo as well as other implementers who want to support additional use cases without blocking on Kubo maintainers.

Kubo has a bunch of battle-tested code over the years.  Unfortunately it’s not easy to consume as a library because of the repo sprawl and having to pull in all the relevant pieces.  It’s also hard for maintainers to keep it updated and we’re reliant on Kubo as the delivery vehicle to specify compatible versions.  Seeing the success go-libp2p has had moving to a monorepo, we will move to a similar pattern where Kubo specifics stay in Kubo but the generally usable parts for anyone writing an IPFS implementation in Go can live in libipfs

Done: Core Kubo functionality is packaged into a library used both by Kubo as well as other implementers who want to support additional use cases without blocking on Kubo maintainers

#### ⚫ Indexer double hashing support
Theme: Privacy

Define and deliver support for double hashing with indexers from Kubo to enhance IPFS privacy.

Shared effort with Probelab, Bedrock, and libp2p.

#### ⚫ Verifiable retrieval in light clients
Theme: Ubiquitous Clients

Deliver Rust library for client-side verifiable retrieval in light clients.

Depends on:

- Enable verifiable retrieval on the gateway

Done:

- Deliver Rust library for client-side verifiable retrieval in light clients

Notes: 

- We need to ensure we have alignment on use of Rust here with stakeholders
- We believe it’s stategic for IP Stewards to invest in building muscle with Rust, and this is a good starting point

### 2023-Q2
#### ⚫ Implement default content routing selection
Theme: Content Routing Innovation

Depends on: 

- Indexer Double Hashing Support
- Spec for Content Routing Selection

Done:

- Full support (Kubo + any necessary infrastructure) to support content routing selection, including default use of cid.content by Kubo

#### ⚫ “Slimmer Kubo”: Trim out unnecessary code
Theme: Engineering Excellence

Clean up old, non-critical functionality from Kubo to limit supported surface area and help team focus on strategic priorities/functionality.

Kubo today has become a bit bloated with functionality that is not critical to our key use cases, has not been touched in a long time, etc. We then get issues opened against that functionality or questions about it, which diverts team time/resources away from key strategic work. We would like to clean some of this out of Kubo to help us be more efficient/effective, and focused on top priorities.

Done: 

1. Remove some specific things: Fuse, graphsync, others based on analysis
    1. This actually requires a multi-part deprecation strategy, so we would start with deprecation, with code removal occurring potentially 6 months later.

### Future
#### ⚫ Hydras Plan
Theme: Content Routing Innovcation

Build long term strategy around hydras in general and hydra/indexer integration specifically for content routing performance.

#### ⚫ Writeable Gateways
Theme: Ubiquitous Clients

Support pushing new data into storage via gateways.

The IPFS Ecosystem is lacking an HTTP API for data ingestion.

This means every service invents their own, re-inventing  the same thing (HTTP upload endpoint) over and over again, but with small changes which mean we are unable to write clients that are compatible with multiple services or IPFS implementations. This creates artificial barriers for adoption and vendor lock-in (people need to pick 1-3 “winners” and have to live with them as the switching cost is too high).

This is a real problem – Brave is currently forced to look at proprietary CAR upload APIs from nft.storage, because we have no generic one.

We have vendor-agnostic API for data retrieval (HTTP gateway and block / car responses, or deserialized version for UnixFS). We need similar flexibility for ingestion: ability to upload a file, Tar stream and let gateway chunk and produce UnixFS, OR accept pre-chunked content addressed data as blocks and CARs. 

#### ⚫ Enhancing support for data mutability and addressing issues in current implementations/protocols
#### ⚫ Make data available through IPFS without re-encoding/re-writing


## On the radar but not planned/committed currently

- WASM/IPVM
    - 2022-10-07: we know there are movements afoot here.  We don’t currently know if/how/where to harness them and how they should affect the roadmap.
