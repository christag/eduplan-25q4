# NotebookLM Lesson Plan: BEC & Token-Theft Drills (Runbook + Rehearsal)

## Sources (15)

https://www.paloaltonetworks.com/resources/datasheets/bec-readiness-assessment
https://frsecure.com/business-email-compromise-response-guide/
https://www.rivialsecurity.com/blog/incident-response-playbook-business-email-compromise-bec
https://www.paloaltonetworks.com/unit42/assess/business-email-compromise
https://www.paloaltonetworks.com/cyberpedia/what-is-business-email-compromise-bec-tactics-and-prevention
https://www.secretservice.gov/investigations/bec
https://www.kroll.com/en/services/cyber-risk/incident-response-litigation-support/business-email-compromise-bec
https://www.pondurance.com/cybersecurity-common-attack-vectors/business-email-compromise-(bec)
https://www.microsoft.com/en-us/security/blog/2022/07/12/from-cookie-theft-to-bec-attackers-use-aitm-phishing-sites-as-entry-point-to-further-financial-fraud/
https://www.microsoft.com/en-us/security/blog/2023/12/12/how-to-defend-against-oauth-phishing-attacks/
https://www.crowdstrike.com/cybersecurity-101/cyberattacks/business-email-compromise-bec/
https://www.proofpoint.com/us/threat-reference/business-email-compromise
https://www.darkreading.com/cyberattacks-data-breaches/session-token-theft-phishing-attack-trend
https://unit42.paloaltonetworks.com/threat-brief-transparent-tribe-targets-education-entities/
https://www.cisa.gov/sites/default/files/publications/TLP-WHITE%20BEC%20Fact%20Sheet-508.pdf

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | BEC Readiness Assessment - Palo Alto | Assessment framework, preparation |
| 2 | BEC Response Guide - FRSecure | Step-by-step response playbook |
| 3 | IR Playbook BEC - Rivial Security | Incident response procedures |
| 4 | Unit 42 BEC Assessment - Palo Alto | Professional assessment services |
| 5 | What is BEC - Palo Alto Cyberpedia | BEC tactics, prevention strategies |
| 6 | BEC Investigations - Secret Service | Government perspective, statistics |
| 7 | BEC Response - Kroll | Fast response, decisive action |
| 8 | BEC Attack Vectors - Pondurance | Common attack patterns |
| 9 | Cookie Theft to BEC - Microsoft | AITM phishing, token theft techniques |
| 10 | Defend OAuth Phishing - Microsoft | Token-based attack prevention |
| 11 | BEC Overview - CrowdStrike | Attack lifecycle, detection |
| 12 | BEC Threat Reference - Proofpoint | Comprehensive threat analysis |
| 13 | Session Token Theft - Dark Reading | Emerging phishing trends |
| 14 | Threat Brief Token Theft - Unit 42 | Real-world attack examples |
| 15 | BEC Fact Sheet - CISA | Government guidance, best practices |

## Audio Overview Prompts

### Overview 1: Understanding BEC and Token Theft Attack Patterns

You are creating an audio overview for a senior IT director at Morning Brew who needs to understand Business Email Compromise and modern token theft attacks - how they work, why they're effective, and why traditional security controls often fail to stop them.

**Cover:** BEC definition - social engineering attacks targeting wire transfers, payroll, sensitive data; BEC scale - FBI IC3 reports 21,489 complaints, $2.9B losses in 2023; Common BEC scenarios - CEO fraud, vendor impersonation, payroll redirect, W-2 phishing; Why BEC works - exploits trust, urgency, authority; Evolution from basic email spoofing to sophisticated techniques; Modern token theft (session hijacking) - bypassing MFA via adversary-in-the-middle (AitM) phishing; How AitM phishing works - proxying legitimate login pages, stealing session cookies/tokens; OAuth phishing - tricking users into granting malicious app permissions; Why MFA doesn't stop token theft - attackers steal authenticated sessions, not passwords; Real-world examples - Lapsus$, Transparent Tribe, nation-state actors; The finance/HR targeting pattern - high-value, time-sensitive operations; Detection challenges - legitimate credentials, normal-looking behavior, short attack windows.

**Exclude:** Response procedures (Overview 2), Drill design (Overview 3), Prevention controls (Overview 4), Program maturity (Overview 5).

### Overview 2: Building Your BEC Incident Response Playbook

You are creating an audio overview for a senior IT director who understands BEC/token theft attacks (from Overview 1) and needs to create an incident response playbook specifically for these financial fraud scenarios.

**Cover:** Why BEC needs a specific playbook - time-sensitive, financial impact, legal considerations; Playbook structure - detection, containment, investigation, remediation, recovery, lessons learned; Detection phase - user reports suspicious emails, unusual wire transfer requests, anomalous logins; Triage and classification - is this actual BEC, what's the potential impact; Immediate containment actions - freezing wire transfers, disabling compromised accounts, revoking OAuth tokens/sessions; Financial institution notification - contacting banks within hours to potentially reverse transfers; Stakeholder notification tree - who to tell, when, what to say (CFO, legal, law enforcement); Investigation steps - email header analysis, login log review, token usage patterns, blast radius assessment; Evidence preservation - maintaining chain of custody for potential legal action; Communication templates - internal notifications, user warnings, external stakeholder updates; Recovery procedures - restoring access, changing credentials, resetting sessions; Post-incident activities - root cause analysis, control improvements, stakeholder debrief; Integration with existing IR plans - where BEC fits with other incident types; Contact information - law enforcement (FBI IC3, Secret Service), legal counsel, cyber insurance.

