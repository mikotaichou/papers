# Probabilistic & Bayesian Approaches

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Advanced](advanced.md) | [Vision](vision.md)

**Overview**: Beyond language models lies a rich world of probabilistic modeling. The core of this area is **probabilistic programming**—expressing generative models as programs and performing Bayesian inference over them—spanning probabilistic data analysis, program synthesis for time series, and scene perception. It is rounded out by the theory of why [diffusion models](glossary.md#diffusion-model) generalize rather than memorize, and Bayesian generative approaches to vision such as MCMC methods and generative graphics programs. While briefer than other areas, these concepts are essential for understanding uncertainty, inference, and generative modeling beyond just text.

## Probabilistic Programming
**Goal**: Build probabilistic models programmatically

1. [A Probabilistic Programming Approach to Probabilistic Data Analysis](https://papers.nips.cc/paper/6060-a-probabilistic-programming-approach-to-probabilistic-data-analysis.pdf) (2016)
   - *Why*: **Automating statistical modeling** - demonstrates that probabilistic programs can express and automatically infer complex statistical models for data analysis tasks; replaces hand-derived inference algorithms with general-purpose probabilistic programming, making Bayesian data analysis accessible to non-experts

2. [Picture: An Imperative Probabilistic Programming Language for Scene Perception](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Kulkarni_Picture_A_Probabilistic_2015_CVPR_paper.pdf) (2015)
   - *Why*: Probabilistic programming for computer vision; demonstrates analysis-by-synthesis

3. [Encapsulating Models and Approximate Inference Programs in Probabilistic Modules](https://arxiv.org/abs/1612.04759) (2016)
   - *Why*: **Composable probabilistic building blocks** - introduces a module system for probabilistic programs where each module encapsulates both a generative model and its paired inference algorithm; enables building complex models by composing simpler ones while preserving inference quality; key step toward scalable, reusable probabilistic software engineering

4. [Measuring the Non-asymptotic Convergence of Sequential Monte Carlo Samplers using Probabilistic Programming](https://arxiv.org/abs/1612.02161) (2016)
   - *Why*: **Diagnosing SMC convergence in finite samples** - uses probabilistic programming to empirically measure how quickly sequential Monte Carlo samplers converge for practical (non-asymptotic) particle counts; provides actionable diagnostics for choosing particle numbers and resampling strategies; bridges theoretical convergence guarantees with real-world inference budgets

5. [Time Series Structure Discovery via Probabilistic Program Synthesis](https://arxiv.org/abs/1611.07051) (2016)
   - *Why*: **Program synthesis for time-series decomposition** - automatically discovers interpretable compositional structure in time-series data (trends, seasonality, changepoints) by synthesizing probabilistic programs from a grammar of kernels; produces human-readable descriptions of temporal patterns; demonstrates that program synthesis can replace manual feature engineering in time-series analysis

6. [MCMC using Hamiltonian dynamics](https://arxiv.org/abs/1206.1901) (2012)
   - *Why*: **Physics-inspired efficient sampling** - uses Hamiltonian dynamics to propose distant MCMC moves that are accepted with high probability, avoiding the random-walk behavior that makes standard Metropolis-Hastings slow in high dimensions; the definitive tutorial on HMC covering leapfrog integration, mass matrices, and the No-U-Turn Sampler; powers Stan and most modern Bayesian inference frameworks

## Diffusion Models
**Goal**: Understand how diffusion models learn and generalize

1. [Why Diffusion Models Don't Memorize: The Role of Implicit Dynamical Regularization in Training](https://arxiv.org/pdf/2505.17638) (2025)
   - *Why*: Theoretical analysis of why diffusion models generalize rather than memorize training data; identifies two distinct training timescales and implicit dynamical regularization

## Generative Models for Vision
**Goal**: Apply probabilistic models to visual understanding

1. [Approximate Bayesian Image Interpretation using Generative Probabilistic Graphics Programs](http://papers.nips.cc/paper/4881-approximate-bayesian-image-interpretation-using-generative-probabilistic-graphics-programs.pdf) (2013)
   - *Why*: **Inverse graphics as Bayesian inference** - treats scene understanding as inverting a graphics rendering pipeline: given an image, infer the 3D scene (objects, poses, lighting) that most likely produced it; uses probabilistic programming to express the generative model as a renderer and performs approximate posterior inference over scene parameters

2. [A Bayesian Framework for Modeling Intuitive Dynamics](https://cocosci.princeton.edu/tom/papers/collisions.pdf) (2009)
   - *Why*: **Bayesian models of intuitive physics** - formalizes human physical intuition (predicting collisions, stability, trajectories) as approximate Bayesian inference over a mental physics simulator; explains systematic biases in human physical reasoning as rational under uncertainty; foundational for cognitive science approaches to physical reasoning in AI
   - *Note*: Institutional repository - may require access

---

**Related**: [Advanced](advanced.md) | [Vision](vision.md) | [Hardware](hardware.md)
