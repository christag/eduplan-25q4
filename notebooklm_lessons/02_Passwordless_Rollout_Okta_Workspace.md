# NotebookLM Lesson Plan: Passwordless Rollout Playbook (Okta+Workspace)

## Sources (15)

https://fidoalliance.org/passkeys/
https://frontegg.com/guides/passwordless-authentication-with-fido2-and-webauthn
https://www.microsoft.com/en-us/security/business/security-101/what-is-fido2
https://www.okta.com/resources/whitepaper-how-to-go-passwordless-with-okta-0/
https://help.okta.com/oie/en-us/content/topics/identity-engine/password-optional/password-optional-disabled.htm
https://www.okta.com/passwordless-authentication/
https://support.google.com/a/answer/13529161
https://workspace.google.com/blog/product-announcements/major-security-innovation-passkeys
https://www.doit.com/blog/implementing-passwordless-login-with-google-workspace/
https://bitwarden.com/blog/what-passwordless-adoption-means-to-enterprises/
https://blog.hypr.com/tips-to-navigate-passkey-adoption
https://www.1kosmos.com/insights/whitepapers/overcoming-change-with-passwordless-mfa/
https://learn.microsoft.com/en-us/windows/security/identity-protection/passwordless-strategy/
https://www.idsalliance.org/blog/a-practical-approach-to-passwordless/
https://www.techtarget.com/searchenterprisedesktop/feature/Passwordless-authentication-options-and-best-practices

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | Passkeys - FIDO Alliance | FIDO2, WebAuthn fundamentals, passkeys overview |
| 2 | Passwordless Authentication with FIDO2 and WebAuthn - Frontegg | Technical implementation, cryptographic protocols |
| 3 | What Is FIDO2? - Microsoft Security | FIDO2 fundamentals, standards overview |
| 4 | How to Go Passwordless with Okta - Okta Whitepaper | Okta implementation strategy, roadmap |
| 5 | Set up passwordless sign-in - Okta Help | Okta configuration, technical setup |
| 6 | Passwordless Authentication - Okta | Okta methods, FastPass, WebAuthn |
| 7 | Allow users to skip passwords - Google Workspace Admin | Workspace admin configuration, setup |
| 8 | Major Security Innovation with Passkeys - Google Workspace Blog | Workspace passkeys announcement, capabilities |
| 9 | Implementing Passwordless Login with Google Workspace - DoiT | Workspace implementation guide, practical steps |
| 10 | What Passwordless Adoption Means to Enterprises - Bitwarden | Enterprise adoption, change management |
| 11 | Navigate Passkey Adoption - HYPR | Adoption strategies, user onboarding |
| 12 | Overcoming Change with Passwordless MFA - 1Kosmos | Change management, resistance strategies |
| 13 | Passwordless Strategy Overview - Microsoft Learn | Enterprise deployment, best practices |
| 14 | A Practical Approach To Passwordless - IDSA | Implementation roadmap, phasing |
| 15 | Passwordless Authentication Options and Best Practices - TechTarget | Security considerations, technology comparison |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: Passwordless Authentication Fundamentals (FIDO2, WebAuthn, Passkeys)

You are creating an audio overview for a senior IT director at Morning Brew who understands traditional MFA (SMS, TOTP, push notifications) and wants to deeply understand passwordless authentication technologies. They need the technical foundation to confidently implement passwordless at their organization.

**Cover in this overview:**
- What passwordless authentication means - the spectrum from "password optional" to "no passwords stored"
- FIDO2 standards architecture: how WebAuthn (W3C) and CTAP (FIDO Alliance) work together
- Public key cryptography fundamentals: how asymmetric keys replace passwords
- Passkeys vs. security keys: single-device vs. multi-device credentials, when to use each
- How passkeys work: registration flow, authentication flow, and what happens behind the scenes
- Platform authenticators (Face ID, Windows Hello, Android biometrics) vs. roaming authenticators (YubiKey, Titan Security Key)
- Phishing resistance: why passkeys are immune to credential theft, man-in-the-middle attacks, and social engineering
- Cross-platform support: current state of passkeys across Apple, Google, Microsoft ecosystems

