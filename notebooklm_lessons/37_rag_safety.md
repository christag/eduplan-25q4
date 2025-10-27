# NotebookLM Lesson Plan: Lightweight RAG Safety Checks

## Sources (15)

https://cloudsecurityalliance.org/blog/2023/11/22/mitigating-security-risks-in-retrieval-augmented-generation-rag-llm-applications
https://arxiv.org/html/2504.18041v1
https://www.promptfoo.dev/blog/rag-poisoning/
https://genai.owasp.org/llmrisk/llm01-2025-prompt-injection/
https://www.nb-data.com/p/building-guardrail-around-your-rag
https://genai.owasp.org/llmrisk/llm082025-vector-and-embedding-weaknesses/
https://ironcorelabs.com/security-risks-rag/
https://www.evidentlyai.com/llm-guide/rag-evaluation
https://qdrant.tech/blog/rag-evaluation-guide/
https://www.mendable.ai/blog/building-safe-rag
https://intelliarts.com/blog/enterprise-rag-system-best-practices/
https://decodingml.substack.com/p/llmops-for-production-agentic-rag
https://www.pinecone.io/learn/nemo-guardrails-intro/
https://developer.nvidia.com/blog/content-moderation-and-safety-checks-with-nvidia-nemo-guardrails/
https://github.com/NVIDIA-NeMo/Guardrails

### Source Details

| # | Title | Coverage |
|---|-------|----------|
| 1 | Mitigating Security Risks in RAG LLM Applications (CSA) | security risks, privacy, vulnerabilities |
| 2 | RAG LLMs are Not Safer (arXiv) | safety analysis, research findings |
| 3 | RAG Data Poisoning: Key Concepts (Promptfoo) | data poisoning, attack vectors |
| 4 | OWASP LLM01:2025 Prompt Injection | prompt injection, mitigations |
| 5 | Building Guardrail Around Your RAG Pipeline | guardrails implementation, architecture |
| 6 | OWASP LLM08:2025 Vector and Embedding Weaknesses | vector database security, embedding attacks |
| 7 | Security Risks with RAG Architectures (IronCore Labs) | infrastructure security, multi-tenant risks |
| 8 | A Complete Guide to RAG Evaluation (EvidentlyAI) | evaluation metrics, hallucination detection |
| 9 | Best Practices in RAG Evaluation (Qdrant) | groundedness, faithfulness metrics |
| 10 | Building Safe RAG with OWASP Top 10 (Mendable) | OWASP framework, enterprise practices |
| 11 | Enterprise RAG System Best Practices (Intelliarts) | implementation, access control |
| 12 | Build Production Agentic RAG With LLMOps | observability, monitoring, production |
| 13 | NeMo Guardrails: The Missing Manual (Pinecone) | implementation tutorial, RAG integration |
| 14 | Content Moderation with NeMo Guardrails (NVIDIA) | safety models, content filtering |
| 15 | NeMo Guardrails GitHub Repository | open-source toolkit, code examples |

**IMPORTANT:** The URLs above are bare links with no formatting, ready to copy-paste directly into NotebookLM.

## Audio Overview Prompts

### Overview 1: Understanding RAG Security Risks

You are creating an audio overview for a senior IT director at a media company (Morning Brew Inc.) who manages an AI hub with various AI models and is beginning to explore RAG (Retrieval-Augmented Generation) implementations. This is a mid-priority topic for building awareness of RAG security before deploying RAG systems.

**Listener Profile:**
The listener is technically sophisticated, understands LLMs and basic AI concepts, and currently manages AI tools in their organization. They may be considering or have already deployed simple RAG applications for internal knowledge bases or document Q&A. They need to understand the security and safety risks specific to RAG systems.

**Coverage Scope:**
Focus on:
- What makes RAG different from standard LLMs and why this introduces new security risks
- Counterintuitive finding: RAG can make LLMs *less* safe, not more safe
- Key risk categories: prompt injection (direct and indirect), data poisoning, privacy leakage, vector database vulnerabilities
- How RAG attack surface differs from traditional application security
- The retrieval component as a new attack vector
- Real-world impact: what can go wrong when RAG systems are compromised
- Why "harvest now, decrypt later" doesn't apply but "poison now, exploit later" does

**DO NOT cover** (these will be addressed in later overviews):
- Specific mitigation techniques and guardrails (Overview 2)
- Evaluation metrics and testing methodologies (Overview 3)
- Production implementation and LLMOps practices (Overview 4)

**Approach:**
Build awareness of the unique risks RAG introduces. Help the listener understand that RAG security is not just LLM security plus database security—it's a distinct problem space. Use clear examples relevant to internal knowledge base or document Q&A use cases. Emphasize that these are current, active threats, not theoretical concerns.

---

### Overview 2: Lightweight Safety Guardrails and Mitigation Techniques

You are creating an audio overview for a senior IT director who understands RAG security risks (from Overview 1) and now needs practical, lightweight mitigation techniques they can implement without massive infrastructure investment.

**Listener Profile:**
Same listener as Overview 1. They understand the risks and want actionable, "lightweight" safety checks that can be implemented quickly for small-to-medium RAG deployments. They're looking for the 80/20 solution—maximum protection with minimal complexity.

