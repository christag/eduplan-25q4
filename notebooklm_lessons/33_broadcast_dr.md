# NotebookLM Lesson Plan: Broadcast DR & Failover Drills

## Sources (15)

https://www.tvtechnology.com/opinion/disaster-recovery-in-the-cloud
https://www.tvunetworks.com/guides/business-continuity-and-disaster-recovery-for-broadcast-media/
https://www.globecast.com/post/blogpost/disaster-recovery-what-every-broadcaster-should-know/
https://imaginecommunications.com/insights-and-resources/disaster-recovery-vs-business-continuity-broadcast-playout/
https://www.amagi.com/blog/disaster-recovery-is-your-broadcasting-network-invincible
https://www.backblaze.com/blog/a-disaster-recovery-game-plan-for-media-teams/
https://www.veset.tv/solutions/disaster-recovery-for-broadcasting
https://www.epiphan.com/blog/no-fail-live-streaming-redundancy/
https://bryghtpath.com/business-continuity-for-media/
https://drj.com/journal_main/it-s-a-wrap-how-to-ensure-media-production-continuity-even-in-the-face-of-disaster/
https://n2ws.com/blog/aws-disaster-recovery/disaster-recovery-testing-drills-how-do-i-know-my-plan-works
https://axcient.com/blog/disaster-recovery-testing-a-comprehensive-guide-for-msps/
https://www.tierpoint.com/blog/why-you-should-test-your-disaster-recovery-plan/
https://thebroadcastknowledge.com/2020/12/14/video-proper-network-designs-and-considerations-for-smpte-st-2110/
https://thebroadcastknowledge.com/2020/09/08/video-network-design-for-live-production/

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | Disaster Recovery in the Cloud - TV Technology | Cloud-based DR, broadcast infrastructure, migration strategies |
| 2 | Business Continuity and DR for Broadcast Media - TVU Networks | BC/DR fundamentals, media workflows, resilience strategies |
| 3 | What Every Broadcaster Should Know - Globecast | DR essentials, broadcaster needs, service offerings |
| 4 | DR vs. Business Continuity for Broadcast Playout - Imagine | Playout systems, BC vs. DR distinction, hot/warm/cold failover |
| 5 | Is Your Broadcasting Network Invincible - Amagi | Network resilience, ransomware protection, broadcast continuity |
| 6 | DR Game Plan for Media Teams - Backblaze | Media data protection, 3-2-1 backup strategy, recovery planning |
| 7 | Disaster Recovery for Broadcasting - Veset | Cloud playout DR, channel failover, geographic redundancy |
| 8 | No-Fail Live Streaming Redundancy - Epiphan | Live streaming redundancy, component backup, failover mechanisms |
| 9 | Business Continuity for Media - Bryghtpath | Media production continuity, strategic planning, resilience |
| 10 | Ensuring Media Production Continuity - DRJ | Production workflows, deadline-driven recovery, continuity planning |
| 11 | DR Testing Drills Guide - N2WS | Testing methodologies, drill procedures, validation approaches |
| 12 | DR Testing Guide for MSPs - Axcient | Testing best practices, tabletop exercises, full failover tests |
| 13 | 5 DR Testing Best Practices - TierPoint | Testing frequency, testing types, continuous improvement |
| 14 | Network Design for SMPTE ST 2110 - Broadcast Knowledge | IP broadcast resilience, SMPTE 2022-7, red/blue networks |
| 15 | Network Design for Live Production - Broadcast Knowledge | Live production architecture, redundancy patterns, network topology |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: Broadcast DR and Business Continuity Fundamentals

You are creating an audio overview for a senior IT director at Morning Brew (a mid-size media company with broadcast and video production operations) who is leveling up to higher-level tech leadership. They understand general IT disaster recovery but need to understand what makes broadcast DR unique, including the "show must go on" mentality and how DR differs from business continuity in media environments.

**Cover in this overview:**
- What makes broadcast DR different from general IT DR: time sensitivity, live production, content deadlines
- The critical distinction between Disaster Recovery (restoring after disruption) and Business Continuity (continuing during disruption)
- Types of threats to broadcast operations: natural disasters, equipment failures, cyberattacks, power outages
- The broadcast resilience spectrum: cold DR (restore later), warm DR (ready to activate), hot DR (simultaneous redundancy)
- Why "the show must go on": audience expectations, advertising commitments, legal obligations (FCC requirements)
- Cloud-based DR for broadcast: advantages, limitations, hybrid approaches
- Geographic redundancy: backup sites, mirrored facilities, distributed operations
- The media production challenge: deadlines don't stop during disasters

