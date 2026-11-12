# Generative AI Foundations — Mindmap

> Visual map of the **154 topics** in the [GenAI reference](../genai/genai-index.md), grouped into 15 categories.

## Mindmap

```mermaid
mindmap
  root((Generative AI Foundations))
    1 GenAI Foundations
      Landscape and Limitations
      Generative vs Discriminative
      Probability and Sampling
      Information Theory
      Representation Learning
      Self-Supervised Learning
      Foundation Models
      Solution Lifecycle
      Use-Case Selection
    2 Deep Generative Models
      Neural Network Refresh
      Optimization Refresh
      Autoencoders
      VAE
      GANs
      GAN Stability
      Autoregressive Models
      Diffusion
      Latent Diffusion
      Model Comparison
    3 NLP Attention Transformers
      NLP Representations
      RNN LSTM GRU
      Attention
      Query Key Value
      Self-Attention and Masking
      Multi-Head Attention
      Positional Encoding
      Transformer Block
      Encoder and Decoder Models
      Complexity and Scaling
    4 LLM Foundations
      Tokenization
      Next-Token Prediction
      Pretraining Objectives
      Pretraining Pipeline
      Scaling Laws
      Context Windows
      Decoding and Sampling
      KV Cache
      Model Families
      Managed vs Open
      LLM Limitations
    5 Prompt and Context Engineering
      Prompt Anatomy
      Few-Shot
      Prompt Patterns
      Reasoning Patterns
      Structured Outputs
      Function Calling
      Context Engineering
      Prompt Versioning
      Prompt Evaluation
      Injection Foundations
    6 Embeddings and Semantic Search
      Embedding Foundations
      Embedding Models
      Similarity and Distance
      Chunking
      Vector Search
      HNSW and IVF
      Vector Databases
      Sparse Dense Hybrid
      Reranking
      Retrieval Metrics
    7 RAG Foundations
      RAG Overview
      Ingestion
      Query Pipeline
      Metadata and Authorization
      Grounded Prompting
      Citations and Provenance
      Answerability
      RAG Evaluation
      Advanced RAG
      RAG Security
    8 Multimodal GenAI
      Multimodal Foundations
      Vision-Language Models
      Image Generation
      Document AI
      Speech and Audio
      Video
      Multimodal Prompting
      Multimodal RAG
      Multimodal Evaluation
      Multimodal Safety
    9 Adaptation and Fine-Tuning
      Prompt vs RAG vs Fine-Tune
      Training Data Preparation
      SFT
      PEFT and LoRA
      QLoRA
      Preference Alignment
      Domain Adaptation
      Fine-Tuning Evaluation
      Fine-Tuning Infrastructure
    10 Application Engineering
      LLM API Engineering
      Async Concurrency
      Retries and Resilience
      Streaming
      Tool Use
      Workflow Orchestration
      MCP
      Agent Foundations
      Human-in-the-Loop
      GenAI API Design
      Caching
      Model Routing
    11 Evaluation and Testing
      Evaluation Strategy
      Golden Datasets
      Deterministic Evaluation
      Semantic Evaluation
      LLM-as-Judge
      Human Evaluation
      Evaluation Tools
      Online Evaluation
      Statistical Confidence
      Regression Testing
      Red Teaming
    12 Safety Security Governance
      Threat Modeling
      Prompt Injection
      Data Exfiltration
      Output Validation
      Tool Security
      Content Safety
      Privacy
      Supply Chain
      Responsible AI
      GenAI Governance
      Security Incident Response
    13 Production and LLMOps
      Observability
      OpenTelemetry
      Registries
      GenAI CI/CD
      Deployment Strategies
      Drift and Regression
      Inference Performance
      Quantization and Serving
      Capacity and Cost
      Production Debugging
      SLO and SLA
      Disaster Recovery
    14 Enterprise GenAI Architecture
      Reference Architecture
      Model Gateway
      Enterprise Data Integration
      Identity and Authorization
      Multi-Tenant GenAI
      Cloud Hybrid On-Prem
      Platform Operating Model
      Vendor Selection
      Cost Governance
      System Design
    15 Capstones and Interviews
      Enterprise Knowledge Assistant
      Document Intelligence
      Human-Approved Workflow
      Evaluation Harness
      Secure Governed Architecture
      System-Design Interviews
      Interview Bank
```

## Category Breakdown

