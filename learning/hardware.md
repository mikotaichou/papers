# Hardware & Systems

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Vision](vision.md) | [Policy](policy.md)

**Overview**: AI doesn't run on theory alone—hardware and systems design fundamentally shape what's possible. This phase examines how memory bandwidth bottlenecks limit model performance, how specialized hardware accelerators exploit AI workload characteristics, and how [distributed training](glossary.md#distributed-training) systems coordinate thousands of [GPUs](glossary.md#gpu-graphics-processing-unit) to train massive models. Understanding the hardware-software co-design is crucial for making informed decisions about model architecture, for optimizing deployment costs, and for anticipating future directions as specialized AI chips become more prevalent.

## Hardware Considerations
**Goal**: Understand hardware-algorithm co-design

1. [Making Deep Learning Go Brrrr From First Principles](https://horace.io/brrr_intro.html) (He, 2022)
   - *Why*: **Essential practitioner guide** - explains GPU memory hierarchy, compute vs memory bound operations, and why FlashAttention works; practical understanding for optimizing ML workloads

2. [Efficiently Scaling Transformer Inference](https://arxiv.org/abs/2211.05102) (Pope et al., 2022)
   - *Why*: **Google's inference optimization guide** - analyzes memory bandwidth vs compute tradeoffs for transformer inference; introduces key concepts like arithmetic intensity and roofline analysis

3. 🔒 [High-dimensional on-chip dataflow sensing and routing using spatial photonic networks](https://www.nature.com/articles/s41566-023-01272-3.pdf) (2023)
   - *Why*: Photonic computing for AI; next-generation hardware
   - *Note*: Paywalled - Nature Photonics journal

4. [A Log-Domain Implementation of the Diffusion Network in Very Large Scale Integration](https://papers.nips.cc/paper_files/paper/2010/file/7bcdf75ad237b8e02e301f4091fb6bc8-Paper.pdf) (Chen & Murray, 2010)
   - *Why*: Early analog VLSI implementation of a stochastic neural model - shows how probabilistic networks can be realized directly in silicon using log-domain circuits; a precursor to today's interest in energy-efficient, hardware-native neural computation

5. [cuGenOpt: A GPU-Accelerated General-Purpose Metaheuristic Framework for Combinatorial Optimization](https://arxiv.org/abs/2603.19163) (Liu, 2026)
   - *Why*: Demonstrates a "one block evolves one solution" CUDA architecture with hardware-aware resource management across GPU generations (T4, V100, A800), outperforming general MIP solvers by orders of magnitude on combinatorial optimization problems.

---

**Related**: [Vision](vision.md) | [Policy](policy.md) | [Safety](safety.md)
