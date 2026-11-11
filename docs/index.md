# AI Solutions Architect — 24-Week Transition Roadmap
### A Rigorous, Practical, and Job-Oriented Plan for Enterprise Technologists

---

> **Learner Profile:** Intermediate Python · ML Fundamentals · Oracle ERP/E-Business Suite · SQL/PL/SQL · Core Java · APIs & Integrations
>
> **Target Roles:** AI Solutions Architect · Generative AI Solutions Architect · Enterprise AI Architect · Agentic AI Architect · Principal AI Engineer (Architecture)
>
> **Weekly Commitment:** 12–15 hours | **Primary Cloud:** Microsoft Azure | **Language:** Python | **Portfolio:** GitHub

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Roadmap at a Glance](#roadmap-at-a-glance)
3. [24-Week Weekly Plan](#24-week-weekly-plan)
4. [Training Catalog](#training-catalog)
5. [Reading & Papers Catalog](#reading--papers-catalog)
6. [Capstone Portfolio](#capstone-portfolio)
7. [Milestones & Stage Gates](#milestones--stage-gates)
8. [Skills Matrix](#skills-matrix)
9. [Architecture Artifacts Checklist](#architecture-artifacts-checklist)
10. [Certification Guidance](#certification-guidance)
11. [Interview & Job-Readiness Plan](#interview--job-readiness-plan)
12. [Progress Tracking Templates](#progress-tracking-templates)
13. [Week 1 Action Checklist](#week-1-action-checklist)
14. [References](#references)

---

## Executive Summary

This roadmap transforms an experienced Oracle ERP/enterprise technologist into a credible **AI Solutions Architect** in 24 weeks (≈ 5–6 months) at 12–15 hours/week. It is sequenced so that each phase builds on the previous one, respects cognitive load, and produces tangible portfolio artifacts at the end of every week.

### Phase Overview

| Phase | Weeks | Theme |
|---|---|---|
| 0 — Foundation | 1–4 | Python for production AI, software engineering, ML refresh, dev tooling |
| 1 — ML Architecture | 5–8 | End-to-end ML lifecycle, cloud AI platforms, architecture trade-offs |
| 2 — GenAI Foundations | 9–12 | Deep learning, transformers, foundation models, prompt engineering |
| 3 — RAG Systems | 13–16 | RAG design, vector databases, evaluation, multimodal, semantic caching |
| 4 — Agentic AI | 17–20 | LangGraph agents, MCP, multi-agent patterns, guardrails, observability |
| 5 — MLOps/LLMOps | 21–22 | MLflow, CI/CD, monitoring, OpenTelemetry, IaC |
| 6 — Governance & Portfolio | 23–24 | Responsible AI, security, capstone polish, interview prep |

**Minimum Viable Path (MVP):** Weeks 1–16 produce enough to interview for mid-level GenAI architect roles.
**Full Path:** Weeks 17–24 add agentic AI, LLMOps, governance depth, and interview readiness.

**Primary cloud is Microsoft Azure** because it provides the broadest integrated AI portfolio (Azure OpenAI Service, Azure AI Foundry, Azure Machine Learning, Azure AI Search, Semantic Kernel, Prompt Flow) and Azure AI certifications (AI-900, AI-102, AZ-204) are widely recognized by enterprise hiring managers. AWS and Google Cloud are covered as comparative architecture study.

---

## Roadmap at a Glance

```
Week  1–2   Python production patterns · packaging · testing · typing · FastAPI · Docker
Week  3–4   NumPy/pandas/scikit-learn refresh · statistics · embeddings essentials · Git/CI
Week  5–6   ML lifecycle · problem framing · data pipelines · training · deployment patterns
Week  7–8   Cloud AI platforms (Azure primary, AWS + GCP comparative) · build vs buy
Week  9–10  PyTorch fundamentals · transformer architecture · tokenization · model families
Week 11–12  Prompt engineering · structured outputs · fine-tuning · PEFT/LoRA · Capstone 1
Week 13–14  RAG fundamentals · document ingestion · chunking · vector DBs · hybrid search
Week 15–16  Advanced RAG · reranking · evaluation · semantic caching · multimodal
Week 17–18  Agent fundamentals · LangGraph · planning · tool use · state · checkpoints
Week 19–20  Multi-agent patterns · MCP · guardrails · agent evaluation · Capstone 2
Week 21–22  MLOps/LLMOps · MLflow · Kubernetes · monitoring · OpenTelemetry · IaC
Week 23–24  Responsible AI · NIST RMF · OWASP LLM Top 10 · Capstone 3 · Case Study
```

---

## 24-Week Weekly Plan

> **Key:** H = Hours | V = Video | R = Reading | L = Lab | D = Documentation/Architecture

---

### Phase 0 — Foundation (Weeks 1–4)

---

#### Week 1 — Python for Production AI

**Theme:** Write type-annotated, testable, packaged Python modules; build a FastAPI microservice
**Hours:** 13 | **Exit Criteria:** Can explain dependency injection in FastAPI; pytest coverage ≥ 80%; package installs cleanly

**Topics**
- Python typing, Pydantic v2, pytest
- uv/poetry packaging, logging, configuration (pydantic-settings)
- FastAPI basics

**🎬 Video Training**
- *Python for Everybody* – Dr. Chuck Severance (freeCodeCamp/YouTube, free)
  <https://www.youtube.com/watch?v=8DvywoWv6fI>
- *Python for Data Engineers* – O'Reilly Learning
  <https://learning.oreilly.com/videos/python-for-data/9781098100728/>

**📖 Reading**
- [FastAPI docs](https://fastapi.tiangolo.com)
- [Pydantic v2 docs](https://docs.pydantic.dev)

**🔬 Hands-On Lab**
Build a typed, tested FastAPI service that returns ML model metadata.

**📦 Deliverable**
`predict_service/` repo scaffold with health endpoint, typed schemas, 10+ unit tests, README.

---

#### Week 2 — Containers & CI/CD

**Theme:** Containerize a Python service; configure a GitHub Actions pipeline
**Hours:** 13 | **Exit Criteria:** Image builds without warnings; CI pipeline passes green; can explain multi-stage build benefits

**Topics**
- Docker multi-stage builds, docker-compose, .env secrets
- GitHub Actions, pre-commit hooks, Makefile conventions

**🎬 Video Training**
- *Docker Deep Dive* – Nigel Poulton (Udemy)
  <https://www.udemy.com/course/docker/>

**📖 Reading**
- [GitHub Actions docs](https://docs.github.com/en/actions)
- [Docker best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

**🔬 Hands-On Lab**
Containerize Week 1 service; add lint → test → build → push Actions pipeline.

**📦 Deliverable**
Dockerfile, docker-compose.yml, `.github/workflows/ci.yml`, README with architecture diagram.

---

#### Week 3 — ML Refresh & Feature Engineering

**Theme:** Retrain and evaluate a scikit-learn pipeline; explain bias-variance trade-off
**Hours:** 14 | **Exit Criteria:** Model AUC > 0.75 on holdout; can explain precision-recall trade-off for imbalanced data

**Topics**
- NumPy, pandas, scikit-learn pipelines
- Cross-validation, feature engineering
- Model evaluation (AUC, F1, calibration), imbalanced data

**🎬 Video Training**
- *Machine Learning with scikit-learn* – Andreas Mueller (O'Reilly video)

**📖 Reading**
- [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)

**🔬 Hands-On Lab**
Build an enterprise churn prediction pipeline with preprocessing, CV, feature importance, and calibration plot.

**📦 Deliverable**
Jupyter notebook + exported `churn_model/` package with trained model, metrics report.

---

#### Week 4 — Statistics, Embeddings & Dev Tooling

**Theme:** Apply statistical tests for data quality; create and compare text embeddings
**Hours:** 13 | **Exit Criteria:** Can explain embedding distance vs keyword search; clusters visually meaningful; Git workflow clean

**Topics**
- Probability distributions, hypothesis testing, Central Limit Theorem
- Cosine similarity, word2vec vs sentence-transformers
- Dimensionality reduction (UMAP/t-SNE), Git branching, pre-commit

**🎬 Video Training**
- *Statistics for Data Science* – Jose Portilla (Udemy)
  <https://www.udemy.com/course/statistics-for-data-science-and-business-analysis/>

**📖 Reading**
- [sentence-transformers docs](https://www.sbert.net)
- [UMAP docs](https://umap-learn.readthedocs.io)

**🔬 Hands-On Lab**
Embed 1,000 Oracle ERP FAQ entries; visualize clusters; build a nearest-neighbor lookup.

**📦 Deliverable**
UMAP cluster visualization, semantic search demo notebook, `embeddings_utils.py` module.

---

### Phase 1 — ML Architecture (Weeks 5–8)

---

#### Week 5 — End-to-End ML Lifecycle

**Theme:** Design a data-to-deployment ML workflow; write an ML system design doc
**Hours:** 13 | **Exit Criteria:** Can articulate batch vs streaming trade-offs; MLflow UI shows tracked params/metrics

**Topics**
- Problem framing, KPI definition, data ingestion, data quality contracts
- Training/validation/test splits, experiment tracking concept
- Batch vs real-time inference

**🎬 Video Training**
- *Designing Machine Learning Systems* – Chip Huyen (Stanford CS329S lecture series, free)
  <https://stanford-cs329s.github.io>
- O'Reilly video companion
  <https://learning.oreilly.com/videos/designing-machine-learning/9781098107994/>

**📖 Book**
- *Designing Machine Learning Systems* – Chip Huyen (O'Reilly) Ch 1–4

**📖 Reading**
- [Google Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml)
- [Data Quality at Scale – Uber blog](https://www.uber.com/blog/monitoring-data-quality-at-scale/)

**🔬 Hands-On Lab**
Add MLflow experiment tracking to Week 3 churn model.

**📦 Deliverable**
MLflow experiment with 5+ runs, best-model artifact, architecture diagram (ML lifecycle).

---

#### Week 6 — Data Pipelines & Feature Stores

**Theme:** Build a simple feature pipeline; explain medallion architecture
**Hours:** 14 | **Exit Criteria:** Pipeline fails loudly on bad data; can explain Delta Lake ACID guarantees

**Topics**
- Data lake layers (bronze/silver/gold), Delta Lake concepts
- Feature stores vs ad-hoc, data contracts, schema evolution
- great_expectations basics

**🎬 Video Training**
- *Data Engineering Zoomcamp* – DataTalks.Club (free)
  <https://github.com/DataTalksClub/data-engineering-zoomcamp>
- *Data Engineering with Python* – O'Reilly Learning
  <https://learning.oreilly.com/videos/data-engineering-with/9781800560413/>

**📖 Book**
- *Data Engineering with Python* – Paul Crickard (O'Reilly) Ch 1–3

**📖 Reading**
- [Databricks Medallion Architecture](https://docs.databricks.com/en/lakehouse/medallion.html)
- [great_expectations docs](https://docs.greatexpectations.io)

**🔬 Hands-On Lab**
Build a DuckDB-based feature pipeline with data-quality checks for procurement data.

**📦 Deliverable**
Feature pipeline code, data-quality report, medallion layer diagram.

---

#### Week 7 — Cloud AI Platforms — Azure Primary

**Theme:** Deploy a model to Azure ML; map equivalent services across clouds
**Hours:** 15 | **Exit Criteria:** Endpoint returns prediction in < 300 ms; can map SageMaker Endpoints ↔ Azure ML endpoints ↔ Vertex AI endpoints

**Topics**
- Azure ML workspace, compute clusters, managed endpoints
- Azure AI Foundry overview
- Service mapping (Azure vs AWS vs GCP)

**🎬 Video Training**
- *Microsoft Azure AI Fundamentals AI-900* – Andrew Brown (freeCodeCamp, free)
  <https://www.youtube.com/watch?v=OwZHNH8EfSU>

**📖 Reading**
- [Azure Architecture Center — AI](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/)
- [AWS AI/ML service overview](https://aws.amazon.com/machine-learning/)

**🔬 Hands-On Lab**
Deploy churn model to Azure ML managed online endpoint with Swagger docs.

**📦 Deliverable**
Deployed endpoint URL, cloud service-mapping table (Azure/AWS/GCP), ARM template.

---

#### Week 8 — Architecture Trade-offs & Non-Functional Requirements

**Theme:** Write an architecture decision record; evaluate build vs buy
**Hours:** 13 | **Exit Criteria:** Proposal addresses all 5 pillars of WAF; ADR follows standard template; reviewer can challenge any decision

**Topics**
- NFRs (availability, latency, throughput, cost, security, maintainability)
- CAP theorem applied to ML, DR patterns
- Blue-green vs canary deployments, build vs buy framework

**🎬 Video Training**
- *Software Architecture Fundamentals* – Neal Ford & Mark Richards (O'Reilly Learning)
  <https://learning.oreilly.com/videos/software-architecture-fundamentals/9781491998991/>
- *Fundamentals of Software Architecture* – O'Reilly Live Training
  <https://learning.oreilly.com/live-events/fundamentals-of-software-architecture/0636920458951/>

**📖 Book**
- *Software Architecture: The Hard Parts* – Ford et al. (O'Reilly) Ch 1–2

**📖 Reading**
- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/)
- [AWS Well-Architected ML Lens](https://docs.aws.amazon.com/wellarchitected/latest/machine-learning-lens/)

**🔬 Hands-On Lab**
Write a 2-page architecture proposal for an ERP invoice anomaly detector.

**📦 Deliverable**
Architecture proposal doc, 2 ADRs (model serving strategy, data storage), trade-off table.

---

### Phase 2 — GenAI Foundations (Weeks 9–12)

---

#### Week 9 — PyTorch & Transformer Architecture

**Theme:** Implement a small transformer from scratch; explain attention
**Hours:** 14 | **Exit Criteria:** Model loss decreases monotonically; can annotate attention matrix visualization

**Topics**
- PyTorch tensors, autograd, training loop
- Transformer blocks, multi-head attention, positional encoding
- Layer normalization

**🎬 Video Training**
- *Deep Learning with PyTorch Step-by-Step* – Daniel Voigt Godoy (O'Reilly Learning)
  <https://learning.oreilly.com/videos/deep-learning-with/9781098135867/>
- *PyTorch for Deep Learning* – Zero to Mastery (Udemy)
  <https://www.udemy.com/course/pytorch-for-deep-learning/>

**📖 Book**
- *Deep Learning with PyTorch* – Eli Stevens (O'Reilly) Ch 1–8

**📖 Reading**
- [The Illustrated Transformer – Jay Alammar](https://jalammar.github.io/illustrated-transformer/)
- [Attention Is All You Need – Vaswani et al. arXiv:1706.03762](https://arxiv.org/abs/1706.03762)

**🔬 Hands-On Lab**
Implement a character-level transformer on a small text corpus.

**📦 Deliverable**
`mini_transformer/` with training loop, loss curve plot, architecture diagram.

---

#### Week 10 — Foundation Models & Model Selection

**Theme:** Select the right model for an enterprise use case; compare OSS vs managed
**Hours:** 13 | **Exit Criteria:** Scorecard includes latency, cost, context window, fine-tune eligibility; can defend any selection

**Topics**
- Model families (GPT-4o, Claude 3.5, Gemini, Llama 3, Mistral, Phi-3)
- Model cards, benchmark reading (MMLU, HumanEval, HELM)
- Context windows, latency/cost/quality matrix, tokenization

**🎬 Video Training**
- *Generative AI with LLMs* – DeepLearning.AI (Coursera) Weeks 1–2
  <https://www.deeplearning.ai/courses/generative-ai-with-llms/>

**📖 Reading**
- [OpenAI model cards](https://platform.openai.com/docs/models)
- [Anthropic model overview](https://docs.anthropic.com/en/docs/about-claude/models/overview)
- [Hugging Face Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)

**🔬 Hands-On Lab**
Build a model-selection scorecard for 5 enterprise use cases (ERP summarization, code review, procurement Q&A, incident triage, document extraction).

**📦 Deliverable**
Model selection scorecard (Markdown), cost comparison calculator, architecture note.

---

#### Week 11 — Prompt Engineering & Structured Outputs

**Theme:** Write production-grade prompts; extract structured JSON from LLMs reliably
**Hours:** 14 | **Exit Criteria:** Extraction accuracy ≥ 90% on 50-item test set; validation rejects malformed outputs automatically

**Topics**
- Zero/few-shot, chain-of-thought, ReAct, function/tool calling
- Structured output with Instructor/Pydantic, system prompts
- Output validation, prompt versioning

**🎬 Video Training**
- *ChatGPT Prompt Engineering for Developers* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/chatgpt-prompt-eng-for-devs>

**📖 Reading**
- [OpenAI Structured Outputs guide](https://platform.openai.com/docs/guides/structured-outputs)
- [Instructor library docs](https://python.useinstructor.com)

**🔬 Hands-On Lab**
Build an ERP PO anomaly extraction pipeline that outputs typed Pydantic models from invoice text.

**📦 Deliverable**
`po_extractor/` service with structured JSON output, prompt templates versioned in YAML, test harness.

---

#### Week 12 — Fine-Tuning, PEFT & Capstone 1

**Theme:** Apply LoRA fine-tuning; deliver Capstone 1
**Hours:** 15 | **Exit Criteria:** Fine-tuned model outperforms base on domain eval by ≥ 5%; Capstone 1 repo public on GitHub

**Topics**
- Fine-tuning vs RAG decision framework
- PEFT/LoRA/QLoRA concepts, Hugging Face PEFT library
- Quantization (GPTQ/AWQ), when NOT to fine-tune

**🎬 Video Training**
- *Generative AI with LLMs* – DeepLearning.AI Weeks 2–3 (continued)
  <https://www.deeplearning.ai/courses/generative-ai-with-llms/>

**📖 Reading**
- [LoRA paper – Hu et al. arXiv:2106.09685](https://arxiv.org/abs/2106.09685)
- [QLoRA paper – Dettmers et al. arXiv:2305.14314](https://arxiv.org/abs/2305.14314)

**🔬 Hands-On Lab**
Fine-tune a small open model (Phi-3-mini or Mistral-7B) on domain-specific Q&A pairs using QLoRA.

**📦 Deliverable**
LoRA adapter checkpoint, before/after eval comparison, **CAPSTONE 1 delivery**.

---

### Phase 3 — RAG Systems (Weeks 13–16)

---

#### Week 13 — RAG Fundamentals

**Theme:** Build a basic RAG pipeline end-to-end
**Hours:** 14 | **Exit Criteria:** Retrieves correct source for 8/10 test questions; citations include page/chunk reference

**Topics**
- Document ingestion (PDF, DOCX, HTML), text parsing
- Chunking strategies (fixed, semantic, recursive)
- Embedding models, vector store indexing (Chroma, FAISS, pgvector), similarity search

**🎬 Video Training**
- *LangChain for LLM Application Development* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/langchain>

**📖 Reading**
- [LangChain docs – RAG](https://python.langchain.com/docs/tutorials/rag/)
- [LlamaIndex docs – Getting Started](https://docs.llamaindex.ai/en/stable/)

**🔬 Hands-On Lab**
Build a RAG pipeline over Oracle ERP release notes (public PDFs) using Azure AI Search.

**📦 Deliverable**
`erp_rag/` with ingestion script, indexed vector store, Q&A CLI, source citations.

---

#### Week 14 — Advanced RAG — Retrieval & Reranking

**Theme:** Improve retrieval precision; implement hybrid search
**Hours:** 13 | **Exit Criteria:** Precision@5 improves ≥ 10% with reranking; can explain BM25 vs dense retrieval trade-off

**Topics**
- Hybrid search (BM25 + vector), metadata filtering
- HyDE, multi-query retrieval
- Cross-encoder reranking (Cohere/BGE), Azure AI Search hybrid
- Lost-in-the-middle mitigation

**🎬 Video Training**
- *Building and Evaluating Advanced RAG* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/building-evaluating-advanced-rag>

**📖 Reading**
- [Azure AI Search hybrid search](https://learn.microsoft.com/en-us/azure/search/hybrid-search-overview)
- [Cohere Rerank docs](https://docs.cohere.com/docs/rerank-2)

**🔬 Hands-On Lab**
Add hybrid search + reranking to Week 13 pipeline; measure precision@5 before and after.

**📦 Deliverable**
Retrieval precision report, reranking integration, updated architecture diagram.

---

#### Week 15 — RAG Evaluation & Access Control

**Theme:** Measure RAG quality systematically; design access-controlled RAG
**Hours:** 14 | **Exit Criteria:** RAGAS faithfulness > 0.75; at least 2 injection attacks blocked; RBAC design reviewed

**Topics**
- RAGAS metrics (faithfulness, answer relevance, context precision/recall)
- RAGAs library, evaluation dataset creation, golden dataset
- Hallucination detection, prompt injection defenses for RAG
- RBAC over document collections

**🎬 Video Training**
- *LangChain & LangSmith for LLM Apps* – James Briggs (YouTube playlist, free)
  <https://www.youtube.com/playlist?list=PLIUOU7oqGTLieV9uTIFMm6_4PXg-hlN6G>

**📖 Reading**
- [RAGAS paper – arXiv:2309.15217](https://arxiv.org/abs/2309.15217)
- [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

**🔬 Hands-On Lab**
Run RAGAS evaluation on Week 14 pipeline; add document-level RBAC simulation.

**📦 Deliverable**
RAGAS evaluation report, RBAC design document, prompt injection test results.

---

#### Week 16 — Semantic Caching, Memory & Multimodal

**Theme:** Reduce latency and cost with caching; handle multimodal inputs
**Hours:** 14 | **Exit Criteria:** Cache reduces repeat-query latency by ≥ 40%; multimodal extraction matches manual labels on 10/10 test invoices

**Topics**
- Semantic caching (GPTCache/Redis), conversation memory strategies (buffer, summary, entity)
- Multimodal document processing (Azure AI Document Intelligence, GPT-4o Vision)
- Cost and latency benchmarks

**🎬 Video Training**
- *Azure AI Document Intelligence – Hands-On Tutorial* – Microsoft Reactor (YouTube, free)
  <https://www.youtube.com/watch?v=WggANPc0bEI>
- Azure AI Skills (LinkedIn Learning)
  <https://www.linkedin.com/learning/topics/azure-ai>

**📖 Reading**
- [Azure AI Document Intelligence docs](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/)
- [GPTCache GitHub](https://github.com/zilliztech/GPTCache)
- [LlamaIndex multimodal guide](https://docs.llamaindex.ai/en/stable/use_cases/multimodal/)

**🔬 Hands-On Lab**
Add semantic caching to RAG service; process a multimodal invoice (PDF + image); measure latency reduction.

**📦 Deliverable**
Cache hit-rate report, multimodal ingestion demo, **CAPSTONE 2 begins**.

---

### Phase 4 — Agentic AI (Weeks 17–20)

---

#### Week 17 — Agent Fundamentals & LangGraph

**Theme:** Build a stateful single agent; explain when agents are appropriate
**Hours:** 14 | **Exit Criteria:** Agent correctly routes 8/10 test scenarios; state is serializable; tools are individually testable

**Topics**
- Agent loop (perceive-plan-act), tool use, function calling, ReAct pattern
- LangGraph basics (nodes, edges, state, compile)
- When NOT to use agents

**🎬 Video Training**
- *AI Agents in LangGraph* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/ai-agents-in-langgraph>

**📖 Reading**
- [LangGraph docs](https://langchain-ai.github.io/langgraph/)
- [ReAct paper – arXiv:2210.03629](https://arxiv.org/abs/2210.03629)

**🔬 Hands-On Lab**
Build a service-request triage agent with 3 tools (ticket lookup, KB search, escalation).

**📦 Deliverable**
`triage_agent/` LangGraph graph, tool definitions, state schema, unit tests.

---

#### Week 18 — Planning, Memory & Human-in-the-Loop

**Theme:** Implement checkpointing and human approval steps
**Hours:** 13 | **Exit Criteria:** Agent resumes correctly after simulated crash; human approval blocks execution until confirmed

**Topics**
- Planning strategies (ToT, Plan-and-Execute)
- LangGraph checkpointers (SQLite, Redis), human-in-the-loop interrupts
- Idempotency patterns, failure recovery, audit logging

**🎬 Video Training**
- *LangGraph: Build Stateful AI Agents* – LangChain official tutorials (YouTube, free)
  <https://www.youtube.com/playlist?list=PLfaIDFEXuae16n2TWUkKq5PgJ0w6Pkwtg>

**📖 Reading**
- [LangGraph persistence docs](https://langchain-ai.github.io/langgraph/concepts/persistence/)
- [Human-in-the-loop patterns](https://langchain-ai.github.io/langgraph/concepts/human_in_the_loop/)

**🔬 Hands-On Lab**
Add SQLite checkpointer + human approval interrupt to triage agent; simulate a mid-task failure and recover.

**📦 Deliverable**
Checkpoint demo, recovery test, human-approval flow video/GIF, audit log sample.

---

#### Week 19 — Multi-Agent Patterns & MCP

**Theme:** Design a multi-agent system; integrate an MCP tool server
**Hours:** 14 | **Exit Criteria:** Each agent has a defined responsibility boundary; MCP tool server returns typed responses; end-to-end test passes

**Topics**
- Supervisor pattern, hierarchical agents, handoff protocols
- Shared vs isolated memory
- MCP architecture, MCP tool server setup (Python SDK), security considerations

**🎬 Video Training**
- *Multi AI Agent Systems with crewAI* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai>

**📖 Reading**
- [Model Context Protocol spec](https://modelcontextprotocol.io/docs)
- [Anthropic MCP blog](https://www.anthropic.com/news/model-context-protocol)

**🔬 Hands-On Lab**
Build a 3-agent procurement workflow (intake → approval → fulfillment) with an MCP tool server for ERP lookup.

**📦 Deliverable**
Multi-agent graph diagram, MCP server code, integration test suite.

---

#### Week 20 — Guardrails, Evaluation & Capstone 2

**Theme:** Implement production guardrails; deliver Capstone 2
**Hours:** 15 | **Exit Criteria:** Task-completion rate ≥ 80%; PII leakage = 0 on test set; Capstone 2 repo public on GitHub

**Topics**
- Guardrails AI / NVIDIA NeMo Guardrails, output validation
- PII detection, content safety (Azure AI Content Safety)
- Agent evaluation (task completion, tool accuracy, hallucination rate)

**🎬 Video Training**
- *Quality and Safety for LLM Applications* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/quality-safety-llm-applications>

**📖 Reading**
- [NVIDIA NeMo Guardrails docs](https://github.com/NVIDIA/NeMo-Guardrails)
- [Guardrails AI docs](https://www.guardrailsai.com/docs)
- [AgentBench paper – arXiv:2308.03688](https://arxiv.org/abs/2308.03688)

**🔬 Hands-On Lab**
Add guardrails to Capstone 2 agent; create evaluation dataset (20 scenarios); measure task-completion rate.

**📦 Deliverable**
Guardrails config, evaluation report, **CAPSTONE 2 delivery**.

---

### Phase 5 — MLOps/LLMOps (Weeks 21–22)

---

#### Week 21 — MLOps: MLflow, CI/CD/CT, Kubernetes

**Theme:** Build a model CI/CD pipeline; deploy on Kubernetes
**Hours:** 14 | **Exit Criteria:** Model promotes from Staging → Production only after eval gate passes; deployment rolls back on health-check failure

**Topics**
- MLflow Model Registry, CI/CD/CT pipeline, model promotion gates
- Docker → Kubernetes deployment, Helm chart basics, rolling updates
- Feature-flag deployment, Infrastructure as Code (Bicep/Terraform)

**🎬 Video Training**
- *MLflow: An Introduction* – Databricks (O'Reilly Learning)
  <https://learning.oreilly.com/videos/mlflow-an-introduction/9781492087250/>
- *MLOps Fundamentals* – LinkedIn Learning
  <https://www.linkedin.com/learning/mlops-foundations>

**📖 Book**
- *MLflow in Action* – Mark Ryan (O'Reilly) Ch 1–6

**📖 Reading**
- [MLflow docs](https://mlflow.org/docs/latest/index.html)
- [Azure MLOps accelerator](https://github.com/Azure/mlops-v2)

**🔬 Hands-On Lab**
Extend Capstone 1 with MLflow Model Registry, GitHub Actions CI/CD → AKS deployment.

**📦 Deliverable**
Helm chart, CI/CD pipeline YAML, MLflow model registry screenshot, Bicep IaC template.

---

#### Week 22 — LLMOps: Monitoring, Observability & Cost

**Theme:** Instrument an LLM application for production observability
**Hours:** 14 | **Exit Criteria:** Every LLM call emits trace with token count and latency; cost dashboard shows per-query cost; alert fires on p99 > 2 s

**Topics**
- Prompt/response logging, latency/cost/token monitoring, drift detection
- Hallucination monitoring, OpenTelemetry traces for LLM
- LangSmith / Azure AI Foundry tracing, alert design, incident response playbook

**🎬 Video Training**
- *LLMOps* – DeepLearning.AI (free)
  <https://learn.deeplearning.ai/courses/llmops>

**📖 Reading**
- [OpenTelemetry for LLMs](https://opentelemetry.io/docs/zero-code/python/)
- [Azure Monitor for AI](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/monitor-applications)

**🔬 Hands-On Lab**
Add OpenTelemetry tracing + cost dashboard to Capstone 2 RAG service.

**📦 Deliverable**
Grafana/Azure Monitor dashboard screenshot, alert rules YAML, cost-per-query metric, incident runbook.

---

### Phase 6 — Governance, Security & Portfolio Finalization (Weeks 23–24)

---

#### Week 23 — Responsible AI, Security & Governance

**Theme:** Threat-model an AI system; complete a Responsible AI assessment
**Hours:** 14 | **Exit Criteria:** At least 8 STRIDE threats identified with mitigations; NIST AI RMF Map section completed; reviewer cannot find an unaddressed OWASP LLM Top 10 item

**Topics**
- NIST AI RMF map/measure/manage
- OWASP LLM Top 10 (prompt injection, insecure output handling, data leakage, model theft, excessive agency)
- MITRE ATLAS, managed identities, RBAC, private endpoints
- PII handling, content safety, ADR governance gates

**🎬 Video Training**
- *AI Security and Privacy* – LinkedIn Learning (Scott Kennedy)
  <https://www.linkedin.com/learning/ai-security-and-privacy>

**📖 Reading**
- [NIST AI RMF](https://airc.nist.gov/RMF)
- [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [MITRE ATLAS](https://atlas.mitre.org)

**🔬 Hands-On Lab**
Threat-model Capstone 2 RAG system using STRIDE; complete NIST AI RMF Map worksheet.

**📦 Deliverable**
Threat model document, NIST AI RMF worksheet, security controls checklist, ADR for identity strategy.

---

#### Week 24 — Capstone 3, Final Case Study & Interview Prep

**Theme:** Deliver Capstone 3 and architecture case study; pass mock interview
**Hours:** 15 | **Exit Criteria:** All 3 capstones public on GitHub; case study addresses all 15+ required sections; mock-interview score ≥ 70%

**Topics**
- Architecture communication (C4, sequence, DFD, deployment diagrams)
- Executive storytelling, 10-slide deck structure
- Interview system-design methodology, 30-day post-roadmap plan

**🎬 Video Training**
- *Architecture Storytelling* – LinkedIn Learning
  <https://www.linkedin.com/learning/communication-foundations>
- *C4 Model for Software Architecture* – Simon Brown (YouTube, free)
  <https://www.youtube.com/watch?v=x2-rSnhpw0g>

**📖 Book**
- *Communicating Architecture* – O'Reilly (selected chapters)

**📖 Reading**
- [C4 model](https://c4model.com)
- [arc42 architecture template](https://arc42.org/overview)

**🔬 Hands-On Lab**
Deliver Capstone 3 agentic workflow; complete final architecture case study; pass 90-minute mock interview.

**📦 Deliverable**
**CAPSTONE 3 delivery**, final architecture case study doc + 10-slide deck, mock-interview scorecard.

---

## Training Catalog

> **Last verified:** 2025-01-01. Exact URLs and durations should be re-confirmed at provider sites before enrolling.
> Courses marked ⚠️ VERIFY could not be confirmed at time of authoring and should be verified before enrollment.

### Required Courses

**Phase 0 — Foundation**

- **Docker Deep Dive** | Nigel Poulton | Udemy | Beginner–Intermediate | ≈ 9 h
  Most concise Docker course for practitioners; Poulton is widely recognized.
  <https://www.udemy.com/course/docker/>

- **Statistics for Data Science and Business Analysis** | 365 Careers | Udemy | Beginner–Intermediate | ≈ 5 h
  Covers probability, distributions, hypothesis testing without excessive math.
  <https://www.udemy.com/course/statistics-for-data-science-and-business-analysis/>

**Phase 1 — ML Architecture**

- **Microsoft Azure AI Fundamentals AI-900** | Andrew Brown | YouTube/freeCodeCamp | Beginner | ≈ 3.5 h
  Free, up-to-date, covers Azure AI service landscape essential for cloud mapping.
  <https://www.youtube.com/watch?v=OwZHNH8EfSU>

**Phase 2 — GenAI Foundations**

- **Generative AI with LLMs** | Andrew Ng / DeepLearning.AI | Coursera | Intermediate | ≈ 16 h
  Covers transformer architecture, fine-tuning, RLHF, PEFT in one structured course.
  <https://www.deeplearning.ai/courses/generative-ai-with-llms/>

- **ChatGPT Prompt Engineering for Developers** | Andrew Ng / Isa Fulford | DeepLearning.AI | Intermediate | ≈ 1.5 h
  Best concise prompt engineering introduction; free; directly applicable.
  <https://learn.deeplearning.ai/courses/chatgpt-prompt-eng-for-devs>

**Phase 3 — RAG**

- **LangChain for LLM Application Development** | Harrison Chase / Andrew Ng | DeepLearning.AI | Intermediate | ≈ 1.5 h
  Introduction to LangChain chains and RAG; free.
  <https://learn.deeplearning.ai/courses/langchain>

- **Building and Evaluating Advanced RAG** | Jerry Liu / Andrew Ng | DeepLearning.AI | Intermediate | ≈ 1.5 h
  Covers hybrid retrieval, reranking, RAG evaluation; free.
  <https://learn.deeplearning.ai/courses/building-evaluating-advanced-rag>

**Phase 4 — Agentic AI**

- **AI Agents in LangGraph** | Tavily / Harrison Chase | DeepLearning.AI | Intermediate | ≈ 2 h
  Hands-on LangGraph agents with tool use, state, and human-in-the-loop; free.
  <https://learn.deeplearning.ai/courses/ai-agents-in-langgraph>

**Phase 5 — LLMOps**

- **LLMOps** | Erwin Huizenga | DeepLearning.AI | Intermediate | ≈ 1.5 h
  Covers prompt/response logging, versioning, evaluation pipelines; free.
  <https://learn.deeplearning.ai/courses/llmops>

**Phase 6 — Governance**

- **AI Security and Privacy** ⚠️ VERIFY | Scott Kennedy | LinkedIn Learning | Intermediate | ≈ 2 h
  Covers AI-specific security threats, privacy regulations, governance frameworks.
  <https://www.linkedin.com/learning/ai-security-and-privacy>

### Required Books

- **Designing Machine Learning Systems** | Chip Huyen | O'Reilly | Advanced | ≈ 400 pp
  Definitive ML systems architecture reference; covers all lifecycle phases.
  <https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/>

- **MLflow in Action** | Mark Ryan | O'Reilly | Intermediate | ≈ 350 pp
  Only comprehensive MLflow book; practical and enterprise-oriented.
  <https://www.oreilly.com/library/view/mlflow-in-action/9781617296628/>

### Optional Courses

- **The Complete Machine Learning, NLP Bootcamp** ⚠️ VERIFY | Lazy Programmer | Udemy | ≈ 20 h
  Deep backup if additional ML foundations needed; selective consumption only.
  <https://www.udemy.com/user/lazy-programmer/>

- **Azure Machine Learning** ⚠️ VERIFY | Multiple instructors | LinkedIn Learning | ≈ 3 h
  Supplemental Azure ML coverage if hands-on labs need more guidance.
  <https://www.linkedin.com/learning/topics/azure-machine-learning>

---

## Reading & Papers Catalog

### Phase 0 — Foundation

**FastAPI documentation** | Official docs | Sebastián Ramírez | Beginner | Week 1
Routing, Pydantic integration, dependency injection.
<https://fastapi.tiangolo.com>

**The Illustrated Transformer** | Blog | Jay Alammar | Intermediate | Week 9
Visual intuition for attention mechanism.
<https://jalammar.github.io/illustrated-transformer/>

---

### Phase 1 — ML Architecture

**Designing Machine Learning Systems** | Book | Chip Huyen (O'Reilly) | Advanced | Weeks 5–8
Full ML lifecycle, feature stores, training, serving, monitoring.
<https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/>

**Azure Architecture Center — AI/ML** | Architecture guide | Microsoft | Intermediate | Weeks 7–8
Azure AI reference architectures, design patterns.
<https://learn.microsoft.com/en-us/azure/architecture/ai-ml/>

**AWS Well-Architected ML Lens** | Architecture guide | AWS | Intermediate | Week 8
AWS ML design pillars — comparative study.
<https://docs.aws.amazon.com/wellarchitected/latest/machine-learning-lens/>

**Google Cloud Architecture Center** | Architecture guide | Google | Intermediate | Week 8
GCP AI patterns — comparative study.
<https://cloud.google.com/architecture>

---

### Phase 2 — GenAI Foundations

**Attention Is All You Need** | Paper | Vaswani et al. (arXiv:1706.03762) | Advanced | Week 9
Original transformer architecture.
<https://arxiv.org/abs/1706.03762>

> *Guiding questions:* (1) What problem does attention solve vs RNNs? (2) How is multi-head attention different from single-head? (3) What would break if you removed positional encoding?

**LoRA: Low-Rank Adaptation of LLMs** | Paper | Hu et al. (arXiv:2106.09685) | Advanced | Week 12
Parameter-efficient fine-tuning.
<https://arxiv.org/abs/2106.09685>

**QLoRA** | Paper | Dettmers et al. (arXiv:2305.14314) | Advanced | Week 12
Quantized fine-tuning on consumer hardware.
<https://arxiv.org/abs/2305.14314>

---

### Phase 3 — RAG Systems

**RAGAS: Automated Evaluation of RAG** | Paper | Es et al. (arXiv:2309.15217) | Intermediate | Week 15
RAG evaluation metrics: faithfulness, relevance, recall.
<https://arxiv.org/abs/2309.15217>

> *Guiding questions:* (1) How does faithfulness differ from answer relevance? (2) Why does context recall matter more than precision for open-domain Q&A? (3) How do you create a golden evaluation dataset without ground-truth labels?

**LangChain RAG tutorial** | Official docs | LangChain | Intermediate | Week 13
End-to-end RAG pipeline with LCEL.
<https://python.langchain.com/docs/tutorials/rag/>

**LlamaIndex documentation** | Official docs | LlamaIndex | Intermediate | Weeks 13–16
Alternative RAG framework; multimodal support.
<https://docs.llamaindex.ai/en/stable/>

---

### Phase 4 — Agentic AI

**ReAct: Synergizing Reasoning and Acting** | Paper | Yao et al. (arXiv:2210.03629) | Intermediate | Week 17
Foundation of ReAct agent pattern.
<https://arxiv.org/abs/2210.03629>

**LangGraph documentation** | Official docs | LangChain | Intermediate | Weeks 17–20
Graph-based agent orchestration.
<https://langchain-ai.github.io/langgraph/>

**Model Context Protocol specification** | Official docs | Anthropic | Intermediate | Week 19
MCP protocol design and tool server implementation.
<https://modelcontextprotocol.io/docs>

**AgentBench** | Paper | Liu et al. (arXiv:2308.03688) | Advanced | Week 20
Agent evaluation methodology.
<https://arxiv.org/abs/2308.03688>

---

### Phase 5 — MLOps/LLMOps

**MLflow documentation** | Official docs | MLflow/Databricks | Intermediate | Week 21
Experiment tracking, model registry, serving.
<https://mlflow.org/docs/latest/index.html>

**Azure MLOps v2 accelerator** | Reference implementation | Microsoft | Advanced | Week 21
Production MLOps on Azure reference architecture.
<https://github.com/Azure/mlops-v2>

---

### Phase 6 — Governance & Security

**NIST AI Risk Management Framework** | Standard | NIST | Intermediate | Week 23
Govern/Map/Measure/Manage AI risk lifecycle.
<https://airc.nist.gov/RMF>

**OWASP Top 10 for LLM Applications** | Standard | OWASP | Intermediate | Weeks 15, 23
Top LLM security risks and mitigations.
<https://owasp.org/www-project-top-10-for-large-language-model-applications/>

> *Guiding questions:* (1) How does prompt injection differ from SQL injection in terms of mitigations? (2) What architectural controls can prevent excessive agency? (3) How does insecure output handling manifest in a RAG pipeline?

**MITRE ATLAS** | Framework | MITRE | Advanced | Week 23
Adversarial ML threat taxonomy.
<https://atlas.mitre.org>

**C4 model** | Architecture guide | Simon Brown | Beginner | Week 24
Architecture diagramming standard.
<https://c4model.com>

---

## Capstone Portfolio

---

### Capstone 1 — Production ML Solution *(Week 12 delivery)*

**Business Problem**
Enterprise procurement anomaly detection: identify fraudulent or erroneous purchase orders using historical ERP transaction data.

**Target Users**
Accounts payable managers, internal audit, procurement controllers.

**Functional Scope**
Ingest PO line-item data → validate schema → train gradient-boosted classifier → expose REST API → monitor for drift.

**Architecture**
FastAPI inference API → Azure ML managed endpoint → MLflow Model Registry → Azure Monitor; batch scoring via Azure ML pipelines.

**Technology Stack**
Python, scikit-learn, XGBoost, MLflow, FastAPI, Docker, GitHub Actions, Azure ML, Azure Monitor.

**Suggested Datasets**
- [UCI Fraud Detection Dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- Synthetic ERP PO data generated with Faker

**Implementation Milestones**

| Milestone | Week | Description |
|---|---|---|
| M1 | W3 | EDA + baseline model |
| M2 | W5 | Pipeline + MLflow |
| M3 | W2 | API + Docker |
| M4 | W7 | AML deploy + CI/CD |
| M5 | W12 | Final delivery |

**Evaluation Metrics**
AUC-ROC, Precision@top-k, F1, calibration error, inference p99 latency.

**Security Controls**
Azure Managed Identity for endpoint auth, no hardcoded secrets, input validation with Pydantic.

**Required Documentation**
Architecture diagram (C4 context + container), ADR for model selection, MLflow experiment README, deployment runbook.

**GitHub Repo Structure**
`capstone1-ml-solution/` → `src/`, `tests/`, `notebooks/`, `infra/`, `docs/`, `mlflow/`, `.github/`

**Demonstration Scenario**
"Here is a CSV of 100 POs — which ones should I review?" Live API call with Swagger UI.

**Stretch Goals**
Add SHAP explanations API, A/B testing endpoint, automated retraining trigger on drift.

**Estimated Effort:** 15–20 hours across Weeks 3–12 (distributed)

---

### Capstone 2 — Enterprise RAG Assistant *(Week 20 delivery)*

**Business Problem**
Oracle ERP Knowledge Assistant: allow procurement and finance staff to query ERP documentation, release notes, and policy documents in natural language.

**Target Users**
ERP end users, support analysts, procurement officers.

**Functional Scope**
Ingest multi-format docs (PDF, DOCX, HTML) → chunk and index → hybrid retrieval → rerank → generate cited responses → access control → monitoring.

**Architecture**
Azure AI Search (hybrid) → Azure OpenAI (GPT-4o) → FastAPI → Azure Container Apps; LangSmith for tracing.

**Technology Stack**
Python, LangChain/LlamaIndex, Azure AI Search, Azure OpenAI, Azure AI Document Intelligence, RAGAS, Pydantic, FastAPI, Docker.

**Suggested Datasets**
Oracle ERP public documentation PDFs, Oracle E-Business Suite release notes (freely available), IT policy documents (synthetic).

**Implementation Milestones**

| Milestone | Week | Description |
|---|---|---|
| M1 | W13 | Ingestion pipeline |
| M2 | W14 | Hybrid retrieval |
| M3 | W15 | Evaluation dataset |
| M4 | W15–16 | Access control + guardrails |
| M5 | W20 | Final delivery |

**Evaluation Metrics**
RAGAS faithfulness ≥ 0.80, context precision ≥ 0.70, answer relevance ≥ 0.80, p99 latency < 3 s, cost per query < $0.01.

**Security Controls**
Azure AD RBAC, managed identity for Azure OpenAI, prompt injection defenses, PII detection (Presidio), content safety filter.

**Required Documentation**
C4 diagrams (all levels), data flow diagram, threat model, RAGAS evaluation report, cost model, ADRs (3+).

**GitHub Repo Structure**
`capstone2-rag-assistant/` → `ingestion/`, `retrieval/`, `generation/`, `evaluation/`, `api/`, `infra/`, `docs/`, `security/`

**Demonstration Scenario**
"What are the period-end closing steps in Oracle R12 GL?" → cited, structured response with source documents.

**Stretch Goals**
Add citation UI with document preview, fine-tuned embedding model, automated nightly evaluation.

**Estimated Effort:** 20–25 hours across Weeks 13–20

---

### Capstone 3 — Agentic Workflow *(Week 24 delivery)*

**Business Problem**
Automated IT service-request fulfillment: an agent triages incoming IT tickets, queries the knowledge base, creates Jira-style tickets, routes for approval, and updates the requester.

**Target Users**
IT service desk, end users, IT managers.

**Functional Scope**
Classify request → search KB → assess automated resolution → escalate or auto-resolve → human approval gate → update ticketing system → notify user → audit log.

**Architecture**
LangGraph multi-agent (classifier → resolver → approver → notifier) → MCP tool servers (KB, ticket system, email) → SQLite checkpointer → Prometheus metrics.

**Technology Stack**
Python, LangGraph, MCP Python SDK, FastAPI, SQLite, Prometheus, Grafana (or Azure Monitor), NVIDIA NeMo Guardrails.

**Implementation Milestones**

| Milestone | Week | Description |
|---|---|---|
| M1 | W17 | Single triage agent |
| M2 | W18 | Checkpointing + human approval |
| M3 | W19 | Multi-agent + MCP |
| M4 | W20 | Guardrails + evaluation |
| M5 | W24 | Final delivery |

**Evaluation Metrics**
Task-completion rate ≥ 80%, PII leakage = 0, mean resolution time, false-escalation rate < 20%, audit log completeness 100%.

**Security Controls**
RBAC per agent role, MCP server input validation, guardrails on output, no PII in logs, idempotent tool calls.

**GitHub Repo Structure**
`capstone3-agentic-workflow/` → `agents/`, `tools/`, `mcp_servers/`, `evaluation/`, `infra/`, `docs/`

**Demonstration Scenario**
"New request: 'My VPN is not connecting from home. User: john.doe@company.com Priority: High'" → live agent run with approval interrupt.

**Stretch Goals**
Add voice input (Azure Speech), Slack integration, self-improving KB via approved resolutions.

**Estimated Effort:** 20–25 hours across Weeks 17–24

---

### Final Architecture Case Study *(Week 24)*

An interview-ready proposal for an **Enterprise Procurement Intelligence Platform** combining classical ML (anomaly detection), RAG (policy assistant), and agentic AI (approval workflow) on Azure.

**Required Sections**

1. Business problem and assumptions
2. Functional and non-functional requirements (latency, throughput, availability, security, cost)
3. Build vs buy analysis (Azure OpenAI vs self-hosted, managed vs custom RAG)
4. Architecture diagrams: Context, Container, Component, Sequence, Data Flow, Deployment (C4)
5. Cloud service selection with Azure/AWS/GCP mapping table
6. STRIDE threat model
7. Responsible AI assessment (NIST AI RMF)
8. Data governance and PII handling
9. Availability (99.9% SLA), scalability (10× load), DR (RTO 4h, RPO 1h)
10. Evaluation strategy (online and offline)
11. Monitoring and incident management
12. Cost model (per-query cost, monthly estimate, 3 scenarios)
13. Delivery roadmap (phased: MVP → production → enhance)
14. Risks and mitigations register
15. Architecture Decision Records (5+)
16. Executive summary and 10-slide presentation outline

---

## Milestones & Stage Gates

---

### 🏁 Week 2 — Python Production & Containers

**Competencies Demonstrated**
Python production coding, containers, CI/CD.

**Evidence / Artifacts**
FastAPI service + Docker + GitHub Actions pipeline.

**Assessment Method**
Self-review against checklist; share with peer.

**Pass Criteria**
CI pipeline green; test coverage ≥ 80%; image < 500 MB.

**Recovery Plan**
Add 1 extra hour/day for 3 days; focus only on failing criteria.

---

### 🏁 Week 4 — Dev Tooling & Embeddings

**Competencies Demonstrated**
Dev tooling, embeddings, statistics.

**Evidence / Artifacts**
Embedding visualization, nearest-neighbor demo.

**Assessment Method**
Demonstrate to a colleague who asks 3 questions.

**Pass Criteria**
Can explain clustering; Git history is clean.

**Recovery Plan**
Revisit Statistics course sections; re-do embedding lab.

---

### 🏁 Week 8 — ML Lifecycle & Architecture

**Competencies Demonstrated**
ML lifecycle, cloud deployment, architecture trade-offs.

**Evidence / Artifacts**
Deployed AML endpoint, ADRs, architecture proposal.

**Assessment Method**
Mock design review — 20-minute presentation.

**Pass Criteria**
All 5 WAF pillars addressed; endpoint live; ADR explains trade-off.

**Recovery Plan**
Re-read Chip Huyen Ch 1–4; add missing NFRs.

---

### 🏁 Week 12 — GenAI Foundations & Capstone 1

**Competencies Demonstrated**
GenAI foundations, fine-tuning, Capstone 1 delivery.

**Evidence / Artifacts**
Capstone 1 GitHub repo + MLflow experiments.

**Assessment Method**
Code review + 10-minute demo.

**Pass Criteria**
Fine-tuned model outperforms base ≥ 5%; all tests pass.

**Recovery Plan**
Extend Week 12 by 1 week; drop LoRA stretch goals.

---

### 🏁 Week 16 — Full RAG Pipeline

**Competencies Demonstrated**
Full RAG pipeline, evaluation, access control.

**Evidence / Artifacts**
RAGAS report, hybrid search demo, RBAC design.

**Assessment Method**
Architecture walkthrough + Q&A (30 min).

**Pass Criteria**
RAGAS faithfulness > 0.75; injection attacks blocked; reviewer cannot break RBAC logic.

**Recovery Plan**
Re-do retrieval lab; focus on weakest RAGAS metric.

---

### 🏁 Week 20 — Agentic AI & Capstone 2

**Competencies Demonstrated**
Agentic AI, multi-agent, MCP, Capstone 2 delivery.

**Evidence / Artifacts**
Capstone 2 GitHub repo + evaluation report + agent graph.

**Assessment Method**
30-minute live demo + architecture Q&A.

**Pass Criteria**
Task-completion ≥ 80%; PII = 0; Capstone 2 public on GitHub.

**Recovery Plan**
Drop stretch goals; fix core evaluation failures first.

---

### 🏁 Week 24 — Full Stack AI Architecture (Final Gate)

**Competencies Demonstrated**
Full stack AI architecture, governance, interview readiness.

**Evidence / Artifacts**
All 3 capstones + case study + mock interview score.

**Assessment Method**
90-minute mock interview with peer or mentor.

**Pass Criteria**
Mock interview score ≥ 70%; case study covers all 15 required sections.

**Recovery Plan**
Add 2-week buffer; prioritize case study over capstone polish.

---

## Skills Matrix

> **Scale:** 1 = No knowledge · 2 = Awareness · 3 = Practical experience · 4 = Advanced practitioner · 5 = Expert / can design for others

| Skill Domain | Start | Target (W24) | Evidence Required |
|---|---|---|---|
| Python / Software Engineering | 3 | 5 | Typed, tested, packaged production service; CI/CD pipeline |
| ML System Design | 2 | 4 | Architecture proposal; ADRs; deployed ML endpoint |
| Deep Learning & Transformers | 1 | 3 | Mini transformer; fine-tuned LoRA adapter |
| Cloud AI Services (Azure) | 2 | 4 | AML deployment; Azure AI Search; Azure Monitor dashboard |
| RAG Architecture | 1 | 5 | Advanced RAG pipeline; RAGAS evaluation; Capstone 2 |
| Agentic AI | 1 | 4 | LangGraph multi-agent; MCP tool server; Capstone 3 |
| MLOps / LLMOps | 2 | 4 | MLflow CI/CD; Kubernetes deployment; OpenTelemetry |
| Data Architecture | 3 | 4 | Medallion pipeline; feature pipeline; data contracts |
| API & Integration Architecture | 4 | 5 | FastAPI services; MCP servers; Azure integration patterns |
| Security | 2 | 4 | Threat model; RBAC design; OWASP LLM mitigations |
| Responsible AI & Governance | 1 | 4 | NIST AI RMF worksheet; Responsible AI assessment; ADRs |
| Observability & Reliability | 2 | 4 | OpenTelemetry traces; cost dashboard; alert rules |
| Cost Optimization | 2 | 4 | Cost model in case study; per-query cost metric |
| Architecture Documentation | 3 | 5 | C4 diagrams; ADRs; executive summary; 10-slide deck |
| Stakeholder Communication | 3 | 5 | 10-minute demos; executive summary; mock interview |

---

## Architecture Artifacts Checklist

Use this checklist for every AI solution you design:

- [ ] **Problem statement** — business problem, success metrics (KPIs), non-goals, constraints
- [ ] **Functional requirements** — user stories or capability statements
- [ ] **Non-functional requirements** — latency, throughput, availability, scalability, security, cost, compliance
- [ ] **Data-source inventory** — sources, formats, volumes, freshness, ownership, access method
- [ ] **Data classification & privacy assessment** — PII identification, data residency, retention policy, consent
- [ ] **Model-selection scorecard** — candidate models, evaluation criteria, benchmark results, cost, final selection rationale
- [ ] **Evaluation plan** — offline metrics, online metrics, evaluation dataset, baseline, human evaluation plan
- [ ] **Architecture diagrams** — C4 Context, Container, Component; Sequence; Data Flow; Deployment
- [ ] **Threat model** — STRIDE analysis, OWASP LLM Top 10 mapping, mitigations
- [ ] **Responsible AI assessment** — bias analysis, fairness metrics, transparency plan, NIST AI RMF mapping
- [ ] **Cost estimate** — per-unit cost (per query/inference), monthly estimate, 3 scenarios (low/medium/high)
- [ ] **Capacity & performance model** — peak load estimate, scaling strategy, resource sizing
- [ ] **Observability plan** — metrics, traces, logs, dashboards, alerts, SLIs/SLOs
- [ ] **Deployment & rollback plan** — deployment strategy, smoke tests, health checks, rollback trigger
- [ ] **DR plan** — RTO, RPO, backup strategy, failover design
- [ ] **Architecture Decision Records** — at least 3 ADRs for key technology/design decisions
- [ ] **Operational runbook** — startup/shutdown, common failure scenarios, escalation paths
- [ ] **Executive presentation** — 10-slide deck: problem → solution → architecture → security → cost → roadmap

---

## Certification Guidance

### ✅ Recommended — Take These

**Microsoft AI-900 (Azure AI Fundamentals)**
- Signals Azure commitment; easy win with minimal effort.
- **Prerequisites:** None
- **Best timing:** Week 7–8
- **Effort:** 10–15 h
- **Verdict:** Take it; low effort, high signal.

**Microsoft AI-102 (Azure AI Engineer Associate)**
- Most relevant cert for this role; covers Azure OpenAI, AI Search, Document Intelligence.
- **Prerequisites:** AI-900, Python basics
- **Best timing:** After Week 16
- **Effort:** 40–60 h
- **Verdict:** Prioritize after Capstone 2 delivery.

**Databricks Generative AI Engineer Associate**
- Databricks is ubiquitous in enterprise; MLflow is a Databricks product.
- **Prerequisites:** Spark basics
- **Best timing:** After Week 22
- **Effort:** 20–30 h
- **Verdict:** Worthwhile if Databricks is in your target stack.

### ⚠️ Conditional — Only If Targeting Those Clouds

**AWS ML Specialty**
- Relevant only if targeting AWS-focused roles.
- **Effort:** 60–80 h | **Timing:** After Week 24
- **Verdict:** Portfolio first; certification later.

**Google Professional ML Engineer**
- Relevant only if targeting GCP-focused roles.
- **Effort:** 60–80 h | **Timing:** After Week 24
- **Verdict:** Portfolio first; certification later.

### ❌ Skip (Unless Targeting GPU-Heavy Roles)

**NVIDIA AI Infrastructure and Operations**
- Low overlap with this roadmap unless working with GPU-intensive infrastructure.
- **Effort:** 20 h

> **Recommendation:** Prioritize AI-900 (Week 8) and AI-102 (after Week 16). These two certifications, combined with your three GitHub capstones, create a compelling interview profile. Avoid scheduling certifications during capstone delivery weeks.

---

## Interview & Job-Readiness Plan

### 20 Key AI Solutions Architect Interview Topics

1. RAG vs fine-tuning — when to use each and hybrid approaches
2. Vector database selection (pgvector vs Azure AI Search vs Pinecone vs Weaviate)
3. Chunking strategy trade-offs for enterprise documents
4. LLM evaluation methodology (offline vs online)
5. Multi-agent vs single-agent design — decision criteria
6. Prompt injection — attack vectors and mitigations
7. Build vs buy for LLM infrastructure
8. MLOps vs LLMOps — key differences
9. Responsible AI principles applied to a real use case
10. Cost optimization for LLM applications at scale
11. Azure OpenAI vs self-hosted open-source model — selection criteria
12. Data governance for AI systems (PII, residency, lineage)
13. Observability design for LLM applications (what to instrument)
14. High availability and DR for AI serving infrastructure
15. Transformer architecture — attention, positional encoding, KV cache
16. MCP protocol — purpose, benefits, security considerations
17. NIST AI RMF — how you would apply it to a new project
18. How to explain an AI architecture to a non-technical executive
19. Architecture trade-off methodology (CAP theorem in AI context)
20. How enterprise ERP/integration experience transfers to AI architecture

---

### 10 System-Design Scenarios

1. Design an enterprise knowledge assistant for a 500,000-document ERP knowledge base
2. Design an ML pipeline that detects procurement fraud in real time
3. Design a multi-modal document processing system for invoice extraction at 1M invoices/month
4. Design a customer-facing chatbot with regulatory compliance constraints (GDPR, HIPAA)
5. Design a code review agent that integrates with GitHub PRs
6. Design an AI platform that serves 50 internal teams with model governance requirements
7. Design a RAG system that must work without internet access (air-gapped)
8. Design a retraining pipeline that triggers automatically when model drift is detected
9. Design an agentic ERP workflow automation that handles purchase order exceptions
10. Design an LLM gateway that enforces rate limiting, PII redaction, cost allocation, and audit logging

---

### 10 Behavioral Questions for Enterprise Technologists

1. "Tell me about a time you had to design a system under significant technical constraints."
2. "Describe a situation where you had to convince a skeptical stakeholder to adopt a new technology."
3. "How have you handled a production incident in a system you designed?"
4. "Tell me about a build vs buy decision you made and what the outcome was."
5. "Describe how you managed technical debt in a large enterprise system."
6. "Tell me about a time you had to rapidly upskill to solve an urgent business problem."
7. "How do you balance security and usability in enterprise systems?"
8. "Describe your approach to leading a technical review for a system you didn't build."
9. "Tell me about a time your architecture recommendation was rejected — what did you do?"
10. "How has your Oracle/ERP experience shaped your approach to data governance and integration architecture?"

---

### Architecture Trade-off Answer Method (TRADED Framework)

Use this framework when answering any trade-off or design question in an interview:

- **T**rade-off — name the competing dimensions (cost vs latency, accuracy vs speed, build vs buy)
- **R**equirements — anchor to stated NFRs and business context
- **A**lternatives — present 2–3 options with pros and cons
- **D**ecision — state your recommended choice
- **E**vidence — cite a benchmark, case study, or first-principles reasoning
- **D**ependencies — flag prerequisites, risks, and reversibility

---

### 30-Day Post-Week-24 Interview Preparation Routine

| Week | Focus |
|---|---|
| 1 | Polish all 3 GitHub repos; write 1-page README for each |
| 2 | Mock system design (2 sessions); refine case study doc |
| 3 | Behavioral interview prep (STAR stories for 10 behavioral questions) |
| 4 | Active applications; LinkedIn outreach; 2 informational interviews |

---

### Resume & LinkedIn Positioning

**Title:** "Senior Software Engineer → AI Solutions Architect (in transition)" or "Enterprise AI Solutions Architect"

**Summary:** Lead with Oracle/ERP + integration depth, then highlight AI upskilling trajectory and GitHub portfolio.

**Key Skills:** Python, LangChain, LangGraph, Azure OpenAI, RAG, MLOps, MLflow, Docker, Kubernetes, Oracle E-Business Suite, REST APIs, Enterprise Integration.

**Projects Section:** Link directly to Capstone 1, 2, 3 GitHub repos with 1-line descriptions.

**Transferable Experience Framing:**
- "Designed and delivered enterprise integrations serving 10,000+ users → AI architecture for enterprise-scale LLM applications"
- "Oracle ERP data model expertise → structured data extraction and document intelligence"

---

## Progress Tracking Templates

### Weekly Scorecard

```markdown
## Week [N] Scorecard — [Date Range]

### Hours Log
| Activity                  | Planned | Actual |
|---|---|---|
| Video learning            |         |        |
| Reading                   |         |        |
| Hands-on lab              |         |        |
| Architecture/documentation|         |        |
| **Total**                 |         |        |

### Completion Checklist
- [ ] Primary video training (target section) completed
- [ ] Required reading completed
- [ ] Hands-on lab completed and pushed to GitHub
- [ ] Deliverable completed
- [ ] Exit criteria met

### Reflections
- What went well?
- What was harder than expected?
- What will I carry forward?

### Risks / Blockers
| Risk | Impact | Mitigation |
|---|---|---|
|      |        |            |
```

---

### Learning Log Template

```markdown
## Learning Log Entry — [Date]

**Topic:** [Topic name]
**Source:** [Course/book/doc + URL]

**Key concepts learned:**
1.
2.
3.

**Code or architecture insight:**
> [Paste snippet or diagram description]

**Questions to investigate:**
-

**How this connects to my Oracle/enterprise background:**
>
```

---

### ADR Template

```markdown
# ADR-[NNN]: [Short title]
**Date:** YYYY-MM-DD
**Status:** Proposed | Accepted | Deprecated | Superseded

## Context
[What is the issue motivating this decision?]

## Decision
[What is the change that is being proposed or has been agreed to?]

## Alternatives Considered
| Option | Pros | Cons |
|---|---|---|
|        |      |      |

## Consequences

**Positive:**
-

**Negative:**
-

**Risks:**
-

## References
-
```

---

### Monthly Retrospective Template

```markdown
## Monthly Retrospective — Month [N] ([Date])

### Progress vs Plan
| Week | Planned Deliverable | Actual | Delta | Reason |
|---|---|---|---|---|
|      |                     |        |       |        |

### Skills Assessment (self-rate 1–5)
| Skill | Start of Month | End of Month | Evidence |
|---|---|---|---|
|       |                |              |          |

### Top 3 wins this month
1.
2.
3.

### Top 3 things to improve next month
1.
2.
3.

### Portfolio Status
| Capstone   | Status | GitHub URL | % Complete |
|---|---|---|---|
| Capstone 1 |        |            |            |
| Capstone 2 |        |            |            |
| Capstone 3 |        |            |            |

### Hours Dashboard
- Planned total this month: 48–60 h
- Actual total: __ h
- Variance: __ h
- Primary cause:
```

---

### 24-Week Dashboard Tracker

```markdown
## AI Solutions Architect — 24-Week Dashboard

| Week | Planned Hours | Actual Hours | Courses Done | Labs Done | GitHub Commits | Blockers |
|---|---|---|---|---|---|---|
| 1  | 13 |  |  |  |  |  |
| 2  | 13 |  |  |  |  |  |
| 3  | 14 |  |  |  |  |  |
| 4  | 13 |  |  |  |  |  |
| 5  | 13 |  |  |  |  |  |
| 6  | 14 |  |  |  |  |  |
| 7  | 15 |  |  |  |  |  |
| 8  | 13 |  |  |  |  |  |
| 9  | 14 |  |  |  |  |  |
| 10 | 13 |  |  |  |  |  |
| 11 | 14 |  |  |  |  |  |
| 12 | 15 |  |  |  |  |  |
| 13 | 14 |  |  |  |  |  |
| 14 | 13 |  |  |  |  |  |
| 15 | 14 |  |  |  |  |  |
| 16 | 14 |  |  |  |  |  |
| 17 | 14 |  |  |  |  |  |
| 18 | 13 |  |  |  |  |  |
| 19 | 14 |  |  |  |  |  |
| 20 | 15 |  |  |  |  |  |
| 21 | 14 |  |  |  |  |  |
| 22 | 14 |  |  |  |  |  |
| 23 | 14 |  |  |  |  |  |
| 24 | 15 |  |  |  |  |  |
| **Total** | **336** | | | | | |
```

---

## Week 1 Action Checklist

Complete these in the **next 48 hours** ⚡

### Immediate Setup (Day 1–2)

- [ ] Install Python 3.12, uv, pyenv, Git, Docker Desktop, VS Code
- [ ] Create GitHub account / organization: `github.com/[yourusername]/ai-architect-journey`
- [ ] Create the master repository: `ai-architect-journey` with README and project board
- [ ] Create sub-repositories: `capstone1-ml-solution`, `capstone2-rag-assistant`, `capstone3-agentic-workflow`
- [ ] Set up Azure free account: <https://azure.microsoft.com/en-us/free/>
- [ ] Sign up for DeepLearning.AI (free): <https://learn.deeplearning.ai>
- [ ] Sign up for O'Reilly Learning (Qualcomm may provide access — check IT portal)
- [ ] Start *ChatGPT Prompt Engineering for Developers* (1.5 h — do this first to get inspired)

### First Architecture Exercise (Day 2–3)

Draw a simple architecture diagram for a **"Oracle ERP Invoice Q&A bot"** using only boxes and arrows. No code needed. Answer these 5 questions:

1. Where does data come from?
2. How does the user ask a question?
3. How does the system find the answer?
4. Where is the answer generated?
5. What could go wrong?

> This is your starting point. By Week 24, you will design this system properly with C4 diagrams, threat models, ADRs, and a cost model.

### First Repository Setup

```bash
# Install uv
curl -LsSf https://astral.sh/uv/install.sh | sh

# Create project
uv init predict_service
cd predict_service
uv add fastapi uvicorn pydantic

# Create GitHub repo and push
git init
git add .
git commit -m "feat: initial FastAPI service scaffold"
gh repo create ai-architect-journey --public --push
```

### First Measurable Assessment (End of Week 2)

> ✅ You pass Week 2 when: `gh actions view` shows a green CI run, `docker pull` succeeds for your image, and you can answer *"What is a multi-stage Docker build and why does it reduce image size?"* in 60 seconds without notes.

---

## Post-Roadmap Backlog

The following topics strengthen the profile further but are deferred to keep the 24-week plan achievable. Tackle after Week 24:

- Spark / Databricks for large-scale ML feature pipelines
- Advanced FinOps for AI (RI pricing, spot instances, model batching optimization)
- Synthetic data generation for model training
- LLM red-teaming and adversarial robustness testing
- Federated learning and privacy-preserving ML
- Edge AI deployment (NVIDIA Jetson, ONNX Runtime)
- Full AWS SageMaker or GCP Vertex AI deep dive

---

## References

- [FastAPI documentation](https://fastapi.tiangolo.com)
- [Pydantic v2 documentation](https://docs.pydantic.dev)
- [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [sentence-transformers documentation](https://www.sbert.net)
- [The Illustrated Transformer – Jay Alammar](https://jalammar.github.io/illustrated-transformer/)
- [Attention Is All You Need – arXiv:1706.03762](https://arxiv.org/abs/1706.03762)
- [LoRA – arXiv:2106.09685](https://arxiv.org/abs/2106.09685)
- [QLoRA – arXiv:2305.14314](https://arxiv.org/abs/2305.14314)
- [RAGAS – arXiv:2309.15217](https://arxiv.org/abs/2309.15217)
- [ReAct – arXiv:2210.03629](https://arxiv.org/abs/2210.03629)
- [AgentBench – arXiv:2308.03688](https://arxiv.org/abs/2308.03688)
- [LangChain documentation](https://python.langchain.com)
- [LangGraph documentation](https://langchain-ai.github.io/langgraph/)
- [LlamaIndex documentation](https://docs.llamaindex.ai)
- [MLflow documentation](https://mlflow.org/docs/latest/)
- [Model Context Protocol](https://modelcontextprotocol.io/docs)
- [Azure Architecture Center – AI/ML](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/)
- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/)
- [AWS Well-Architected ML Lens](https://docs.aws.amazon.com/wellarchitected/latest/machine-learning-lens/)
- [Google Cloud Architecture Center](https://cloud.google.com/architecture)
- [NIST AI Risk Management Framework](https://airc.nist.gov/RMF)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [MITRE ATLAS](https://atlas.mitre.org)
- [C4 model](https://c4model.com)
- [Databricks Medallion Architecture](https://docs.databricks.com/en/lakehouse/medallion.html)
- [OpenAI model documentation](https://platform.openai.com/docs/models)
- [Anthropic Claude model documentation](https://docs.anthropic.com/en/docs/about-claude/models/overview)
- [Hugging Face Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
- [Azure MLOps v2 accelerator](https://github.com/Azure/mlops-v2)
- [Generative AI with LLMs – DeepLearning.AI](https://www.deeplearning.ai/courses/generative-ai-with-llms/)
- [DeepLearning.AI free short courses](https://learn.deeplearning.ai)
