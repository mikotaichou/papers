# Interpretability & Analysis

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Architectures](architectures.md) | [Safety](safety.md)

**Overview**: Neural networks are often treated as black boxes, but what's really happening inside? This phase dives into [interpretability](glossary.md#mechanistic-interpretability)—the science of understanding and explaining model behavior. You'll learn about mechanistic interpretability that reverse-engineers learned algorithms, activation analysis techniques like sparse autoencoders that reveal hidden structure, theoretical frameworks like the [Neural Tangent Kernel](glossary.md#neural-tangent-kernel) that explain why deep learning works, and methods for detecting when models are truthful or deceptive. As AI systems become more powerful and deployed in high-stakes settings, interpretability becomes crucial for trust, debugging, and safety.

## Understanding Model Behavior
**Goal**: Interpret what models learn and how they work

1. [Towards A Rigorous Science of Interpretable Machine Learning](https://arxiv.org/abs/1702.08608) (2017)
   - *Why*: **Defining interpretability as a science** - introduces a taxonomy of evaluation approaches (application-grounded, human-grounded, and functionally-grounded) for explanation methods; establishes rigorous criteria for when interpretability is needed and how to measure explanation quality

2. [Axiomatic Attribution for Deep Networks (Integrated Gradients)](https://arxiv.org/abs/1703.01365) (2017)
   - *Why*: **Axiomatic foundation for attribution** - introduces Integrated Gradients, which satisfies two fundamental axioms (Sensitivity and Implementation Invariance) that prior methods violate; computes attributions by integrating gradients along the path from a baseline to the input, requiring no model modification

3. [LIME: "Why Should I Trust You?" Explaining the Predictions of Any Classifier](https://arxiv.org/abs/1602.04938) (2016)
   - *Why*: **Model-agnostic local explanations** - approximates any classifier's decision boundary locally with an interpretable surrogate model; generates explanations by perturbing inputs and observing prediction changes, working with any model type without access to internals

4. [Methods for Interpreting and Understanding Deep Neural Networks](https://arxiv.org/abs/1706.07979) (2017)
   - *Why*: **Unified interpretability survey** - categorizes interpretation methods into optimization-based, propagation-based, and network analysis approaches; provides a mathematical framework connecting gradient-based attribution, deconvolution, and layer-wise relevance propagation under a common lens

5. [SmoothGrad: Removing Noise by Adding Noise](https://arxiv.org/abs/1706.03825) (2017)
   - *Why*: **Denoising sensitivity maps** - reduces visual noise in gradient-based attributions by averaging gradients computed on multiple noisy copies of the input; simple technique that dramatically sharpens attribution maps for any gradient-based method without model modification

6. [Deep Taylor Decomposition: Explaining Nonlinear Classification Decisions](https://arxiv.org/abs/1512.02479) (2015)
   - *Why*: **Mathematical foundation for LRP** - extends layer-wise relevance propagation with formal theoretical grounding using first-order Taylor expansions at each layer; decomposes network output into per-input relevance scores with provable conservation properties across layers

7. [Learning How to Explain Neural Networks: PatternNet and PatternAttribution](https://arxiv.org/abs/1705.05598) (2017)
   - *Why*: **Data-driven explanation learning** - separates signal direction from noise in neuron activations to produce cleaner attributions; shows that standard gradient-based methods conflate signal and noise, producing misleading explanations; learns data-dependent patterns that yield more faithful feature attributions

8. [Understanding Black-box Predictions via Influence Functions](https://arxiv.org/abs/1703.04730) (2017)
   - *Why*: Tracing predictions back to training data; identifying influential examples

9. [Weight-sparse transformers have interpretable circuits](https://cdn.openai.com/pdf/41df8f28-d4ef-43e9-aed2-823f9393e470/circuit-sparsity-paper.pdf) (Gao et al., OpenAI, 2025)
   - *Why*: **Training models for interpretability from scratch** - constrains most weights to zero so neurons have few connections; produces circuits with unprecedented human understandability through weight sparsity rather than post-hoc analysis; validates circuits with mean ablation showing they are necessary and sufficient for task performance

10. [H-Neurons: On the Existence, Impact, and Origin of Hallucination-Associated Neurons in LLMs](https://arxiv.org/abs/2512.01797) (Gao et al., Tsinghua, 2025)
    - *Why*: **Neuron-level mechanistic view of hallucinations** - identifies a sparse subset (<0.1%) of feedforward neurons ([H-Neurons](glossary.md#h-neurons-hallucination-associated-neurons)) that reliably predict hallucination; shows they drive over-compliance behaviors (invalid premises, misleading context, sycophancy, harmful instructions) and originate in pre-training; bridges macro-behavioral patterns with micro-neural mechanisms for detection and intervention

11. [Farther the Shift, Sparser the Representation: Analyzing OOD Mechanisms in LLMs](https://arxiv.org/abs/2603.03415) (Jin et al., 2026)
    - *Why*: **Sparsity as an adaptive OOD mechanism** - reveals that LLM last hidden states become substantially sparser as input difficulty increases (harder reasoning, longer contexts, more answer choices); demonstrates this is not incidental but an adaptive strategy for stabilizing reasoning under distribution shift; leverages the insight to design Sparsity-Guided Curriculum In-Context Learning (SG-ICL) for improved few-shot performance

## Model Evaluation & Robustness
**Goal**: Properly evaluate and benchmark models

1. [TruthfulQA: Measuring How Models Mimic Human Falsehoods](https://arxiv.org/abs/2109.07958) (Lin et al., 2022)
   - *Why*: **Factuality benchmark** - reveals that larger models can be less truthful; critical for understanding model limitations

2. [Forget What You Know about LLMs Evaluations -- LLMs are Like a Chameleon](https://arxiv.org/pdf/2502.07445) (2025)
   - *Why*: **Fragility of LLM benchmarks** - demonstrates that benchmark scores are highly sensitive to superficial prompt format changes (ordering, spacing, templates); shows models adapt chameleon-like to evaluation framing rather than exhibiting stable capabilities, challenging the reliability of standard evaluation practices

3. [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) (2024)
   - *Why*: **End-to-end ML engineering benchmark** - evaluates AI agents on 75 real Kaggle competitions spanning tabular, NLP, and vision tasks; tests the full ML pipeline from data processing through model selection and tuning; establishes a practical measure of autonomous ML engineering capability

4. [On Calibration of Modern Neural Networks](https://arxiv.org/abs/1706.04599) (2017)
   - *Why*: **Revealing systematic overconfidence** - shows that modern deep networks are poorly calibrated despite high accuracy, with confidence scores that systematically overestimate correctness; introduces temperature scaling as a simple, effective post-hoc calibration method; foundational for understanding when to trust model predictions

5. [The Illusion of Thinking](https://ml-site.cdn-apple.com/papers/the-illusion-of-thinking.pdf) (2025)
   - *Why*: **Stress-testing reasoning models** - evaluates chain-of-thought models (o1, o3) on novel compositional tasks outside training distributions; demonstrates that CoT reasoning often mimics pattern matching rather than genuine logical inference, with performance degrading sharply on problems requiring novel reasoning steps

---

**Related**: [Architectures](architectures.md) | [Safety](safety.md) | [Language Models](language-models.md)