**Exclude:** Attack mechanics (Overview 1), Drill execution (Overview 3), Technical controls (Overview 4), Long-term program (Overview 5).

### Overview 3: Designing and Running Tabletop Exercises

You are creating an audio overview for a senior IT director who has a BEC response playbook (from Overviews 1-2) and needs to test it through realistic tabletop exercises that prepare the team for actual incidents.

**Cover:** Why tabletop exercises matter - finding playbook gaps before real incidents, building muscle memory; Tabletop vs. live drills - simulated discussion vs. actual execution; Exercise objectives - testing specific procedures, identifying gaps, training responders; Scenario design - realistic BEC scenarios based on your environment (CEO fraud, vendor impersonation); Injects and plot twists - complications that test adaptability (CFO unavailable, wire already sent, attacker still active); Participant selection - finance, IT, security, HR, legal, executives; Facilitation best practices - neutral facilitator, safe environment, no-blame culture; Exercise flow - introduction, scenario presentation, injects, group discussion, decision-making; Time pressure simulation - making decisions with incomplete information, under urgency; Role-playing - assign roles (incident commander, communications lead, technical lead); Documentation during exercise - decisions made, gaps identified, timing issues; After-action review (AAR) - what went well, what didn't, what to improve; Red team perspective - thinking like attacker to stress-test defenses; Frequency and iteration - quarterly exercises, varying scenarios, increasing complexity; Building relationships - finance and IT collaboration, external contacts (FBI, legal).

**Exclude:** Playbook content (Overview 2), Prevention controls (Overview 4), Program maturity (Overview 5).

### Overview 4: Prevention and Detection Controls

You are creating an audio overview for a senior IT director who can respond to BEC (from Overviews 1-3) but needs to implement preventive and detective controls to reduce BEC risk and catch attacks earlier.

**Cover:** User awareness training - recognizing BEC red flags, verifying requests via alternate channel; Phishing-resistant MFA - FIDO2, passkeys that can't be phished; Conditional access policies - blocking legacy auth, geo-fencing, device trust; Email security controls - SPF, DKIM, DMARC for domain spoofing; Advanced email filtering - ML-based anomaly detection, display name spoofing detection; Token binding and protection - device-bound tokens, limiting token lifetime; Impossible travel detection - alerting on session replay from different location; OAuth app governance - preventing malicious app consent, reviewing permissions; Financial controls - dual approval for wire transfers, callback verification for large transfers; Change management for sensitive changes - payroll, W-2 requests, vendor updates require additional verification; Out-of-band verification procedures - calling known numbers, never numbers in suspicious emails; User reporting mechanisms - easy "report phishing" button, security-aware culture; SIEM use cases for BEC - unusual file access, after-hours wire requests, token anomalies; Threat intelligence - known BEC campaigns, C2 domains, attacker TTPs; Regular control testing - simulated phishing, BEC attempts, token theft scenarios.

**Exclude:** Attack patterns (Overview 1), Response procedures (Overview 2), Drill mechanics (Overview 3), Program maturity (Overview 5).

### Overview 5: Building a Mature BEC Defense Program

You are creating an audio overview for a senior IT director who has playbooks, drills, and controls (from Overviews 1-4) and needs to build a mature, continuously-improving BEC defense program.

**Cover:** Program maturity model - reactive to proactive to predictive; Metrics that matter - attempted BECs detected, time to detect, false positive rate, employee reporting rate; Continuous improvement - applying lessons from exercises and real incidents; Red team engagements - hiring professional services to attempt BEC, finding weaknesses; Bug bounty programs - incentivizing external researchers to find social engineering weaknesses; Scenario library - maintaining varied, realistic exercise scenarios based on emerging threats; Cross-functional partnerships - deep integration between IT, finance, HR, legal; Executive sponsorship - CISO and CFO partnership, board reporting; Simulated BEC campaigns - sanctioned tests with real employees (with boundaries); Measuring awareness - phishing simulation click rates, reporting rates, time to report; Technology evolution - adopting new controls as they mature (FIDO2, FAPI, token binding); Threat intelligence integration - incorporating latest BEC TTPs into training and controls; Benchmarking - comparing your program to peer organizations; Insurance and risk transfer - cyber insurance for BEC, understanding coverage limits; Regulatory compliance - SEC disclosure requirements, customer notifications; Building organizational resilience - BEC defense as part of broader security culture.

**Exclude:** Core attack types (Overview 1), Initial playbook creation (Overview 2), First tabletop exercise (Overview 3), Basic controls (Overview 4).

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Copy all URLs from the Sources section and paste into NotebookLM
3. Generate audio overviews using the prompts in sequence (1→2→3→4→5)

This learning path takes you from understanding BEC and token theft through response planning, drill execution, prevention controls, and program maturity.
