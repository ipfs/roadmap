# Dynamic Data & Capabilities Working Group Roadmap for 2019

> Construct the building blocks that enable developers to create DApps on top of IPFS and libp2p.
> More precisely:
> Research and development of building blocks that enable collaborative applications, providing solutions for security, identity, access control, concurrency, synchronization, version control, offline and near-real-time collaboration that can be integrated into IPFS. The Working Group also creates proof of concept applications and works with projects looking to create and maintain production quality dynamic applications built on top of IPFS and libp2p.

**Responsibilities**
- Research solutions for decentralised applications that require security, identity, access control, concurrency, synchronization, offline and near-real-time collaborations.
- Deliver and support  a set of building blocks and frameworks that allow the construction of world-class DApps on top of IPFS and libp2p.
- Ensure that, over time, IPFS core develops new features that support dynamic data.

## 🚀 2019 Major goals

- Improve DX: Create the DApp Toolkit that will allow developers to easily create web DApps that have the capabilities usually provided by generic Web 2.0 dev toolkits.
- Improve UX: Improve User Experience for DApps built on top of IPFS / libp2p.
- End-goal: Increase developer adoption: enable the top 3 Productivity Apps to exist and be used on the DWeb.

## 💎 Milestones

All these milestones are related to the “Decentralised Web” Top Level Priority for 2019 as defined in this document.

### 1. DX

#### 1.1. (DX) Peer-base interfaces and types are well defined, documented, tested and implemented (P0):

*   **Membership**: for a given collaboration, replicate member peers (their addresses, identities and more) to other members
*   **Gossip**: allow peers in an application or collaboration to share a secure channel for sharing data about each other
*   **Identity**: allow peers to identify themselves before others and offer ways for peers to verify that identity
*   **Collaboration**: allow peers to form groups that will collaborate on a given task
*   **Persistence**:
    *   Local persistence (allow data to be persisted locally)
    *   Remote persistence
        *   Collaborative pinning (allow data to be persisted remotely without any centralised service)
        *   Pinning service (allow data to be persisted remotely through a specific service)
*   **Access Control**: based on identity, and for a given collaboration, allow peers to define which sets of operations they're going to accept
*   **Remote Presence**: allow collaborating peers to be informed about each others' presence and actions
*   **Authentication**: allow a peer to authenticate a given piece of data
*   **Identity-based P2P secret sharing**: allow a peer to share a secret that will be authenticated and secret
*   **Personal** **feeds**: allow any peer to expose a set of activity feeds to any permissioned peer
*   **Causal broadcast channel**: create a group messaging channel that respects causality
*   **Collaborative replication**: multi-writer-enabled data types
    *   Op-based CRDTs (Conflict-free replicated data types that are based on a growing set of operations)
    *   Delta state-based CRDTs Conflict-free replicated data types that are based on transmitting deltas or entire states)

#### 1.2. (DX) Peer-base release management is well defined and optimal (P0)

*   Change logs
*   Support migrations for breaking changes
*   Long-lived schema management

#### 1.3. (DX) A methodology for supporting peer-base libraries is defined and implemented (P0)

(look at other OSS projects like IPFS, Node.js)

#### 1.4. (DX) Developers building dynamic DApps on top of IPFS / libp2p are supported (P1)

Identify package maintainers and their responsibilities.

#### 1.5. (DX) Public runtime infrastructure (run by PL) exists and is stable (P1)

Services:
*   Pinners
*   Gateways
*   Websocket-star
*   Replace websocket-star with:
    *   Rendez-vous nodes
    *   Circuit-relay nodes
*   Explore:
    *   Signaling (for signal persistence and execution (support for offline delivery, push messages, etc.))

Notes:
*   Make sure we outsource it to the infra team.
*   Define QoS contract.
*   Gather data about infrastructure usage.
*   Private infrastructure: maybe start conversation about enabling this (talk about features, economics, …).
*   (Talk to partners, like Textile, about needs, scaling, volunteering, ...)

#### 1.6. (DX) Deployment tools, code, instructions and images exist, and are supported (P2)

For deploying apps and all the required services.

Notes:
*   (Requires cooperation with IPFS core, infra, …?)
*   Define which tools should exist
*   Assess which tools exist, who maintains them
*   Idea: piggyback on IPFS desktop?
*   Idea: support infrastructure donation?

#### 1.7. (DX) peer-base v1 has been released (P3)

Depends on M1.1.
Signifies stability to developers.

What does it contain, look like?

#### 1.8. (DX) Online Materials (text mainly, perhaps video) exist and are supported (P3)

*   Logo and Website
*   Text tutorials first (easier to maintain)
    *   Beginner
    *   Intermediate
    *   Advanced
*   Video perhaps, but only for events

#### 1.9. (DX) The working group has partnered with a third party on development of a production-quality collaborative application (P1)

