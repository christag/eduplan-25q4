# NotebookLM Lesson Plan: Episodic Storage & Archival Tiers

## Sources (15)

https://www.nakivo.com/blog/storage-tiering/
https://cloud.google.com/blog/products/storage-data-transfer/archive-media-for-the-long-term-with-preservation-masters
https://www.purestorage.com/knowledge/what-is-tiered-data-storage.html
https://scalelogicinc.com/blog/data-archiving-preserving-valuable-media-assets/
https://www.studionetworksolutions.com/solutions/archival/
https://www.tvtechnology.com/equipment/for-longterm-video-archiving-tape-is-still-king
https://elements.tv/blog/storage-tiering-in-post-production/
https://massive.io/file-transfer/online-vs-offline-vs-nearline-storage/
https://aws.amazon.com/s3/storage-classes/glacier/
https://docs.aws.amazon.com/AmazonS3/latest/userguide/glacier-storage-classes.html
https://www.pump.co/blog/aws-s3-glacier-storage-class
https://massive.io/file-transfer/hot-storage-vs-cold-storage/
https://www.ctera.com/blog/differences-hot-warm-cold-file-storage/
https://www.backblaze.com/blog/whats-the-diff-hot-and-cold-data-storage/
https://www.vida.studio/blog-posts/an-introduction-to-hot-and-cold-cloud-storage-tiers

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | Storage Tiering Guide - NAKIVO | Tiering fundamentals, cost optimization, performance |
| 2 | Archive Media with Preservation Masters - Google Cloud | Long-term archival, preservation strategies, cloud workflows |
| 3 | What is Tiered Data Storage - Pure Storage | Storage tiers overview, architecture, benefits |
| 4 | Data Archiving for Media Assets - Scale Logic | Media preservation, archival strategies, asset management |
| 5 | Video Archive Solutions - EVO/Studio Network | Nearline, LTO tape, cloud archival systems |
| 6 | LTO for Video Archiving - TV Technology | Tape archive, LTO benefits, long-term storage |
| 7 | Storage Tiering in Post Production - ELEMENTS | Post-production workflows, tiering strategies, performance |
| 8 | Online vs Nearline vs Offline Storage - MASV | Storage tier definitions, use cases, cost comparison |
| 9 | Amazon S3 Glacier Storage Classes - AWS | Cloud archival, S3 Glacier tiers, retrieval options |
| 10 | Understanding S3 Glacier Storage Classes - AWS Docs | Glacier Instant/Flexible/Deep Archive, technical details |
| 11 | AWS S3 Glacier Storage - Pump | Glacier cost analysis, storage class comparison |
| 12 | Hot Storage vs Cold Storage - MASV | Hot/cold comparison, use cases, performance tradeoffs |
| 13 | Hot, Warm, and Cold File Storage - CTERA | Three-tier model, lifecycle management, automation |
| 14 | Hot and Cold Data Storage - Backblaze | Storage tier fundamentals, cost analysis, best practices |
| 15 | Hot and Cold Cloud Storage Tiers - VIDA | Cloud storage tiers, video production workflows, optimization |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: Storage Tiering Fundamentals for Media

You are creating an audio overview for a senior IT director at Morning Brew who manages media production and broadcast operations. They need to understand storage tiering fundamentals: the difference between hot, warm, and cold storage, and why media companies use tiered storage architectures to balance performance and cost.

**Cover in this overview:**
- What storage tiering is: storing data on different storage tiers based on access frequency and performance needs
- Hot storage: fast access (SSD/NVMe), frequently accessed data, active projects, high cost per TB
- Warm/Nearline storage: moderate access speed (HDD), semi-active content, medium cost
- Cold storage: infrequent access (tape/cloud archive), completed projects, low cost per TB
- Why media needs tiering: balancing performance for active editing with cost for vast archives
- Cost comparison: concrete numbers showing SSD vs. HDD vs. tape vs. cloud archive costs
- Access time tradeoffs: milliseconds (hot) vs. seconds/minutes (warm) vs. hours (cold)
- When content moves between tiers: project lifecycle, monetization potential, regulatory retention

**Exclude from this overview:**
- Specific storage technologies and vendors (covered in Overview 2)
- Cloud storage options and S3 Glacier (covered in Overview 3)
- Lifecycle policies and automation (covered in Overview 4)
- Implementation strategies (covered in Overview 5)

**Approach:**
Make storage tiering intuitive using media production examples. Help the listener understand this is about economics—keeping fast storage for what's needed now, moving everything else to cheaper tiers. Use concrete cost examples. They should understand the fundamental tradeoff between performance and cost.

### Overview 2: Storage Technologies - LTO, Nearline, and Cloud

You are creating an audio overview for a senior IT director at Morning Brew who understands storage tiering concepts. They need to learn about specific storage technologies: LTO tape, nearline disk systems, and cloud storage options, including when each technology fits in a media workflow.

**Cover in this overview:**
- LTO (Linear Tape-Open) tape: lowest cost per TB, 30-year lifespan, offline storage, cartridge-based
- Why tape persists for media: durability, cost efficiency, air-gapped security, proven longevity
- LTO generations and capacities: LTO-7, LTO-8, LTO-9 progression, roadmap
- Nearline storage: disk-based intermediate tier, faster than tape, slower than online, perfect for "might need soon"
- Object storage systems: scale-out architecture, cloud or on-prem, metadata-rich
- Hybrid architectures: combining on-prem nearline with cloud archive
- Retrieval time realities: tape requires mount time, nearline is near-instant, cloud varies by tier
- Total cost of ownership: purchase price, power, cooling, maintenance, migration costs

