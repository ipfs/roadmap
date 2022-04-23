# IPFS Project Roadmap v0.6.0

## Table of Contents

- [IPFS Mission Statement](#ipfs-mission-statement)
- [2021 & 2022 Priorities](#2021--2022-priorities)
- [2020 Priority](#2020-priority)
  - [📞 Content Routing](#-content-routing)
- [2019 Priority](#2019-priority)
  - [📦 Package Managers](#-package-managers-d1-e5-i3)
- [Future Goals](#future-goals)
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
  - [🗃 Interplanetary DevOps](#-interplanetary-devops-d4-e2-i2)
  - [📖 The World's Knowledge becomes accessible through the DWeb](#-the-worlds-knowledge-becomes-accessible-through-the-dweb-d5-e2-i5)
  - [🌐 WebOS](#-webos-d5-e2-i3)

## IPFS Mission Statement

**The mission of IPFS is to create a resilient, upgradable, open network to preserve and grow humanity’s knowledge.**

## 2021 & 2022 Priorities
For 2021 and 2022, core IPFS implementation planning & progress tracking has moved to GitHub projects for more iterative sprint planning. You can track past and upcoming releases - and the improvements they contain - here:
- [go-ipfs](https://github.com/ipfs/go-ipfs)
  -  Past releases: https://github.com/ipfs/go-ipfs/releases
  -  Upcoming priorities: https://github.com/orgs/ipfs/projects/16/views/3
- [js-ipfs](https://github.com/ipfs/js-ipfs/)
  - Past releases: https://github.com/ipfs/js-ipfs/releases
  - Upcoming priorities: https://github.com/orgs/ipfs/projects/13
- [rust-ipfs](https://github.com/rs-ipfs/rust-ipfs)
  - Progress: https://areweipfsyet.rs/
- [IPFS GUIs](https://github.com/ipfs/ipfs-webui)
  - Past releases: https://github.com/ipfs/ipfs-webui/releases, https://github.com/ipfs/ipfs-desktop/releases
  - Upcoming priorities: https://github.com/orgs/ipfs/projects/17

## 2020 Priority

### 📞 Content Routing
Our core goal for 2020 was to **improve the performance and reliability of *content routing* in the IPFS network**. 'Content routing' is the process of finding a node hosting the content you're looking for, such that you can fetch the desired data and quickly load your website/dapp/video/etc. As the IPFS network scaled in 2019 (over 30x!), it ran into new problems in our distributed routing algorithms - struggling to find content spread across many unreliable nodes. This was especially painful for [IPNS](https://docs.ipfs.io/guides/concepts/ipns/), which relied on _multiple_ of these slow/unreliable queries to find the latest version of a file. These performance gaps caused IPFS to lag and stall while searching for the needed content, hurting the end user experience and making IPFS "feel broken". Searching the network to find desired content (aka, using IPFS as a decentralized CDN) is one of the most common actions for new IPFS users and is required by most ipfs-powered dapp use cases - therefore, it was the main pain point we needed to mitigate in order to unlock increased adoption and scalability of the network.

We considered a number of other potential goals - especially all the great [2020 Theme Proposals](https://github.com/ipfs/roadmap/issues/) - before selecting this priority. However, we decided it was more important to focus core working group dev time on the main blockers and pain points to enable the entire ecosystem to grow and succeed. Being able to focus narrowly on IPFS Content Routing performance had major wins! Content routing speed is now ~0.5 seconds on average to find new content added to the IPFS Public Network, a >60x improvement from the start of 2020, and 10x better than our 2020 goal!

### Graded 2020 Epics
1. Build IPFS dev capacity and velocity (research development, DevGrants, Github cleanups, dev tooling, focus) 🔁✅
2. Improve content routing performance such that 95th percentile content routing speed is <5s (libp2p DHT, Testground, performance monitoring) ✅
3. Invest in IPFS community enablement and support (IPFS in browsers, documentation, collabs) ✅


## 2019 Priority

Our core goal for 2019 was to make large-scale improvements to the IPFS network around scalability, performance, and usability. By focusing on the **📦 Package Managers** use case, we hoped to identify, prioritize, and demonstrably resolve performance/usability issues, while driving adoption via a common and compelling use case that all developers experience daily. We hoped this focus would help us hone IPFS to be production ready (in functionality and practice), help scale network usage to millions of nodes, and accelerate our project and community growth/velocity.

### Graded 2019 Epics
1. The reference implementations of the IPFS Protocol (Go & JS) become Production Ready 🔁✅
1. Support Software Package Managers in entering the Distributed Web ❗️
1. Scale the IPFS Network 🔁
1. The IPFS Community of Builders gets together for the 1st IPFS Conf ✅
1. IPFS testing, benchmarks, and performance optimizations 🔁
1. Support the growing IPFS Community ✅

You can see the details in what work we took on in each milestone, and which we achieved in the archived [2019 IPFS Project Roadmap](https://github.com/ipfs/roadmap/blob/master/2019-IPFS-Project-Roadmap.md).

### Sorting Function
> D = Difficulty (or "Delta" or "Distance"), E = Ecosystem Growth, I = Importance

To identify our top focus for 2019 and rank the future goals in our upgrade path, we used a sorting function to prioritize potential focus areas. Each goal was given a score from 1 (low) - 5 (high) on each axis. We sorted first in terms of low difficulty or "delta" (i.e. minimal additional requirements and fewer dependencies from the capabilities IPFS has now), then high ecosystem growth (growing our community and resources to help us gravity assist and accelerate our progress), and finally high importance (we want IPFS to have a strong, positive impact on the world). Future goals below are listed in priority order using this sorting function.

### 📦 Package Managers (D1 E5 I3)

> The most used code and binary Package Managers are powered by IPFS.

Package Managers collect and curate sizable datasets. Top package managers distribute code libraries (eg npm, pypi, cargo, ...), binaries and program source code (eg apt, pacman, brew ...), full applications (app stores), datasets, and more. They are critical components of the programming and computing experience, and are the perfect use case for IPFS.

Most package managers can benefit tremendously from the content-addressing, peer-to-peer, decentralized, and offline capabilities of IPFS. Existing Package Managers should switch over to using IPFS as a default, or at least an optional way of distributing their assets, and their own updates. New Package Managers should be built entirely on IPFS. --- Code libraries, programs, and datasets should become permanent, resilient, partition tolerant, and authenticated, and IPFS can get them there. Registries become curators and seeds, but do not have to bear the costs of the entire bandwidth. Registries could become properly decentralized. --- We have a number of challenges ahead to make this a reality, but we are already beyond half-way. We should be able to get top package managers to (a) use IPFS as an optional distribution mechanism, then (b) use that to test all kinds of edge cases in the wild and to drive performance improvements , then (c) get package managers to switch over the defaults.

## Future Goals

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

We constantly lose access to important information, either because it ceases to exist or simply due to _virtual virtual_ barriers (i.e. censorship, lack of connectivity and so on). Information also often loses its way into the peers that most needed it and there aren't good ways to signal that some dataset wasn't contemplated, referenced. We want to improve this dramatically, making the data that is produced more easy to access through making it versionased, secure and easier to replicate and locate.

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
