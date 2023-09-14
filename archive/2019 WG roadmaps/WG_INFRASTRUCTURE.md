# IPFS Infrastructure Working Group 2019 Roadmap
The IPFS Infrastructure Working Group supports infra tooling and systems for the IPFS Organization.

### Responsibilities include:
* Manage and maintain the IPFS HTTP Gateway.
* Manage and maintain the IPFS Bootstrapper nodes.
* Manage and maintain the IPFS Preload nodes
* Manage and maintain the IPFS pinning service, pinbot.
* Monitor services and hosts used by the IPFS dev teams.
* Provide wisdom to other users that want to host IPFS nodes.

## Current Projects
* Gateway maintenance/redeployment
* js preload/bootstrapper redeployment
* CI prototyping for js-ipfs
* kubernetes cluster standup for ipfs-cluster 

## Major 2019 goals to achieve
* 1) Each Package Management system implemented is supported by infra team as a 24/7 production service
   * ensures ease of adoption for our end users to use the management systems we provide via IPFS
* 2) IPFS teams have the performance testing environments needed
   * aids dev teams in iterating through protocol changes quickly and safely
* 3) Support teams with an interface to track project KPIs
   * provides visibility and tracking on progress for essential project KPIs

## Milestones

* M (P?): performance testing environment is available to all IPFS working groups 🗂 🔄 🤝 🧠 📦
   * work between dev and infra to design & implement testing environment
* M (P1): migrate gateway to <cidv1b32>.ipfs.dweb.link 🔄
* M (P2): gateway is implemented in a way to discourage long term dependency on IPFS centralized services 🔄
* M (P?+1): support npm-on-ipfs infra needs 📦
   * team of at least 4 engineers (2 js and 2 infra) designs & implements service
   * service SLA is designed and implemented
      * required specs: performance, uptime, monitoring, alerting, update workflow, oncall needs, etc.
   * More information on existing npm server + mirrors:
      * https://github.com/ipfs/infrastructure/issues/444
      * https://github.com/ipfs/infrastructure/issues/437
      * https://github.com/ipfs/infrastructure/issues/432
      * https://github.com/ipfs/infrastructure/issues/423
* M (P?+2): support any additional ipfs-run services 📦
   * team of at least 4 engineers (2 ??? and 2 infra) designs & implements
   * production service SLA is designed and implemented
      * required specs: performance, uptime, monitoring, alerting, update workflow, oncall needs, etc.

## Timeline
- Q1
- Q2
- Q3
- Q4

## ⁉️ Want to get involved?
- File an issue here with questions, or make a PR to suggest an alternate path or addition
- Want to help make this happen? [Open an issue on the ipfs-infra Working Group repo!](https://github.com/ipfs/infra/issues)
