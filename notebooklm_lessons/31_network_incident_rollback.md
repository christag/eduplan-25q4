# NotebookLM Lesson Plan: Network Incident Rollback & Change Control

## Sources (15)

https://www.techtarget.com/searchnetworking/tip/5-principles-of-the-network-change-management-process
https://www.algosec.com/blog/network-change-management-best-practices
https://netboxlabs.com/blog/network-change-management/
https://www.firemon.com/blog/change-management-best-practices/
https://www.atlassian.com/itsm/change-management
https://whatfix.com/blog/itil-change-management/
https://www.atlassian.com/itsm/change-management/change-advisory-board
https://wiki.en.it-processmaps.com/index.php/Change_Management
https://www.guidepointsecurity.com/incident-response-playbook-and-runbook-creation/
https://incident.io/blog/what-are-runbooks
https://www.atlassian.com/incident-management/incident-response/how-to-create-an-incident-response-playbook
https://www.techtarget.com/searchnetworking/tip/Automate-network-validation-for-smoother-changes
https://ipfabric.io/blog/testing-procedures-for-network-changes/
https://codilime.com/blog/ansible-vs-terraform-in-networks/
https://www.rogerperkin.co.uk/git/using-git-for-network-configuration-management/

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | 5 Principles of Network Change Management - TechTarget | Change management framework, principles, process |
| 2 | Network Change Management Best Practices - AlgoSec | Best practices, automation, risk reduction |
| 3 | Introduction to Network Change Management - NetBox Labs | Change management overview, key concepts |
| 4 | Network Configuration and Change Management - FireMon | Configuration management, compliance, best practices |
| 5 | IT Change Management: ITIL Framework - Atlassian | ITIL framework, change types, approval process |
| 6 | What Is IT Change Management? - Whatfix | Benefits, types, implementation |
| 7 | Change Advisory Board Explained - Atlassian | CAB structure, roles, responsibilities |
| 8 | Change Management - IT Process Wiki | Comprehensive ITIL change management reference |
| 9 | Incident Response Playbooks & Runbooks - GuidePoint Security | Runbook creation, playbook development |
| 10 | What Are Runbooks? - incident.io | Runbook definition, incident management integration |
| 11 | How to Create an Incident Response Playbook - Atlassian | Playbook creation, incident response procedures |
| 12 | Automate Network Validation - TechTarget | Pre/post-change validation, automation |
| 13 | Testing Procedures for Network Changes - IP Fabric | Testing methodologies, validation procedures |
| 14 | Ansible vs Terraform in Networks - Codilime | Infrastructure as code, automation tools |
| 15 | Using Git for Network Configuration Management - Roger Perkin | Version control, configuration tracking |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: ITIL Change Management Framework and Process

You are creating an audio overview for a senior IT director at Morning Brew (a mid-size media company) who is leveling up to higher-level tech leadership. They have hands-on experience managing network infrastructure but want to understand formal change management frameworks, particularly ITIL, to bring more maturity and rigor to their network change processes.

**Cover in this overview:**
- The ITIL change management framework: what it is, why it exists, and how it structures network changes
- The three types of changes (standard, normal, emergency) and when each applies
- The change management lifecycle: request, assessment, approval, implementation, review
- The five core principles of network change management: planning, communication, testing, rollback readiness, and documentation
- How change management reduces risk, prevents outages, and improves accountability
- The balance between agility and control in change management processes
- How change management fits into IT service management (ITSM) and overall IT maturity

**Exclude from this overview:**
- Detailed Change Advisory Board (CAB) processes (covered in Overview 2)
- Specific rollback procedures and testing methodologies (covered in Overview 3)
- Automation tools and infrastructure as code (covered in Overview 4)
- Runbook creation and post-incident learning (covered in Overview 5)

**Approach:**
Take a strategic, maturity-focused perspective. Help the listener understand why formal change management matters for growing IT organizations and how it prevents the chaos of ad-hoc network changes. Use concrete examples of how different change types work in practice (e.g., patching vs. major network redesign). The listener should come away understanding the business value of structured change management and be able to articulate why this process matters to leadership and the organization.

### Overview 2: Change Advisory Board (CAB) and Approval Processes

You are creating an audio overview for a senior IT director at Morning Brew who now understands the ITIL change management framework (from Overview 1). They need to learn how to establish and run an effective Change Advisory Board (CAB) appropriate for a small-to-mid-size organization, including how to make the CAB process efficient without becoming bureaucratic.

**Cover in this overview:**
- What a CAB is: purpose, composition, and responsibilities
- Who should be on the CAB: technical experts, business stakeholders, change manager role
- How CAB meetings work: agenda, evaluation criteria, decision-making process
- The difference between CAB and Emergency CAB (eCAB) for urgent changes
- How to assess change requests: technical impact, business risk, resource requirements, timing
- Approval workflows and decision documentation
- Right-sizing the CAB process for smaller organizations: avoiding bureaucracy while maintaining rigor
- How to handle standard changes (pre-approved) vs. normal changes requiring full CAB review
- Common pitfalls: becoming a bottleneck, rubber-stamping changes, inadequate technical review

**Exclude from this overview:**
- ITIL framework fundamentals (already covered in Overview 1)
- Technical rollback procedures and testing (covered in Overview 3)
- Automation and infrastructure as code tools (covered in Overview 4)
- Runbook development and post-incident processes (covered in Overview 5)

**Approach:**
Make this practical and actionable for a small IT team. The listener should understand how to establish a lightweight but effective CAB that provides real value without slowing down their team. Emphasize the balance between governance and agility. Use examples of what good vs. bad CAB processes look like. The listener should feel equipped to propose and implement a CAB process at their organization.

