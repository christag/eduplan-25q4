# NotebookLM Lesson Plan: Automated Cost Guardrails

## Sources (15)

https://medium.com/cloud-cost-savings/aws-cost-savings-playbook-4-cost-guardrails-e90407984eda
https://www.finops.org/framework/capabilities/anomaly-management/
https://www.finops.org/framework/capabilities/allocation/
https://portkey.ai/blog/budget-limits-and-alerts-in-llm-apps/
https://www.truefoundry.com/blog/llm-cost-tracking-solution
https://www.truefoundry.com/blog/rate-limiting-in-llm-gateway
https://medium.com/@ladibnasr/enforcing-secure-and-cost-effective-infrastructure-as-code-with-terraform-opa-and-infracost-22b4b4c880c2
https://www.infracost.io/
https://www.bettercloud.com/monitor/saas-spend-management-for-it/
https://www.zluri.com/blog/saas-spend-management-tools
https://www.finout.io/virtual-tagging
https://www.finout.io/blog/showback-vs-chargeback
https://cloud.google.com/blog/topics/cost-management/introducing-cost-anomaly-detection
https://konghq.com/blog/engineering/ai-guardrails
https://spacelift.io/blog/terraform-policy-as-code

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | AWS Cost Savings Playbook: Cost Guardrails | AWS budgets, automated actions, controls |
| 2 | FinOps Anomaly Management Capability | anomaly detection, alerting, ML-based |
| 3 | FinOps Allocation Capability | tagging, chargeback, showback |
| 4 | Budget Limits and Alerts in LLM Apps | AI cost controls, token budgets |
| 5 | LLM Cost Tracking Solution | observability, governance, optimization |
| 6 | Rate Limiting in AI Gateway | token-based limiting, quotas |
| 7 | Terraform, OPA, and Infracost for IaC Cost Controls | policy-as-code, pre-deployment cost checks |
| 8 | Infracost: Shift FinOps Left | Terraform cost estimation, PR comments |
| 9 | SaaS Spend Management for IT (BetterCloud) | license optimization, automated reclamation |
| 10 | Top SaaS Spend Management Tools (Zluri) | SaaS discovery, usage tracking, spend optimization |
| 11 | Instant Virtual Tagging (Finout) | automated cost allocation, patented technology |
| 12 | Showback vs Chargeback (Finout) | cost visibility, accountability models |
| 13 | GCP Cost Anomaly Detection | machine learning anomaly detection |
| 14 | AI Guardrails for Cost Control (Kong) | LLM rate limiting, budget enforcement |
| 15 | Terraform Policy as Code (Spacelift) | OPA/Sentinel, infrastructure cost policies |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: Understanding Automated Cost Guardrails

You are creating an audio overview for a senior IT director at a media company (Morning Brew Inc.) who manages cloud infrastructure, SaaS applications, and an AI hub. This is a mid-priority topic for implementing automated controls to prevent cost overruns and improve financial accountability.

**Listener Profile:**
The listener manages a lean IT team and has experienced cost surprises from cloud resources, AI/LLM usage, or SaaS license sprawl. They understand basic FinOps concepts and want to implement automated cost guardrails to prevent runaway spending without adding manual overhead.

**Coverage Scope:**
Focus on:
- What automated cost guardrails are and why they matter for small IT teams
- The problem: cost surprises from cloud, AI/LLM, SaaS, and shadow IT
- Three pillars of cost guardrails: prevention (pre-deployment), detection (anomaly monitoring), and response (automated actions)
- Cost anomaly detection using machine learning (FinOps Foundation framework)
- Automated budget alerts and actions (AWS Budgets, Azure Cost Management, GCP Budget Actions)
- Difference between preventive controls (policy-as-code) and reactive controls (anomaly detection + alerts)
- Real-world cost blowup scenarios: misconfigured auto-scaling, zombie resources, uncapped AI inference, unused SaaS licenses

**DO NOT cover** (these will be addressed in later overviews):
- Specific implementation for AI/LLM cost controls (Overview 2)
- Infrastructure-as-code cost policies (Overview 3)
- SaaS spend management and chargeback/showback (Overview 4)

**Approach:**
Build awareness of the three-layer approach: prevent, detect, respond. Help the listener understand that automated guardrails reduce manual toil and catch problems before they become expensive. Use relatable examples from cloud, AI, and SaaS contexts.

---

### Overview 2: AI and LLM Cost Controls

You are creating an audio overview for a senior IT director who understands automated cost guardrails (from Overview 1) and now needs specific techniques for controlling AI and LLM costs, which are particularly volatile and difficult to predict.

**Listener Profile:**
Same listener. They manage an AI hub with various LLM integrations and have experienced unpredictable AI costs due to token-based pricing. They want automated controls specific to LLM workloads.

**Coverage Scope:**
Focus on:
- Why LLM cost control is different: token-based pricing, variable compute load, unpredictable usage patterns
- Token-based rate limiting (not request-based): tokens_per_minute, tokens_per_hour, tokens_per_day
- Multi-level quotas: per-user, per-team, per-environment, per-model
- Budget limits and alerts for LLM applications (real-time tracking, threshold alerts)
- LLM gateway pattern: centralized inference traffic for observability and control
- Automated tagging for cost attribution: by feature, team, workflow, use case
- Preventing "runaway" AI workloads (infinite loops, uncapped batch processing)
- Model-specific cost policies: restricting expensive models to production, cheaper models for dev/test
- Kong, Portkey, LiteLLM, TrueFoundry as LLM gateway/control platforms