**Exclude from this overview:**
- Specific redundancy architectures and technical designs (covered in Overview 2)
- Testing procedures and drill methodologies (covered in Overview 3)
- IP broadcast and SMPTE standards details (covered in Overview 4)
- Building a comprehensive DR program (covered in Overview 5)

**Approach:**
Help the listener understand the unique pressure and requirements of broadcast DR. Use concrete examples of broadcast failures and their business impact. The listener should come away understanding why broadcast operations require higher availability than typical IT systems and be able to articulate the DR requirements to leadership and vendors. Make the business case clear: why investing in broadcast DR matters beyond just technical resilience.

### Overview 2: Redundancy Architectures and Failover Mechanisms

You are creating an audio overview for a senior IT director at Morning Brew who now understands broadcast DR fundamentals (from Overview 1). They need to learn the specific redundancy architectures used in broadcast environments, including playout redundancy, network redundancy, and how failover actually works in practice.

**Cover in this overview:**
- Playout redundancy configurations: 1+1 (dual active), N+1 (shared backup), N+M (multiple backups)
- Red/Blue network architecture: dual identical networks for IP broadcast facilities
- Hot failover systems: simultaneous redundant playout running 24/7
- Warm failover: content prepped and ready, activated on disaster trigger
- Component-level redundancy: encoders, switchers, storage, network paths
- Automated vs. manual failover: detection mechanisms, switchover procedures, operator intervention
- Live streaming redundancy: input redundancy, output redundancy, CDN redundancy
- The 3-2-1 backup strategy for media: 3 copies, 2 different media types, 1 offsite
- Content synchronization: keeping backup systems current, delta sync, full mirrors
- Failback procedures: returning to primary after disaster resolution

**Exclude from this overview:**
- BC/DR fundamentals and business drivers (already covered in Overview 1)
- Testing and drill procedures (covered in Overview 3)
- IP broadcast protocol specifics (covered in Overview 4)
- DR program governance and continuous improvement (covered in Overview 5)

**Approach:**
Make redundancy architectures concrete and understandable. Use diagrams (described verbally) to explain red/blue networks and 1+1 vs. N+1 configurations. Help the listener understand the tradeoffs: cost vs. resilience, complexity vs. reliability. Use examples of how different broadcast organizations size their redundancy based on their needs (24/7 news vs. scheduled programming). The listener should feel equipped to evaluate redundancy proposals from vendors and make informed architecture decisions.

### Overview 3: DR Testing, Drills, and Validation

You are creating an audio overview for a senior IT director at Morning Brew who understands broadcast DR fundamentals and redundancy architectures (from Overviews 1-2). Now they need to learn how to test DR systems, conduct failover drills, and validate that their DR plans actually work when needed.

**Cover in this overview:**
- Why DR testing is critical: untested DR plans fail when needed, assumption vs. reality
- Types of DR tests: tabletop exercises, isolated rehearsals, non-isolated tests, full failover tests
- Tabletop exercises: scenario-based walkthroughs, communication testing, decision-making practice
- Isolated (bubble) tests: sandbox testing without affecting production
- Full failover tests: complete switchover to DR, run operations, fail back to primary
- Testing frequency: quarterly for light tests, annually for full simulations
- What to test: failover procedures, communication plans, recovery time objectives (RTO), recovery point objectives (RPO)
- Measuring test success: RTO achieved, RPO achieved, gaps identified, lessons learned
- Testing in media environments: scheduled testing during low-traffic periods, protecting live programming
- Common test failures: outdated documentation, missing credentials, configuration drift, untested network paths
- Post-test activities: updating runbooks, fixing identified issues, re-training teams

**Exclude from this overview:**
- BC/DR fundamentals (already covered in Overview 1)
- Redundancy architecture details (already covered in Overview 2)
- IP broadcast technical protocols (covered in Overview 4)
- Long-term DR program development (covered in Overview 5)

**Approach:**
Make testing practical and actionable. Help the listener understand that testing reveals problems before disasters do. Use examples of what goes wrong during tests and how organizations learn from failures. Emphasize the importance of realistic testing—don't just test the happy path. The listener should come away with concrete plans for implementing a testing schedule appropriate for their organization's size and risk profile.

