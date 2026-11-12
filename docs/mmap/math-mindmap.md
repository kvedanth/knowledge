# Essential Math for AI — Mindmap

> Visual map of the **15 math topics** in the [Math reference](../math/math-index.md), grouped into 4 categories.

## Mindmap

```mermaid
mindmap
  root((Essential Math for AI))
    Linear Algebra
      Vectors and Matrices
        Dot product and norms
        Cosine similarity
        Matrix multiplication
      Vector Spaces
        Span and basis
        Rank
        Embeddings as vector spaces
      Matrix Decompositions
        Eigenvalues and eigenvectors
        SVD and PCA
        Low-rank compression
      Tensors
        Shapes and broadcasting
        einsum
        Attention-shaped tensors
    Calculus
      Multivariate Calculus
        Loss landscapes
        Conditioning
      Derivatives
        Partial derivatives and gradients
        Gradient checking
      The Chain Rule
        Backpropagation
        Autograd
        Vanishing gradients
      Jacobian and Hessian
        VJP and JVP
        Curvature
        Saddle detection
    Probability and Statistics
      Probability Distributions
        Gaussian and Bernoulli
        Binomial and Poisson
        Losses as likelihoods
      Bayesian Statistics
        Bayes theorem
        Priors and posteriors
        Thompson sampling
      Estimations
        MLE
        MAP
        Regularization as priors
      Information Theory
        Entropy
        Cross-entropy and KL
        Perplexity and drift
    Optimization Methods
      Gradient Descent Variants
        SGD and mini-batch
        Gradient accumulation
        Momentum
      Advanced Optimizers
        AdaGrad and RMSprop
        Adam and AdamW
        Optimizer state memory
      Optimization Landscapes
        Convexity
        Saddle points
        Sharp vs flat minima
```

## Category Breakdown

| # | Category | Topics | Core Idea |
|---|---|---|---|
| 1 | Linear Algebra | 01–04 | Data, embeddings and weights as vectors, matrices and tensors |
| 2 | Calculus | 05–08 | How loss changes with parameters: gradients, chain rule, curvature |
| 3 | Probability and Statistics | 09–12 | Uncertainty, likelihood-based losses, information measures |
| 4 | Optimization Methods | 13–15 | Turning gradients into stable, efficient parameter updates |

## Topic Links by Category

| Category | Topics |
|---|---|
| Linear Algebra | [01 Vectors and Matrices](../math/01_Vectors%20and%20Matrices.md) · [02 Vector Spaces](../math/02_Vector%20Spaces.md) · [03 Matrix Decompositions](../math/03_Matrix%20Decompositions.md) · [04 Tensors](../math/04_Tensors.md) |
| Calculus | [05 Multivariate Calculus](../math/05_Multivariate%20Calculus.md) · [06 Derivatives](../math/06_Derivatives.md) · [07 The Chain Rule](../math/07_The%20Chain%20Rule.md) · [08 Jacobian and Hessian](../math/08_Jacobian%20and%20Hessian.md) |
| Probability and Statistics | [09 Probability Distributions](../math/09_Probability%20Distributions.md) · [10 Bayesian Statistics](../math/10_Bayesian%20Statistics.md) · [11 Estimations](../math/11_Estimations.md) · [12 Information Theory](../math/12_Information%20Theory.md) |
| Optimization Methods | [13 Gradient Descent Variants](../math/13_Gradient%20Descent%20Variants.md) · [14 Advanced Optimizers](../math/14_Advanced%20Optimizers.md) · [15 Optimization Landscapes](../math/15_Optimization%20Landscapes.md) |

## Learning Paths (from the Math index)

```mermaid
mindmap
  root((Math Learning Paths))
    Foundations
      01 Vectors
      02 Vector Spaces
      04 Tensors
      05 to 07 Calculus
      09 and 11 Probability
      13 Gradient Descent
    How Training Works
      Loss and gradients
      Chain rule
      Estimation
      Information theory
      Optimizers
    Training Stability and Scale
      Decompositions
      Chain rule
      Curvature
      Optimizers
      Landscapes
    LLM Architect
      Tensors
      Chain rule
      Information theory
      MLE and MAP
      Adam
      Hessian
      Landscapes
    Evaluation and Production
      Distributions
      Bayesian statistics
      Estimation
      Information theory
```

## Architect's Question Map

```mermaid
mindmap
  root((Where the math lives))
    GPU memory for training
      Gradients 06
      Activations 07
      Optimizer state 14
    Why training diverges
      Exploding gradients 07
      Curvature vs LR 08
      Adam settings 14
    Compress or quantize
      Low-rank SVD 03
      Flat vs sharp minima 15
    Is model B better
      Binomial intervals 09
    Traffic routing
      Thompson sampling 10
    Choosing a loss
      Likelihoods 09 and 11
    Data drift detection
      KL and PSI 12
    Scaling batch and LR
      Mini-batch rules 13
```
