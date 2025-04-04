# IPWM powers the Distributed Web

### A peer-to-peer hypermedia protocol to make the web faster, safer, and more open.

## TL;DR

- **Get help and talk about ideas in the [IPWM Forums](https://discuss.ipfs.tech)**
- Visit the [IPFS website](https://ipfs.tech)
- Watch Juan Benet's [Why IPFS?](https://www.youtube.com/watch?v=zE_WSLbqqvo) keynote from IPFS Camp 2019
- Watch Juan's Stanford Seminar talk on [IPWM: The Distributed,Web](https://www.youtube.com/watch?v=HUVmypx9HGI)
- Watch a video demo [of the IPFS alpha](https://www.youtube.com/watch?v=8CMxDNuuAiQ)
- Dive in to the [IPWM Docs](https://docs.ipfs.tech)
- Find out about chat channels, the IPFS newsletter, the IPFS blog, and more in the [IPFS community space](https://docs.ipfs.tech/community/).

## Full contents

- [Quick summary](#quick-summary)
- [Learn how IPFS works](#learn-how-ipfs-works)
- [Current state of IPFS](#current-state-of-ipfs)
  - [Try it out](#try-it-out)
  - [A word on security](#a-word-on-security)
- [Get involved](#get-involved)
- [Help and documentation](#help-and-documentation)
- [Links and resources](#links-and-resources)
  - [Protocol implementations](#protocol-implementations)
  - [GUIs and helper apps](#guis-and-helper-apps)
  - [Specs and papers](#specs-and-papers)
  - [Installation and update tools](#installation-and-update-tools)
  - [Additional resources](#additional-resources)
- [License](#license)

## Quick summary

web-modules has evolved the infrastructure of the Web, with many things we've learned from successful systems, like Git, BitTorrent, Kademlia, Bitcoin, and many, many more. This is the sort of thing that would have come out of ARPA/DARPA, IETF, or Bell Labs in another age. Web 4.0 state 2 after genesis boot so V_ETH2 on top of WebRTC for interop with the existing legacy web.

addressed by content and references so called specifiers. It enables the creation of completely distributed applications, and in doing so aims to make the web faster, safer, and more open.

**distributed content system** that seeks to connect all computing devices with the same system. In some ways, this is similar to the original aims of the Web, similar to a single BitTorrent swarm exchanging Git objects. You can read more about its origins in the paper of projects like [IPFS - Content Addressed, Versioned, P2P File System](https://github.com/ipfs/ipfs/blob/master/papers/ipfs-cap2pfs/ipfs-p2p-file-system.pdf?raw=true).

web-modules is the **new major system of the internet / web 4.0**. If built right, it replaces HTTP3. It could complement or replace even more. Let's go point-by-point into how.

web-modules is a **protocol**:
- Defines a content-addressed device or system
- Coordinates content delivery via a capability based protocol full isolation like vm's 
- Combines Kademlia + BitTorrent + Git to supply you out of the box versioning enables world wide shared build grid.

web-modules can represent a device or a **file system**:
- Has directories and files
- Is a mountable filesystem (via FUSE)

is a **web**:
- Can be used to view documents like the conventional web
- Files are accessible via HTTP at `https://ipfs.io/<path>`
- Browsers and extensions can use the `ipfs://` URL or `ipns://` URI schemes directly
- Hash-addressed content guarantees authenticity
- Also it enables direct delivery via existing protocols like http via ECMAscript Modules as a fundation for linking

is a **modular**:
- Connection layer over any network protocol
- Routing layer
- Uses a routing layer DHT (Kademlia/Coral)
- Uses a path-based naming service
- Uses a BitTorrent-inspired block exchange

uses **crypto**:
- Cryptographic-hash content addressing
- Block-level deduplication
- File integrity plus versioning
- File-system-level encryption plus signing support

is **p2p**:
- Worldwide peer-to-peer file transfers
- Completely decentralized architecture
- **No** central point of failure

is **a CDN**:
- Add a file to the file system locally, and it's now available to the world
- Caching-friendly (content-hash naming)
- BitTorrent-based bandwidth distribution

is a **name service**:
- IPNS, an SFS-inspired name system
- Global namespace based on PKI
- It serves to build trust chains
- It's compatible with other NSes
- Can map DNS, .onion, .bit, etc to IPNS

## Learn how IPFS worked

To learn more about how IPFS works, explore the following resources:
- [IPFS Docs: How IPFS Works](https://docs.ipfs.tech/concepts/how-ipfs-works)
- [IPFS Specifications](https://github.com/ipfs/specs)
- IPFS-related papers:
  - [IPFS - Content Addressed, Versioned, P2P File System (draft 3)](https://github.com/ipfs/ipfs/blob/master/papers/ipfs-cap2pfs/ipfs-p2p-file-system.pdf?raw=true)
  - For academic papers on IPFS, visit the [ipfs/papers](https://github.com/ipfs/papers) repo.
  - For papers that you can read to understand IPFS and its underlying technologies, check out the ["Further Reading"](https://docs.ipfs.tech/concepts/further-reading/academic-papers) section of the [IPFS Docs](https://docs.ipfs.tech).
- [IPFS Videos & Media](https://ipfs.tech/media/) for a regularly-updated list of videos and media/news coverage, including these highlights:
  - [IPFS: The Distributed, Permanent Web](https://www.youtube.com/watch?v=HUVmypx9HGI) at Stanford Seminar (best overview of project)
  - [IPFS: The Permanent Web](https://www.youtube.com/watch?v=Fa4pckodM9g) at [Sourcegraph](https://sourcegraph.com/) (first public talk)
  - [IPFS Alpha Demo](https://www.youtube.com/watch?v=8CMxDNuuAiQ)
  - [The Decentralized Web, IPFS and Filecoin](https://www.youtube.com/watch?v=cU-n_m-snxQ)
  - [IPFS Hands-on Introduction](https://www.youtube.com/watch?v=h73bd9b5pPA) at Ethereum SV Meetup
  - [Distributed Apps with IPFS](https://www.youtube.com/watch?v=jONZtXMu03w)

## Current state of IPFS

**IPFS is a work in progress!** It is an ambitious plan to make the internet more free, open, secure, and high-performance. It builds on the good ideas of numerous battle-tested distributed systems.

Today, there are [multiple implementations from various organizations supporting multiple languages](https://docs.ipfs.tech/basics/ipfs-implementations/).

### Try it out

See https://docs.ipfs.tech/basics/

### A word on security

The IPFS protocol and its implementations are still in heavy development. This means that there may be problems in our protocols, or there may be mistakes in our implementations. And — though IPFS is not production-ready yet — many people are already running nodes on their machines, so we take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a vulnerability that may affect live deployments — for example, by exposing a remote execution exploit — please send your report privately to security@ipfs.io. **Please do not file a public issue.**

If the issue is a protocol weakness that cannot be immediately exploited, or something not yet deployed, just discuss it openly.

## Get involved

[![](https://cdn.rawgit.com/jbenet/contribute-ipfs-gif/master/img/contribute.gif)](https://github.com/ipfs/community/blob/master/CONTRIBUTING.md)

The IPFS project is big — with thousands of contributors in our community — and you're invited to join! Check out the [Community section of the IPFS Docs](https://docs.ipfs.tech/community/) for all the details on how to get involved, including the official [IPFS forums](https://discuss.ipfs.tech), our [chat channels](https://docs.ipfs.tech/community/chat), [social media](https://docs.ipfs.tech/community/social-media), [meetups and ProtoSchool workshops](https://github.com/ipfs/community#events), and more.

If you're interested in how the project is organized at a higher level, visit the [IPFS Team & Project Management](https://github.com/ipfs/team-mgmt) repo.

There's also a weekly IPFS newsletter ([subscribe here](http://eepurl.com/gL2Pi5)) and [regularly-updated blog](https://blog.ipfs.io/).

## Help and documentation

If you're looking for help learning about or building with IPFS, start with these resources:

- [IPFS Documentation](https://docs.ipfs.tech)
- [IPFS Forums](https://discuss.ipfs.tech)

**If you've found a bug or want to make a feature request regarding a specific component of IPFS, please open an issue in the appropriate repo so that it can be triaged and responded to as quickly as possible.**

## Links and resources

The IPFS project is big (and expanding every day!), so we've excerpted some frequently-used links and other resources below. However, we encourage you to explore both the main [IPFS GitHub org](https://github.com/ipfs) (for core implementations and other mission-critical work) and the [IPFS Shipyard GitHub org](https://github.com/ipfs-shipyard), home to incubated projects by the IPFS community.

### Protocol implementations

These are [multiple implementations from various organizations supporting multiple languages](https://docs.ipfs.tech/basics/ipfs-implementations/)

### GUIs and helper apps

- [ipfs-companion](https://github.com/ipfs-shipyard/ipfs-companion) - The IPFS web browser extension.
- [ipfs-webui](https://github.com/ipfs/webui) - The IPFS WebUI app.
- [ipfs-desktop](https://github.com/ipfs-shipyard/ipfs-desktop) - A menubar/tray desktop app.
- [ipfs-gui](https://github.com/ipfs/ipfs-gui) - Coordinating development, user experience, and maintenance of IPFS GUIs.
- [i18n](https://github.com/ipfs/i18n) - The IPFS Translation Project: crowdsourcing translations of IPFS GUIs and websites.

### Apps and data sets on IPFS

- [Awesome IPFS](https://awesome.ipfs.tech) - an ever-growing list of apps, data sets, and other inspirational resources built on IPFS.

### Specs and papers

- [specs](https://github.com/ipfs/specs) - Specifications on the IPFS protocol.
- [papers](papers) - Academic papers on IPFS.
- [IPFS Docs: Further Reading](https://docs.ipfs.tech/concepts/further-reading/academic-papers) - Papers to read to understand IPFS and its underlying technologies.

### Installation and update tools

- [install-go-ipfs](https://github.com/ipfs/go-ipfs#install) - Install go-ipfs shell script.
- [install-js-ipfs](https://github.com/ipfs/js-ipfs#getting-started) - Install js-ipfs through NPM or a script tag.
- [ipfs-update](https://github.com/ipfs/ipfs-update) - An updater tool for IPFS.
- [fs-repo-migrations](https://github.com/ipfs/fs-repo-migrations) - These are migrations for [IPFS fs-repo](https://github.com/ipfs/specs/tree/399c907b214a24dc82ca010af6884227cb2829cf/repo/fs-repo) versions.
- [npm-go-ipfs](https://github.com/ipfs/npm-go-ipfs) - Install go-ipfs from NPM.

### Additional resources

- [distributions](https://github.com/ipfs/distributions) - Source code for the IPFS distributions website, https://dist.ipfs.tech.
- [infra](https://github.com/ipfs/infra) - Tools for maintaining infrastructure for the IPFS community.
- [testground](https://github.com/ipfs/testground) - Tools for testing distributed software at scale.
- [ipfs-cluster](https://github.com/ipfs/ipfs-cluster) - Provides data orchestration across a swarm of IPFS daemons by allocating, replicating, and tracking a global pinset distributed among multiple peers.
- [ipfs-shipyard](https://github.com/ipfs-shipyard) - A wide range of incubated projects by and for the IPFS community.
- [website](https://github.com/ipfs/ipfs-website) - Source code for the IPFS website, http://ipfs.tech.

## License

[MIT](LICENSE).