### Overview 4: IP Broadcast Resilience and SMPTE Standards

You are creating an audio overview for a senior IT director at Morning Brew who understands broadcast DR, redundancy architectures, and testing (from Overviews 1-3). Now they need to learn how modern IP-based broadcast systems implement resilience, particularly using SMPTE standards like ST 2022-7 for seamless protection and ST 2110 for professional media over IP.

**Cover in this overview:**
- The shift from SDI to IP broadcast: benefits for DR and redundancy
- SMPTE ST 2110: professional media over IP, separating video/audio/data streams
- SMPTE ST 2022-7: seamless protection switching, packet-based redundancy
- Red/Blue network implementation: dual network paths, packet selection, seamless failover
- How ST 2022-7 works: receivers select packets from redundant paths, handling packet loss transparently
- Network design for resilience: layer 3 multicast routing, QoS, bandwidth management
- Achieving "aviation-class" redundancy: IP systems approaching carrier-grade reliability
- IP resilience vs. SDI failover: faster detection, automatic recovery, no black frames
- PTP (Precision Time Protocol) for synchronization: timing resilience, redundant grandmasters
- Challenges in IP broadcast DR: network complexity, timing dependencies, multicast management

**Exclude from this overview:**
- Business continuity vs. DR fundamentals (already covered in Overview 1)
- General redundancy architectures (already covered in Overview 2)
- Testing and drill procedures (already covered in Overview 3)
- DR program governance (covered in Overview 5)

**Approach:**
Make IP broadcast resilience understandable without overwhelming technical detail. Help the listener understand the key concepts: red/blue networks, seamless protection, packet-based redundancy. Use analogies to make SMPTE standards accessible. The listener should come away understanding how modern IP broadcast achieves higher resilience than legacy SDI systems and be able to discuss these capabilities with broadcast engineers and vendors.

### Overview 5: Building and Operating a Broadcast DR Program

You are creating an audio overview for a senior IT director at Morning Brew who now understands broadcast DR fundamentals, redundancy architectures, testing procedures, and IP resilience (from Overviews 1-4). Now they need to learn how to build a comprehensive DR program, establish governance, maintain DR capabilities over time, and continuously improve resilience.

**Cover in this overview:**
- Defining DR program scope: what systems are critical, what RTO/RPO targets are acceptable
- Risk assessment for broadcast: likelihood vs. impact, prioritizing protection investments
- DR program governance: ownership, responsibilities, escalation procedures, communication plans
- Documentation requirements: DR runbooks, contact lists, system diagrams, recovery procedures
- Keeping DR plans current: quarterly reviews, updates after infrastructure changes, configuration management
- Training and awareness: ensuring teams know their DR roles, regular drill participation
- Vendor and partner coordination: cloud providers, playout vendors, CDN providers, connectivity carriers
- Measuring DR program maturity: from ad-hoc to optimized, continuous improvement
- Balancing cost vs. resilience: right-sizing redundancy, avoiding over-engineering
- DR program metrics: test success rate, RTO/RPO achievement, time since last successful test
- Integration with broader IT DR: broadcast-specific needs vs. general IT recovery
- Building organizational resilience: not just technology, but people and processes

**Exclude from this overview:**
- BC vs. DR fundamentals (already covered in Overview 1)
- Specific redundancy architectures (already covered in Overview 2)
- Testing methodologies and drill types (already covered in Overview 3)
- IP broadcast and SMPTE technical details (already covered in Overview 4)

**Approach:**
Focus on building sustainable, mature DR programs rather than one-time projects. Help the listener understand that DR requires ongoing attention—technology changes, people change, procedures become outdated. Emphasize pragmatic approaches suitable for mid-size media organizations. Use examples of program maturity progression. The listener should feel equipped to establish DR governance, maintain DR readiness over time, and build organizational capability that improves continuously.

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Select and copy all URLs from the "Sources" section above (they are plain URLs with no formatting)
3. Paste the URLs directly into NotebookLM's source input
4. For each audio overview:
   - Click "Generate Audio Overview"
   - Copy and paste the corresponding prompt above
   - Generate the overview
5. Listen to overviews in sequence (1→2→3→4→5)

Each overview builds on the previous ones, creating a comprehensive learning path from broadcast DR fundamentals through building and operating a mature DR program.

This learning path is tailored for IT leaders at media companies transitioning from traditional IT DR to broadcast-specific resilience requirements.
