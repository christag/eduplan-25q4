# NotebookLM Lesson Plan: Service Accounts & Automation Identities Hygiene

## Sources (15)

https://www.beyondtrust.com/blog/entry/how-to-manage-and-secure-service-accounts-best-practices
https://nhimg.org/community/nhi-best-practices/nhi-101-best-practices-for-securing-service-accounts/
https://www.zluri.com/blog/service-accounts-best-practices
https://www.strongdm.com/blog/service-accounts
https://www.securden.com/educational/service-account-management.html
https://www.idsalliance.org/identity-defined-security-101-best-practices/
https://www.syteca.com/en/blog/service-account-security
https://www.oasis.security/resources/blog/what-are-service-accounts-and-how-should-you-secure-them
https://astrix.security/learn/blog/the-service-account-guide-part-2-challenges-compliance-and-best-practices/
https://specopssoft.com/blog/service-account-security-best-practices/
https://www.wiz.io/academy/non-human-identity-security
https://www.crowdstrike.com/cybersecurity-101/identity-protection/non-human-identity-security/
https://www.paloaltonetworks.com/cyberpedia/what-is-non-human-identity-management
https://www.cyberark.com/what-is/machine-identity/
https://sonraisecurity.com/learn/non-human-identities-guide/

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | Service Accounts Best Practices - BeyondTrust | Management, security practices |
| 2 | NHI Best Practices - NHI Management Group | Non-human identity fundamentals |
| 3 | Service Accounts Best Practices - Zluri | SaaS service accounts, 7 practices |
| 4 | Service Accounts Guide - StrongDM | Definition, security, access control |
| 5 | Service Account Management 101 - Securden | Practical management guide |
| 6 | Identity Defined Security - IDSA | IAM best practices, identity principles |
| 7 | Service Account Security - Syteca | 5 best practices, safeguarding |
| 8 | What Are Service Accounts - Oasis | Fundamentals, securing guidance |
| 9 | Service Account Compliance - Astrix | Challenges, compliance, best practices |
| 10 | Service Account Security AD - Specops | Active Directory specific practices |
| 11 | Non-Human Identity Security - Wiz Academy | NHI landscape, cloud focus |
| 12 | NHI Security - CrowdStrike | NHI threats, protection strategies |
| 13 | Non-Human Identity Management - Palo Alto | NHI management overview |
| 14 | Machine Identity - CyberArk | Machine credentials, PKI |
| 15 | Non-Human Identities Guide - Sonrai | Cloud NHI, comprehensive guide |

## Audio Overview Prompts

### Overview 1: Understanding Service Accounts and Non-Human Identities

You are creating an audio overview for a senior IT director at Morning Brew who manages service accounts somewhat ad-hoc and needs to understand the scope of the non-human identity problem and why it demands systematic management.

**Cover:** What service accounts are - non-human privileged accounts for applications and services; Types of NHIs - service accounts, API keys, OAuth tokens, certificates, machine identities, bot accounts; The scope problem - NHIs often outnumber human identities 10:1 or more; Why NHIs are high-risk - long-lived credentials, excessive privileges, poor visibility; 80% of breaches involve compromised service accounts; 94% of organizations lack complete NHI oversight; Real-world breach examples via service account compromise; The lifecycle problem - creation is easy, tracking is hard, removal is forgotten; Cloud amplification - every microservice, Lambda, container gets service identities.

**Exclude:** Discovery and inventory methods (Overview 2), Security controls (Overview 3), Platform-specific implementation (Overview 4), Governance programs (Overview 5).

**Approach:** Create urgency around this oft-neglected problem. Help them realize service account sprawl is likely worse than they think and represents significant unmanaged risk.

### Overview 2: Discovery, Inventory, and Visibility

You are creating an audio overview for a senior IT director who understands the NHI risk (from Overview 1) and needs practical methods to discover and inventory all service accounts and automation identities across their environment.

**Cover:** Discovery challenges - service accounts in AD, cloud IAM, SaaS apps, databases, CI/CD systems; Automated discovery tools - identity scanners, CIEM platforms, NHI management solutions; Manual discovery methods - AD queries, cloud IAM exports, application configuration reviews; Creating a comprehensive inventory - identity type, owner, purpose, permissions, last used, credential age; Identity classification - system vs. application vs. infrastructure vs. user-facing; Cloud-specific discovery - AWS IAM roles, Azure service principals, GCP service accounts; SaaS service accounts - Okta service accounts, Workspace service accounts, GitHub tokens; Secret scanning - finding hardcoded credentials in code repositories; Continuous discovery vs. point-in-time inventory.