### Overview 3: Rollback Procedures, Testing, and Validation

You are creating an audio overview for a senior IT director at Morning Brew who understands change management frameworks and CAB processes (from Overviews 1-2). Now they need deep technical knowledge on how to design rollback procedures, test network changes, and validate that changes work as intended before and after implementation.

**Cover in this overview:**
- Why rollback procedures are critical: preventing extended outages, reducing change risk
- Designing effective rollback procedures: identifying rollback points, documentation, time constraints
- Pre-implementation testing strategies: lab environments, staging networks, configuration validation
- Network validation approaches: model-based analysis, emulation, operational state testing
- Pre-change and post-change validation: what to check, how to verify success
- Automated vs. manual testing: when each is appropriate, tools for automation
- Testing procedures for network changes: pre-checks, continuous checks, post-checks
- Tools for network validation: Batfish, IP Fabric, and other validation frameworks
- Time-boxing changes: knowing when to rollback vs. troubleshooting forward
- Testing rollback procedures themselves: ensuring the rollback actually works

**Exclude from this overview:**
- ITIL change management framework overview (already covered in Overview 1)
- CAB structure and approval processes (already covered in Overview 2)
- Infrastructure as code and automation platforms (covered in Overview 4)
- Runbook creation and post-incident reviews (covered in Overview 5)

**Approach:**
This should be highly technical and practical. The listener should come away with concrete strategies for testing network changes and designing rollback procedures they can implement immediately. Use real-world examples of changes that failed and how proper testing/rollback procedures would have prevented or minimized the impact. Emphasize the "fail fast" principle and knowing when to rollback. The listener should feel confident designing comprehensive testing and rollback strategies.

### Overview 4: Automation, Infrastructure as Code, and Version Control

You are creating an audio overview for a senior IT director at Morning Brew who understands change management processes and rollback procedures (from Overviews 1-3). Now they want to learn how modern automation tools, infrastructure as code practices, and version control systems can make network change management more reliable, repeatable, and auditable.

**Cover in this overview:**
- Infrastructure as Code (IaC) for network management: what it is and why it matters
- Version control for network configurations using Git: tracking changes, rollback capability, collaboration
- Ansible vs. Terraform for network automation: use cases, strengths, when to use each
- How IaC enables automated rollbacks: version-tagged configurations, instant reversion
- Configuration management tools: automated backups, drift detection, compliance validation
- CI/CD pipelines for network changes: automated testing, staged deployments, rollback triggers
- Monitoring and automated rollback triggers: detecting failures, automatic reversion
- The relationship between automation and change management: speed vs. control
- Starting small: pilot automation projects, building automation maturity
- How automation improves change documentation and audit trails

**Exclude from this overview:**
- ITIL framework and change management basics (already covered in Overview 1)
- CAB processes and approval workflows (already covered in Overview 2)
- Manual rollback procedures and testing methodologies (already covered in Overview 3)
- Runbook documentation and incident response (covered in Overview 5)

**Approach:**
Bridge the gap between traditional change management and modern automation practices. Help the listener see how automation accelerates change management rather than bypassing it. Use concrete examples of how Git, Ansible, and Terraform fit into the change management lifecycle. The listener should understand the maturity path from manual changes to fully automated network deployments. Emphasize practical first steps appropriate for a small IT team at a mid-size company.

### Overview 5: Runbooks, Documentation, and Post-Incident Learning

You are creating an audio overview for a senior IT director at Morning Brew who now understands change management frameworks, CAB processes, rollback procedures, and automation tools (from Overviews 1-4). Now they need to learn how to create effective runbooks, maintain change documentation, and establish post-incident learning processes that continuously improve the change management program.

**Cover in this overview:**
- What runbooks are and how they differ from playbooks and incident response plans
- Creating effective network change runbooks: step-by-step procedures, decision trees, contact information
- Essential elements to include in runbooks: system layouts, dependencies, startup/shutdown sequences, rollback steps
- Documentation best practices: keeping runbooks current, quarterly validation, post-incident updates
- The relationship between runbooks and change management: using runbooks for standard changes
- Post-implementation reviews (PIRs): what went well, what went wrong, lessons learned
- Post-incident learning rituals: blameless postmortems, process improvements, knowledge sharing
- Change failure analysis: identifying patterns, preventing repeat failures
- Building organizational memory: documenting decisions, capturing context, knowledge management
- Continuous improvement of change processes: metrics, feedback loops, process refinement
- Creating a culture of documentation: making it valuable, keeping it lightweight

**Exclude from this overview:**
- ITIL change management framework (already covered in Overview 1)
- CAB structure and processes (already covered in Overview 2)
- Technical rollback and testing procedures (already covered in Overview 3)
- Automation tools and infrastructure as code (already covered in Overview 4)

**Approach:**
Focus on building sustainable, learning-oriented practices that improve over time. Help the listener understand that great change management requires great documentation and a commitment to learning from failures. Use examples of effective runbooks and post-incident review processes. Emphasize pragmatic documentation that provides real value without becoming burdensome. The listener should feel equipped to establish documentation standards and post-incident learning rituals that make their change management program continuously better.

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Select and copy all URLs from the "Sources" section above (they are plain URLs with no formatting)
3. Paste the URLs directly into NotebookLM's source input
4. For each audio overview:
   - Click "Generate Audio Overview"
   - Copy and paste the corresponding prompt above
   - Generate the overview
5. Listen to overviews in sequence (1→2→3→4→5)

Each overview builds on the previous ones, creating a comprehensive learning path from change management frameworks through automation and continuous improvement.

This learning path is tailored for IT leaders at mid-size companies transitioning to more mature change management practices.
