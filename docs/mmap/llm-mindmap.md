# LLM Engineering — Mindmap

> Visual map of the **140 topics** in the [LLM reference](../llm/llm-index.md), grouped into 15 categories.

## Mindmap

```mermaid
mindmap
  root((LLM Engineering))
    1 Foundations
      Engineering Lifecycle
      Language Modeling and Logits
      Transformer for LLM Engineers
      Tokenization and Token Economics
      Context Windows
      Model Families
      Managed vs Open Models
      Model Selection
    2 API and Application Engineering
      Chat and Responses APIs
      Generation Parameters
      Streaming and SSE
      Async Rate Limits Retries
      Structured Outputs
      Function Calling
      Resilience and Fallbacks
      Token Cost Accounting
      Provider Routing
    3 Prompt Engineering
      Prompt Anatomy
      Zero and Few-Shot
      Prompt Patterns
      Reasoning Prompting
      Decomposition and Planning
      Templates and Versioning
      Prompt Testing
      Context Engineering
      Long-Context Strategies
      Injection Defenses
    4 Embeddings and Retrieval
      Embedding Foundations
      Similarity Metrics
      Embedding Model Selection
      Chunking Strategies
      Metadata Filtering
      Vector Indexes
      Vector Databases
      Hybrid Search
      Reranking
      Retrieval Evaluation
    5 RAG
      RAG Architecture
      Ingestion Pipeline
      Query Pipeline
      Grounding and Citations
      Advanced RAG
      Agentic RAG
      GraphRAG
      SQL RAG
      Multimodal RAG
      RAG Security
      RAG Evaluation
      RAG Production Optimization
    6 Tool Use and Workflows
      Tool Use Foundations
      Reliable Tool Calling
      API Integration
      Code Sandboxes
      Human Approval
      Deterministic Workflows
      State Machines
      MCP
    7 Agentic AI
      Agent Foundations
      ReAct and Plan-Execute
      LangGraph
      Agent Memory
      Multi-Agent Systems
      Agent Planning
      Agent Evaluation
      Agent Observability
      Agent Security
      Production Agent Patterns
    8 Evaluation and Testing
      Evaluation Strategy
      Golden Datasets
      Deterministic Evaluators
      LLM-as-Judge
      Human Evaluation
      Evaluation Tools
      Online Evaluation
      Regression Testing CI
      Red Teaming
      Evaluation Statistics
    9 Fine-Tuning and Adaptation
      Prompt Retrieve or Fine-Tune
      Training Data Preparation
      SFT
      PEFT LoRA QLoRA
      Preference Optimization
      Domain Adaptation
      Fine-Tuning Evaluation
      Fine-Tuning Infrastructure
      Model Merging
    10 Security and Governance
      Threat Modeling
      OWASP LLM Risks
      Prompt Injection
      Data Exfiltration
      Output Validation
      Secrets and Identity
      Content Safety
      Privacy and Retention
      Model Supply Chain
      Responsible AI
      Incident Response
    11 Serving and Performance
      Inference Foundations
      Quantization
      Inference Engines
      Continuous Batching
      Speculative Decoding
      Caching
      Capacity Planning
      Autoscaling and Load Shedding
      Edge and Local LLMs
      Serving Benchmarks
    12 LLMOps and Observability
      Prompt and Model Registry
      Tracing OpenTelemetry
      LLM Observability
      Feedback Loops
      LLM CI/CD
      Release Strategies
      Drift
      Production Debugging
      SLO and Cost Governance
      Incident Management
    13 Multimodal
      Multimodal Models
      Vision-Language Prompting
      Document AI Pipelines
      Audio and Speech LLMs
      Multimodal Structured Outputs
      Production Multimodal RAG
      Multimodal Safety
    14 Enterprise Architecture
      Use-Case Selection and ROI
      Reference Architecture
      API and Model Gateway
      Enterprise Data Integration
      Identity-Aware Retrieval
      Multi-Tenant Architecture
      Cloud Hybrid On-Prem
      Platform Operating Model
      Vendor Portability
      Enterprise System Design
    15 Capstones and Interviews
      Production RAG Capstone
      Agentic Workflow Capstone
      Evaluation Harness Capstone
      Secure Architecture Capstone
      System-Design Interviews
      Interview Bank
```

## Category Breakdown

