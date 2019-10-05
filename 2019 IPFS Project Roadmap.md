# 2019 IPFS Project Roadmap
_This is an archive of the 2019 IPFS project roadmap and goals for the year._

## Table of Contents
- [IPFS Mission Statement](#ipfs-mission-statement)
- [2019 Priorities](#2019-priorities)
- [2019 Working Groups Roadmaps](#2019-working-groups-roadmaps)
- [2019 IPLD & libp2p Roadmaps](#2019-ipld--libp2p-roadmaps)
- [2019 Epics](#2019-epics)
- [2019 Goal (expanded)](#2019-goal-expanded)
  - [📦 Package Managers](#-package-managers-d1-e5-i3)

## IPFS Mission Statement

In order to:
- Ensure that all people have the ability to efficiently access and grow humanity's knowledge.
- Mindfully develop new technologies that preserve and promote rights of individuals.
- Support a persistent, upgradable, and open internet.

We believe that:

**All information on the internet should be uniquely and permanently content-addressed on a distributed peer-to-peer web.**

## 2019 Priority

We will be focusing our efforts for 2019 into a single (lazer focus) priority. **📦 Package Managers**

Adding end-to-end support for package managers will provide a verifiable and co-hostable foundation for a vital use-case that we rely on. It will focus us on delivering performance and stability improvements while introducing IPFS to a huge community who have the skills to contribute back. See inbound interest [here](https://github.com/ipfs/notes/issues?q=is%3Aissue+is%3Aopen+label%3A%22package+managers%22).

At the same time, we will continue supporting **🤝 Community Growth** in the best way we can, without diverging too much from our main Priority. We want ensure that we are setting up our community for success by addressing key needs to unlock their growth in 2019. Making our users successful and delivering on their top needs to ensure they have a smooth and productive experience with IPFS helps us retain and gain adoption, grow our community, increase our impact, and demonstrate our maturity as a project.

**Why setting a single priority?**

The 2019 priority is geared to grow our maturity as a project, increase our adoption and community, and set ourselves up for the future. To be successful, we need to level-up our ability to land complete, polished, and accessible improvements that meet our user's needs for stability, scalability, privacy, and security. We need to keep growing intelligently, both by the types of communities that can help us accelerate growth and by the number of users they can help us reach. And we need to set ourselves up with the understanding and capabilities to reach our future goals for the project and scale our impact. We are confident that by aligning on *one* ambitious priority, we will be leveling up the core baseline of the IPFS Protocol, making it ready to tackle all the other goals that follow. 

To help us identify our top priority, we designed a sorting function to prioritize goals that 1) we can land end-to-end in 2019, 2) will bring new partners and users into the community, and 3) will set us up for future goals while delivering near-term value. After sorting, we identified what was the most achiavable (lower D) with largest Ecosystem Growth (higher E) and that would translate into Impact to our Ecosystems and Project (higher I).

**Sorting Function Explanation**

> **D** = Difficulty (or "Delta" or "Distance"), **E** = Ecosystem Growth, **I** = Importance

Each goal was given a score from 1 (low) - 5 (high) on each axis. We sorted first in terms of low difficulty or "delta" (i.e.  minimal additional requirements and fewer dependencies from the capabilities IPFS has now), then high ecosystem growth (growing our community and resources to help us gravity assist and accelerate our progress), and finally high importance (we want IPFS to have a strong, positive impact on the world). See the [2019 Goals (expanded)](#2019-goals-expanded) and [2020+ Goals](#2020-goals) sections for sorted priorities.

**February Roadmap Update**

We rescoped our 2019 priorities in early Q1 2019 to narrow in from 3 top-level priorities (also including [Large Files](README.md/#-large-files-d1-e4-i3) and [Decentralized Web](README.md/#-decentralized-web-d2-e4-i3)) to one ([Package Managers](README.md/#-package-managers-d1-e5-i3)) - so we could focus on doing the most important work *really well* instead of spreading ourselves too thin on many priorities, which we already felt ourselves doing. This descoping impacted the working group roadmaps we had drafted, and the Q1 OKRs we had already taken on. However, we decided to finish out our Q1 endeavors while we descoped our working group roadmaps and packaged up out-of-scope projects to set down smoothly, and to start our revamped roadmaps in Q2 with more focused and streamlined objectives, initiatives, and goals.

## 2019 Working Groups Roadmaps

The IPFS project is the collective work of serveral focused teams, called Working Groups. Each group defines its own roadmap with tasks and priorities derived from the main IPFS Project Priority for 2019 described above. You can drill-down into each roadmap to get the full picture, or jump to the [2019 epics](#2019-epics) section below for the highlights.

- [Project WG](2019%20WG%20roadmaps/WG_PROJECT.md)
- [JS Core](2019%20WG%20roadmaps/WG_JS_CORE.md)
- [Go Core](2019%20WG%20roadmaps/WG_GO_CORE.md)
- [GUI](2019%20WG%20roadmaps/WG_GUI.md)
- [Cluster](2019%20WG%20roadmaps/WG_CLUSTER.md)
- [IPFS Infrastructure](2019%20WG%20roadmaps/WG_INFRASTRUCTURE.md)
- [Community](2019%20WG%20roadmaps/WG_COMMUNITY.md)
- [Integration in Web Browsers](2019%20WG%20roadmaps/WG_INTEGRATION_IN_WEB_BROWSERS.md)
- [Dynamic Data & Capabilities](2019%20WG%20roadmaps/WG_DYNAMIC_DATA_AND_CAPABILITIES.md)
- [Decentralized Data Stewardship](2019%20WG%20roadmaps/WG_DECENTRALIZED_DATA_STEWARDSHIP.md)

## 2019 IPLD & libp2p Roadmaps

You can find the IPFS sister projects' Roadmaps for 2019 at:

- [libp2p](https://docs.google.com/document/d/1Rd4yNw1TNQBvfRrKeEMSTseb6fvPzS-C--obOn0nul8/edit)
- [IPLD](https://github.com/ipld/roadmap)

## 2019 Epics

We've distilled the key themes from the Working Group Roadmaps into a list of **Epic Endeavours** that give an overview of the primary targets IPFS has for 2019. See the call to action (CTA) for each section below for how you can get involved.

### 1. The reference implementations of the IPFS Protocol (Go & JS) becomes Production Ready

We've been working hard on improving and iterating on the IPFS Protocol to make sure it serves its users needs and achieves the goal of giving the Web a new super power: Content Addressing. In 2019 we will solidify the core components and ensure IPFS is ready for production systems. Our goals include:
- IPFS core solidified and APIs revamped/crystalized to be future-proof 🔁 / ❌
- Complete Specification of the Protocol ❌
- Security Audits and Security Program 🔁
- Go and JS IPFS enable modern IPFS data formats ([UnixFSv2](https://github.com/ipfs/unixfs-v2), [CIDv1](https://github.com/ipld/cid), raw blocks) by default and in a reproducible way 🔁 / ✅
- The migration to Base32 CIDs is completed across all projects and IPFS Gateway. ✅

You can contribute to these Epic by testing, debugging, documenting or coding on either Go or JS IPFS. Both teams have a chat every week that you can join. [Go](https://github.com/ipfs/team-mgmt/blob/master/MGMT_GOLANG_CORE_DEV.md) & [JS](https://github.com/ipfs/team-mgmt/blob/master/MGMT_JS_CORE_DEV.md#weekly-core-dev-team-calls).

### 2. Support Software Package Managers in entering the Distributed Web

Software Package Managers are an ideal use-case for Content Addressing. Developers could fetch packages team mates on their local network instead of asking a centralized Package Registries and our tools could verify that the code we run is exactly the code that the authors intended.
- Kick-off a Package Managers Working Group to work closely with different Package Managers and understand each one challenges and needs. ✅
- Publish a report on the results from adding the NPM Registry to IPFS. 🔁
- Meet the scalability and performance needs to serve the Package Management user-case. 🔁

We will be booting the Package Managers Working Group in early 2019, meanwhile, check out [NPM on IPFS](https://github.com/ipfs-shipyard/npm-on-ipfs) & [GX](https://github.com/whyrusleeping/gx) to get a feel for what IPFS can contribute to Package Management.

### 3. Scale the IPFS Network

To support the continued growth of the IPFS Network, we will be testing and benchmarking the protocol at scale.
- Deploy a P2P testbed for Distributed Protocols that enables us to spin up hundreds of thousands of nodes on demand and run tests on them. 🔁
- IPFS has an opt-in Telemetry system so that tests can collect key data to understand the experiments. ❌

Our friends from libp2p will be playing the larger role in achieving this goal. If you are a Networks specialist and/or if you like scaling systems to serve hundreds of millions, join the conversation in the [Bi-Weekly Libp2p Call](https://github.com/libp2p/team-mgmt#bi-weekly-call) and learn more.

### 4. The IPFS Community of Builders gets together for the 1st [IPFS Camp](https://github.com/ipfs/camp)

Yes, you read the title right. The IPFS Community is going to meet for the first large IPFS Event. This will be an event for all the users and builders of the DWeb to come together to learn about the exciting progress that has been happening.
- Host the 1st Conference for the IPFS Community. ✅

More details will be public soon. Subscribe for updates [here](https://github.com/ipfs/camp).

### 5. IPFS testing, benchmarks, and performance optimizations

In order to prepare ourselves for production readiness and ensure IPFS is optimized for a variety of real-world use cases, we'll double down on testing and benchmarking in 2019.
- Testing harness and environments that simulate different topologies / network configurations. 🔁
- Tests for Interoperability, Performance Benchmarks, Reliability, and Network churn. ~✅
- Performance overhaul for resolving (IPNS), finding (Providers), transferring, and adding files. 🔁

### 6. Support the growing IPFS Community

The IPFS Community is composed of many enthusiasts from the DWeb, P2P, Crypto, Privacy, builders, Web 3.0, Blockchain and many more. Today we have an impressive 3700+ contributors directly improving the IPFS, libp2p, IPLD and Multiformats repos, but there are tens of thousands more contributing to Apps, Libraries and Systems that build on top of IPFS everyday! In 2019, we want to provide a rich platform for all these contributors to share their ideas, get their questions heard, cross-pollinate and tackle new challenges!
- The documentation on IPFS and its libraries gets revamped and becomes part of continuous delivery. 🔁
- Increase awareness and adoption through Community outreach via presentations, guides / how-tos, meetups, and quarterly IPFS Project updates. ✅
- Support contributor productivity and impact through Quarterly User Reports, fast code reviews, and DevOps automation. ❌
- Create IPFS Dev Grant and Research Grant programs to encourage global engagement with the cutting-edge work in the IPFS ecosystem. 🔁
- Launch [ProtoSchool](https://proto.school/), an interactive way to learn how to build on the P2P Web. ✅
- IPFS Community Meetups receive an upgrade with education materials (guides, tutorials, workshops, talks) to boost the leveling up DWeb communities. 🔁

## 2019 Goal (expanded)

### 📦 Package Managers (D1 E5 I3)

> The most used code and binary Package Managers are powered by IPFS.

Package Managers collect and curate sizable datasets. Top package managers distribute code libraries (eg npm, pypi, cargo, ...), binaries and program source code (eg apt, pacman, brew ...), full applications (app stores), datasets, and more. They are critical components of the programming and computing experience, and are the perfect use case for IPFS.

Most package managers can benefit tremendously from the content-addressing, peer-to-peer, decentralized, and offline capabilities of IPFS. Existing Package Managers should switch over to using IPFS as a default, or at least an optional way of distributing their assets, and their own updates. New Package Managers should be built entirely on IPFS. --- Code libraries, programs, and datasets should become permanent, resilient, partition tolerant, and authenticated, and IPFS can get them there. Registries become curators and seeds, but do not have to bear the costs of the entire bandwidth. Registries could become properly decentralized. --- We have a number of challenges ahead to make this a reality, but we are already beyond half-way. We should be able to get top package managers to (a) use IPFS as an optional distribution mechanism, then (b) use that to test all kinds of edge cases in the wild and to drive performance improvements , then (c) get package managers to switch over the defaults.