**DO NOT cover** (already covered or will be covered later):
- General cost guardrail concepts (Overview 1)
- Infrastructure-as-code policies (Overview 3)
- SaaS/license management (Overview 4)

**Approach:**
Be specific to the AI/LLM domain. Emphasize that traditional cloud cost controls don't translate directly to LLMs because of token-based pricing. Provide concrete examples of token quotas and budget thresholds. Highlight the LLM gateway pattern as the key architectural control point.

---

### Overview 3: Infrastructure-as-Code Cost Policies

You are creating an audio overview for a senior IT director who understands cost guardrails and AI cost controls (from Overviews 1-2) and now wants to implement "shift-left" cost controls using infrastructure-as-code policy enforcement.

**Listener Profile:**
Same listener. They use Terraform or similar IaC tools and want to prevent costly infrastructure from being deployed in the first place, rather than discovering it in billing data later.

**Coverage Scope:**
Focus on:
- "Shift FinOps left": catching cost problems before deployment, not after
- Policy-as-code for cost controls: Open Policy Agent (OPA) and HashiCorp Sentinel
- Infracost: automated Terraform cost estimation in pull requests
- Pre-deployment cost checks: estimating infrastructure costs before apply
- Policy examples: restricting instance types in dev (t2.micro only), blocking expensive SKUs, setting environment-specific cost limits
- Terraform + OPA + Infracost integration: automated, policy-enforced cost governance
- Pull request cost comments: making cost visible in code review workflow
- Enforcing cost policies in CI/CD pipelines (fail builds that exceed thresholds)
- Balancing developer velocity with cost control

**DO NOT cover** (already covered or will be covered later):
- General cost guardrail framework (Overview 1)
- AI/LLM-specific controls (Overview 2)
- SaaS spend management (Overview 4)

**Approach:**
Be practical about shift-left FinOps. Help the listener understand that preventing expensive infrastructure from being deployed is more effective than reacting to cost anomalies. Emphasize Infracost as a lightweight, developer-friendly tool that integrates into existing Terraform workflows. Connect to their DevOps practices (PR reviews, CI/CD).

---

### Overview 4: SaaS Spend Management and Cost Allocation

You are creating an audio overview for a senior IT director who understands cloud and AI cost controls (from Overviews 1-3) and now needs to tackle SaaS spend management, license optimization, and cost allocation (chargeback/showback).

**Listener Profile:**
Same listener. They manage dozens or hundreds of SaaS applications, often with shadow IT, duplicate subscriptions, and unused licenses. They want automated discovery, usage tracking, and cost allocation for accountability.

**Coverage Scope:**
Focus on:
- The SaaS spend problem: 60% of apps unknown, 55% increase in per-employee SaaS cost since 2021, unused licenses, duplicates
- Automated SaaS discovery: finding sanctioned and shadow IT applications
- License optimization: usage monitoring, automated reclamation of unused licenses, identifying underutilized apps
- SaaS management platforms: BetterCloud, Zluri, Trelica, Zylo, Flexera
- Cost allocation through tagging: assigning costs to teams, departments, projects
- Showback vs. chargeback: visibility vs. financial accountability (recommend starting with showback)
- Virtual tagging (Finout): automated cost attribution without manual tagging
- Automated reporting: integrating with finance tools, dashboards for team visibility
- SaaS procurement policies: centralizing purchases to improve visibility and control

**DO NOT cover** (already covered in previous overviews):
- General cost guardrail concepts (Overview 1)
- AI/LLM cost controls (Overview 2)
- IaC cost policies (Overview 3)

**Approach:**
Be pragmatic about SaaS sprawl. Help the listener understand that SaaS spend is often invisible until you implement discovery and tracking. Emphasize automated license reclamation as quick ROI. Explain showback as the recommended starting point before implementing full chargeback. Provide a framework: discover → track → optimize → allocate.

---

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Select and copy all URLs from the "Sources" section above (they are plain URLs with no formatting)
3. Paste the URLs directly into NotebookLM's source input
4. For each audio overview:
   - Click "Generate Audio Overview"
   - Copy and paste the corresponding prompt above
   - Generate the overview
5. Listen to overviews in sequence (1→2→3→4)

---

## Learning Objectives

After completing all four audio overviews, you will:

1. Understand the three-pillar approach to cost guardrails: prevention, detection, response
2. Know how to implement cloud cost anomaly detection and automated budget actions
3. Understand AI/LLM-specific cost controls: token-based rate limiting, quotas, budgets
4. Be familiar with the LLM gateway pattern for centralizing AI cost control
5. Know how to implement "shift-left" FinOps using Terraform, OPA, and Infracost
6. Understand policy-as-code for preventing costly infrastructure deployments
7. Have a framework for SaaS spend management: discover, track, optimize, allocate
8. Understand showback vs. chargeback and when to use each approach
