# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository contains a curated list of IT leadership and security learning topics designed to level up from a senior IT director role at Morning Brew Inc to a higher-level tech leader position. The topics are stored in `topics.json` and are intended to be converted into NotebookLM notebooks using the `notebooklm-creator` skill.

## Key Context

- **Topics are pre-prioritized**: The topics in `topics.json` have already been ordered and prioritized based on the user's current skills vs. what they're trying to learn. When creating NotebookLM prompts, ensure they reflect this personalized learning path.

- **Priority system**: Topics use a numeric priority system (98 being highest, 35 being lowest) combined with "fit" categories:
  - `near-term`: Immediate focus areas (priority 74-98)
  - `mid`: Medium-term learning goals (priority 52-69)
  - `park`: Future awareness topics (priority 35-38)

- **Effort levels**: Each topic includes an effort indicator:
  - `S` (Small): Quick learning topics or tactical implementations
  - `M` (Medium): Moderate depth topics
  - `L` (Large): Comprehensive, multi-faceted topics

## Data Structure

The `topics.json` file contains a backlog array with topic objects structured as:
```json
{
  "title": "Topic name",
  "origin": "Reference to source material/framework",
  "fit": "near-term|mid|park",
  "effort": "S|M|L",
  "priority": 35-98,
  "why": "Rationale for this topic's importance"
}
```

## Working with NotebookLM

When using the `notebooklm-creator` skill to generate learning content:

1. Consider the user's current role context (senior IT director at Morning Brew)
2. Frame topics as progression toward higher-level tech leadership
3. Respect the priority ordering - higher priority topics should be more immediately actionable
4. Use the "why" field to understand the strategic importance
5. The "origin" field references frameworks or existing organizational context that should inform the learning approach

## Common Topic Themes

Topics span several key areas:
- **Zero Trust & Identity**: Passwordless auth, least privilege, micro-segmentation
- **Compliance & Risk**: CISv8, FAIR risk frameworks, privacy engineering
- **AI/ML Operations**: AI hub management, cost controls, model lifecycle
- **Endpoint & Device Management**: Jamf DDM, zero-touch onboarding
- **Security Operations**: BEC drills, incident response, alert management
- **FinOps & Cost Management**: License hygiene, unit economics, cost guardrails
- **Media/Broadcast Operations**: NDI/SDI, Dante, IP video distribution
- **Team & Process Maturity**: Documentation as product, service catalogs, change management