**Coverage Scope:**
Focus on:
- Input validation and sanitization: treating all inputs as untrusted
- Simple relevance checks: validating retrieved documents match query intent
- PII detection and redaction: filtering sensitive data before vector storage
- Prompt injection detection: using models like Meta's PromptGuard
- The RAG Triad evaluation: context relevance, groundedness, answer relevance
- Content filtering: basic topic controls and output guardrails
- Access control: permission-aware retrieval, metadata filtering
- Document source validation: verifying data provenance
- NVIDIA NeMo Guardrails as a lightweight, open-source toolkit
- Semantic similarity checks for determining when RAG is needed (lightweight vs. agent-based)
- Output sanitization: redacting PII from responses

**DO NOT cover** (already covered or will be covered later):
- General RAG risk landscape (Overview 1)
- Advanced evaluation metrics (Overview 3)
- Production monitoring and LLMOps (Overview 4)

**Approach:**
Be practical and implementation-focused. Provide a toolkit of lightweight safety checks that can be layered together. Emphasize "defense in depth" with multiple simple checks rather than one complex system. Connect to familiar security practices (input validation, access control) so it doesn't feel entirely novel. Highlight NeMo Guardrails as a concrete, free tool to get started.

---

### Overview 3: Evaluation Metrics and Testing for RAG Safety

You are creating an audio overview for a senior IT director who understands RAG risks and basic mitigations (from Overviews 1-2) and now needs to know how to evaluate and test RAG systems for safety and quality.

**Listener Profile:**
Same listener. They have or are planning to implement basic guardrails and want to know how to measure effectiveness, detect hallucinations, and systematically test their RAG implementations.

**Coverage Scope:**
Focus on:
- Groundedness/Faithfulness metrics: measuring if answers are supported by retrieved context
- Hallucination detection methods: fact verification, named-entity consistency, source attribution
- Answer hallucination vs. context hallucination
- The RAG evaluation triad: retrieval quality, generation quality, end-to-end performance
- Retrieval metrics: Precision@k, Recall@k, MRR (Mean Reciprocal Rank), NDCG
- Context adherence: ensuring responses stay within retrieved information bounds
- Evaluation frameworks: RAGAS (LLM-powered RAG evaluation), TLM (Trustworthy Language Model), LLM-as-a-Judge
- Red teaming for RAG: testing prompt injection resilience, data poisoning detection
- Continuous evaluation vs. point-in-time testing
- Human-in-the-loop evaluation for edge cases

**DO NOT cover** (already covered or will be covered later):
- RAG security risks overview (Overview 1)
- Implementation of specific guardrails (Overview 2)
- Production monitoring infrastructure (Overview 4)

**Approach:**
Be systematic and metrics-focused. Help the listener understand that RAG safety isn't binary—it's measurable and improvable. Provide a framework for thinking about what to measure (retrieval quality vs. generation quality vs. end-to-end). Emphasize that evaluation should be continuous, not one-time. Connect to their existing testing and QA processes.

---

### Overview 4: Production Deployment, Monitoring, and LLMOps

You are creating an audio overview for a senior IT director who understands RAG risks, mitigations, and evaluation (from Overviews 1-3) and is ready to think about production deployment, ongoing monitoring, and operational excellence for RAG systems.

**Listener Profile:**
Same listener. They're moving from experimentation to production or want to mature their existing RAG deployments. They need operational practices and tooling for running RAG safely at scale.

**Coverage Scope:**
Focus on:
- LLMOps for RAG: the operational discipline for production LLM applications
- Observability pillars: monitoring prompts, responses, costs, latency, errors
- Key production metrics: network latency, vector database latency, LLM API latency, retrieval accuracy, hallucination rates
- Versioning: tracking prompt changes, model versions, data updates over time
- RAGOps framework: managing diverse data structures, dynamic updates, continuous improvement
- User feedback loops: capturing ratings, corrections, edge cases
- Monitoring tools: Opik (open-source), Langfuse, Langsmith, Phoenix
- Vector database monitoring: embedding quality, index performance, retrieval latency
- Incident response: detecting and responding to safety violations in production
- Balancing safety and performance: latency vs. thoroughness tradeoffs
- Progressive rollout strategies: canary deployments for RAG changes
- "You can't manage what you can't measure" philosophy

**DO NOT cover** (already covered in previous overviews):
- RAG risk landscape (Overview 1)
- Specific guardrail implementations (Overview 2)
- Evaluation metrics (Overview 3)

**Approach:**
Be operational and tool-focused. Help the listener build a production mindset: reliability, observability, continuous improvement. Connect RAG operations to their existing DevOps/SRE practices. Emphasize that production RAG is about systems and processes, not just algorithms. Provide a mental model for the monitoring stack and what signals to watch.

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

1. Understand that RAG systems have unique security risks distinct from standard LLMs
2. Recognize the major threat vectors: prompt injection, data poisoning, vector database attacks, privacy leakage
3. Know how to implement lightweight safety guardrails using tools like NeMo Guardrails
4. Understand the RAG Triad (context relevance, groundedness, answer relevance) for evaluation
5. Be familiar with hallucination detection and groundedness metrics
6. Know how to systematically test RAG systems for safety (red teaming, continuous evaluation)
7. Understand LLMOps practices for production RAG deployment
8. Have a framework for monitoring RAG systems in production (observability, versioning, feedback loops)
