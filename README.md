# AI/ML Research Papers Collection

> A curated, pedagogically-organized collection of essential research papers spanning the landscape of modern artificial intelligence and machine learning.

[![Papers](https://img.shields.io/badge/papers-254-blue.svg)](by-date.md)
[![Learning Path](https://img.shields.io/badge/learning-14_areas-green.svg)](learning-path.md)
[![Glossary](https://img.shields.io/badge/glossary-161_terms-purple.svg)](learning/glossary.md)

---

## 🎯 What's Inside

This repository contains **254 carefully selected research papers and policy documents** organized in three complementary ways:

1. **📚 [Structured Learning Path](learning-path.md)** - Topic areas and curated tracks from foundations to cutting-edge research
2. **📅 [Chronological Timeline](by-date.md)** - Papers organized by publication date (1997-2026)
3. **📖 [Comprehensive Glossary](learning/glossary.md)** - 161 terms, concepts, and acronyms explained with context

**Plus**: [Recommended tracks](#-how-to-use-this-repository), [notes on learning](#paper-reading-tips), and [quick start guides](#-quick-start) tailored to your role (beginner, practitioner, researcher, engineer, security specialist).

---

## 🚀 Quick Start

### For Beginners
Start with the **[Learning Path](learning-path.md)** and follow **Foundations**. Read papers in sequence, focusing on the "Why" explanations. Check the **[Glossary](learning/glossary.md)** whenever you encounter unfamiliar terms.

### For Practitioners
Jump to relevant areas:
- **LLMs & Training**: [Language Models](learning/language-models.md)
- **Efficient Models**: [Attention](learning/attention.md)
- **Production AI**: [Retrieval](learning/retrieval.md) (RAG), [Safety](learning/safety.md) (Security & Safety)

### For Researchers
Browse the **[Chronological View](by-date.md)** to see latest 2026 research, or deep-dive into:
- [Alternative Architectures](learning/architectures.md)
- [Interpretability](learning/interpretability.md)
- [Advanced Topics](learning/advanced.md)

### Quick Reference
**Need a definition?** → Check the **[📖 Glossary](learning/glossary.md)** for 161 terms organized by category (architectures, training, NLP, security, etc.)

---

## 🎓 How to Use This Repository

### Reading Strategies

**🌱 The Beginner Path** (3-6 months)
1. Start with [Foundations](learning/foundations.md)
2. Read key papers: [Attention Is All You Need](https://arxiv.org/abs/1706.03762) → [BERT](https://arxiv.org/abs/1810.04805) → [GPT-3](https://arxiv.org/abs/2005.14165)
3. Focus on "Why" explanations before diving deep
4. Take notes on connections between papers

**⚡ The Practitioner Sprint** (1-2 months)
1. Read Foundations summaries for context
2. Deep-dive: [Language Models](learning/language-models.md) + [Attention](learning/attention.md) + [Retrieval](learning/retrieval.md)
3. Skim related work sections to understand landscape
4. Implement key techniques from papers

**🔬 The Researcher Deep-Dive** (Ongoing)
1. Use [chronological view](by-date.md) for latest research
2. Focus on specific areas relevant to your research
3. Read citations and follow paper connections
4. Compare approaches across different papers

**🛠️ The Engineer Focus** (2-4 weeks)
1. Priority: [Attention](learning/attention.md) (Efficiency), [Safety](learning/safety.md) (Security & Safety), [Hardware](learning/hardware.md)
2. Focus on implementation details and benchmarks
3. Note production considerations and trade-offs

**🛡️ The Security Specialist** (1-2 weeks)
1. Core: [Safety](learning/safety.md)
2. Context: [Language Models](learning/language-models.md) (LLM basics), [Reasoning](learning/reasoning.md) (Alignment)
3. Focus on threat models, defense mechanisms, and safety evaluation

### Paper Reading Tips

1. **Start with abstracts** - Understand the core contribution
2. **Read "Why" annotations** - Context before content
3. **Check the [📖 Glossary](learning/glossary.md)** - Look up unfamiliar terms
4. **Follow the narrative** - Papers build on each other
5. **Take notes** - Document connections and insights
6. **Implement key ideas** - Hands-on learning reinforces concepts

---

## 📖 Learning Path Overview

The learning path is organized into **14 topic areas**; use [learning-path.md](learning-path.md) for curated **tracks** (reading sequences by goal).

| Area | Topic | Papers | Focus |
|------|-------|--------|-------|
| **[Foundations](learning/foundations.md)** | 🏗️ **Foundations (Start Here)** | 25 | Deep learning basics, embeddings, CNNs, RNNs, GANs, tokenization |
| **[Language Models](learning/language-models.md)** | 🤖 **Large Language Models** | 21 | Transformers, BERT, GPT, training at scale |
| **[Attention](learning/attention.md)** | ⚡ **Attention Mechanisms & Context** | 11 | FlashAttention 1 & 2, efficient attention, long context |
| **[Retrieval](learning/retrieval.md)** | 🔍 **Retrieval & Knowledge Systems** | 11 | THE RAG paper, dense retrieval, kNN-LM, semantic search |
| **[Reasoning](learning/reasoning.md)** | 🧠 **Reasoning & Agents** | 22 | RLHF, chain-of-thought, agentic systems |
| **[Architectures](learning/architectures.md)** | 🏛️ **Novel Architectures & Theory** | 18 | RWKV, Mamba, state-space models, theory |
| **[Interpretability](learning/interpretability.md)** | 🔬 **Interpretability & Evaluation** | 16 | LIME, integrated gradients, weight-sparse circuits |
| **[Safety](learning/safety.md)** | 🛡️ **Security, Safety & Robustness** | 36 | Alignment, security threats, safety evaluation, bias & fairness, harmful content, long-term safety |
| **[Advanced](learning/advanced.md)** | 🎯 **Advanced Topics & Applications** | 8 | Multimodal, scientific AI, test-time compute |
| **[Probabilistic](learning/probabilistic.md)** | 🎲 **Probabilistic & Bayesian Approaches** | 9 | Diffusion, probabilistic programming |
| **[Vision](learning/vision.md)** | 👁️ **Vision & Multimodal Systems** | 11 | ViT, CLIP, SAM, LLaVA, vision-language models |
| **[Hardware](learning/hardware.md)** | ⚙️ **Hardware & Systems** | 5 | GPU optimization, inference scaling, photonic computing |
| **[Human-AI Interaction](learning/human-ai-interaction.md)** | 🧠 **Human-AI Interaction & Cognition** | 11 | Trust, automation bias, cognitive effects, human-AI teams |
| **[Policy](learning/policy.md)** | 📜 **Policy, Safety & Societal Impact** | 53 | GDPR, EU AI Act, US federal & state AI law, NIST AI RMF |

**Total**: 254 papers across 14 areas (including 53 policy documents & frameworks)

---

## 📊 Coverage by Topic

<!-- COVERAGE:START (generated by scripts/validate.py --fix; do not hand-edit) -->
This collection spans the full spectrum of modern AI/ML research, organized by area:

### 🏗️ Foundations
- **Deep Learning Basics**: [Deep Learning (Nature Review)](https://www.nature.com/articles/nature14539) · [Understanding the Difficulty of Training Deep Feedforward Neural Networks](https://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf) · [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://arxiv.org/abs/1502.03167) · [Gradient-Based Learning Applied to Document Recognition (LeNet)](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf) · [ImageNet Classification with Deep Convolutional Neural Networks (AlexNet)](https://papers.nips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) · [Going Deeper with Convolutions (GoogLeNet)](https://arxiv.org/abs/1409.4842) · [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) · [Identity Mappings in Deep Residual Networks](https://arxiv.org/abs/1603.05027) · [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122) · [The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks](https://arxiv.org/abs/1803.03635)
- **Word Embeddings & Representations**: [Efficient Estimation of Word Representations in Vector Space (Word2Vec)](https://arxiv.org/abs/1301.3781) · [GloVe: Global Vectors for Word Representation](https://aclanthology.org/D14-1162/) · [Sequence to Sequence Learning with Neural Networks](https://arxiv.org/abs/1409.3215) · [Pointer Networks](https://arxiv.org/abs/1506.03134)
- **Sequence Models**: [Long Short-Term Memory (LSTM)](https://www.researchgate.net/publication/13853244_Long_Short-term_Memory) · [Recurrent Neural Network Regularization](https://arxiv.org/abs/1409.2329) · [MOMENT: A Family of Open Time-series Foundation Models](https://arxiv.org/pdf/2402.03885)
- **Generative Models**: [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) · [Variational Lossy Autoencoder](https://arxiv.org/abs/1611.02731) · [Dualscale Diffusion: Adaptive Feature Balancing for Low-Dimensional Generative Models](https://sakana.ai/assets/ai-scientist/adaptive_dual_scale_denoising.pdf)
- **Tokenization & Subword Models**: [Neural Machine Translation of Rare Words with Subword Units (BPE)](https://arxiv.org/abs/1508.07909) · [SentencePiece: A simple and language independent subword tokenizer and detokenizer](https://arxiv.org/abs/1808.06226) · [Greed is All You Need: An Evaluation of Tokenizer Inference Methods](https://arxiv.org/abs/2403.01289) · [Understanding and Mitigating Tokenization Bias in Language Models](https://arxiv.org/abs/2406.16829) · [Bytes Are All You Need: Transformers Operating Directly On File Bytes](https://arxiv.org/pdf/2306.00238)

### 🤖 Language Models
- **LLM Foundations**: [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473) · [Attention Is All You Need](https://arxiv.org/abs/1706.03762) · [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) · [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361) · [Language Models are Few-Shot Learners (GPT-3)](https://arxiv.org/abs/2005.14165) · [ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators](https://arxiv.org/abs/2003.10555) · [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783) · [OpenELM: An Efficient Language Model Family with Open-source Training and Inference Framework](https://arxiv.org/pdf/2404.14619) · [EuroLLM: Multilingual Language Models for Europe](https://arxiv.org/pdf/2409.11741)
- **Training at Scale**: [GPipe: Easy Scaling with Micro-Batch Pipeline Parallelism](https://arxiv.org/abs/1811.06965) · [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053) · [ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/abs/1910.02054) · [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473) · [The Potential of Second-Order Optimization for LLMs: A Study with Full Gauss-Newton](https://arxiv.org/pdf/2510.09378) · [MegaTrain: Full Precision Training of 100B+ Parameter Large Language Models on a Single GPU](https://arxiv.org/abs/2604.05091)
- **Memory & Efficiency Optimizations**: [Cut Your Losses in Large-Vocabulary Language Models](https://arxiv.org/abs/2411.09009) · [Scalable MatMul-free Language Modeling](https://arxiv.org/pdf/2406.02528) · [The Era of 1-bit LLMs: All Large Language Models are in 1.58 Bits](https://arxiv.org/pdf/2402.17764) · [TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate](https://arxiv.org/abs/2504.19874) · [Do LLMs Benefit From Their Own Words?](https://arxiv.org/abs/2602.24287) · [DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation](https://arxiv.org/abs/2607.05147)

### ⚡ Attention
- **Efficient Attention**: [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/abs/2205.14135) · [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://arxiv.org/abs/2307.08691) · [Retentive Network: A Successor to Transformer for Large Language Models](https://arxiv.org/abs/2307.08621) · [Efficient streaming language models with attention sinks](https://arxiv.org/pdf/2309.17453.pdf) · [Leave No Context Behind: Efficient Infinite Context Transformers with Infini-attention](https://arxiv.org/pdf/2404.07143v1.pdf) · [Native Sparse Attention: Hardware-Aligned and Natively Trainable Sparse Attention](https://arxiv.org/abs/2502.11089) · [SSA: Sparse Sparse Attention by Aligning Full and Sparse Attention Outputs in Feature Space](https://arxiv.org/abs/2511.20102)
- **Long Context & Compression**: [TriForce: Lossless Acceleration of Long Sequence Generation with Hierarchical Speculative Decoding](https://arxiv.org/pdf/2404.11912v1.pdf) · [DeepSeek-OCR: Contexts Optical Compression](https://arxiv.org/pdf/2510.18234) · [Agentic Context Engineering: Evolving Contexts for Self-Improving Language Models](https://arxiv.org/abs/2510.04618) · [Recursive Language Models](https://arxiv.org/abs/2512.24601)

### 🔍 Retrieval & RAG
- **Retrieval-Augmented Generation (RAG)**: [Dense Passage Retrieval for Open-Domain Question Answering](https://arxiv.org/abs/2004.04906) · [REALM: Retrieval-Augmented Language Model Pre-Training](https://arxiv.org/abs/2002.08909) · [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) · [Generalization through Memorization: Nearest Neighbor Language Models (kNN-LM)](https://arxiv.org/abs/1911.00172) · [A Survey of Context Engineering for Large Language Models](https://arxiv.org/abs/2507.13334) · [REFRAG: Rethinking RAG based Decoding](https://arxiv.org/pdf/2509.01092) · [Semantic IDs for Joint Generative Search and Recommendation](https://arxiv.org/abs/2508.10478) · [Is Table Retrieval a Solved Problem? Exploring Join-Aware Multi-Table Retrieval](https://arxiv.org/pdf/2404.09889) · [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) · [Engram: Conditional Memory via Scalable Lookup](https://github.com/deepseek-ai/Engram/blob/main/Engram_paper.pdf)
- **Federated & Distributed Learning**: [Federated Learning with Ad-hoc Adapter Insertions: The Case of Soft-Embeddings for Training Classifier-as-Retriever](https://arxiv.org/pdf/2509.16508)

### 🧠 Reasoning & Agents
- **Teaching Models to Reason**: [Deep Reinforcement Learning from Human Preferences](https://arxiv.org/abs/1706.03741) · [Proximal Policy Optimization Algorithms (PPO)](https://arxiv.org/abs/1707.06347) · [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) · [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) · [Hierarchical Reasoning Model](https://arxiv.org/pdf/2506.21734) · [Less is More: Recursive Reasoning with Tiny Networks](https://arxiv.org/pdf/2510.04871) · [Reinforcement Pre-Training](https://arxiv.org/abs/2506.08007) · [A Simple Neural Network Module for Relational Reasoning](https://arxiv.org/abs/1706.01427) · [Embarrassingly Simple Self-Distillation Improves Code Generation](https://arxiv.org/abs/2604.01193) · [Scaling Latent Reasoning via Looped Language Models](https://arxiv.org/abs/2510.25741) · [A Formal Comparison Between Chain of Thought and Latent Thought](https://arxiv.org/abs/2509.25239) · [NL2LOGIC: AST-Guided Translation of Natural Language into First-Order Logic with Large Language Models](https://arxiv.org/abs/2602.13237)
- **Agentic Systems**: [A Generalist Agent](https://arxiv.org/pdf/2205.06175) · [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/pdf/2402.01030) · [DynaSaur: Large Language Agents Beyond Predefined Actions](https://arxiv.org/abs/2411.01747) · [MAS-ZERO: Designing Multi-Agent Systems with Zero Supervision](https://arxiv.org/pdf/2505.14996) · [Small Language Models are the Future of Agentic AI](https://arxiv.org/abs/2506.02153) · [Learning in Stackelberg Mean Field Games: A Non-Asymptotic Analysis](https://arxiv.org/pdf/2509.15392) · [Embedded Universal Predictive Intelligence: a coherent framework for multi-agent learning](https://arxiv.org/pdf/2511.22226) · [Artificial Intelligent Disobedience: Rethinking the Agency of Our Artificial Teammates](https://arxiv.org/abs/2506.22276) · [TRINITY: An Evolved LLM Coordinator](https://arxiv.org/abs/2512.04695) · [Learning to Orchestrate Agents in Natural Language with the Conductor](https://arxiv.org/abs/2512.04388)

### 🏛️ Architectures
- **Alternative Architectures**: [Neural Turing Machines](https://arxiv.org/abs/1410.5401) · [Relational Recurrent Neural Networks](https://arxiv.org/abs/1806.01822) · [RWKV: Reinventing RNNs for the Transformer Era](https://arxiv.org/abs/2305.13048) · [Nested Learning: The Illusion of Deep Learning Architectures](https://abehrouz.github.io/files/NL.pdf) · [Kolmogorov–Arnold Networks (KAN)](https://arxiv.org/pdf/2404.19756) · [U-Nets as Belief Propagation: Efficient Classification, Denoising, and Diffusion in Generative Hierarchical Models](https://arxiv.org/pdf/2404.18444) · [Mamba or RWKV: Exploring High-Quality and High-Efficiency Segment Anything Model](https://arxiv.org/pdf/2409.15254) · [Learning Convolutional Neural Networks for Graphs](http://proceedings.mlr.press/v48/niepert16.pdf) · [Order Matters: Sequence to Sequence for Sets](https://arxiv.org/abs/1511.06391) · [mHC: Manifold-Constrained Hyper-Connections](https://arxiv.org/abs/2512.24880) · [LeWorldModel: Stable End-to-End Joint-Embedding Predictive Architecture from Pixels](https://arxiv.org/abs/2603.19312) · [A Network of Biologically Inspired Rectified Spectral Units (ReSUs) Learns Hierarchical Features Without Error Backpropagation](https://arxiv.org/abs/2512.23146) · [Mixture-of-Transformers: A Sparse and Scalable Architecture for Multi-Modal Foundation Models](https://arxiv.org/abs/2411.04996) · [Lattice Deduction Transformers](https://arxiv.org/abs/2605.08605)
- **Theoretical Foundations**: [Neural Tangent Kernel: Convergence and Generalization in Neural Networks](https://arxiv.org/abs/1806.07572) · [Token embeddings violate the manifold hypothesis](https://arxiv.org/abs/2504.01002) · [How much do language models memorize?](https://arxiv.org/pdf/2505.24832) · [Accelerating Training With Neuron Interaction And Nowcasting Networks](https://arxiv.org/pdf/2409.04434)

### 🔬 Interpretability
- **Understanding Model Behavior**: [Towards A Rigorous Science of Interpretable Machine Learning](https://arxiv.org/abs/1702.08608) · [Axiomatic Attribution for Deep Networks (Integrated Gradients)](https://arxiv.org/abs/1703.01365) · [LIME: "Why Should I Trust You?" Explaining the Predictions of Any Classifier](https://arxiv.org/abs/1602.04938) · [Methods for Interpreting and Understanding Deep Neural Networks](https://arxiv.org/abs/1706.07979) · [SmoothGrad: Removing Noise by Adding Noise](https://arxiv.org/abs/1706.03825) · [Deep Taylor Decomposition: Explaining Nonlinear Classification Decisions](https://arxiv.org/abs/1512.02479) · [Learning How to Explain Neural Networks: PatternNet and PatternAttribution](https://arxiv.org/abs/1705.05598) · [Understanding Black-box Predictions via Influence Functions](https://arxiv.org/abs/1703.04730) · [Weight-sparse transformers have interpretable circuits](https://cdn.openai.com/pdf/41df8f28-d4ef-43e9-aed2-823f9393e470/circuit-sparsity-paper.pdf) · [H-Neurons: On the Existence, Impact, and Origin of Hallucination-Associated Neurons in LLMs](https://arxiv.org/abs/2512.01797) · [Farther the Shift, Sparser the Representation: Analyzing OOD Mechanisms in LLMs](https://arxiv.org/abs/2603.03415)
- **Model Evaluation & Robustness**: [TruthfulQA: Measuring How Models Mimic Human Falsehoods](https://arxiv.org/abs/2109.07958) · [Forget What You Know about LLMs Evaluations -- LLMs are Like a Chameleon](https://arxiv.org/pdf/2502.07445) · [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) · [On Calibration of Modern Neural Networks](https://arxiv.org/abs/1706.04599) · [The Illusion of Thinking](https://ml-site.cdn-apple.com/papers/the-illusion-of-thinking.pdf)

### 🛡️ Safety & Security
- **AI Alignment & Safety Training**: [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) · [Training language models to follow instructions with human feedback (InstructGPT)](https://arxiv.org/abs/2203.02155) · [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073) · [Weak-to-Strong Generalization: Eliciting Strong Capabilities With Weak Supervision](https://arxiv.org/abs/2312.09390) · [Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations](https://arxiv.org/abs/2312.06674)
- **Security Threats & Attacks**: [Pr$εε$mpt: Sanitizing Sensitive Prompts for LLMs](https://arxiv.org/abs/2504.05147) · [Enterprise-Grade Security for the Model Context Protocol (MCP): Frameworks and Mitigation Strategies](https://arxiv.org/pdf/2504.08623) · [A2AS: Agentic AI Runtime Security and Self-Defense](https://arxiv.org/pdf/2510.13825) · [Breaking Agent Backbones: Evaluating the Security of Backbone LLMs in AI Agents](https://arxiv.org/abs/2510.22620) · [Large Language Models are Unreliable for Cyber Threat Intelligence](https://arxiv.org/abs/2503.23175) · [SEC-bench: Automated Benchmarking of LLM Agents on Real-World Software Security Tasks](https://openreview.net/pdf?id=QQhQIqons0) · [Your Agent Is Mine: Measuring Malicious Intermediary Attacks on the LLM Supply Chain](https://arxiv.org/abs/2604.08407) · [Bad Memory: Evaluating Prompt Injection Risks from Memory in Agentic Systems](https://arxiv.org/abs/2607.14611) · [AI Agents May Always Fall for Prompt Injections](https://arxiv.org/abs/2605.17634)
- **Safety Evaluation & Red Teaming**: [Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned](https://arxiv.org/abs/2209.07858) · [Automated Red Teaming with GOAT: the Generative Offensive Agent Tester](https://arxiv.org/abs/2410.01606) · [HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal](https://arxiv.org/abs/2402.04249) · [WildGuard: Open One-Stop Moderation Tools for Safety Risks, Jailbreaks, and Refusals of LLMs](https://arxiv.org/abs/2406.18495) · [TruthfulQA: Measuring How Models Mimic Human Falsehoods](https://arxiv.org/abs/2109.07958) · [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218) · [Agents of Chaos](https://arxiv.org/abs/2602.20021) · [Beyond Red-Teaming: Formal Guarantees of LLM Guardrail Classifiers](https://arxiv.org/abs/2605.10901) · [GPTFuzzer: Red Teaming Large Language Models with Auto-Generated Jailbreak Prompts](https://arxiv.org/abs/2309.10253)
- **Bias, Fairness & Robustness**: [Equality of Opportunity in Supervised Learning](https://arxiv.org/abs/1610.02413) · [Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification](http://proceedings.mlr.press/v81/buolamwini18a.html) · [Understanding and Mitigating Tokenization Bias in Language Models](https://arxiv.org/abs/2406.16829) · [On Calibration of Modern Neural Networks](https://arxiv.org/abs/1706.04599)
- **Harmful Content & Misinformation**: [RealToxicityPrompts: Evaluating Neural Toxic Degeneration in Language Models](https://arxiv.org/abs/2009.11462) · [Perspective API](https://perspectiveapi.com/) · [The Pile: An 800GB Dataset of Diverse Text for Language Modeling](https://arxiv.org/abs/2101.00027)
- **Long-term Safety Research**: [Sleeper Agents: Training Deceptive LLMs That Persist Through Safety Training](https://arxiv.org/abs/2401.05566) · [Scalable Oversight](https://www.anthropic.com/research/measuring-progress-on-scalable-oversight-for-large-language-models) · [AI Safety Gridworlds](https://arxiv.org/abs/1711.09883) · [Interpretability in the Wild: a Circuit for Indirect Object Identification in GPT-2 small](https://arxiv.org/abs/2211.00593) · [Towards Guaranteed Safe AI: A Framework for Ensuring Robust and Reliable AI Systems](https://arxiv.org/abs/2405.06624) · [Subliminal Learning: Language Models Transmit Behavioral Traits via Hidden Signals in Data](https://arxiv.org/pdf/2507.14805)

### 🎯 Advanced
- **Automated AI Research**: [The AI Scientist: Towards Fully Automated Open-Ended Scientific Discovery](https://arxiv.org/pdf/2408.06292) · [An AI system to help scientists write expert-level empirical software](https://arxiv.org/pdf/2509.06503) · [AlphaGo Moment for Model Architecture Discovery](https://arxiv.org/pdf/2507.18074)
- **Specialized Applications**: [Stable Audio Open](https://arxiv.org/pdf/2407.14358) · [Breaking the Molecular Dynamics Timescale Barrier Using a Wafer-Scale System](https://arxiv.org/pdf/2405.07898) · [TabPFN: A transformer that solves small tabular classification problems in a second](https://arxiv.org/pdf/2207.01848v3.pdf)
- **Consciousness & AGI**: [Consciousness in Artificial Intelligence: Insights from the Science of Consciousness](https://arxiv.org/pdf/2308.08708v3.pdf) · [If LLMs Have Human-Like Attributes, Then So Does Age of Empires II](https://arxiv.org/abs/2605.31514)

### 🎲 Probabilistic
- **Probabilistic Programming**: [A Probabilistic Programming Approach to Probabilistic Data Analysis](https://papers.nips.cc/paper/6060-a-probabilistic-programming-approach-to-probabilistic-data-analysis.pdf) · [Picture: An Imperative Probabilistic Programming Language for Scene Perception](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Kulkarni_Picture_A_Probabilistic_2015_CVPR_paper.pdf) · [Encapsulating Models and Approximate Inference Programs in Probabilistic Modules](https://arxiv.org/abs/1612.04759) · [Measuring the Non-asymptotic Convergence of Sequential Monte Carlo Samplers using Probabilistic Programming](https://arxiv.org/abs/1612.02161) · [Time Series Structure Discovery via Probabilistic Program Synthesis](https://arxiv.org/abs/1611.07051) · [MCMC using Hamiltonian dynamics](https://arxiv.org/abs/1206.1901)
- **Diffusion Models**: [Why Diffusion Models Don't Memorize: The Role of Implicit Dynamical Regularization in Training](https://arxiv.org/pdf/2505.17638)
- **Generative Models for Vision**: [Approximate Bayesian Image Interpretation using Generative Probabilistic Graphics Programs](http://papers.nips.cc/paper/4881-approximate-bayesian-image-interpretation-using-generative-probabilistic-graphics-programs.pdf) · [A Bayesian Framework for Modeling Intuitive Dynamics](https://cocosci.princeton.edu/tom/papers/collisions.pdf)

### 👁️ Vision & Multimodal
- **Vision Transformers**: [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale (Vision Transformer/ViT)](https://arxiv.org/abs/2010.11929) · [Learning Transferable Visual Models From Natural Language Supervision (CLIP)](https://arxiv.org/abs/2103.00020) · [Segment Anything (SAM)](https://arxiv.org/abs/2304.02643) · [Visualizing and Understanding Convolutional Networks (DeconvNet)](https://arxiv.org/abs/1311.2901) · [Striving for Simplicity: The All Convolutional Net](https://arxiv.org/abs/1412.6806) · [Semantic Segmentation using Adversarial Networks](https://arxiv.org/abs/1611.08408)
- **Multimodal & Speech**: [Visual Instruction Tuning (LLaVA)](https://arxiv.org/abs/2304.08485) · [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](https://arxiv.org/abs/1512.02595)
- **Vision Interpretability**: [Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps](https://arxiv.org/abs/1312.6034) · [Visualizing Deep Neural Network Decisions: Prediction Difference Analysis](https://arxiv.org/abs/1702.04595) · [Synthesizing the Preferred Inputs for Neurons via Deep Generator Networks](https://arxiv.org/abs/1605.09304)

### ⚙️ Hardware & Systems
- **Hardware Considerations**: [Making Deep Learning Go Brrrr From First Principles](https://horace.io/brrr_intro.html) · [Efficiently Scaling Transformer Inference](https://arxiv.org/abs/2211.05102) · [High-dimensional on-chip dataflow sensing and routing using spatial photonic networks](https://www.nature.com/articles/s41566-023-01272-3.pdf) · [A Log-Domain Implementation of the Diffusion Network in Very Large Scale Integration](https://papers.nips.cc/paper_files/paper/2010/file/7bcdf75ad237b8e02e301f4091fb6bc8-Paper.pdf) · [cuGenOpt: A GPU-Accelerated General-Purpose Metaheuristic Framework for Combinatorial Optimization](https://arxiv.org/abs/2603.19163)

### 🧠 Human-AI Interaction
- **Trust, Reliance & Automation Bias**: [Thinking, Fast and Slow](https://us.macmillan.com/books/9780374533557/thinkingfastandslow) · [Humans and Automation: Use, Misuse, Disuse, Abuse](https://journals.sagepub.com/doi/10.1518/001872097778543886) · [Trust in Automation: Designing for Appropriate Reliance](https://journals.sagepub.com/doi/10.1518/hfes.46.1.50_30392) · [Algorithm Aversion: People Erroneously Avoid Algorithms After Seeing Them Err](https://psycnet.apa.org/record/2014-48748-001)
- **Cognitive Effects of AI**: [The Extended Mind](https://academic.oup.com/analysis/article-abstract/58/1/7/153111) · [Cognitive Offloading](https://www.cell.com/trends/cognitive-sciences/abstract/S1364-6613(16) · [Your Brain on ChatGPT: Accumulation of Cognitive Debt when Using an AI Assistant for Essay Writing Task](https://arxiv.org/abs/2506.08872) · [Thinking—Fast, Slow, and Artificial: How AI is Reshaping Human Reasoning and the Rise of Cognitive Surrender](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6097646)
- **Human-AI Decision-Making**: [The Principles and Limits of Algorithm-in-the-Loop Decision Making](https://dl.acm.org/doi/10.1145/3359152) · [Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance](https://arxiv.org/abs/2006.14779) · [To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI in AI-Assisted Decision-Making](https://arxiv.org/abs/2102.09692)

### 📜 Policy & Governance
- **Financial Services & Model Risk Management**: [OCC 2011-12: Supervisory Guidance on Model Risk Management](https://web.archive.org/web/20240616095814/https://www.occ.gov/news-issuances/bulletins/2011/bulletin-2011-12a.pdf) · [SR 11-7: Guidance on Model Risk Management](https://web.archive.org/web/20250103073254/https://www.federalreserve.gov/supervisionreg/srletters/sr1107.htm) · [Model Risk Management Handbook](https://web.archive.org/web/20241220200407/https://occ.gov/publications-and-resources/publications/comptrollers-handbook/files/model-risk-management/index-model-risk-management.html) · [Principles for the Sound Management of Operational Risk](https://www.bis.org/publ/bcbs195.pdf)
- **Data Protection & Privacy Law**: [General Data Protection Regulation (GDPR)](https://gdpr-info.eu/) · [California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA)](https://oag.ca.gov/privacy/ccpa) · [AI and Data Protection Convention (Modernized Convention 108+)](https://www.coe.int/en/web/data-protection/convention108-and-protocol) · [Framework Convention on Artificial Intelligence and Human Rights, Democracy and the Rule of Law (CETS No. 225)](https://www.coe.int/en/web/artificial-intelligence/the-framework-convention-on-artificial-intelligence)
- **AI-Specific Legislation & Executive Action**: [EU Artificial Intelligence Act (Regulation (EU) 2024/1689)](https://eur-lex.europa.eu/eli/reg/2024/1689/oj) · [General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai) · [National AI Initiative Act](https://www.ai.gov/) · [Blueprint for an AI Bill of Rights](https://bidenwhitehouse.archives.gov/ostp/ai-bill-of-rights/) · [Executive Order 14110 on Safe, Secure, and Trustworthy AI](https://www.federalregister.gov/documents/2023/11/01/2023-24283/safe-secure-and-trustworthy-development-and-use-of-artificial-intelligence) · [Executive Order 14179: Removing Barriers to American Leadership in Artificial Intelligence](https://www.federalregister.gov/documents/2025/01/31/2025-02172/removing-barriers-to-american-leadership-in-artificial-intelligence) · [OMB M-25-21: Accelerating Federal Use of AI through Innovation, Governance, and Public Trust](https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf) · [Winning the AI Race: America's AI Action Plan](https://www.ai.gov/action-plan) · [Executive Order 14365: Ensuring a National Policy Framework for Artificial Intelligence](https://www.federalregister.gov/documents/2025/12/16/2025-23092/ensuring-a-national-policy-framework-for-artificial-intelligence) · [California SB 53: Transparency in Frontier Artificial Intelligence Act (TFAIA)](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260SB53) · [California SB 243: Companion Chatbots](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260SB243) · [Texas HB 149: Responsible Artificial Intelligence Governance Act (TRAIGA)](https://capitol.texas.gov/BillLookup/History.aspx?LegSess=89R&Bill=HB149) · [Illinois HB 3773: AI in Employment (amending the Illinois Human Rights Act)](https://www.ilga.gov/Legislation/BillStatus?DocNum=3773&GAID=17&DocTypeID=HB&LegID=157807&SessionID=112) · [Utah SB 149: Artificial Intelligence Policy Act](https://le.utah.gov/~2024/bills/static/SB0149.html) · [Colorado SB 26-189: Automated Decision-Making Technology](https://leg.colorado.gov/bills/sb26-189) · [New York S6953B/A6453B: Responsible AI Safety and Education (RAISE) Act](https://www.nysenate.gov/legislation/bills/2025/S6953) · [China's Generative AI Regulations](http://www.cac.gov.cn/2023-07/13/c_1690898327029107.htm) · [Measures for Labeling AI-Generated Synthetic Content](https://www.cac.gov.cn/2025-03/14/c_1743654684782215.htm) · [Framework Act on Artificial Intelligence Development and Trust Base Creation](https://www.law.go.kr/LSW/eng/engLsSc.do?menuId=2&query=ARTIFICIAL+INTELLIGENCE) · [India AI Governance Guidelines](https://www.indiaai.gov.in/) · [Brazil PL 2338/2023: Proposed AI Framework](https://www25.senado.leg.br/web/atividade/materias/-/materia/157233)
- **Risk Management Frameworks & Standards**: [NIST AI Risk Management Framework (AI RMF)](https://www.nist.gov/itl/ai-risk-management-framework) · [NIST AI 600-1: Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) · [Center for AI Standards and Innovation (CAISI)](https://www.nist.gov/aisi) · [ISO/IEC 42001: AI Management System](https://www.iso.org/standard/81230.html) · [ISO/IEC 42005: AI System Impact Assessment](https://www.iso.org/standard/44545.html) · [ISO/IEC 23053: Framework for AI Systems Using ML](https://www.iso.org/standard/74438.html) · [IEEE 7000 Series on AI Ethics](https://standards.ieee.org/initiatives/autonomous-intelligence-systems/standards/) · [OECD AI Principles](https://oecd.ai/en/ai-principles)
- **Sector-Specific AI Guidance**: [FDA's Artificial Intelligence/Machine Learning (AI/ML) Software as a Medical Device Action Plan](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-aiml-enabled-medical-devices) · [EU Medical Device Regulation (MDR) & In-Vitro Diagnostic Regulation (IVDR)](https://health.ec.europa.eu/medical-devices-new-regulations_en) · [HIPAA Privacy Rule and AI](https://www.hhs.gov/hipaa/index.html) · [EEOC Guidance on AI and Title VII Adverse Impact](https://web.archive.org/web/20240527151347/https://www.eeoc.gov/laws/guidance/select-issues-assessing-adverse-impact-software-algorithms-and-artificial) · [NYC Local Law 144 (Automated Employment Decision Tools)](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page) · [Algorithmic Accountability in Criminal Justice (Various state laws)](https://www.ncsl.org/technology-and-communication/artificial-intelligence-2025-legislation)
- **Dual-Use AI & National Security**: [Dual-User Foundation Models with Widely Available Model Weights](https://www.ntia.gov/sites/default/files/publications/ntia-ai-open-model-report.pdf) · [Export Controls on AI & Emerging Technologies](https://www.bis.doc.gov/index.php/policy-guidance/advanced-computing-and-semiconductor-manufacturing-items) · [NSCAI Final Report](https://web.archive.org/web/20240104154550/https://www.nscai.gov/2021-final-report/) · [Blueprint for an AI Bill of Rights Concerning National Security Systems](https://www.dni.gov/index.php/newsroom/reports-publications)
- **Responsible AI & Industry Best Practices**: [Partnership on AI Guidelines](https://partnershiponai.org/) · [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) · [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) · [AI Incident Database](https://incidentdatabase.ai/) · [Microsoft Responsible AI Standard](https://www.microsoft.com/en-us/ai/responsible-ai) · [Google's AI Principles](https://ai.google/responsibility/principles/)
<!-- COVERAGE:END -->

---

## 🤝 Contributing

We welcome contributions! There are many ways to help:

| Contribution Type | How to Help |
|-------------------|-------------|
| 📄 **Suggest Papers** | [Open an issue](../../issues/new?template=paper-suggestion.yml) with paper details |
| 🔗 **Fix Broken Links** | [Report](../../issues/new?template=broken-link.yml) or submit a PR |
| 📖 **Improve Glossary** | [Suggest terms](../../issues/new?template=glossary-term.yml) or definitions |
| ✏️ **Better Annotations** | Improve "Why" explanations via PR |
| 💬 **Discuss Papers** | Join [Discussions](../../discussions) |

**📋 [Read the full Contributing Guide](CONTRIBUTING.md)** for detailed instructions, paper selection criteria, and style guidelines

---

## 📚 Additional Resources

### Related Collections
- [Papers We Love](https://github.com/papers-we-love/papers-we-love) - Classic CS papers
- [Awesome Deep Learning Papers](https://github.com/terryum/awesome-deep-learning-papers) - DL fundamentals
- [ML Papers of The Week](https://github.com/dair-ai/ML-Papers-of-the-Week) - Weekly updates

### Tools & Platforms
- [arXiv](https://arxiv.org/) - Preprint repository
- [Papers With Code](https://paperswithcode.com/) - Papers + implementations
- [Semantic Scholar](https://www.semanticscholar.org/) - AI-powered paper search
- [Connected Papers](https://www.connectedpapers.com/) - Visual paper exploration

### Conference Deadlines
- 🎓 **[AI Deadlines](https://aideadlin.es/?sub=ML,CV,CG,NLP,RO,SP,DM,AP,KR,HCI)** - Track ML/AI conference submissions

---

## 📄 License

The curation, organization, and annotations in this repository are licensed under the [Apache License 2.0](LICENSE).

The linked papers themselves remain under their original licenses and copyrights held by their authors and publishers; this repository only links to them.

---

## 🙏 Acknowledgments

Papers compiled from:
- Major AI/ML conferences (NeurIPS, ICML, ICLR, CVPR, ACL, etc.)
- Leading research institutions and labs
- arXiv preprint server
- Open access initiatives

Special thanks to the researchers, authors, and institutions making their work freely available.

---

## 📬 Contact & Feedback

Found this helpful? Have suggestions? Want to discuss a paper?

- **Issues**: [Open an issue](../../issues) for bugs, suggestions, or paper recommendations
- **Discussions**: [Start a discussion](../../discussions) for paper analysis or learning questions

---

**Happy Reading! 📖🚀**

*Building knowledge, one paper at a time.*