| # | Category | Topics | Level | Est. Time |
|---|---|---|---|---|
| 1 | Generative AI Foundations | 01–09 | Foundational | 54–90 h |
| 2 | Neural and Deep Generative Foundations | 10–19 | Foundational | 60–100 h |
| 3 | NLP, Attention and Transformer Foundations | 20–31 | Foundational | 72–120 h |
| 4 | LLM Foundations | 32–42 | Foundational | 66–110 h |
| 5 | Prompt and Context Engineering Foundations | 43–52 | Intermediate | 60–100 h |
| 6 | Embeddings and Semantic Search Foundations | 53–62 | Intermediate | 60–100 h |
| 7 | RAG Foundations | 63–72 | Intermediate | 60–100 h |
| 8 | Multimodal Generative AI | 73–82 | Intermediate | 60–100 h |
| 9 | Model Adaptation and Fine-Tuning Foundations | 83–91 | Intermediate | 54–90 h |
| 10 | GenAI Application Engineering | 92–103 | Intermediate | 72–120 h |
| 11 | Evaluation and Testing | 104–114 | Advanced | 66–110 h |
| 12 | Safety, Security, Responsible AI and Governance | 115–125 | Advanced | 66–110 h |
| 13 | Production GenAI and LLMOps Foundations | 126–137 | Advanced | 72–120 h |
| 14 | Enterprise GenAI Architecture | 138–147 | Architecture | 60–100 h |
| 15 | Capstones and Interview Preparation | 148–154 | Architecture | 42–70 h |

> Each topic lives at `../genai/NNN-<slug>.md`; the full per-topic list with links is in the [GenAI index](../genai/genai-index.md#repository-file-map).

## Learning Path

```mermaid
flowchart TD
    A[GenAI foundations] --> B[Deep generative models]
    B --> C[Attention and Transformers]
    C --> D[LLM foundations]
    D --> E[Prompt and context]
    E --> F[Embeddings and semantic search]
    F --> G[RAG]
    G --> H[Multimodal]
    H --> I[Fine-tuning and adaptation]
    I --> J[Application engineering]
    J --> K[Evaluation]
    K --> L[Security and Responsible AI]
    L --> M[Production and LLMOps]
    M --> N[Enterprise architecture]
    N --> O[Capstones]
```

## Generative Model Families

```mermaid
mindmap
  root((Generative Model Families))
    Autoregressive
      Next-token prediction
      LLMs
      Sequential generation
    VAE
      Latent probabilistic model
      Reparameterization trick
      KL regularization
    GAN
      Adversarial training
      Sharp samples
      Mode collapse risk
    Diffusion
      Noise schedule
      Iterative denoising
      Latent diffusion
```

## Technique Selection Map

```mermaid
mindmap
  root((Technique Choices))
    Traditional ML vs GenAI
      Bounded prediction
      Generation and transformation
    Managed vs Self-hosted
      Time to market
      Privacy and control
    Prompt vs RAG vs Fine-tune
      Instruction gap
      Evidence gap
      Adaptation gap
    Long context vs Retrieval
      Modest context
      Large changing corpus
    Structured vs Free text
      Downstream automation
      Human-facing creative
    Workflow vs Agent
      Known path
      Observation-driven
    Single vs Multimodal
      One modality enough
      Evidence spans modalities
    Full FT vs LoRA
      Full adaptation
      Efficient adapters
```

## GenAI Math Cheat Sheet

```mermaid
mindmap
  root((GenAI Math))
    Likelihood
      Negative log-likelihood loss
    Softmax
      Logits to distribution
    Cross-entropy
      Penalizes low target probability
    KL divergence
      VAEs
      Alignment regularization
    Embeddings
      Semantic vectors
    Cosine similarity
      Retrieval
    Attention
      softmax QK over sqrt dk times V
    Sampling
      Temperature
      Top-k
      Top-p
```

## Reference Architectures

```mermaid
mindmap
  root((Reference Architectures))
    Enterprise copilot
      Identity gateway
      Policy and context
      Model gateway
      Authorized RAG
      Validation
    Production RAG assistant
      Versioned ingestion
      Hybrid retrieval
      Rerank
      Citation verification
    Document intelligence
      OCR layout tables
      Multimodal model
      Schema validation
      Exception review
    Multimodal assistant
      Modality processors
      Grounded response
      Provenance
    Human-approved workflow
      State machine
      Authorization
      Human approval
      Audit
    Managed multi-model API
      Model gateway
      Router
      Cost controls
    Self-hosted GenAI platform
      Scheduler
      GPU pool
      Cache
      Registry and rollback
```

## Study Schedules

```mermaid
mindmap
  root((Study Schedules))
    18-week intensive
      Weeks 1 to 4 foundations
      Weeks 5 to 9 LLM prompt embeddings RAG
      Weeks 10 to 14 multimodal adaptation apps eval security
      Weeks 15 to 18 production architecture capstones
    32-week balanced
      1 to 2 weeks per category
    48-week part-time
      6 to 10 hours weekly
```
