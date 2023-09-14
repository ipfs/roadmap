# 2020 IPFS Project Planning

It’s that time of the year again! Q4 is upon us, and as such it is time to reflect on IPFS progress and status, how the wider ecosystem and internet has evolved over the past year, and chart a course for our work in 2020 that optimizes for the long term success of [our mission as a Project](https://github.com/ipfs/roadmap/blob/master/README.md#ipfs-mission-statement).

## 2019 Project State
This has been an absolutely huge year for IPFS adoption - be that applications building on IPFS, end users of applications powered by IPFS, or total nodes in the IPFS network (see more in [this video from IPFS Camp](https://www.youtube.com/watch?v=jpQnQbfhuBc)). More and more tools - inside and outside the web3 ecosystem - are using IPFS to benefit from content-addressing or empower their users to operate peer-to-peer. In the past year, we’ve seen a proliferation of **IPFS on mobile** with [Haven](https://gethaven.app/), [Textile](https://textile.photos), and [Berty](https://berty.tech); we’ve seen new solutions for **identity** emerge on top of IPFS in [3box](https://3box.io), [uPort](https://www.uport.me), and [IDM](https://github.com/ipfs-shipyard/pm-idm); we’ve seen great strides in support for **IPFS in web browsers** from [Brave & Opera](https://blog.ipfs.io/2019-10-08-ipfs-browsers-update/), and groups like [ENS](https://medium.com/the-ethereum-name-service/ethdns-9d56298fa38a); and we’ve seen a whole host of **supporting tools** be created like HTTP gateways ([Cloudflare](https://developers.cloudflare.com/distributed-web/ipfs-gateway/)), pinning services ([Pinata](https://pinata.cloud) & [Eternum](https://eternum.io)), and IPFS infrastructure ([Infura](http://infura.io) & [Temporal](https://temporal.cloud/)) to support IPFS users and developers. 

This increase in adoption also opened up new challenges for the IPFS Project - especially around accommodating new scalability needs for our DHT, infrastructure, and testing. In addition to continuing work on our core focus for the year - improving IPFS performance and tooling to support adding, updating, and fetching large directories of data from IPFS (aka our “package managers” use case) - we also launched important new work streams to improve IPFS reliability via significant investments in IPFS infrastructure, end-to-end network simulation & testing, and improved documentation ([read more about that here](https://blog.ipfs.io/2019-07-31-operation-task-force/)). We expect those threads of work to continue into 2020 as well, however we also want to hear from folks throughout the community if there are focus areas for 2020 that deserve more attention, research, or prioritization as the Project heads into planning for the next year. **We’d love your input! 👂**

## Call for _Theme_ Proposals
To that end, please share your **proposals** for _themes_ for the IPFS Project to invest in more deeply in 2020. These could be specific use cases (like [IPFS for large files](https://github.com/ipfs/roadmap#-large-files-d1-e4-i3)), specific improvement areas (like IPFS developer usability), specific markets (like IPFS for enterprise), specific integrations (like IPFS x blockchain), or more! To suggest a _theme_, please create a new [**2020 Theme Proposal** issue](https://github.com/ipfs/roadmap/issues/new/choose) in this repo ([here’s a first example](https://github.com/ipfs/roadmap/issues/42)). The hope with using github issues is to help others build on your great ideas in issue comments, and also be inspired to propose their own thoughts for discussion. You aren't limited to only one! ✍️


### The [2020 Theme Proposal template](https://github.com/ipfs/roadmap/issues/new/choose) includes:
- Theme title
- Problem statement description
- Core needs & gaps
- Why focus this year
- Milestones & rough roadmap
- Desired / expected impact
But also feel free to include any other relevant content!

### Known 2020 Milestones 🎯
To help identify **good** _themes_, here is an incomplete list of some exciting milestones coming up in the next year, which may open up new opportunities for IPFS to create value in 2020 and beyond:
1. Many IPFS-powered dapps will launch betas in early-mid 2020, including a number of teams in attendance at IPFS Camp 2019
2. Eth2.0 is launching sometime in Q1 2020, building on libp2p as their networking layer
3. Filecoin is aiming to launch their mainnet in ~March 2020
4. We will have basic ipfs:// support in 1+ browser out-of-the-box, and other browsers actively investing in more experimentation by early 2020
5. IPLD schemas work will come to fruition, along with codegen for go-ipld-prime
6. We will have more gatherings to get the wider IPFS community together! (timing TBD)
7. <Others? Add more here!>


### 2020 Planning Process Timeline 📆
- **Oct 23 - Nov 8**: Open call for 2020 Theme Proposals _(add yours [here](https://github.com/ipfs/roadmap/issues/new/choose))_
- **Nov 11 - Nov 15**: IPFS 2020 Planning “Spike”
- **Nov 18 - Nov 22**: Review and feedback on 2020 theme(s) with key stakeholders
- **Dec 2 - Dec 6**: Finalize and present 2020 theme(s) and updated roadmap
- **Dec 9 - Dec 20**: Project and working group Q1 2020 OKRs

### Credit 🙏
In planning this year’s roadmapping process, we borrowed a lot of great ideas from the [Rust Roadmapping efforts](https://github.com/rust-lang/rfcs/blob/master/text/1728-north-star.md) of the past few years in addition to learning from what worked well and what we wanted to iterate on from [last year's IPFS planning process](https://blog.ipfs.io/78-ipfs-2019-roadmap/). Check out [the Rust 2019 Roadmap](https://github.com/rust-lang/rfcs/blob/master/text/2657-roadmap-2019.md) for some great exemplars!
