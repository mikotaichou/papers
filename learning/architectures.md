# Novel Architectures & Theory

[← Back to Learning Path](../learning-path.md) | [← Prev: Reasoning](reasoning.md) | [Next: Interpretability →](interpretability.md) | [📖 Glossary](glossary.md)

**Overview**: [Transformers](glossary.md#transformer) dominate modern AI, but are they the final answer? This area explores alternative architectures that challenge the transformer's supremacy: [state-space models](glossary.md#state-space-model) like [Mamba](glossary.md#mamba) that achieve linear-time inference, [retention networks](glossary.md#retnet-retentive-network) that blend RNN and transformer properties, [RWKV](glossary.md#rwkv)'s parallelizable RNN approach, and hybrid architectures that combine different mechanisms. Each offers different trade-offs between performance, efficiency, and scaling properties. Understanding these alternatives gives you insight into the fundamental principles that make architectures work—and hints at what might come next.

## Alternative Architectures
**Goal**: Explore beyond standard transformers

1. [Neural Turing Machines](https://arxiv.org/abs/1410.5401) (Graves et al., 2014)
   - *Why*: **Foundational memory-augmented architecture** - introduces external memory and attention mechanisms that inspired modern architectures; demonstrates how neural networks can learn to use memory

2. [Relational Recurrent Neural Networks](https://arxiv.org/abs/1806.01822) (Santoro et al., 2018)
   - *Why*: **Memory-augmented RNNs** - extends RNNs with relational memory for better long-term dependencies; combines recurrence with relational reasoning

3. [RWKV: Reinventing RNNs for the Transformer Era](https://arxiv.org/abs/2305.13048) (Peng et al., 2023)
   - *Why*: **Foundational non-transformer alternative** - combines efficient parallelizable training with O(1) inference; scaled to 14B parameters

4. [Nested Learning: The Illusion of Deep Learning Architectures](https://abehrouz.github.io/files/NL.pdf) (Behrouz et al., 2025) - NeurIPS 2025
   - *Why*: **New paradigm unifying architecture and optimization** - views models as nested optimization problems at multiple time scales; introduces Hope, a self-modifying architecture with continuum memory systems that achieves superior continual learning and mitigates catastrophic forgetting

5. [Kolmogorov–Arnold Networks (KAN)](https://arxiv.org/pdf/2404.19756) (2024)
   - *Why*: **Learnable activation functions on edges** - replaces fixed activations (ReLU, GELU) with learnable univariate spline functions placed on network edges rather than nodes, inspired by the Kolmogorov-Arnold representation theorem; achieves better accuracy with smaller networks on scientific tasks; produces more interpretable models where each edge learns a meaningful function

6. [U-Nets as Belief Propagation: Efficient Classification, Denoising, and Diffusion in Generative Hierarchical Models](https://arxiv.org/pdf/2404.18444) (2024)
   - *Why*: **U-Nets are approximate belief propagation** - proves that the U-Net architecture's skip connections and encoder-decoder structure correspond to message-passing in hierarchical probabilistic graphical models; provides a theoretical framework explaining why U-Nets excel at denoising and diffusion tasks; bridges deep learning architectures with classical probabilistic inference

7. [Mamba or RWKV: Exploring High-Quality and High-Efficiency Segment Anything Model](https://arxiv.org/pdf/2409.15254) (2024)
   - *Why*: **SSMs vs. linear RNNs for vision** - benchmarks Mamba (state-space model) and RWKV (linear RNN) as backbones for SAM-style image segmentation, comparing their quality-efficiency tradeoffs against transformer baselines; provides practical guidance on when sub-quadratic architectures can replace transformers in dense prediction tasks

8. [Learning Convolutional Neural Networks for Graphs](http://proceedings.mlr.press/v48/niepert16.pdf) (2016)
   - *Why*: Applying CNNs to graph-structured data; foundation for graph neural networks

9. [Order Matters: Sequence to Sequence for Sets](https://arxiv.org/abs/1511.06391) (Vinyals et al., 2015)
   - *Why*: **Handling set-structured data** - extends sequence-to-sequence models to handle unordered sets; important for tasks like set prediction and permutation-invariant learning

10. [mHC: Manifold-Constrained Hyper-Connections](https://arxiv.org/abs/2512.24880) (Xie et al., 2025)
    - *Why*: **Extends Hyper-Connections with stability guarantees** - projects residual connection space onto a constrained manifold to restore identity mapping property; addresses training instability and scalability issues in HC while maintaining performance gains; demonstrates effectiveness at scale (3B-27B models) with improved stability

11. [LeWorldModel: Stable End-to-End Joint-Embedding Predictive Architecture from Pixels](https://arxiv.org/abs/2603.19312) (Maes et al., 2026)
    - *Why*: **First stable end-to-end JEPA from raw pixels** - trains a Joint Embedding Predictive Architecture using only a prediction loss and a Gaussian regularizer, eliminating the complex multi-term losses and EMA tricks prior JEPAs required; plans up to 48x faster than foundation-model-based world models on 2D/3D control tasks with ~15M parameters on a single GPU

12. [A Network of Biologically Inspired Rectified Spectral Units (ReSUs) Learns Hierarchical Features Without Error Backpropagation](https://arxiv.org/abs/2512.23146) (Qin et al., 2025)
    - *Why*: **Backprop-free hierarchical feature learning grounded in biology** - introduces Rectified Spectral Units that learn locally via canonical correlation analysis on input history, encoding information in synaptic weights and temporal filters; a two-layer network trained on natural scenes spontaneously develops temporal filters matching Drosophila post-photoreceptor neurons and direction-selective second-layer units resembling connectome-derived motion detectors, offering both a model of sensory circuits and a credible alternative to error backpropagation

13. [Mixture-of-Transformers: A Sparse and Scalable Architecture for Multi-Modal Foundation Models](https://arxiv.org/abs/2411.04996) (Liang et al., 2024)
    - *Why*: **Sparse multimodal architecture** - decouples feedforward layers, attention matrices, and layer norms into modality-specific experts while sharing self-attention across modalities; achieves equivalent multimodal performance with substantially fewer FLOPs than dense models; demonstrates that modality-specific sparsity is more efficient than uniform scaling for vision-language tasks

14. [Lattice Deduction Transformers](https://arxiv.org/abs/2605.08605) (Davis et al., 2026)
    - *Why*: **Recurrent transformer with sound deduction guarantees** - projects the latent state onto an abstract lattice between forward passes so each pass acts as a sound deduction step, trained on-policy in a constraint-solver-style loop with abstract-interpretation-based supervision; an 800K-parameter model reaches 100% accuracy on Sudoku-Extreme and Snowflake Sudoku and a 1.8M-parameter variant hits 99.9% on Maze-Hard, while frontier LLMs score 0% on all three, suggesting abstract interpretation can give small recurrent reasoners both correctness and competence.

## Theoretical Foundations
**Goal**: Understand the mathematical foundations

1. [Neural Tangent Kernel: Convergence and Generalization in Neural Networks](https://arxiv.org/abs/1806.07572) (Jacot et al., 2018)
   - *Why*: **Bridges theory and deep learning** - shows ANNs are equivalent to kernel methods in infinite-width limit; explains generalization

2. [Token embeddings violate the manifold hypothesis](https://arxiv.org/abs/2504.01002) (2025)
   - *Why*: **Challenging assumptions about embedding geometry** - demonstrates that learned token embeddings in LLMs do not lie on smooth low-dimensional manifolds as widely assumed; shows embedding spaces have fractal-like, non-manifold structure with implications for interpolation, representation analysis, and theoretical models of how transformers organize knowledge

3. [How much do language models memorize?](https://arxiv.org/pdf/2505.24832) (2025)
   - *Why*: **Quantifying memorization in LLMs** - develops rigorous methods to measure how much of the training set language models can reproduce verbatim; distinguishes extractable memorization from latent memorization; reveals that memorization scales predictably with model size, data repetition, and sequence length, informing privacy and data governance decisions

4. [Accelerating Training With Neuron Interaction And Nowcasting Networks](https://arxiv.org/pdf/2409.04434) (2024)
   - *Why*: **Predicting weight updates to skip training steps** - trains a small auxiliary network to predict future gradient updates by modeling neuron interactions; enables "nowcasting" of weight trajectories to skip multiple optimization steps; achieves training speedups by reducing the total number of forward-backward passes needed for convergence

---

**Related**: [Reasoning](reasoning.md) | [Interpretability](interpretability.md) | [Safety](safety.md)