#### 1.10. (DX) peer-base interfaces and types are formally defined (language agnostic) (P4)

Notes:
*   Discuss this with libp2p and IPFS teams.
*   Check out WebIDL.
*   Try to make this more iterative (not waterfall) as peer-base stabilizes so that we can start implementing some of these components in other languages / platforms.

#### 1.11. (DX) Identity Manager PoC v0.1 is released and is easy to integrate into an existing web DApp (well tested and documented) (P4)


#### 1.12. (DX/UX) Chart a collection of UX patterns for DApps (P4)

Notes:

*   Also depends on developers and users to gain literacy about the decentralised concepts

#### 1.13. (DX) Research and document tooling to help with e2e testing for DApps (P3)

### 2. UX

#### 2.1. (UX) An evolving spec for human-friendly way to identify users in DApps was debated and approved - IDM Spec v0.1 (P1)

IDM = Identity Manager

#### 2.2. (UX) A PoC reference implementation for the IDM Spec exists (P2)

Note: (Consider also having a milestone for releasing an IDM MVP).

#### 2.3. (UX) Can replicate app/domain storage using Identity

(Depends on M2.1)

*   It's expected that the same user uses the same DApps on different devices. Research and implement a way for application data produced by the same identity (user) to be synced among devices.
*   It should support multi-writer scenarios

#### 2.4. (UX) It is possible to build web DApps based on peer-base with good performance attributes (P0)

#### Performance

*   Reduce the number of IPFS nodes when running multiple DApps
*   Prevent main thread blocking when:
    *   Doing crypto stuff, perhaps offload to web workers
    *   Accessing IndexedDB
*   Explore: using WebRTC as an alternative web sockets?
*   Replace WS-Star with:
    *   Rendez-vous
    *   Circuit-relay
*   Suggestion: Support Companion and libdweb (libp2p p2p streams over WS + feed of discovery events, exposed by IPFS daemon)
*   **Required: Measure** (automated) and iterate

#### Reliability

*   Solve concurrency problems when two tabs use the same IPFS node

### 3. DApps

### 3.1

#### 3.1.1 (DApps) - PeerPad used as the primary note taking tool inside PL (not be at feature parity with Cryptpad but "good enough", internal users do not rebel) (P1)

#### 3.1.2 (DApps) - PeerPad has comprehensive E2E/load tests (P2)

*   PP tests use common PL testbed (being developed currently by libp2p team) // _cross-team dependency_
*   range of scenarios tested  (single player, normal WG scale, single bad actor, overwhelming load that shows degenerate behavior, etc)

#### 3.1.3 (DApps/UX) - PeerPad feature requirements established based on best industry examples  (P2)

*   cryptpad
*   other \*-pad products: hackmd, dillinger, etherpad, etc
*   single player: gist
*   (bonus) richer editors: dbx paper

#### 3.1.4 (DApps/UX) - Some PeerPad user testing completed  (P3)

*   dogfooding

#### 3.1.5 (DApps/DX) - PeerPad useful as teaching tool  (P2)

*   "Make your own PeerPad (Nano)" tutorial, text + video at 1.0
*   event workshop

#### 3.1.6 (DApps/UX) - UX improved  (P3)

*   dead feature cleanup
*   polished desktop experience
*   adequate mobile experience

#### 3.1.7 (DApps/UX) - True PeerPad 1.0 release (P1) _// depends on 3.1.4, 3.1.5, 3.1.6_

*   matches requirements gathered in 3.1.3

#### 3.1.8 PeerPad Core usable as whitelabeled editor backend (P1)

*   can build CryptPad, HackMD, etc on top of peerpad core

#### 3.2. (DApps) Launch Discussify v1.0 (P1)

(Depends on M2.1, 2.2, 2.3)

*   Basic features implemented on the extension
    *   View discussions on any URI in a truly p2p fashion
    *   Synchronize comments from other users, in near real-time fashion
    *   Ability to create, edit, remove comments
    *   Ability to reply to comments
*   Ability to view comment history such as edits and removals
*   Guarantee the persistency of the data by integrating the pinner
*   Have Identity & Authentication by integrating IDM
*   Make it cryptographically secure by signing and checking signatures of comments
*   Ability to verify user's identities, including their claims & proofs
*   Ability to view discussions I have participated in the past, including receiving notifications about new activity on any of them
*   Ability to subscribe/mute discussions
*   Ability to discuss on specific parts of the page, using Web Annotations
*   Ability to invite other users to a public discussion
*   Ability to have private discussions with other users through invitation
*   Ensure that it's performant, stable and not resource hungry
*   Define (and execute) a plan for the launch of Discussify as a decentralized product

### 4. Staffing

#### 4.1 (Staffing) - Full time PM for Peer-base ecosystem (P1)



