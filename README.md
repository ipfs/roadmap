# IPFS Project Roadmap v0.5.0

## Table of Contents

- [IPFS Mission Statement](#ipfs-mission-statement)
- [2019 Priorities](#2019-priorities)
- [2019 Working Groups Roadmaps](#2019-working-groups-roadmaps)
- [2019 IPLD & libp2p Roadmaps](#2019-ipld--libp2p-roadmaps)
- [2019 Epics](#2019-epics)
- [2019 Goals (expanded)](#2019-goals-expanded)
  - [📦 Package Managers](#-package-managers-d1-e5-i3)
- [2020+ Goals](#2020-goals)
  - [🗂 Large Files](#-large-files-d1-e4-i3)
  - [🔄 Decentralized Web](#-decentralized-web-d2-e4-i3)
  - [🔒 Encrypted Web](#-encrypted-web-d2-e3-i4)
  - [♻️ Distributed Web](#%EF%B8%8F-distributed-web-d2-e2-i4)
  - [👩🏽‍💻 Personal Web](#-personal-web-d3-e4-i2)
  - [👟 Sneaker Web](#-sneaker-web-d3-e2-i4)
  - [🚀 Interplanetary Web - Mars 2024](#-interplanetary-web---mars-2024-d3-e3-i4)
  - [💾 Packet Switched Web](#-packet-switched-web-d3-e2-i3)
  - [📑 Data Web](#-data-web-d4-e3-i3)
  - [✉️ Package Switched Web](#%EF%B8%8F-package-switched-web-d4-e2-i2)
  - [⛓ Self-Archiving Web](#-self-archiving-web-d4-e4-i4)
  - [🏷 Versioning Datasets](#-versioning-datasets-d4-e3-i3)
  - [🗃 Interplanetary DevOp](#-interplanetary-devops-d4-e2-i2)
  - [📖 The World's Knowledge becomes accessible through the DWeb](#-the-worlds-knowledge-becomes-accessible-through-the-dweb-d5-e2-i5)
  - [🌐 WebOS](#-webos-d5-e2-i3)

## IPFS Mission Statement

In order to:
- Ensure that all people have the ability to efficiently access and grow humanity's knowledge.
- Mindfully develop new technologies that preserve and promote rights of individuals.
- Support a persistent, upgradable, and open internet.

We believe that:

**All information on the internet should be uniquely and permanently content-addressed on a distributed peer-to-peer web.**

## 2019 Priority

We will be focusing our efforts into a single (lazer focus) priority. **📦 Supporting Package Managers**

Adding end-to-end support for package managers will provide a verifiable and co-hostable foundation for a vital use-case that we rely on. It will focus us on delivering performance and stability improvements while introducing IPFS to a huge community who have the skills to contribute back. See inbound interest [here](https://github.com/ipfs/notes/issues?q=is%3Aissue+is%3Aopen+label%3A%22package+managers%22).

At the same time, we will continue supporting **🤝 Supporting community growth** in best way we can, without diverging too much from our main Priority. We want ensure that we are setting up our community for success by addressing key needs to unlock their growth in 2019. Making our users successful and delivering on their top needs to ensure they have a smooth and productive experience with IPFS helps us retain and gain adoption, grow our community, increase our impact, and demonstrate our maturity as a project.

**Why setting a single priority?**

The 2019 priority is geared to grow our maturity as a project, increase our adoption and community, and set ourselves up for the future. To be successful, we need to level-up our ability to land complete, polished, and accessible improvements that meet our user's needs for stability, scalability, privacy, and security. We need to keep growing intelligently, both by the types of communities that can help us accelerate growth and by the number of users they can help us reach. And we need to set ourselves up with the understanding and capabilities to reach our future goals for the project and scale our impact. We are confident that by aligning on *one* ambitious priority, we will be leveling up the core baseline of the IPFS Protocol, making it ready to tackle all the other goals that follow. 

To help us identify our top priority, we designed a sorting function to prioritize goals that 1) we can land end-to-end in 2019, 2) will bring new partners and users into the community, and 3) will set us up for future goals while delivering near-term value. After sorting, we identified what was the most achiavable (lower D) with largest Ecosystem Growth (higher E) and that would translate into Impact to our Ecosystems and Project (higher I).

**Sorting Function Explanation**

> **D** = Difficulty (or "Delta" or "Distance"), **E** = Ecosystem Growth, **I** = Importance

Each goal was given a score from 1 (low) - 5 (high) on each axis. We sorted first in terms of low difficulty or "delta" (i.e.  minimal additional requirements and fewer dependencies from the capabilities IPFS has now), then high ecosystem growth (growing our community and resources to help us gravity assist and accelerate our progress), and finally high importance (we want IPFS to have a strong, positive impact on the world). See the [2019 Goals (expanded)](#2019-goals-expanded) and [2020+ Goals](#2020-goals) sections for sorted priorities.

## 2019 Working Groups Roadmaps

The IPFS project is the collective work of serveral focused teams, called Working Groups. Each group defines its own roadmap with tasks and priorities derived from the main IPFS Project Priority for 2019 described above. You can drill-down into each roadmap to get the full picture, or jump to the [2019 epics](#2019-epics) section below for the highlights.

- [Project WG](WG_PROJECT.md)
- [JS Core](WG_JS_CORE.md)
- [Go Core](WG_GO_CORE.md)
- [GUI](WG_GUI.md)
- [Cluster](WG_CLUSTER.md)
- [IPFS Infrastructure](WG_INFRASTRUCTURE.md)
- [Community](WG_COMMUNITY.md)
- [Integration in Web Browsers](WG_INTEGRATION_IN_WEB_BROWSERS.md)
- [Dynamic Data & Capabilities](WG_DYNAMIC_DATA_AND_CAPABILITIES.md)
- [Decentralized Data Stewardship](WG_DECENTRALIZED_DATA_STEWARDSHIP.md)

## 2019 IPLD & libp2p Roadmaps

You can find the IPFS sister projects Roadmaps at:

- [libp2p](https://docs.google.com/document/d/1Rd4yNw1TNQBvfRrKeEMSTseb6fvPzS-C--obOn0nul8/edit)
- [IPLD](https://github.com/ipld/roadmap)

## 2019 Epics

We've distilled the key themes from the Working Group Roadmaps into a list Epic Endeavours that give an overview of the primary targets IPFS has for 2019. If you are pumped about these Epics and want to help, you can get involved! See the call to action (CTA) for each section below.

### 1. The reference implementations of the IPFS Protocol (Go & JS) becomes Production Ready

We've been working hard on improving and iterating on the IPFS Protocol to make sure it serves its users needs and achieves the goal of giving the Web a new super power: Content Addressing. In 2019 we will solidify the core components and ensure IPFS is ready for production systems. Our goals include:
- IPFS core solidified and APIs revamped/crystalized to be future-proof
- Complete Specification of the Protocol
- Security Audits and Security Program
- Go and JS IPFS enable modern IPFS data formats ([UnixFSv2](https://github.com/ipfs/unixfs-v2), [CIDv1](https://github.com/ipld/cid), raw blocks) by default
- Bring js-ipfs and go-ipfs to v1.0.0

You can contribute to these Epic by testing, debugging, documenting or coding on either Go or JS IPFS. Both teams have a chat every week that you can join. [Go](https://github.com/ipfs/team-mgmt/blob/master/MGMT_GOLANG_CORE_DEV.md) & [JS](https://github.com/ipfs/team-mgmt/blob/master/MGMT_JS_CORE_DEV.md#weekly-core-dev-team-calls).

### 2. Support Software Package Managers into entering the Distributed Web

Software Package Managers are an ideal use-case for Content Addressing. Developers could fetch packages team mates on their local network instead of asking a centralized Package Registries and our tools could verify that the code we run is exactly the code that the authors intended.
- Kick-off a Package Managers Working Group to work closely with different Package Managers and understand each one challenges and needs.
- Publish a report on the results from adding the NPM Registry to IPFS.
- Meet the scalability and performance needs to serve the Package Management user-case.

We will be booting the Package Managers Working Group in early 2019, meanwhile, check out [NPM on IPFS](https://github.com/ipfs-shipyard/npm-on-ipfs) & [GX](https://github.com/whyrusleeping/gx) to get a feel for what IPFS can contribute to Package Management.

### 3. Scale the IPFS Network

To support the continued growth of the IPFS Network, we will be testing, benchmarking the protocol at scale.
- Deploy a P2P testbed for Distributed Protocols that enables us to spin up hundreds of thousands of nodes on demand and run tests on them.
- IPFS has an opt-in Telemetry system so that tests can collect key data to understand the experiments.

Our friends from libp2p will be playing the larger role into achieving this goal. If you are a Networks specialist and/or if you like scaling systems to serve hundreds of millions, join the conversation at [Bi-Weekly Call](https://github.com/libp2p/team-mgmt#bi-weekly-call) and learn more.

### 4. The IPFS Community gets together for the 1st [IPFS Conf](https://github.com/ipfs/conf)

Yes, you read the title right. The IPFS Community is going to organise the first "IPFS Conf" in the beautiful city of Lisbon. This will be an event for all the users and builders of the DWeb to come together to learn about the exciting progress that has been happening.
- Host the 1st Conference for the IPFS Community.

More details will be public soon, meanwhile, make plans to visit Lisbon in June! Subscribe for updates [here](https://github.com/ipfs/conf#ipfsconf-lisbon-2019).

### 5. IPFS testing, benchmarks, and performance optimizations

In order to prepare ourselves for production readiness and ensure IPFS is optimized for a variety of real-world use cases, we'll double down on testing and benchmarking in 2019.
- Testing harness and environments that simulate different topologies / network configurations.
- Tests for Interoperability, Performance Benchmarks, Reliability, and Network churn.
- Performance overhaul for resolving (IPNS), finding (Providers), transferring, and adding files.

### 6. Support the growing IPFS Community

The IPFS Community is composed of many enthusiasts from the DWeb, P2P, Crypto, Privacy, builders, Web 3.0, Blockchain and many more. Today we have an impressive 3700+ contributors directly improving the IPFS, libp2p, IPLD and Multiformats repos, but there are tens of thousands more contributing to Apps, Libraries and Systems that build on top of IPFS everyday! In 2019, we want to provide a rich platform for all these contributors to share their ideas, get their questions heard, cross-pollinate and tackle new challenges!
- The documentation on IPFS and its libraries gets revamped and becomes part of continuous delivery.
- Increase awareness and adoption through Community outreach via presentations, guides / how-tos, meetups, and quarterly IPFS Project updates.
- Support contributor productivity and impact through Quarterly User Reports, fast code reviews, and DevOps automation.
- Create IPFS Dev Grant and Research Grant programs to encourage global engagement with the cutting-edge work in the IPFS ecosystem.
- Launch [ProtoSchool](https://proto.school/), an interactive way to learn how to build on the P2P Web.
- IPFS Community Meetups receive an upgrade with education materials (guides, tutorials, workshops, talks) to boost the leveling up DWeb communities.

## 2019 Goal (expanded)

### 📦 Package Managers (D1 E5 I3)

> The most used code and binary Package Managers are powered by IPFS.

Package Managers collect and curate sizable datasets. Top package managers distribute code libraries (eg npm, pypi, cargo, ...), binaries and program source code (eg apt, pacman, brew ...), full applications (app stores), datasets, and more. They are critical components of the programming and computing experience, and are the perfect use case for IPFS.

Most package managers can benefit tremendously from the content-addressing, peer-to-peer, decentralized, and offline capabilities of IPFS. Existing Package Managers should switch over to using IPFS as a default, or at least an optional way of distributing their assets, and their own updates. New Package Managers should be built entirely on IPFS. --- Code libraries, programs, and datasets should become permanent, resilient, partition tolerant, and authenticated, and IPFS can get them there. Registries become curators and seeds, but do not have to bear the costs of the entire bandwidth. Registries could become properly decentralized. --- We have a number of challenges ahead to make this a reality, but we are already beyond half-way. We should be able to get top package managers to (a) use IPFS as an optional distribution mechanism, then (b) use that to test all kinds of edge cases in the wild and to drive performance improvements , then (c) get package managers to switch over the defaults.

## 2020+ Goals

The following years' plan will be laid out during 2019. One of the goals for 2019 is to have a high-level 5 year (or decade) long view of the IPFS Project focus.

### 🗂 Large Files (D1 E4 I3)

> By 2020, IPFS becomes the default way to distribute files or collections of files above 1GB

HTTP is not good for distributing large files or large collections of small files. Anything above 1GB starts running into problems (resuming, duplication, centralized bandwidth limitations, etc). BitTorrent works well for single archives that won't change, or won't duplicate, but fails in a number of places. IPFS has solved most of the hard problems but hasn't yet made the experience so easy that people default to IPFS to distribute large files. IPFS should solve this problem so well, it should be so easy and delightful to use, and it should be so high performance that it becomes the default way to move anything above 1GB world-wide. This is a massive hole right now that IPFS is well-poised to fill -- we just need to solve some performance and usability problems.

### 🔄 Decentralized Web (D2 E4 I3)

> IPFS supports decentralized web apps built on p2p connections with power and capabilities at the edges.

In web 2.0, control of the web is centralized - its location-addressing model and client-server architecture encourage reliance and trust of centralized operators to host services, data, and intermediate connections. Walled gardens are common, and our data is locked into centralized systems that increase the risk of privacy breaches, state control, or that a single party can shut down valued services. The decentralized web is all about peer-to-peer connections and putting users in control of their tools and data. It does this by connecting users directly to each other and using verifiable tools like hash-links and encryption to ensure the power and control in the network is retained by the participants themselves. The decentralized web (as distinguished from Distributed Web) is NOT about partition tolerance, or making the web work equally well in local-area networks/mobile/offline - the focus here is on the control and ownership of services.

IPFS has solved most of the hard underlying design problems for decentralized web, but hasn't yet made the experience easy enough for end-users to experience it in the applications, tools, and services they use. This requires tooling and solutions for developers to sustainably run their business without any centralized intermediary facilitating the network (though centralized providers may still exist to augment and improve the experience for services that already work decentralized by design). Designing Federation for interop with current systems is key for the Migration Path.

### 🔒 Encrypted Web (D2 E3 I4)

> Apps and Data are fully end-to-end encrypted at rest. Users have reader, writer, and usage privacy.

Apps and user data on IPFS are completely end-to-end encrypted, at rest, with only users having access. Users get reader and writer privacy by default. Any nodes providing services usually do so over encrypted data and never get access to the plain data. The apps themselves are distributed encrypted, decrypted and loaded in a safe sandbox in the users' control. Attackers (including ISPs) lose the ability to spy on users' data, and even which applications users are using. This works with all top use case apps -- email, chat, forums, collaboration tools, etc.

### ♻️ Distributed Web (D2 E2 I4)

> Info and apps function equally well in local area networks and offline. The Web is a partitionable fabric, like the internet.

The web and mobile -- the most important application platforms on the planet -- are capable of working entirely in sub-networks. The norm for networked apps is to use the available data and connections, to sync asynchronously, and to leverage local connectivity protocols. The main apps for every top use case work equally well in offline or local network settings. It means IPFS and apps on top work excellently on desktops, the browser, and mobile. Users can use webapps like email, chat, forums, social networks, collaboration tools, games, and so on without having to be connected to the global internet. Oh, and getting files from one computer to another right next to it finally becomes an easy thing to do (airdrop level of easy).

### 👩🏽‍💻 Personal Web (D3 E4 I2)

> Personal Data and programs are under user control.

The memex becomes reality. The web becomes a drastically more personal thing. Users' data and exploration is under the users' control -- similar to how a "personal computer" is under the user's control, and "the cloud" is not. Users decide which apps and other people get access to their data. Explorations can be recorded for the user in memex fashion. The user gets to keep copies of all the data they have observed through the web. A self-archiving personal record forms, which the user can always go back to, explore, and use -- whether or not those applications are still in development by their authors.

### 👟 Sneaker Web (D3 E2 I4)

> The web functions over disconnected sneaker networks, spreading information, app data, apps, and more.

The web is capable of working fully distributed, and can even hop across disconnected components of the internet. Apps and their data can flow across high latency, intermittent, asynchronous links across them. People in disconnected networks get the same applications, the same quality of experience, and the same ability to distribute their contributions as anybody in the strongest connected component ("the backbone of the internet"). The Web is totally resistant to large scale partitions. Information can flow so easily across disconnected components that there is no use in trying to block or control information at the borders.

### 🚀 Interplanetary Web - Mars 2024. (D3 E3 I4)

> **Mars**. Let's live the interplanetary dream!**

SpaceX plans to land on mars in 2022, and send humans in 2024. By then, IPFS should be the default/best choice for SpaceX networking. The first humans on mars should use IPFS to run the top 10 networked apps. That means truly excellent and well-known IPFS apps addressing the top 10 networked use cases must exist. For that to happen, the entire system needs to be rock solid, audited, performant, powerful, easy-to-use, well known, and so on. It means IPFS must work on a range of platforms (desktop, servers, web, mobile), and to work with both special purpose local area networks, and across interplanetary distances. If we achieve this, while solving for general use and general users (not specifically for the Mars use case, then IPFS will be in tremendous standing.

### 💾 Packet Switched Web (D3 E2 I3)

> IPFS protocols use packet switching, and the network can relay all kinds of traffic easily, tolerating switch failures.

The infrastructure protocols (libp2p, IPFS, etc.) and the end-user app protocols (the logic of the app) can work entirely over a packet switching layer. Protocols like BitSwap, DHT, PubSub become drastically higher performance, and unconstrained by packets sent before theirs. Web applications can form their own isolated virtual networks, allowing their users to distribute the packets. Users can form their own groups and their own virtual networks, allowing users to only operate in a subnet they trust, and ensure all of their traffic is moving between trusted switches. The big public network uses packet switching by default.

### 📑 Data Web (D4 E3 I3)

> Large Datasets are open, easy to access, easy to replicate, version controlled, secure, permanent.

We constantly loose access to important information, either because it ceasis to exist or simply due to _virtual virtual_ barriers (i.e. censorship, lack of connectivity and so on). Information also often looses its way into the peers that most needed it and there aren't good ways to signal that some dataset wasn't contemplated, referenced. We want to improve this dramatically, making the data that is produced more easy to access through making it versionased, secure and easier to replicate and locate.

### ✉️ Package Switched Web (D4 E2 I2)

> Data in the web can be moved around over a package switching network. Shipping TB or PB hard drives of data becomes normal.

Beyond circuit switching and packet switching, the web works over package switching! It is possible to send apps, app assets, app user generated data, and so on through hard drives means. This means that the network stack and the IPLD graph sync layers are natively capable of using data in external, removable media. It is easy for a user Alice to save a lot of data to a removable drive, for Alice to mail the drive to another user Bob, and for Bob to plug in the drive to see his application finish loading what Alice wanted to show Bob. Instead of having to fumble with file exports, file systems, OS primitives, and worse -- IPFS, libp2p, and the apps just work -- there is a standard way to say "i want this data in this drive", and "i want to use the data from this drive". Once that happens, it can enable proper sneakernet web.

### ⛓ Self-Archiving Web (D4 E4 I4)

> The Web becomes permanent, no more broken Links. Increase the lifespan of a Webpage from 6 months to ∞ (as good as a book).

The Internet Archive(s, plural) Content Address their snapshots to maximize deduplications and hit factor. IPFS becomes the platform that enables the multiple Internet Archives to store, replicate and share responsibility over who possesses what. It becomes simple for any institution (from large organization to small local library) to become an Internet Archive node. Users can search through these Internet Archives nodes, fully compliant with data protection laws.

### 🏷 Versioning Datasets (D4 E3 I3)

> IPFS becomes the default way to version datasets, and unlocks a dataset distribution and utility explosion similar to what VCS did for code.

IPFS emerged from dataset versioning, package management, and distribution concerns. There are huge gaping holes in this space because large datasets are very unwieldy and defy most systems that make small files easy to version, package, and distribute. IPFS was designed with this kind of problem in mind and has the primitives in place to solve many of these problems. There are many things missing: (a) most importantly, a toolchain for version history management that works with these large graphs (most of what git does). (b) Better deduplication and representation techniques. (c) Virtual filesystem support -- to plug under existing architectures. (d) Ways to easily wrap existing data layouts (filestore) -- to plug on top existing architectures. (e) An unrelenting focus on extremely high performance. (f) primitives to retrieve and query relevant pieces of versioned datasets (IPLD Selectors and Queries). --- But luckily, all of these things can be added incrementally to enhance the tooling and win over more user segments.

### 🗃 Interplanetary DevOps (D4 E2 I2)

> Versioning, packaging, distribution, and loading of Programs, Containers, OSes, VMs, defaults to IPFS.

IPFS is great for versioning, deduping, packaging, distributing assets, through a variety of mediums. IPFS can revolutionize computing infrastructure systems. It has the potential to become the default way for datacenter and server infrastructure users to set up their infrastructure. This can happen at several different layers. (a) In the simplest sense, IPFS can help distribute programs to servers, by sitting within the OS, and plugging in as the downloading mechanism (replace wget, rsync, etc.).  (b) IPFS can also distribute containers -- it can sit alongside docker, kubernetes, and similar systems to help version, dedup, and distribute containerized services. (c) IPFS can also distribute OSes themselves, by plugging in at the OS package manager level, and by distributing OS installation media. (d) IPFS can also version, dedup, and distribute VMs, first by sitting alongside host OSes and hypervisors moving around VM snapshots, and then by modeling VMs themselves on top of IPFS/IPLD. --- To get there, we will need to solve many of the same problems as package managers, and more. We will need the IPLD importers to model and version the media super-effectively.

### 📖 The World's Knowledge becomes accessible through the DWeb (D5 E2 I5)

Humanity deserves equal access to the Knowledge. Platforms such as Wikipedia, Coursera, Edx, Khan Academy and others need to be available independently of Location and Connectivity. The content of this services need to exist everywhere. These replicas should be part of the whole world's dataset and not disjoint dataset. Anyone should be able to access these through the protocol, without having to deploy new services per area.

### 🌐 WebOS (D5 E2 I3)

> The Web Platform and the OS'es merge.

The rift between the web and the OS is finally healed. The OS and local programs and WebApps merge. They are not just indistinguishable, they are _the same thing_. "Installing" becomes pinning applications to the local computer. "Saving" things locally is also just pinning. The browser and the OS are no longer distinguishable. The entire OS data itself is modelled on top of IPLD, and the internal FileSystem is IPFS (or something on top, like unixfs). The OS and programs can manipulate IPLD data structures natively. The entire state of the OS itself can be represented and stored as IPLD. The OS can be frozen or snapshotted, and then resumed. A computer boots from the same OS hash, drastically reducing attack surface.
