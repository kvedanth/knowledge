# AI Solutions Architect — 24-Week Transition Roadmap
### A Rigorous, Practical, and Job-Oriented Plan for Enterprise Technologists

---

> **Learner Profile:** Intermediate Python · ML Fundamentals · Oracle ERP/E-Business Suite · SQL/PL/SQL · Core Java · APIs & Integrations
> **Target Roles:** AI Solutions Architect · Generative AI Solutions Architect · Enterprise AI Architect · Agentic AI Architect · Principal AI Engineer (Architecture)
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

**Phase overview:**

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

> **Column key:** H = Hours | V = Video | R = Reading | L = Lab | D = Documentation/Architecture

---

### Phase 0 — Foundation (Weeks 1–4)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Python for Production AI | Write type-annotated, testable, packaged Python modules; build a FastAPI microservice | Python typing, Pydantic v2, pytest, uv/poetry packaging, logging, configuration (pydantic-settings), FastAPI basics | *Python for Data Engineers* – O'Reilly (selected chapters 1–5) <br><br>🎬 **Video:** *Python for Everybody* – Dr. Chuck Severance (freeCodeCamp/YouTube, free) [https://www.youtube.com/watch?v=8DvywoWv6fI](https://www.youtube.com/watch?v=8DvywoWv6fI) · *Python for Data Engineers* – O'Reilly Learning [https://learning.oreilly.com/videos/python-for-data/](https://learning.oreilly.com/videos/python-for-data/9781098100728/)| [FastAPI docs](https://fastapi.tiangolo.com) · [Pydantic v2 docs](https://docs.pydantic.dev) | Build a typed, tested FastAPI service that returns ML model metadata | `predict_service/` repo scaffold with health endpoint, typed schemas, 10+ unit tests, README | 13 | Can explain dependency injection in FastAPI; pytest coverage ≥ 80%; package installs cleanly |
| 2 | Containers & CI/CD | Containerize a Python service; configure a GitHub Actions pipeline | Docker multi-stage builds, docker-compose, .env secrets, GitHub Actions, pre-commit hooks, Makefile conventions | *Docker Deep Dive* – Nigel Poulton (Udemy) [https://www.udemy.com/course/docker/](https://www.udemy.com/course/docker/) | [GitHub Actions docs](https://docs.github.com/en/actions) · [Docker best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/) | Containerize Week 1 service; add lint → test → build → push Actions pipeline | Dockerfile, docker-compose.yml, `.github/workflows/ci.yml`, README with architecture diagram | 13 | Image builds without warnings; CI pipeline passes green; can explain multi-stage build benefits |
| 3 | ML Refresh & Feature Engineering | Retrain and evaluate a scikit-learn pipeline; explain bias-variance trade-off | NumPy, pandas, scikit-learn pipelines, cross-validation, feature engineering, model evaluation (AUC, F1, calibration), imbalanced data | *Machine Learning with scikit-learn* – Andreas Mueller (O'Reilly video) | [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html) | Build an enterprise churn prediction pipeline with preprocessing, CV, feature importance, and calibration plot | Jupyter notebook + exported `churn_model/` package with trained model, metrics report | 14 | Model AUC > 0.75 on holdout; can explain precision-recall trade-off for imbalanced data |
| 4 | Statistics, Embeddings & Dev Tooling | Apply statistical tests for data quality; create and compare text embeddings | Probability distributions, hypothesis testing, Central Limit Theorem, cosine similarity, word2vec vs sentence-transformers, dimensionality reduction (UMAP/t-SNE), Git branching, pre-commit | *Statistics for Data Science* – Jose Portilla (Udemy) [https://www.udemy.com/course/statistics-for-data-science-and-business-analysis/](https://www.udemy.com/course/statistics-for-data-science-and-business-analysis/) | [sentence-transformers docs](https://www.sbert.net) · [UMAP docs](https://umap-learn.readthedocs.io) | Embed 1,000 Oracle ERP FAQ entries; visualize clusters; build a nearest-neighbor lookup | UMAP cluster visualization, semantic search demo notebook, `embeddings_utils.py` module | 13 | Can explain embedding distance vs keyword search; clusters visually meaningful; Git workflow clean |

---

### Phase 1 — ML Architecture (Weeks 5–8)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 5 | End-to-End ML Lifecycle | Design a data-to-deployment ML workflow; write an ML system design doc | Problem framing, KPI definition, data ingestion, data quality contracts, training/validation/test splits, experiment tracking concept, batch vs real-time inference | *Designing Machine Learning Systems* – Chip Huyen (O'Reilly book) Ch 1–4 <br><br>🎬 **Video:** *Designing Machine Learning Systems* – Chip Huyen lecture series (Stanford CS329S, free) [https://stanford-cs329s.github.io](https://stanford-cs329s.github.io) · O'Reilly video companion [https://learning.oreilly.com/videos/designing-machine-learning/](https://learning.oreilly.com/videos/designing-machine-learning/9781098107994/)| [Google Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml) · [Data Quality at Scale – Uber blog](https://www.uber.com/blog/monitoring-data-quality-at-scale/) | Add MLflow experiment tracking to Week 3 churn model | MLflow experiment with 5+ runs, best-model artifact, architecture diagram (ML lifecycle) | 13 | Can articulate batch vs streaming trade-offs; MLflow UI shows tracked params/metrics |
| 6 | Data Pipelines & Feature Stores | Build a simple feature pipeline; explain medallion architecture | Data lake layers (bronze/silver/gold), Delta Lake concepts, feature stores vs ad-hoc, data contracts, schema evolution, great_expectations basics | *Data Engineering with Python* – Paul Crickard (O'Reilly book) Ch 1–3 <br><br>🎬 **Video:** *Data Engineering Zoomcamp* – DataTalks.Club (free) [https://github.com/DataTalksClub/data-engineering-zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) · *Data Engineering with Python* – O'Reilly Learning [https://learning.oreilly.com/videos/data-engineering-with/](https://learning.oreilly.com/videos/data-engineering-with/9781800560413/)| [Databricks Medallion Architecture](https://docs.databricks.com/en/lakehouse/medallion.html) · [great_expectations docs](https://docs.greatexpectations.io) | Build a DuckDB-based feature pipeline with data-quality checks for procurement data | Feature pipeline code, data-quality report, medallion layer diagram | 14 | Pipeline fails loudly on bad data; can explain Delta Lake ACID guarantees |
| 7 | Cloud AI Platforms — Azure Primary | Deploy a model to Azure ML; map equivalent services across clouds | Azure ML workspace, compute clusters, managed endpoints, Azure AI Foundry overview, service mapping (Azure vs AWS vs GCP) | *Microsoft Azure AI Fundamentals AI-900* – Andrew Brown (freeCodeCamp, free) [https://www.youtube.com/watch?v=OwZHNH8EfSU](https://www.youtube.com/watch?v=OwZHNH8EfSU) | [Azure Architecture Center — AI](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/) · [AWS AI/ML service overview](https://aws.amazon.com/machine-learning/) | Deploy churn model to Azure ML managed online endpoint with Swagger docs | Deployed endpoint URL, cloud service-mapping table (Azure/AWS/GCP), ARM template | 15 | Endpoint returns prediction in < 300 ms; can map SageMaker Endpoints ↔ Azure ML endpoints ↔ Vertex AI endpoints |
| 8 | Architecture Trade-offs & Non-Functional Requirements | Write an architecture decision record; evaluate build vs buy | NFRs (availability, latency, throughput, cost, security, maintainability), CAP theorem applied to ML, DR patterns, blue-green vs canary deployments, build vs buy framework | *Software Architecture: The Hard Parts* – Ford et al. (O'Reilly book) Ch 1–2 <br><br>🎬 **Video:** *Software Architecture Fundamentals* – Neal Ford & Mark Richards (O'Reilly Learning) [https://learning.oreilly.com/videos/software-architecture-fundamentals/](https://learning.oreilly.com/videos/software-architecture-fundamentals/9781491998991/) · *Fundamentals of Software Architecture* – O'Reilly Live Training [https://learning.oreilly.com/live-events/fundamentals-of-software-architecture/](https://learning.oreilly.com/live-events/fundamentals-of-software-architecture/0636920458951/)| [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/) · [AWS Well-Architected ML Lens](https://docs.aws.amazon.com/wellarchitected/latest/machine-learning-lens/) | Write a 2-page architecture proposal for an ERP invoice anomaly detector | Architecture proposal doc, 2 ADRs (model serving strategy, data storage), trade-off table | 13 | Proposal addresses all 5 pillars of WAF; ADR follows standard template; reviewer can challenge any decision |

---

### Phase 2 — GenAI Foundations (Weeks 9–12)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 9 | PyTorch & Transformer Architecture | Implement a small transformer from scratch; explain attention | PyTorch tensors, autograd, training loop, transformer blocks, multi-head attention, positional encoding, layer normalization | *Deep Learning with PyTorch* – Eli Stevens (O'Reilly book) Ch 1–8 <br><br>🎬 **Video:** *Deep Learning with PyTorch Step-by-Step* – Daniel Voigt Godoy (O'Reilly Learning) [https://learning.oreilly.com/videos/deep-learning-with/](https://learning.oreilly.com/videos/deep-learning-with/9781098135867/) · *PyTorch for Deep Learning* – Zero to Mastery (Udemy) [https://www.udemy.com/course/pytorch-for-deep-learning/](https://www.udemy.com/course/pytorch-for-deep-learning/)| [The Illustrated Transformer – Jay Alammar](https://jalammar.github.io/illustrated-transformer/) · [Attention Is All You Need – Vaswani et al. arXiv:1706.03762](https://arxiv.org/abs/1706.03762) | Implement a character-level transformer on a small text corpus | `mini_transformer/` with training loop, loss curve plot, architecture diagram | 14 | Model loss decreases monotonically; can annotate attention matrix visualization |
| 10 | Foundation Models & Model Selection | Select the right model for an enterprise use case; compare OSS vs managed | Model families (GPT-4o, Claude 3.5, Gemini, Llama 3, Mistral, Phi-3), model cards, benchmark reading (MMLU, HumanEval, HELM), context windows, latency/cost/quality matrix, tokenization | *Generative AI with LLMs* – Coursera/DeepLearning.AI (Andrew Ng) [https://www.deeplearning.ai/courses/generative-ai-with-llms/](https://www.deeplearning.ai/courses/generative-ai-with-llms/) weeks 1–2 | [OpenAI model cards](https://platform.openai.com/docs/models) · [Anthropic model overview](https://docs.anthropic.com/en/docs/about-claude/models/overview) · [Hugging Face Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard) | Build a model-selection scorecard for 5 enterprise use cases (ERP summarization, code review, procurement Q&A, incident triage, document extraction) | Model selection scorecard (Excel/Markdown), cost comparison calculator, architecture note | 13 | Scorecard includes latency, cost, context window, fine-tune eligibility; can defend any selection |
| 11 | Prompt Engineering & Structured Outputs | Write production-grade prompts; extract structured JSON from LLMs reliably | Zero/few-shot, chain-of-thought, ReAct, function/tool calling, structured output with Instructor/Pydantic, system prompts, output validation, prompt versioning | *ChatGPT Prompt Engineering for Developers* – DeepLearning.AI (free) [https://learn.deeplearning.ai/courses/chatgpt-prompt-eng-for-devs](https://learn.deeplearning.ai/courses/chatgpt-prompt-eng-for-devs) | [OpenAI Structured Outputs guide](https://platform.openai.com/docs/guides/structured-outputs) · [Instructor library docs](https://python.useinstructor.com) | Build an ERP PO anomaly extraction pipeline that outputs typed Pydantic models from invoice text | `po_extractor/` service with structured JSON output, prompt templates versioned in YAML, test harness | 14 | Extraction accuracy ≥ 90% on 50-item test set; validation rejects malformed outputs automatically |
| 12 | Fine-Tuning, PEFT & Capstone 1 | Apply LoRA fine-tuning; deliver Capstone 1 | Fine-tuning vs RAG decision framework, PEFT/LoRA/QLoRA concepts, Hugging Face PEFT library, quantization (GPTQ/AWQ), when NOT to fine-tune | *Generative AI with LLMs* – DeepLearning.AI weeks 2–3 (continued) | [LoRA paper – Hu et al. arXiv:2106.09685](https://arxiv.org/abs/2106.09685) · [QLoRA paper – Dettmers et al. arXiv:2305.14314](https://arxiv.org/abs/2305.14314) | Fine-tune a small open model (Phi-3-mini or Mistral-7B) on domain-specific Q&A pairs using QLoRA | LoRA adapter checkpoint, before/after eval comparison, **CAPSTONE 1 delivery** | 15 | Fine-tuned model outperforms base on domain eval by ≥ 5%; Capstone 1 repo public on GitHub |

---

### Phase 3 — RAG Systems (Weeks 13–16)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 13 | RAG Fundamentals | Build a basic RAG pipeline end-to-end | Document ingestion (PDF, DOCX, HTML), text parsing, chunking strategies (fixed, semantic, recursive), embedding models, vector store indexing (Chroma, FAISS, pgvector), similarity search, response generation | *LangChain for LLM Application Development* – DeepLearning.AI (free) [https://learn.deeplearning.ai/courses/langchain](https://learn.deeplearning.ai/courses/langchain) | [LangChain docs – RAG](https://python.langchain.com/docs/tutorials/rag/) · [LlamaIndex docs – Getting Started](https://docs.llamaindex.ai/en/stable/) | Build a RAG pipeline over Oracle ERP release notes (public PDFs) using Azure AI Search | `erp_rag/` with ingestion script, indexed vector store, Q&A CLI, source citations | 14 | Retrieves correct source for 8/10 test questions; citations include page/chunk reference |
| 14 | Advanced RAG — Retrieval & Reranking | Improve retrieval precision; implement hybrid search | Hybrid search (BM25 + vector), metadata filtering, HyDE, multi-query retrieval, cross-encoder reranking (Cohere/BGE), Azure AI Search hybrid, lost-in-the-middle mitigation | *Building and Evaluating Advanced RAG* – DeepLearning.AI (free) [https://learn.deeplearning.ai/courses/building-evaluating-advanced-rag](https://learn.deeplearning.ai/courses/building-evaluating-advanced-rag) | [Azure AI Search hybrid search](https://learn.microsoft.com/en-us/azure/search/hybrid-search-overview) · [Cohere Rerank docs](https://docs.cohere.com/docs/rerank-2) | Add hybrid search + reranking to Week 13 pipeline; measure precision@5 before and after | Retrieval precision report, reranking integration, updated architecture diagram | 13 | Precision@5 improves ≥ 10% with reranking; can explain BM25 vs dense retrieval trade-off |
| 15 | RAG Evaluation & Access Control | Measure RAG quality systematically; design access-controlled RAG | RAGAS metrics (faithfulness, answer relevance, context precision/recall), RAGAs library, evaluation dataset creation, golden dataset, hallucination detection, prompt injection defenses for RAG, RBAC over document collections | *LangSmith & LangChain Evaluation* – LangChain docs tutorials <br><br>🎬 **Video:** *LangChain & LangSmith for LLM Apps* – James Briggs (YouTube playlist, free) [https://www.youtube.com/playlist?list=PLIUOU7oqGTLieV9uTIFMm6_4PXg-hlN6G](https://www.youtube.com/playlist?list=PLIUOU7oqGTLieV9uTIFMm6_4PXg-hlN6G)| [RAGAS paper – arXiv:2309.15217](https://arxiv.org/abs/2309.15217) · [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | Run RAGAS evaluation on Week 14 pipeline; add document-level RBAC simulation | RAGAS evaluation report, RBAC design document, prompt injection test results | 14 | RAGAS faithfulness > 0.75; at least 2 injection attacks blocked; RBAC design reviewed |
| 16 | Semantic Caching, Memory & Multimodal | Reduce latency and cost with caching; handle multimodal inputs | Semantic caching (GPTCache/Redis), conversation memory strategies (buffer, summary, entity), multimodal document processing (Azure AI Document Intelligence, GPT-4o Vision), cost and latency benchmarks | [Azure AI Document Intelligence docs](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/) <br><br>🎬 **Video:** *Azure AI Document Intelligence – Hands-On Tutorial* – Microsoft Reactor (YouTube, free) [https://www.youtube.com/watch?v=WggANPc0bEI](https://www.youtube.com/watch?v=WggANPc0bEI) · Azure AI Skills (LinkedIn Learning) [https://www.linkedin.com/learning/topics/azure-ai](https://www.linkedin.com/learning/topics/azure-ai)| [GPTCache GitHub](https://github.com/zilliztech/GPTCache) · [LlamaIndex multimodal guide](https://docs.llamaindex.ai/en/stable/use_cases/multimodal/) | Add semantic caching to RAG service; process a multimodal invoice (PDF + image); measure latency reduction | Cache hit-rate report, multimodal ingestion demo, **CAPSTONE 2 begins** | 14 | Cache reduces repeat-query latency by ≥ 40%; multimodal extraction matches manual labels on 10/10 test invoices |

---

### Phase 4 — Agentic AI (Weeks 17–20)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 17 | Agent Fundamentals & LangGraph | Build a stateful single agent; explain when agents are appropriate | Agent loop (perceive-plan-act), tool use, function calling, ReAct pattern, LangGraph basics (nodes, edges, state, compile), when NOT to use agents | *AI Agents in LangGraph* – DeepLearning.AI (free) [https://learn.deeplearning.ai/courses/ai-agents-in-langgraph](https://learn.deeplearning.ai/courses/ai-agents-in-langgraph) | [LangGraph docs](https://langchain-ai.github.io/langgraph/) · [ReAct paper – arXiv:2210.03629](https://arxiv.org/abs/2210.03629) | Build a service-request triage agent with 3 tools (ticket lookup, KB search, escalation) | `triage_agent/` LangGraph graph, tool definitions, state schema, unit tests | 14 | Agent correctly routes 8/10 test scenarios; state is serializable; tools are individually testable |
| 18 | Planning, Memory & Human-in-the-Loop | Implement checkpointing and human approval steps | Planning strategies (ToT, Plan-and-Execute), LangGraph checkpointers (SQLite, Redis), human-in-the-loop interrupts, idempotency patterns, failure recovery, audit logging | *LangGraph advanced tutorials* – LangChain docs <br><br>🎬 **Video:** *LangGraph: Build Stateful AI Agents* – LangChain official tutorials (YouTube, free) [https://www.youtube.com/playlist?list=PLfaIDFEXuae16n2TWUkKq5PgJ0w6Pkwtg](https://www.youtube.com/playlist?list=PLfaIDFEXuae16n2TWUkKq5PgJ0w6Pkwtg)| [LangGraph persistence docs](https://langchain-ai.github.io/langgraph/concepts/persistence/) · [Human-in-the-loop patterns](https://langchain-ai.github.io/langgraph/concepts/human_in_the_loop/) | Add SQLite checkpointer + human approval interrupt to triage agent; simulate a mid-task failure and recover | Checkpoint demo, recovery test, human-approval flow video/GIF, audit log sample | 13 | Agent resumes correctly after simulated crash; human approval blocks execution until confirmed |
| 19 | Multi-Agent Patterns & MCP | Design a multi-agent system; integrate an MCP tool server | Supervisor pattern, hierarchical agents, handoff protocols, shared vs isolated memory, MCP architecture, MCP tool server setup (Python SDK), security considerations for MCP | *Multi-Agent Systems* – LangGraph docs tutorials <br><br>🎬 **Video:** *Multi-Agent Systems with AutoGen & CrewAI* – DeepLearning.AI *Multi AI Agent Systems with crewAI* (free) [https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai)| [Model Context Protocol spec](https://modelcontextprotocol.io/docs) · [Anthropic MCP blog](https://www.anthropic.com/news/model-context-protocol) | Build a 3-agent procurement workflow (intake → approval → fulfillment) with an MCP tool server for ERP lookup | Multi-agent graph diagram, MCP server code, integration test suite | 14 | Each agent has a defined responsibility boundary; MCP tool server returns typed responses; end-to-end test passes |
| 20 | Guardrails, Evaluation & Capstone 2 | Implement production guardrails; deliver Capstone 2 | Guardrails AI / NVIDIA NeMo Guardrails, output validation, PII detection, content safety (Azure AI Content Safety), agent evaluation (task completion, tool accuracy, hallucination rate), **CAPSTONE 2 delivery** | [NVIDIA NeMo Guardrails docs](https://github.com/NVIDIA/NeMo-Guardrails) <br><br>🎬 **Video:** *Responsible AI & Guardrails* – DeepLearning.AI *Quality and Safety for LLM Applications* (free) [https://learn.deeplearning.ai/courses/quality-safety-llm-applications](https://learn.deeplearning.ai/courses/quality-safety-llm-applications)| [Guardrails AI docs](https://www.guardrailsai.com/docs) · [AgentBench paper – arXiv:2308.03688](https://arxiv.org/abs/2308.03688) | Add guardrails to Capstone 2 agent; create evaluation dataset (20 scenarios); measure task-completion rate | Guardrails config, evaluation report, **CAPSTONE 2 delivery** | 15 | Task-completion rate ≥ 80%; PII leakage = 0 on test set; Capstone 2 repo public on GitHub |

---

### Phase 5 — MLOps/LLMOps (Weeks 21–22)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 21 | MLOps: MLflow, CI/CD/CT, Kubernetes | Build a model CI/CD pipeline; deploy on Kubernetes | MLflow Model Registry, CI/CD/CT pipeline, model promotion gates, Docker → Kubernetes deployment, Helm chart basics, rolling updates, feature-flag deployment, Infrastructure as Code (Bicep/Terraform) | *MLflow in Action* – Mark Ryan (O'Reilly book) Ch 1–6 <br><br>🎬 **Video:** *MLflow: An Introduction* – Databricks (O'Reilly Learning) [https://learning.oreilly.com/videos/mlflow-an-introduction/](https://learning.oreilly.com/videos/mlflow-an-introduction/9781492087250/) · *MLOps Fundamentals* – LinkedIn Learning [https://www.linkedin.com/learning/mlops-foundations](https://www.linkedin.com/learning/mlops-foundations)| [MLflow docs](https://mlflow.org/docs/latest/index.html) · [Azure MLOps accelerator](https://github.com/Azure/mlops-v2) | Extend Capstone 1 with MLflow Model Registry, GitHub Actions CI/CD → AKS deployment | Helm chart, CI/CD pipeline YAML, MLflow model registry screenshot, Bicep IaC template | 14 | Model promotes from Staging → Production only after eval gate passes; deployment rolls back on health-check failure |
| 22 | LLMOps: Monitoring, Observability & Cost | Instrument an LLM application for production observability | Prompt/response logging, latency/cost/token monitoring, drift detection, hallucination monitoring, OpenTelemetry traces for LLM, LangSmith / Azure AI Foundry tracing, alert design, incident response playbook | *LLMOps* – DeepLearning.AI (free) [https://learn.deeplearning.ai/courses/llmops](https://learn.deeplearning.ai/courses/llmops) | [OpenTelemetry for LLMs – OTEL docs](https://opentelemetry.io/docs/zero-code/python/) · [Azure Monitor for AI](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/monitor-applications) | Add OpenTelemetry tracing + cost dashboard to Capstone 2 RAG service | Grafana/Azure Monitor dashboard screenshot, alert rules YAML, cost-per-query metric, incident runbook | 14 | Every LLM call emits trace with token count and latency; cost dashboard shows per-query cost; alert fires on p99 > 2 s |

---

### Phase 6 — Governance, Security & Portfolio Finalization (Weeks 23–24)

| Week | Theme | Learning Objectives | Topics | Primary Video Training | Reading | Hands-On Lab | Deliverable | Hours | Exit Criteria |
|---|---|---|---|---|---|---|---|---|---|
| 23 | Responsible AI, Security & Governance | Threat-model an AI system; complete a Responsible AI assessment | NIST AI RMF map/measure/manage, OWASP LLM Top 10 (prompt injection, insecure output handling, data leakage, model theft, excessive agency), MITRE ATLAS, managed identities, RBAC, private endpoints, PII handling, content safety, ADR governance gates | *AI Security and Privacy* – LinkedIn Learning (Scott Kennedy) [https://www.linkedin.com/learning/ai-security-and-privacy](https://www.linkedin.com/learning/ai-security-and-privacy) | [NIST AI RMF](https://airc.nist.gov/RMF) · [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/) · [MITRE ATLAS](https://atlas.mitre.org) | Threat-model Capstone 2 RAG system using STRIDE; complete NIST AI RMF Map worksheet | Threat model document, NIST AI RMF worksheet, security controls checklist, ADR for identity strategy | 14 | At least 8 STRIDE threats identified with mitigations; NIST AI RMF Map section completed; reviewer cannot find an unaddressed OWASP LLM Top 10 item |
| 24 | Capstone 3, Final Case Study & Interview Prep | Deliver Capstone 3 and architecture case study; pass mock interview | Architecture communication (C4, sequence, DFD, deployment diagrams), executive storytelling, 10-slide deck structure, interview system-design methodology, 30-day post-roadmap plan | *Communicating Architecture* – O'Reilly (selected chapters) <br><br>🎬 **Video:** *Communicating with Executives: Architecture Storytelling* – LinkedIn Learning [https://www.linkedin.com/learning/communication-foundations](https://www.linkedin.com/learning/communication-foundations) · *C4 Model for Software Architecture* – Simon Brown (YouTube, free) [https://www.youtube.com/watch?v=x2-rSnhpw0g](https://www.youtube.com/watch?v=x2-rSnhpw0g)| [C4 model](https://c4model.com) · [arc42 architecture template](https://arc42.org/overview) | Deliver Capstone 3 agentic workflow; complete final architecture case study; pass 90-minute mock interview | **CAPSTONE 3 delivery**, final architecture case study doc + 10-slide deck, mock-interview scorecard | 15 | All 3 capstones public on GitHub; case study addresses all 15+ required sections; mock-interview score ≥ 70% |

---

## Training Catalog

> **Last verified:** 2025-01-01 (Exact URLs and durations should be re-confirmed at provider sites before enrolling. Courses marked ⚠️ VERIFY could not be confirmed at time of authoring and should be verified before enrollment.)

| Phase | Platform | Course/Video Title | Instructor | Level | Duration | Why Selected | Required/Optional | Official URL |
|---|---|---|---|---|---|---|---|---|
| 0 — Foundation | Udemy | Docker Deep Dive | Nigel Poulton | Beginner–Inter. | ≈ 9 h | Most concise Docker course for practitioners; Poulton is widely recognized | Required | https://www.udemy.com/course/docker/ |
| 0 — Foundation | Udemy | Statistics for Data Science and Business Analysis | 365 Careers | Beginner–Inter. | ≈ 5 h | Covers probability, distributions, hypothesis testing without excessive math | Required | https://www.udemy.com/course/statistics-for-data-science-and-business-analysis/ |
| 1 — ML Arch. | YouTube/freeCodeCamp | Microsoft Azure AI Fundamentals AI-900 | Andrew Brown | Beginner | ≈ 3.5 h | Free, up-to-date, covers Azure AI service landscape essential for cloud mapping | Required | https://www.youtube.com/watch?v=OwZHNH8EfSU |
| 2 — GenAI Found. | DeepLearning.AI | Generative AI with LLMs | Andrew Ng / DeepLearning.AI | Intermediate | ≈ 16 h | Covers transformer architecture, fine-tuning, RLHF, PEFT in one structured course | Required | https://www.deeplearning.ai/courses/generative-ai-with-llms/ |
| 2 — GenAI Found. | DeepLearning.AI | ChatGPT Prompt Engineering for Developers | Andrew Ng / Isa Fulford | Intermediate | ≈ 1.5 h | Best concise prompt engineering introduction; free; directly applicable | Required | https://learn.deeplearning.ai/courses/chatgpt-prompt-eng-for-devs |
| 3 — RAG | DeepLearning.AI | LangChain for LLM Application Development | Harrison Chase / Andrew Ng | Intermediate | ≈ 1.5 h | Introduction to LangChain chains and RAG; free; complemented by docs | Required | https://learn.deeplearning.ai/courses/langchain |
| 3 — RAG | DeepLearning.AI | Building and Evaluating Advanced RAG | Jerry Liu / Andrew Ng | Intermediate | ≈ 1.5 h | Covers hybrid retrieval, reranking, RAG evaluation; free | Required | https://learn.deeplearning.ai/courses/building-evaluating-advanced-rag |
| 4 — Agentic AI | DeepLearning.AI | AI Agents in LangGraph | Tavily / Harrison Chase | Intermediate | ≈ 2 h | Hands-on LangGraph agents with tool use, state, and human-in-the-loop; free | Required | https://learn.deeplearning.ai/courses/ai-agents-in-langgraph |
| 5 — LLMOps | DeepLearning.AI | LLMOps | Erwin Huizenga | Intermediate | ≈ 1.5 h | Covers prompt/response logging, versioning, evaluation pipelines; free | Required | https://learn.deeplearning.ai/courses/llmops |
| 6 — Governance | LinkedIn Learning | AI Security and Privacy ⚠️ VERIFY | Scott Kennedy | Intermediate | ≈ 2 h | Covers AI-specific security threats, privacy regulations, governance frameworks | Required | https://www.linkedin.com/learning/ai-security-and-privacy |
| Supplemental | O'Reilly | Designing Machine Learning Systems | Chip Huyen | Advanced | Book (≈ 400 pp) | Definitive ML systems architecture reference; covers all lifecycle phases | Required | https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/ |
| Supplemental | O'Reilly | MLflow in Action | Mark Ryan | Intermediate | Book (≈ 350 pp) | Only comprehensive MLflow book; practical and enterprise-oriented | Required | https://www.oreilly.com/library/view/mlflow-in-action/9781617296628/ |
| Optional | Udemy | The Complete Machine Learning, NLP Bootcamp ⚠️ VERIFY | Lazy Programmer (Eric Lazyprogrammer) | Intermediate | ≈ 20 h | Deep backup if additional ML foundations needed; selective consumption only | Optional | https://www.udemy.com/user/lazy-programmer/ |
| Optional | LinkedIn Learning | Azure Machine Learning ⚠️ VERIFY | Multiple instructors | Intermediate | ≈ 3 h | Supplemental Azure ML coverage if hands-on labs need more guidance | Optional | https://www.linkedin.com/learning/topics/azure-machine-learning |

---

## Reading & Papers Catalog

| Phase | Title | Type | Author/Org | Difficulty | What to Learn | When to Read | URL |
|---|---|---|---|---|---|---|---|
| 0 | FastAPI documentation | Official docs | Sebastián Ramírez | Beginner | Routing, Pydantic integration, dependency injection | Week 1 | https://fastapi.tiangolo.com |
| 0 | The Illustrated Transformer | Blog | Jay Alammar | Intermediate | Visual intuition for attention mechanism | Week 9 | https://jalammar.github.io/illustrated-transformer/ |
| 1 | Designing Machine Learning Systems | Book | Chip Huyen (O'Reilly) | Advanced| Full ML lifecycle, feature stores, training, serving, monitoring | Weeks 5–8 | https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/ |
| 1 | Azure Architecture Center — AI/ML | Architecture guide | Microsoft | Intermediate| Azure AI reference architectures, design patterns | Weeks 7–8 | https://learn.microsoft.com/en-us/azure/architecture/ai-ml/ |
| 1 | AWS Well-Architected ML Lens | Architecture guide | AWS | Intermediate| AWS ML design pillars — comparative study | Week 8 | https://docs.aws.amazon.com/wellarchitected/latest/machine-learning-lens/ |
| 1 | Google Cloud Architecture Center | Architecture guide | Google | Intermediate| GCP AI patterns — comparative study | Week 8 | https://cloud.google.com/architecture |
| 2 | Attention Is All You Need | Paper | Vaswani et al. (arXiv:1706.03762) | Advanced | Original transformer architecture | Week 9 | https://arxiv.org/abs/1706.03762 |
| 2 | LoRA: Low-Rank Adaptation of LLMs | Paper | Hu et al. (arXiv:2106.09685) | Advanced | Parameter-efficient fine-tuning | Week 12 | https://arxiv.org/abs/2106.09685 |
| 2 | QLoRA | Paper | Dettmers et al. (arXiv:2305.14314) | Advanced | Quantized fine-tuning on consumer hardware | Week 12 | https://arxiv.org/abs/2305.14314 |
| 3 | RAGAS: Automated Evaluation of RAG | Paper | Es et al. (arXiv:2309.15217) | Intermediate | RAG evaluation metrics: faithfulness, relevance, recall | Week 15 | https://arxiv.org/abs/2309.15217 |
| 3 | LangChain RAG tutorial | Official docs | LangChain | Intermediate | End-to-end RAG pipeline with LCEL | Week 13 | https://python.langchain.com/docs/tutorials/rag/ |
| 3 | LlamaIndex documentation | Official docs | LlamaIndex | Intermediate | Alternative RAG framework; multimodal support | Week 13–16 | https://docs.llamaindex.ai/en/stable/ |
| 4 | ReAct: Synergizing Reasoning and Acting | Paper | Yao et al. (arXiv:2210.03629) | Intermediate | Foundation of ReAct agent pattern | Week 17 | https://arxiv.org/abs/2210.03629 |
| 4 | LangGraph documentation | Official docs | LangChain | Intermediate | Graph-based agent orchestration | Week 17–20 | https://langchain-ai.github.io/langgraph/ |
| 4 | Model Context Protocol specification | Official docs | Anthropic | Intermediate | MCP protocol design and tool server implementation | Week 19 | https://modelcontextprotocol.io/docs |
| 4 | AgentBench | Paper | Liu et al. (arXiv:2308.03688) | Advanced | Agent evaluation methodology | Week 20 | https://arxiv.org/abs/2308.03688 |
| 5 | MLflow documentation | Official docs | MLflow/Databricks | Intermediate| Experiment tracking, model registry, serving | Week 21 | https://mlflow.org/docs/latest/index.html |
| 5 | Azure MLOps v2 accelerator | Reference impl. | Microsoft | Advanced| Production MLOps on Azure reference architecture | Week 21 | https://github.com/Azure/mlops-v2 |
| 6 | NIST AI Risk Management Framework | Standard | NIST | Intermediate| Govern/Map/Measure/Manage AI risk lifecycle | Week 23 | https://airc.nist.gov/RMF |
| 6 | OWASP Top 10 for LLM Applications | Standard | OWASP | Intermediate| Top LLM security risks and mitigations | Week 15, 23 | https://owasp.org/www-project-top-10-for-large-language-model-applications/ |
| 6 | MITRE ATLAS | Framework | MITRE | Advanced| Adversarial ML threat taxonomy | Week 23 | https://atlas.mitre.org |
| 6 | C4 model | Architecture guide | Simon Brown | Beginner| Architecture diagramming standard | Week 24 | https://c4model.com |

> **Guiding questions per key paper:**
> - **Attention Is All You Need:** (1) What problem does attention solve vs RNNs? (2) How is multi-head attention different from single-head? (3) What would break if you removed positional encoding?
> - **RAGAS:** (1) How does faithfulness differ from answer relevance? (2) Why does context recall matter more than precision for open-domain Q&A? (3) How do you create a golden evaluation dataset without ground-truth labels?
> - **OWASP LLM Top 10:** (1) How does prompt injection differ from SQL injection in terms of mitigations? (2) What architectural controls can prevent excessive agency? (3) How does insecure output handling manifest in a RAG pipeline?

---

## Capstone Portfolio

### Capstone 1 — Production ML Solution (Week 12 delivery)

| Item | Details |
|---|---|
| Business problem | Enterprise procurement anomaly detection: identify fraudulent or erroneous purchase orders using historical ERP transaction data |
| Target users | Accounts payable managers, internal audit, procurement controllers |
| Functional scope | Ingest PO line-item data → validate schema → train gradient-boosted classifier → expose REST API → monitor for drift |
| Architecture | FastAPI inference API → Azure ML managed endpoint → MLflow Model Registry → Azure Monitor; batch scoring via Azure ML pipelines |
| Technology stack | Python, scikit-learn, XGBoost, MLflow, FastAPI, Docker, GitHub Actions, Azure ML, Azure Monitor |
| Suggested datasets | [UCI Fraud Detection Dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients) or synthetic ERP PO data generated with Faker |
| Implementation milestones | M1: EDA + baseline model (W3) → M2: Pipeline + MLflow (W5) → M3: API + Docker (W2) → M4: AML deploy + CI/CD (W7) → M5: Final delivery (W12) |
| Evaluation metrics | AUC-ROC, Precision@top-k, F1, calibration error, inference p99 latency |
| Security controls | Azure Managed Identity for endpoint auth, no hardcoded secrets, input validation with Pydantic |
| Required documentation | Architecture diagram (C4 context + container), ADR for model selection, MLflow experiment README, deployment runbook |
| GitHub repo structure | `capstone1-ml-solution/` → `src/`, `tests/`, `notebooks/`, `infra/`, `docs/`, `mlflow/`, `.github/` |
| Demonstration scenario | "Here is a CSV of 100 POs — which ones should I review?" Live API call with Swagger UI |
| Stretch goals | Add SHAP explanations API, A/B testing endpoint, automated retraining trigger on drift |
| Estimated effort | 15–20 hours across Weeks 3–12 (distributed) |
| Portfolio/interview value | Demonstrates full ML lifecycle, cloud deployment, MLOps fundamentals, and enterprise domain expertise |

---

### Capstone 2 — Enterprise RAG Assistant (Week 20 delivery)

| Item | Details |
|---|---|
| Business problem | Oracle ERP Knowledge Assistant: allow procurement and finance staff to query ERP documentation, release notes, and policy documents in natural language |
| Target users | ERP end users, support analysts, procurement officers |
| Functional scope | Ingest multi-format docs (PDF, DOCX, HTML) → chunk and index → hybrid retrieval → rerank → generate cited responses → access control → monitoring |
| Architecture | Azure AI Search (hybrid) → Azure OpenAI (GPT-4o) → FastAPI → Azure Container Apps; LangSmith for tracing |
| Technology stack | Python, LangChain/LlamaIndex, Azure AI Search, Azure OpenAI, Azure AI Document Intelligence, RAGAS, Pydantic, FastAPI, Docker |
| Suggested datasets | Oracle ERP public documentation PDFs, Oracle E-Business Suite release notes (freely available), IT policy documents (synthetic) |
| Implementation milestones | M1: Ingestion pipeline (W13) → M2: Hybrid retrieval (W14) → M3: Evaluation dataset (W15) → M4: Access control + guardrails (W15–W16) → M5: Delivery (W20) |
| Evaluation metrics | RAGAS faithfulness ≥ 0.80, context precision ≥ 0.70, answer relevance ≥ 0.80, p99 latency < 3 s, cost per query < $0.01 |
| Security controls | Azure AD RBAC, managed identity for Azure OpenAI, prompt injection defenses, PII detection (Presidio), content safety filter |
| Required documentation | C4 diagrams (all levels), data flow diagram, threat model, RAGAS evaluation report, cost model, ADRs (3+) |
| GitHub repo structure | `capstone2-rag-assistant/` → `ingestion/`, `retrieval/`, `generation/`, `evaluation/`, `api/`, `infra/`, `docs/`, `security/` |
| Demonstration scenario | "What are the period-end closing steps in Oracle R12 GL?" → cited, structured response with source documents |
| Stretch goals | Add citation UI with document preview, fine-tuned embedding model, automated nightly evaluation |
| Estimated effort | 20–25 hours across Weeks 13–20 |
| Portfolio/interview value | Demonstrates advanced RAG, enterprise integration, security-conscious design, evaluation methodology, and Oracle domain expertise |

---

### Capstone 3 — Agentic Workflow (Week 24 delivery)

| Item | Details |
|---|---|
| Business problem | Automated IT service-request fulfillment: an agent triages incoming IT tickets, queries the knowledge base, creates Jira-style tickets, routes for approval, and updates the requester |
| Target users | IT service desk, end users, IT managers |
| Functional scope | Classify request → search KB → assess automated resolution → escalate or auto-resolve → human approval gate → update ticketing system → notify user → audit log |
| Architecture | LangGraph multi-agent (classifier → resolver → approver → notifier) → MCP tool servers (KB, ticket system, email) → SQLite checkpointer → Prometheus metrics |
| Technology stack | Python, LangGraph, MCP Python SDK, FastAPI, SQLite, Prometheus, Grafana (or Azure Monitor), NVIDIA NeMo Guardrails |
| Suggested datasets | [SNOW IT Ticket dataset (Kaggle)](https://www.kaggle.com) or synthetic IT ticket data generated with Faker |
| Implementation milestones | M1: Single triage agent (W17) → M2: Checkpointing + human approval (W18) → M3: Multi-agent + MCP (W19) → M4: Guardrails + evaluation (W20) → M5: Delivery (W24) |
| Evaluation metrics | Task-completion rate ≥ 80%, PII leakage = 0, mean resolution time, false-escalation rate < 20%, audit log completeness 100% |
| Security controls | RBAC per agent role, MCP server input validation, guardrails on output, no PII in logs, idempotent tool calls |
| Required documentation | Agent graph diagram, state schema, tool interface specs, guardrails config, evaluation report, incident runbook, ADRs (2+) |
| GitHub repo structure | `capstone3-agentic-workflow/` → `agents/`, `tools/`, `mcp_servers/`, `evaluation/`, `infra/`, `docs/` |
| Demonstration scenario | "New request: 'My VPN is not connecting from home. User: john.doe@company.com Priority: High'" → live agent run with approval interrupt |
| Stretch goals | Add voice input (Azure Speech), Slack integration, self-improving KB via approved resolutions |
| Estimated effort | 20–25 hours across Weeks 17–24 |
| Portfolio/interview value | Demonstrates agentic architecture, multi-agent orchestration, MCP, human-in-the-loop, audit/governance, and production reliability patterns |

---

### Final Architecture Case Study (Week 24)

An interview-ready proposal for an **Enterprise Procurement Intelligence Platform** combining classical ML (anomaly detection), RAG (policy assistant), and agentic AI (approval workflow) on Azure.

**Required sections:**
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

| Milestone | Competencies Demonstrated | Evidence/Artifacts | Assessment Method | Pass Criteria | Recovery Plan |
|---|---|---|---|---|---|
| **Week 2** | Python production, containers, CI | FastAPI service + Docker + GitHub Actions pipeline | Self-review against checklist; share with peer | CI pipeline green; coverage ≥ 80%; image < 500 MB | Add 1 extra hour/day for 3 days; focus only on failing criteria |
| **Week 4** | Dev tooling, embeddings, statistics | Embedding visualization, nearest-neighbor demo | Demonstrate to a colleague who asks 3 questions | Can explain clustering; Git history is clean | Revisit Statistics course sections; re-do embedding lab |
| **Week 8** | ML lifecycle, cloud deployment, architecture | Deployed AML endpoint, ADRs, architecture proposal | Mock design review — 20-minute presentation | All 5 WAF pillars addressed; endpoint live; ADR explains trade-off | Re-read Chip Huyen Ch 1–4; add missing NFRs |
| **Week 12** | GenAI foundations, fine-tuning, Capstone 1 | Capstone 1 GitHub repo + MLflow experiments | Code review + 10-minute demo | Fine-tuned model outperforms base ≥ 5%; all tests pass | Extend Week 12 by 1 week; drop LoRA stretch goals |
| **Week 16** | Full RAG pipeline, evaluation, access control | RAGAS report, hybrid search demo, RBAC design | Architecture walkthrough + Q&A (30 min) | RAGAS faithfulness > 0.75; injection attacks blocked; reviewer cannot break RBAC logic | Re-do retrieval lab; focus on weakest RAGAS metric |
| **Week 20** | Agentic AI, multi-agent, MCP, Capstone 2 | Capstone 2 GitHub repo + evaluation report + agent graph | 30-minute live demo + architecture Q&A | Task-completion ≥ 80%; PII = 0; Capstone 2 public | Drop stretch goals; fix core evaluation failures first |
| **Week 24** | Full stack AI architecture, governance, interview readiness | All 3 capstones + case study + mock interview score | 90-minute mock interview with peer or mentor | Mock interview score ≥ 70%; case study covers all 15 required sections | Add 2-week buffer; prioritize case study over capstone polish |

---

## Skills Matrix

| Skill Domain | Starting Level | Target Level (Week 24) | Evidence Required | Assessment Week |
|---|---|---|---|---|
| Python / Software Engineering | 3 | 5 | Typed, tested, packaged production service; CI/CD pipeline | W2, W12 |
| ML System Design | 2 | 4 | Architecture proposal; ADRs; deployed ML endpoint | W8, W12 |
| Deep Learning & Transformers | 1 | 3 | Mini transformer implementation; fine-tuned LoRA adapter | W9, W12 |
| Cloud AI Services (Azure primary) | 2 | 4 | AML deployment; Azure AI Search integration; Azure Monitor dashboard | W7, W22 |
| RAG Architecture | 1 | 5 | Advanced RAG pipeline; RAGAS evaluation report; Capstone 2 | W16, W20 |
| Agentic AI | 1 | 4 | LangGraph multi-agent; MCP tool server; Capstone 3 | W20, W24 |
| MLOps / LLMOps | 2 | 4 | MLflow CI/CD; Kubernetes deployment; OpenTelemetry tracing | W21, W22 |
| Data Architecture | 3 | 4 | Medallion pipeline; feature pipeline; data contracts | W6 |
| API & Integration Architecture | 4 | 5 | FastAPI services; MCP servers; Azure integration patterns | W1, W19 |
| Security | 2 | 4 | Threat model; RBAC design; OWASP LLM mitigations | W15, W23 |
| Responsible AI & Governance | 1 | 4 | NIST AI RMF worksheet; Responsible AI assessment; ADRs | W23 |
| Observability & Reliability | 2 | 4 | OpenTelemetry traces; cost dashboard; alert rules | W22 |
| Cost Optimization | 2 | 4 | Cost model in case study; per-query cost metric | W22, W24 |
| Architecture Documentation | 3 | 5 | C4 diagrams; ADRs; executive summary; 10-slide deck | W8, W24 |
| Stakeholder Communication | 3 | 5 | 10-minute demos; executive summary; mock interview | W8, W20, W24 |

> **Scale:** 1 = No knowledge · 2 = Awareness · 3 = Practical experience · 4 = Advanced practitioner · 5 = Expert / can design for others

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

| Certification | Worth Pursuing? | Prerequisites | Best Timing | Effort | Overlap with Roadmap | Portfolio vs Cert? |
|---|---|---|---|---|---|---|
| **Microsoft AI-900** (Azure AI Fundamentals) | ✅ Yes — signals Azure commitment; easy win | None | Week 7–8 | 10–15 h | Directly maps to Week 7 | Take it; low effort |
| **Microsoft AI-102** (Azure AI Engineer Associate) | ✅ Yes — most relevant cert for this role | AI-900, Python basics | After Week 16 | 40–60 h | Covers Azure OpenAI, AI Search, Document Intelligence | Prioritize after Capstone 2 |
| **AWS ML Specialty** | ⚠️ Conditional — if targeting AWS roles | AWS practitioner-level | After Week 24 | 60–80 h | Partial overlap (SageMaker, Rekognition) | Portfolio first |
| **Google Professional ML Engineer** | ⚠️ Conditional — if targeting GCP roles | GCP Associate | After Week 24 | 60–80 h | Partial overlap | Portfolio first |
| **Databricks Generative AI Engineer Associate** | ✅ Yes — Databricks is ubiquitous in enterprise | Spark basics | After Week 22 | 20–30 h | MLflow, Lakehouse, GenAI | Worthwhile if Databricks is in target stack |
| **NVIDIA AI Infrastructure and Operations** | ⚠️ Optional | GPU basics | Post-roadmap | 20 h | Low overlap | Skip unless targeting GPU-heavy roles |

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

### 10 Behavioral Questions for Enterprise Technologists Transitioning to AI Architecture

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

### Architecture Trade-off Answer Method (TRADED Framework)

**T**rade-off — name the competing dimensions (cost vs latency, accuracy vs speed, build vs buy)  
**R**equirements — anchor to stated NFRs and business context  
**A**lternatives — present 2–3 options with pros and cons  
**D**ecision — state your recommended choice  
**E**vidence — cite a benchmark, case study, or first-principles reasoning  
**D**ependencies — flag prerequisites, risks, and reversibility

### 30-Day Post-Week-24 Interview Preparation Routine

| Week | Focus |
|---|---|
| 1 | Polish all 3 GitHub repos; write 1-page README for each |
| 2 | Mock system design (2 sessions); refine case study doc |
| 3 | Behavioral interview prep (STAR stories for 10 behavioral questions) |
| 4 | Active applications; LinkedIn outreach; 2 informational interviews |

### Resume & LinkedIn Positioning

- **Title:** "Senior Software Engineer → AI Solutions Architect (in transition)" or "Enterprise AI Solutions Architect"
- **Summary:** Lead with Oracle/ERP + integration depth, then highlight AI upskilling trajectory and GitHub portfolio
- **Key skills section:** Python, LangChain, LangGraph, Azure OpenAI, RAG, MLOps, MLflow, Docker, Kubernetes, Oracle E-Business Suite, REST APIs, Enterprise Integration
- **Projects section:** Link directly to Capstone 1, 2, 3 GitHub repos with 1-line descriptions
- **Transferable experience framing:** "Designed and delivered enterprise integrations serving 10,000+ users → AI architecture for enterprise-scale LLM applications"; "Oracle ERP data model expertise → structured data extraction and document intelligence"

---

## Progress Tracking Templates

### Weekly Scorecard

```markdown
## Week [N] Scorecard — [Date Range]

### Hours Log
| Activity | Planned | Actual |
|---|---|---|
| Video learning | | |
| Reading | | |
| Hands-on lab | | |
| Architecture/documentation | | |
| **Total** | | |

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
| | | |
```

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

### Project Decision Log Template

```markdown
## Decision Log — [Project Name]

| ID | Date | Decision | Context | Alternatives Considered | Rationale | Consequences |
|---|---|---|---|---|---|---|
| D001 | | | | | | |
```

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
| | | |

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

### Monthly Retrospective Template

```markdown
## Monthly Retrospective — Month [N] ([Date])

### Progress vs Plan
| Week | Planned Deliverable | Actual | Delta | Reason |
|---|---|---|---|---|
| | | | | |

### Skills Assessment (self-rate 1–5)
| Skill | Start of Month | End of Month | Evidence |
|---|---|---|---|
| | | | |

### Top 3 wins this month
1.
2.
3.

### Top 3 things to improve next month
1.
2.
3.

### Portfolio status
| Capstone | Status | GitHub URL | % Complete |
|---|---|---|---|
| Capstone 1 | | | |
| Capstone 2 | | | |
| Capstone 3 | | | |

### Hours dashboard
- Planned total this month: 48–60 h
- Actual total: __ h
- Variance: __ h
- Primary cause:
```

### Dashboard Tracker

```markdown
## AI Solutions Architect — 24-Week Dashboard

| Week | Planned Hours | Actual Hours | Courses Completed | Labs Done | GitHub Commits | Architecture Artifacts | Assessment Score | Blockers |
|---|---|---|---|---|---|---|---|---|
| 1 | 13 | | |
| 2 | 13 | | | | | | | |
| ... | | | | | | | | |
| 24 | 15 | | |
| **Total** | **312–360** | | | | | | | |
```

---

## Week 1 Action Checklist

Complete these in the **next 48 hours**:

### Immediate Setup (Day 1–2)
- [ ] Install Python 3.12, uv, pyenv, Git, Docker Desktop, VS Code
- [ ] Create GitHub account / organization: `github.com/[yourusername]/ai-architect-journey`
- [ ] Create the master repository: `ai-architect-journey` with README and project board
- [ ] Create sub-repositories: `capstone1-ml-solution`, `capstone2-rag-assistant`, `capstone3-agentic-workflow`
- [ ] Set up Azure free account: https://azure.microsoft.com/en-us/free/
- [ ] Sign up for DeepLearning.AI (free): https://learn.deeplearning.ai
- [ ] Sign up for O'Reilly Learning (Qualcomm may provide access — check IT portal)
- [ ] Start *ChatGPT Prompt Engineering for Developers* (1.5 h — do this first to get inspired)

### First Architecture Exercise (Day 2–3)
Draw a simple architecture diagram for a **"Oracle ERP Invoice Q&A bot"** using only boxes and arrows. No code needed. Answer:
1. Where does data come from?
2. How does the user ask a question?
3. How does the system find the answer?
4. Where is the answer generated?
5. What could go wrong?

This is your starting point. By Week 24, you will design this system properly with C4 diagrams, threat models, ADRs, and a cost model.

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
> You pass Week 2 when: `gh actions view` shows a green CI run, `docker pull` succeeds for your image, and you can answer "What is a multi-stage Docker build and why does it reduce image size?" in 60 seconds without notes.

---

## Post-Roadmap Backlog (Lower Priority — Tackle After Week 24)

The following topics strengthen the profile further but are deferred to keep the 24-week plan achievable:

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
- [Deeplearning.AI free short courses](https://learn.deeplearning.ai)