**Exclude from this overview:**
- Okta-specific implementation (covered in Overview 2)
- Google Workspace-specific implementation (covered in Overview 3)
- User adoption and change management strategies (covered in Overview 4)
- Enterprise deployment roadmap and rollout phasing (covered in Overview 5)

**Approach:**
Make the technology accessible but don't oversimplify - this listener needs to understand "how it really works" to make informed decisions and explain it to both technical and executive stakeholders. Use concrete examples like "when you tap your YubiKey, here's what happens..." The listener should come away understanding why passwordless is more secure than traditional MFA, not just that "it is."

### Overview 2: Okta Passwordless Implementation

You are creating an audio overview for a senior IT director at Morning Brew who already understands passwordless fundamentals (from Overview 1) and uses Okta as their identity platform. They need practical, step-by-step guidance on implementing passwordless in Okta.

**Cover in this overview:**
- Okta's passwordless methods: Okta FastPass, WebAuthn/FIDO2, Okta Verify with biometrics, email magic links
- Okta FastPass deep dive: how it works, device trust, platform support (Windows, macOS, iOS, Android), why it doesn't require AD domain join
- Configuration walkthrough: authenticator enrollment policies, authentication policies, global session policies
- Factor sequencing: allowing users to skip passwords by using secondary factors as primary
- App integration considerations: which Okta-integrated apps support passwordless, limitations with legacy apps
- Coexistence strategy: running password and passwordless side-by-side during transition
- Admin experience: policy configuration, monitoring enrollment, troubleshooting common issues
- Real-world implementation patterns: phased rollout approaches, pilot groups, which authenticators to enable first

**Exclude from this overview:**
- Passwordless fundamentals (already covered in Overview 1)
- Google Workspace-specific configuration (covered in Overview 3)
- User adoption strategies and change management (covered in Overview 4)
- Detailed rollout planning and timelines (covered in Overview 5)

**Approach:**
This should feel like a technical implementation guide from an experienced Okta admin. Walk through the actual configuration steps in logical order. Address common gotchas and decision points ("should you require device trust?" "which authenticators for which user groups?"). The listener should feel confident opening their Okta admin console and beginning the configuration. Reference the official Okta documentation and whitepapers for specific policy examples.

### Overview 3: Google Workspace Passwordless Integration

You are creating an audio overview for a senior IT director at Morning Brew who understands passwordless technology (from Overview 1) and Okta implementation (from Overview 2). Their organization uses Google Workspace, and they need to understand how passkeys work specifically with Workspace and how to integrate with their Okta deployment.

**Cover in this overview:**
- Google Workspace passkeys: how they differ from standard Google account passkeys, what's generally available vs. beta
- Admin setup in Google Workspace: navigating Security > Authentication > Passwordless in the admin console
- Passwordless vs. 2SV: allowing users to skip passwords entirely vs. using passkeys as a second factor
- Device compatibility: which platforms and browsers support Workspace passkeys, mobile considerations
- The integration flow: how Okta and Google Workspace work together with passkeys (federated identity considerations)
- User enrollment process: g.co/passkeys, creating/managing passkeys, device-specific vs. synced passkeys
- Security key restrictions: when to limit passkeys to physical security keys only (compliance requirements)
- Audit and monitoring: tracking passkey enrollment, identifying users still on passwords, security logs
- Advanced capabilities: Account Takeover Protection, Device Bound Session Credentials (DBSC)

**Exclude from this overview:**
- Core passkeys and FIDO2 fundamentals (already covered in Overview 1)
- Okta configuration details (already covered in Overview 2)
- User change management and adoption strategies (covered in Overview 4)
- Overall enterprise rollout timeline and phases (covered in Overview 5)

**Approach:**
Focus on the intersection of Workspace and Okta - how these two systems work together for passwordless. Help the listener understand the admin experience in Workspace and how it complements their Okta configuration. Address the practical question: "If we're using Okta for SSO, what happens with Workspace passkeys?" The listener should understand both the technical architecture and the admin workflows.

### Overview 4: User Adoption and Change Management

