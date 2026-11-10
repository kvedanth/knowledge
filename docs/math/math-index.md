# Essential Math for AI — Master Reference

A practical reference covering the **15 core math topics** behind modern AI systems, from vectors and matrices to the chain rule, information theory, and optimizer design. Each topic links the math to **architectural decisions**: memory budgets, training stability, compression, evaluation rigor, and serving capacity.

---

## How to Use This Reference

Each file follows a consistent structure:

| Section | Purpose |
|---|---|
| **Overview** | Concept summary table and where it shows up in AI |
| **Why It Matters** | Mermaid diagram of the concept's role in ML systems |
| **Explanation** | Definitions, formulas, and key properties |
| **Worked Example** | Small hand-computed example you can verify on paper |
| **Diagram** | ASCII / Mermaid intuition |
| **Architectural Relevance** | How the concept drives real system-design decisions |
| **Python Implementation** | NumPy / PyTorch code with **verified output** |
| **Common Mistakes** | Pitfalls and better approaches |
| **Interview Questions** | Beginner → Intermediate → Architect-level Q&A |
| **Key Takeaways** | Concise summary bullets |

---

## Topic Index

### Linear Algebra

| # | Topic | Key Concepts |
|---|---|---|
| 01 | [Vectors and Matrices](01_Vectors%20and%20Matrices.md) | Dot product, norms, cosine similarity, matrix multiplication, transpose, inverse |
| 02 | [Vector Spaces](02_Vector%20Spaces.md) | Span, basis, linear independence, rank, embeddings as vector spaces |
| 03 | [Matrix Decompositions](03_Matrix%20Decompositions.md) | Eigenvalues/eigenvectors, SVD, PCA, low-rank compression, power iteration |
| 04 | [Tensors](04_Tensors.md) | Shapes, broadcasting, `einsum`, attention-shaped tensors, contiguity |

### Calculus

| # | Topic | Key Concepts |
|---|---|---|
| 05 | [Multivariate Calculus](05_Multivariate%20Calculus.md) | Functions of many variables, contours, loss landscapes, conditioning |
| 06 | [Derivatives](06_Derivatives.md) | Partial derivatives, gradients, directional derivatives, gradient checking |
| 07 | [The Chain Rule](07_The%20Chain%20Rule.md) | Backpropagation, autograd engines, vanishing gradients, checkpointing |
| 08 | [Jacobian and Hessian](08_Jacobian%20and%20Hessian.md) | VJP/JVP, curvature, saddle detection, HVPs, learning-rate limits |

### Probability & Statistics

| # | Topic | Key Concepts |
|---|---|---|
| 09 | [Probability Distributions](09_Probability%20Distributions.md) | Gaussian, Bernoulli, Binomial, Poisson; losses as likelihoods, capacity planning |
| 10 | [Bayesian Statistics](10_Bayesian%20Statistics.md) | Bayes' theorem, priors, posteriors, Thompson sampling, uncertainty |
| 11 | [Estimations](11_Estimations.md) | MLE, MAP, NLL losses, regularization as priors |
| 12 | [Information Theory](12_Information%20Theory.md) | Entropy, cross-entropy, KL divergence, perplexity, distillation, drift |

### Optimization Methods

| # | Topic | Key Concepts |
|---|---|---|
| 13 | [Gradient Descent Variants](13_Gradient%20Descent%20Variants.md) | SGD, mini-batch, gradient accumulation, momentum, Nesterov |
| 14 | [Advanced Optimizers](14_Advanced%20Optimizers.md) | AdaGrad, RMSprop, Adam, AdamW, optimizer-state memory |
| 15 | [Optimization Landscapes](15_Optimization%20Landscapes.md) | Convexity, local minima, saddle points, sharp vs flat minima, SAM |

---

## Learning Paths

### Path 1: Foundations (read in order)
Start here if the math is new or rusty.

```
01 → 02 → 04 → 05 → 06 → 07 → 09 → 11 → 13
```

### Path 2: How Training Works
From the loss function to the parameter update.

```
05 → 06 → 07 → 11 → 12 → 13 → 14
```

### Path 3: Training Stability & Scale
Why runs diverge, and how architectures and optimizers prevent it.

```
03 → 07 → 08 → 13 → 14 → 15
```

### Path 4: LLM Architect
The math most directly behind Transformer training, alignment, and serving.

```
01 → 04 → 07 → 12 → 11 → 14 → 08 → 15
```

### Path 5: Evaluation, Uncertainty & Production
Rigorous evals, A/B tests, monitoring, and uncertainty-aware systems.

```
09 → 10 → 11 → 12
```

---

## Quick Reference: Key Formulas

| Concept | Formula | Topic |
|---|---|---|
| Cosine similarity | $\cos\theta = \frac{\mathbf a\cdot\mathbf b}{\lVert\mathbf a\rVert\lVert\mathbf b\rVert}$ | 01 |
| SVD | $A = U\Sigma V^\top$ | 03 |
| Scaled dot-product attention | $\text{softmax}\!\left(\frac{QK^\top}{\sqrt{d_k}}\right)V$ | 04 |
| Gradient descent | $\theta \leftarrow \theta - \eta\nabla_\theta\mathcal L$ | 06, 13 |
| Chain rule | $\frac{\partial\mathcal L}{\partial x} = \frac{\partial\mathcal L}{\partial y}\cdot\frac{\partial y}{\partial x}$ | 07 |
| GD stability limit | $\eta < 2/\lambda_{max}(H)$ | 08 |
| Bayes' theorem | $P(\theta\mid D) \propto P(D\mid\theta)\,P(\theta)$ | 10 |
| MAP objective | $-\log P(D\mid\theta) - \log P(\theta)$ | 11 |
| Cross-entropy / KL | $H(P,Q) = H(P) + D_{KL}(P\Vert Q)$ | 12 |
| Mini-batch noise | $\text{std} \propto 1/\sqrt{B}$ | 13 |
| Adam update | $\theta \leftarrow \theta - \eta\,\hat m/(\sqrt{\hat v} + \epsilon)$ | 14 |

---

## Architect's Cheat Sheet

| Question | Where the math lives |
|---|---|
| How much GPU memory does training need? | Gradients (06), activations (07), optimizer state (14) |
| Why did my training run diverge? | Exploding gradients (07), curvature vs LR (08), Adam settings (14) |
| Can I compress / quantize this model? | Low-rank SVD (03), flat vs sharp minima (15) |
| Is model B really better than model A? | Binomial confidence intervals (09) |
| How do I route traffic between models? | Thompson sampling (10) |
| Which loss should I use? | Choosing a likelihood (09, 11) |
| How do I detect data drift? | KL / PSI (12) |
| How should batch size and LR change with more GPUs? | Mini-batch scaling rules (13) |

---

## Verifying the Code

Every `python` block is followed by its **Output** block. The outputs were produced by running the code (NumPy, SciPy, PyTorch), so the numbers in the text match what you will see. Small differences can appear across library versions or hardware for random-seeded examples.

---

*This reference is for engineers and architects who want to understand the math behind the AI systems they design, train, and deploy.*