**Exclude:** Fundamental concepts (Overview 1), Security controls (Overview 3), Platform-specific securing (Overview 4), Long-term governance (Overview 5).

**Approach:** Make discovery practical and achievable. Provide a roadmap for going from "we don't know what we have" to "complete inventory with metadata."

### Overview 3: Security Controls - Credentials, Permissions, and Monitoring

You are creating an audio overview for a senior IT director who has inventoried their service accounts (from Overviews 1-2) and needs to implement security controls to reduce risk.

**Cover:** Credential hygiene - eliminating passwords where possible, certificate-based authentication, managed identities; Password management when required - secure storage in vaults (HashiCorp Vault, Azure Key Vault, AWS Secrets Manager), rotation policies; Least privilege for service accounts - scoping permissions to minimum required; Time-based access for automation - JIT service accounts for temporary tasks; Secrets management - centralized vs. decentralized, rotation automation; Service account authentication methods - managed identities vs. service principals vs. access keys; Monitoring service account usage - behavioral baselines, anomaly detection; Alerting on suspicious activity - unusual access patterns, privilege escalation, credential sharing; Audit logging for forensics; Disabling vs. deleting unused accounts.

**Exclude:** Discovery methods (Overview 2), Platform-specific implementation (Overview 4), Program governance (Overview 5).

**Approach:** Focus on practical security controls that reduce risk without breaking automation. Address the tension between security and operational needs.

### Overview 4: Platform-Specific Implementation (AWS, Azure, GCP, Active Directory)

You are creating an audio overview for a senior IT director who understands service account security principles (from Overviews 1-3) and needs platform-specific implementation guidance.

**Cover:** AWS - IAM roles vs. users for services, instance profiles, cross-account access, access keys rotation, AWS Secrets Manager; Azure - service principals, managed identities (system-assigned vs. user-assigned), Key Vault integration, workload identity federation; GCP - service accounts, workload identity, Secret Manager, short-lived tokens; Active Directory - service account OUs, Group Managed Service Accounts (gMSA), password policies, tiering (Tier 0/1/2); Kubernetes - service account tokens, pod identity, secret management; CI/CD platforms - GitHub Actions secrets, GitLab CI variables, Jenkins credentials; Cross-platform patterns - federated identity, workload identity, OIDC trust; Migration paths - from long-lived keys to managed identities.

**Exclude:** General concepts (Overview 1), Discovery (Overview 2), Generic controls (Overview 3), Program management (Overview 5).

**Approach:** Provide platform-specific technical guidance. Help them understand the native capabilities of each platform and how to leverage them for better NHI security.

### Overview 5: Governance, Compliance, and Continuous Improvement

You are creating an audio overview for a senior IT director who has implemented service account security controls (from Overviews 1-4) and needs to build a sustainable governance program.

**Cover:** Service account lifecycle management - request/approval, provisioning, regular review, deprovisioning; Ownership and accountability - assigning owners to every service account, owner responsibilities; Access certification for service accounts - quarterly or semi-annual reviews; Compliance requirements - SOX, PCI DSS, HIPAA service account controls; Automation of governance - automatic discovery, policy enforcement, remediation workflows; Metrics and KPIs - accounts without owners, accounts with excessive permissions, stale credentials, rotation compliance; Integration with ITSM - service account requests through ServiceNow, Jira; Policy enforcement - blocking creation of non-compliant service accounts; Incident response for service account compromise; Continuous improvement - reducing service account count, improving credential hygiene, automating more controls.

**Exclude:** Fundamentals (Overview 1), Initial discovery (Overview 2), Technical controls (Overviews 3-4).

**Approach:** Help them build a program that sustains itself through automation and clear accountability. Emphasize that service account hygiene requires ongoing discipline, not one-time cleanup.

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Copy all URLs from the Sources section and paste into NotebookLM
3. Generate audio overviews using the prompts in sequence (1→2→3→4→5)

This learning path takes you from understanding the service account risk through practical security controls to sustainable governance.