**Exclude from this overview:**
- Basic tiering concepts (already covered in Overview 1)
- Cloud-specific services like S3 Glacier (covered in Overview 3)
- Automation and lifecycle management (covered in Overview 4)
- Implementation planning (covered in Overview 5)

**Approach:**
Make storage technology choices concrete. Help the listener understand the real-world characteristics of each technology—not just specs, but practical considerations like "tape requires a robot to load cartridges" and "nearline gives you breathing room before archiving to tape." They should be able to evaluate vendor proposals intelligently.

### Overview 3: Cloud Archival with S3 Glacier and Alternatives

You are creating an audio overview for a senior IT director at Morning Brew who understands storage tiers and technologies. They need to learn about cloud-based archival, particularly AWS S3 Glacier storage classes, and how cloud archive compares to on-prem tape for media storage.

**Cover in this overview:**
- S3 Glacier Instant Retrieval: millisecond access, for rarely-accessed hot data, moderate cost
- S3 Glacier Flexible Retrieval: minutes-to-hours access, for true archive, low cost
- S3 Glacier Deep Archive: 12-hour retrieval, lowest cloud cost, regulatory/compliance archives
- Cost structure: storage cost vs. retrieval cost vs. egress cost—the hidden complexity
- When cloud archive makes sense: scalability, no hardware management, geographic redundancy
- When tape still wins: very large archives, regulatory air-gap requirements, egress cost concerns
- Hybrid strategies: cloud for accessibility, tape for deepest archive
- Other cloud options: Google Cloud Archive, Azure Cool/Archive tiers, Backblaze B2

**Exclude from this overview:**
- Storage tiering fundamentals (already covered in Overview 1)
- LTO and nearline technologies (already covered in Overview 2)
- Lifecycle automation implementation (covered in Overview 4)
- Complete deployment strategies (covered in Overview 5)

**Approach:**
Make cloud archival economics clear, especially the retrieval/egress cost surprise. Help the listener understand cloud isn't always cheaper—it depends on access patterns. Use examples: "10TB archive, accessed twice a year" vs. "10TB archive, never accessed." They should be able to model cloud vs. tape costs for their specific use case.

### Overview 4: Lifecycle Management and Tiering Automation

You are creating an audio overview for a senior IT director at Morning Brew who understands storage tiers, technologies, and cloud options. Now they need to learn how to automate data movement between tiers using lifecycle policies, and how to define retention policies for media assets.

**Cover in this overview:**
- What lifecycle management is: automated data movement based on age, access patterns, or rules
- Defining lifecycle rules: "move to nearline after 90 days inactive, archive to tape after 1 year"
- Cloud lifecycle policies: S3 Lifecycle, Azure Lifecycle Management, automated tier transitions
- Retention policies: legal requirements, business value, monetization windows
- The episodic content challenge: TV episodes, podcast archives, seasonal content with varying value
- Access pattern analysis: identifying what's actually accessed vs. what just sits there
- Metadata-driven policies: using project status, content type, rights windows to drive archival
- Testing lifecycle policies: ensuring automated moves don't break workflows
- Balancing automation with manual exceptions: keeping editorial control when needed

**Exclude from this overview:**
- Basic tiering concepts (already covered in Overview 1)
- Storage technology details (already covered in Overview 2)
- Cloud platform specifics (already covered in Overview 3)
- Full implementation and deployment (covered in Overview 5)

**Approach:**
Make lifecycle automation practical and safe. Help the listener understand this isn't "set and forget"—it requires thoughtful policy design and monitoring. Use media-specific examples like "keep all raw footage in nearline for 6 months post-air, then archive to tape." They should feel equipped to design lifecycle rules that match their business.

### Overview 5: Implementing a Tiered Storage Strategy

You are creating an audio overview for a senior IT director at Morning Brew who understands tiers, technologies, cloud options, and lifecycle automation. Now they need to actually implement a tiered storage strategy: assessing current state, designing the target architecture, migrating data, and operating the tiered environment.

**Cover in this overview:**
- Assessing current storage: what you have, what it costs, what's being accessed
- Calculating storage economics: cost per TB at each tier, total cost projection
- Designing tier architecture: how much capacity at each tier, technology choices
- Migration planning: moving existing archives to new tiers without disrupting production
- Checksum validation: ensuring data integrity during and after migration
- Operational procedures: monitoring tier usage, rebalancing, capacity planning
- Metadata and asset management integration: keeping MAM systems aware of tier locations
- User experience: making tiered storage transparent to editors and producers
- Common mistakes: under-sizing tiers, poor lifecycle rules, ignoring retrieval costs
- Building the business case: showing ROI from storage tiering, cost savings projections

**Exclude from this overview:**
- Tiering fundamentals (already covered in Overview 1)
- Technology comparisons (already covered in Overview 2)
- Cloud-specific details (already covered in Overview 3)
- Lifecycle policy design (already covered in Overview 4)

**Approach:**
Make implementation realistic and comprehensive. Help the listener understand this is a multi-month project requiring planning, testing, and gradual rollout. Use examples of successful tiered storage deployments at media companies. They should come away with a clear implementation roadmap and realistic expectations about effort, timeline, and benefits.

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Select and copy all URLs from the "Sources" section above (they are plain URLs with no formatting)
3. Paste the URLs directly into NotebookLM's source input
4. For each audio overview:
   - Click "Generate Audio Overview"
   - Copy and paste the corresponding prompt above
   - Generate the overview
5. Listen to overviews in sequence (1→2→3→4→5)

Each overview builds on the previous ones, creating a comprehensive learning path from storage tiering fundamentals through implementation.

This learning path is tailored for IT leaders at media companies managing large content archives and optimizing storage costs.