| # | Category | Topics | Level | Est. Time |
|---|---|---|---|---|
| 1 | LLM Engineering Foundations | 01–08 | Foundational | 48–80 h |
| 2 | LLM API and Application Engineering | 09–17 | Foundational | 54–90 h |
| 3 | Prompt Engineering | 18–27 | Foundational | 60–100 h |
| 4 | Embeddings and Semantic Retrieval | 28–37 | Intermediate | 60–100 h |
| 5 | Retrieval-Augmented Generation | 38–49 | Intermediate | 72–120 h |
| 6 | Tool Use and Workflow Automation | 50–57 | Intermediate | 48–80 h |
| 7 | Agentic AI Engineering | 58–67 | Intermediate | 60–100 h |
| 8 | LLM Evaluation and Testing | 68–77 | Advanced | 60–100 h |
| 9 | Fine-Tuning and Model Adaptation | 78–86 | Advanced | 54–90 h |
| 10 | LLM Security, Safety and Governance | 87–97 | Advanced | 66–110 h |
| 11 | LLM Serving and Performance Engineering | 98–107 | Advanced | 60–100 h |
| 12 | LLMOps and Observability | 108–117 | Advanced | 60–100 h |
| 13 | Multimodal LLM Engineering | 118–124 | Advanced | 42–70 h |
| 14 | Enterprise LLM Architecture | 125–134 | Architecture | 60–100 h |
| 15 | Capstones and Interview Preparation | 135–140 | Architecture | 36–60 h |

> Each topic lives at `../llm/NNN-<slug>.md`; the full per-topic list with links is in the [LLM index](../llm/llm-index.md#repository-file-map).

## Learning Path

```mermaid
flowchart TD
    A[LLM foundations] --> B[APIs]
    B --> C[Prompt and context engineering]
    C --> D[Embeddings and retrieval]
    D --> E[RAG]
    E --> F[Tools and workflows]
    F --> G[Agents]
    G --> H[Evaluation]
    H --> I[Fine-tuning and adaptation]
    I --> J[Security and governance]
    J --> K[Serving and performance]
    K --> L[LLMOps]
    L --> M[Multimodal]
    M --> N[Enterprise architecture]
    N --> O[Capstones]
```

## Solution Selection Map

```mermaid
mindmap
  root((LLM Solution Choices))
    Prompt vs RAG vs Fine-tune
      Behavior gap
      Knowledge gap
      Stable adaptation
    Managed vs Self-hosted
      Reliability and speed
      Control and economics
    Small vs Large model
      Bounded and cheap
      Hard reasoning
    Long context vs Retrieval
      Modest corpus
      Large changing corpus
    Sparse vs Dense vs Hybrid
      Exact identifiers
      Semantic intent
    Workflow vs Agent
      Known path
      Observation-driven
    Single vs Multi-agent
      Most tasks
      Distinct expertise
    Function call vs MCP
      App-local tools
      Interoperable ecosystem
    Full FT vs LoRA
      Max adaptation
      Efficient adapters
    Sync vs Async vs Batch
      Interactive
      Decoupled or offline
    Exact vs Judge vs Human eval
      Deterministic output
      Nuanced rubric
```

## Reference Architectures

```mermaid
mindmap
  root((Reference Architectures))
    Secure enterprise chat
      Identity gateway
      Policy and model gateway
      Authorized retrieval
      Output validation
    Production RAG
      Ingest and version
      Hybrid retrieve and rerank
      Citation validation
    Document intelligence
      OCR layout tables
      Validated schema
      Human exception queue
    Tool-using workflow
      State machine
      Bounded model decisions
      Tool gateway
    Human-approved automation
      Policy and authorization
      Human review
      Idempotent executor
    Multimodal RAG
      Multimodal index
      Source-highlighted answer
    Self-hosted serving
      Queue and scheduler
      GPU pool
      Autoscaling and fallback
    Multi-provider gateway
      Central routing
      Provider adapters
      Cost and eval
```

## Playbooks

```mermaid
mindmap
  root((Playbooks))
    Evaluation
      Taxonomy and golden tasks
      Deterministic checks
      Retrieval measured separately
      Calibrated judges
      Red-team
      CI gates
    Security Checklist
      AuthZ outside prompts
      Injection tested
      RAG ACLs
      Validated tool args
      Least privilege
      Sandboxing
      Kill switch
    Production Debugging
      Hallucination
      Wrong citations
      Malformed JSON
      Agent loops
      Latency and rate limits
      Cost spikes
      Context overflow
      Permission leakage
      Provider outage
```