You are creating an audio overview for a senior IT director at Morning Brew who understands passwordless technology and has configuration knowledge for Okta and Workspace (from Overviews 1-3). Now they need to understand how to drive user adoption and manage organizational change - the "people side" of passwordless.

**Cover in this overview:**
- The paradox: users hate passwords but resist change - why adoption requires deliberate strategy
- Coexistence approach: giving users choice during transition, side-by-side login experiences, progressive migration
- Pilot programs: selecting early adopter groups, characteristics of good pilot users, pilot success criteria
- Communications strategy: customizing messages by role (executives vs. mobile workers vs. desk workers), timing, channels
- Training approaches: hands-on enrollment sessions, video walkthroughs, self-service guides, office hours
- UX benefits messaging: faster login, no password resets, works offline, cross-device convenience
- Handling resistance: common objections ("what if I lose my device?"), addressing security concerns, FUD management
- Support readiness: help desk training, expected ticket volume, self-service password reset considerations
- Measuring success: enrollment rates, login success rates, help desk ticket trends, user satisfaction surveys
- Real-world case studies: what worked at other organizations (Netflix, Accenture examples from sources)

**Exclude from this overview:**
- Technical fundamentals (already covered in Overview 1)
- System configuration (already covered in Overviews 2 and 3)
- Detailed deployment timeline and phases (covered in Overview 5)

**Approach:**
This is about change management, not technology. Draw on organizational psychology and change management principles. The listener should come away with a toolkit of strategies for driving adoption, handling resistance, and making passwordless feel like an upgrade rather than a mandate. Emphasize empathy for users while maintaining momentum. Use concrete examples of communications, training materials, and engagement tactics from the case studies.

### Overview 5: Enterprise Deployment Roadmap and Security Considerations

You are creating an audio overview for a senior IT director at Morning Brew who understands passwordless technology, system configuration, and user adoption strategies (from Overviews 1-4). Now they need an end-to-end deployment roadmap and must understand critical security considerations.

**Cover in this overview:**
- Pre-deployment: scope definition (which users, which apps, which devices), stakeholder alignment, success criteria
- Phased rollout approach: pilot > early adopters > general rollout > holdout management
- Timeline considerations: realistic timeframes for each phase, dependency sequencing
- Application inventory and readiness: which apps support passwordless, legacy app strategies (factor sequencing, exception policies)
- Device considerations: BYOD vs. corporate-managed, platform fragmentation (Windows/Mac/iOS/Android), backup authenticators
- Security policy decisions: requiring device trust, security key restrictions, attestation requirements, conditional access integration
- Privileged access: different approach for admin accounts, "oil and water" mentality between regular and privileged auth
- Backup and recovery: account recovery flows, what happens when users lose devices, locked-out scenarios
- Monitoring and metrics: real-time enrollment dashboards, authentication success rates, security incident tracking
- Business case: cost savings from reduced password resets ($70 per incident), help desk efficiency, security ROI
- Long-term maintenance: deprecating old authenticators, updating policies as technology evolves, continuous improvement

**Exclude from this overview:**
- Passwordless fundamentals (already covered in Overview 1)
- Detailed Okta and Workspace configuration (already covered in Overviews 2 and 3)
- Change management principles (already covered in Overview 4)

**Approach:**
This is the "putting it all together" overview - a practical roadmap from day 1 to full deployment. Help the listener think through sequencing, dependencies, and decision points. Address both the happy path and contingencies. The listener should be able to create their own project plan after this overview. Emphasize pragmatic choices for resource-constrained IT teams - what's essential vs. nice-to-have. Use the Microsoft and IDSA sources for enterprise best practices and phasing strategies.

## Usage Instructions

1. Create a new notebook in Google NotebookLM
2. Select and copy all URLs from the "Sources" section above (they are plain URLs with no formatting)
3. Paste the URLs directly into NotebookLM's source input
4. For each audio overview:
   - Click "Generate Audio Overview"
   - Copy and paste the corresponding prompt above
   - Generate the overview
5. Listen to overviews in sequence (1→2→3→4→5)

This learning path takes you from passwordless fundamentals through technical implementation in your specific environment (Okta + Workspace) to successful organizational rollout.
