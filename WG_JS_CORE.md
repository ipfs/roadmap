# JS Core Dev Team 2019 Roadmap

> Oversees the development of the JS implementation of the IPFS protocol and related projects.
 
**Responsibilities include:**
- Implement and maintain the IPFS protocol and tools
- Enable IPFS usage in Node.js, browsers and other JavaScript runtimes
- Maintain interoperability with other IPFS implementations
- Incubate and grow projects that will encourage IPFS adoption

**Current Projects**
- JS IPFS
- JS IPFS API
- Go & JS IPFS Interop
- Npm on IPFS
- IPFS Service Worker Gateway
- IPFS Geo IP
- IPFS Performance Profiling
- benchmark-js.ipfs.io


## 🚀 Major 2019 Goals to achieve

The major goals below and following milestones have been labeled with the emoji for the goal in the IPFS Project Roadmap that they contribute towards:
 
📦 = Package Managers  🗂 = Large Files  🔄 = Decentralized Web  🤝 = Partner Use Cases  🧠 = Strategic Projects
 
- JS IPFS is ready for use in production. It is stable, performant, and interoperable with other IPFS implementations 📦 🗂 🔄 🤝 🧠
- JS IPFS can ingest and move data with similar speeds to rsync or wget 📦 🗂 🔄 🤝
- Data on JS IPFS is searchable both online and offline 📦 🔄 🤝
- Developer experience is a joy  🔄 🤝 🧠

## 💎 Milestones

- `M (P0)`: Production ready 📦 🗂 🔄 🤝 🧠. JS IPFS has for a long time now been under heavy development with a focus on implementing features. We’re now at a stage where it has a good level of feature parity to Go IPFS. Implementing the last key missing features and focused attention on performance, stability and security issues will allow JS IPFS to be a viable alternative to Go IPFS.
  - A JS IPFS daemon runs as part of the IPFS gateway cluster for at least 1 month without crashing
  - Performance metrics for a JS IPFS node are measurable:
  - Tools can process and graph performance data
  - Data can be queried to track down bugs and performance bottlenecks
  - Benchmarks exist to assert that:
    - Memory footprint remains stable and should not consume more than 20% more memory than a Go IPFS node
    - Network throughput is within an acceptable magnitude of Go IPFS
    - Data can be fetched with comparable speeds to tools like bittorrent, wget or rsync when 5 peers are connected who already have the data
    - Data can be exchanged with another IPFS node within 2x the speed a Go IPFS node would exchange it
  - An interoperable DHT exists and scales to hundreds of thousands of nodes
  - A gossipsub implementation exists
  - An IPFS log API is implemented and tests ensure log messages are part of the API
  - A security audit is conducted on the code base and all issues resolved

- `M (P1)`: Optimized for browser environments 🔄 🤝 🧠. One of the biggest challenges that faces JS IPFS is that it will be used in many different environments where the tools and resources available to it differ significantly. JS IPFS can be run in a browser (Chrome, Firefox etc.), in a web extension, in Node.js on a laptop or on a server, in Electron, on mobile or even on IoT devices. Not only does the runtime differ - Node.js, Blink, SpiderMonkey etc. but the APIs available (no filesystem or low level network in a browser) as well as the hardware resources available e.g. mobile or IoT.
  - Default performance profiles exist and can be enabled to adapt IPFS behaviour appropriately to its environment. In addition to the profiles described here, the following profiles also exist:
    - Browser
    - Electron
    - Mobile
    - IoT
  - The JS IPFS build can be customised to exclude functionality or include different modules that are more appropriate for a particular runtime environment
  - At least 2 recommended builds for common environments will be provided in addition to the full build
  - Developers can tailor an IPFS build to their specific needs
  - Full build bundle size is monitored and does not exceed 2MB (minified)
  - Examples for bundling JS IPFS with common tools such as webpack/parcel exist
  - A JS IPFS daemon can run on a Raspberry Pi for at least 1 month
  - Example projects exist for running JS IPFS in a web view on iOS and Android

- `M (P1)`: Installable npm modules via JS IPFS 📦 🗂 🔄 🧠. The npm registry is one of the biggest data sets JS developers interact with daily. There’s a myriad of benefits to it being accessible on the IPFS network. We’ll enable this at the same time as proving out the ability for JS IPFS to deal with large data sets.
  - There is an option to select IPFS as a transport on npm/yarn
  - A CLI tool exists to install packages directly from IPFS
  - JS IPFS can ingest the entire npm registry
  - Installing npm modules over LAN never fails (provided the module is available on another IPFS node connected to the LAN)
  - Installing any module is faster than using npm when 5 peers on the local network already have the package
Node.js binaries are distributed via IPFS (making the whole Node.js/NPM installation process happen over IPFS)
 
- `M (P2)`: Discoverable npm modules via JS IPFS 📦 🗂 🔄 🧠. One of the big features that IPFS lacks right now is content discoverability. A mechanism of searching for content on the IPFS network would greatly improve the situation. Considering our milestone of installing npm modules via JS IPFS, it makes sense to augment it with a search component to make it more attractive and useful as well as allowing us to achieve our major goal of adding search to JS IPFS.
 
  - Users can search for modules in the npm registry via IPFS
  - Users can learn about the latest registry index (module updates) via IPFS
  - Unixfs v2 is finalized and is the default format for new content added to IPFS
  - Improved documentation, specs and examples 🔄 🤝 🧠 (P2)
  - Improving the docs, specs and having great tutorials and examples goes a long way to realising the distributed web for the simple reason that if people can’t drop by and pick up IPFS easily they’re less likely to use it. This milestone addresses that problem and also helps people already invested in IPFS to continue to build on top of it.
  - Code level:
    - Functions/methods all have meaningful descriptions
    - Functions/methods all have inline examples
    - Parameters are all documented, including types and defaults
    - Return values are documented, including object properties and types
    - Onboarding documentation exists to explain domain concepts and provide tutorials/examples for achieving common tasks

- `M (P0)`: Revamped APIs 🔄 🤝 🧠 (P0). Revamping the APIs will make them easier to use and simpler to understand. Using modern syntax will make JS IPFS appealing to a wider segment of the JS community, aiding adoption and contributions. It also gives us scope to make performance optimisations and stability/debuggability improvements.
  - Async/await is used throughout the codebase and callback APIs are dropped
  - Support ArrayBuffer as an alternative to Buffer input argument
  - Streaming APIs switch to using async iterators/iterables
  - The files API is revamped:
  - Files functions moved to the root namespace
  - Non-MFS and MFS functions are merged
  - A revamped RESTful HTTP API exists
  - Old APIs are deprecated and removed (e.g. object, block)
  - At least one alternative API exists for JS IPFS (e.g. Graphql)

- `M P(3)`: Support for specific use cases 🔄 🤝 🧠 (P3). This milestone focuses in on how JS IPFS can refine and augment it’s existing tech stack to better serve specific use cases.
  - Default chunkers exist for particular file types to optimise for example deduplication or seeking/direct access in tar archives and video files
  - High priority features requested from other working groups that have experienced pain points with the JS IPFS API are implemented e.g. Pagination and “Live” streams
  - IPFS nodes can discover one another for specific topics via the rendezvous protocol
-star servers are no longer in use
  - IPFS nodes work and are compliant with the MDNS spec
  - Libp2p discovery and transport modules exist for bluetooth and libdweb, sound and potentially other exotic technologies

## Timeline

- Q1
- Q2
- Q3
- Q4
