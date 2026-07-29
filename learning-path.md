# Learning Path: AI/ML Research Curriculum

A structured curriculum organizing papers from this collection. Content is organized by **topic areas** (browse by interest); **tracks** are curated reading sequences for specific goals.

---

## 📚 How to Use This Learning Path

This collection is organized in two complementary ways:

- **Areas** = Topic-based paper collections. No implied order—browse any area based on your interests. Each area is in its own file.
- **Tracks** = Curated reading sequences that suggest an order across areas for a given goal (e.g., "ML Engineer," "Safety Specialist").

You can **follow a track** for a guided path, **jump to specific areas** based on interest, or **mix both**.

---

## Table of Contents

### Core Areas

- **[Foundations (Start Here)](learning/foundations.md)**
  - Deep Learning Basics
  - Word Embeddings & Representations
  - Sequence Models
  - Generative Models
  - Tokenization & Subword Models

- **[Large Language Models](learning/language-models.md)**
  - LLM Foundations (Transformers, BERT, GPT-3)
  - Training at Scale (Megatron, ZeRO)
  - Memory & Efficiency Optimizations

- **[Attention Mechanisms & Context](learning/attention.md)**
  - Efficient Attention (FlashAttention, RetNet)
  - Long Context & Compression

- **[Retrieval & Knowledge Systems](learning/retrieval.md)**
  - Retrieval-Augmented Generation (RAG)
  - Federated & Distributed Learning

- **[Reasoning & Agents](learning/reasoning.md)**
  - Teaching Models to Reason (RLHF, PPO, ReAct)
  - Agentic Systems

- **[Novel Architectures & Theory](learning/architectures.md)**
  - Alternative Architectures (RWKV, KAN)
  - Theoretical Foundations (Neural Tangent Kernel)

- **[Interpretability & Evaluation](learning/interpretability.md)**
  - Understanding Model Behavior
  - Model Evaluation & Robustness (TruthfulQA)

- **[Security, Safety & Robustness](learning/safety.md)**
  - AI Alignment & Safety Training (InstructGPT, Constitutional AI)
  - Security Threats & Attacks (jailbreaking, prompt injection)
  - Safety Evaluation & Red Teaming
  - Bias, Fairness & Robustness
  - Harmful Content & Misinformation
  - Long-term Safety Research

- **[Advanced Topics & Applications](learning/advanced.md)**
  - Automated AI Research
  - Specialized Applications
  - Consciousness & AGI

### Specialized Areas

- **[Probabilistic & Bayesian Approaches](learning/probabilistic.md)**
  - Probabilistic Programming
  - Diffusion Models
  - Generative Models for Vision

- **[Vision & Multimodal Systems](learning/vision.md)**
  - Vision Transformers (ViT, CLIP, SAM)
  - Multimodal & Speech
  - Vision Interpretability

- **[Hardware & Systems](learning/hardware.md)**
  - Hardware Considerations (GPU optimization, inference scaling, photonics)

- **[Human-AI Interaction & Cognition](learning/human-ai-interaction.md)**
  - Trust, Reliance & Automation Bias
  - Cognitive Effects of AI
  - Human-AI Decision-Making

- **[Policy, Safety & Societal Impact](learning/policy.md)**
  - Financial Services & Model Risk Management (OCC 2011-12, SR 11-7)
  - Data Protection & Privacy Law (GDPR, CCPA, CoE Framework Convention)
  - AI-Specific Legislation (EU AI Act, US federal executive orders, US state laws, Korea, China)
  - Risk Management Frameworks (NIST AI RMF, ISO/IEC Standards)
  - Sector-Specific Guidance (Healthcare, Employment, Criminal Justice)
  - Dual-Use AI & National Security
  - Responsible AI & Industry Best Practices
  - Practical Compliance Tools & Resources

---

## 🎯 Recommended Tracks

Tracks suggest an order across areas for different goals. Pick one that fits your role or goal, then follow the listed areas in sequence (or skip around as needed).

### Comprehensive Track
Full curriculum in a logical order: [Foundations](learning/foundations.md) → [Language Models](learning/language-models.md) → [Attention](learning/attention.md) → [Retrieval](learning/retrieval.md) → [Reasoning](learning/reasoning.md) → [Architectures](learning/architectures.md) → [Interpretability](learning/interpretability.md) → [Safety](learning/safety.md) → [Advanced](learning/advanced.md) → [Probabilistic](learning/probabilistic.md) → [Vision](learning/vision.md) → [Hardware](learning/hardware.md) → [Human-AI Interaction](learning/human-ai-interaction.md) → [Policy](learning/policy.md).

### For Beginners
Start with [Foundations](learning/foundations.md) and [Language Models — LLM Foundations](learning/language-models.md#llm-foundations), then explore based on interests.

### ML Practitioner Track
[Language Models](learning/language-models.md) → [Attention](learning/attention.md) → [Reasoning](learning/reasoning.md) → [Interpretability](learning/interpretability.md). Add [Retrieval](learning/retrieval.md) and [Safety](learning/safety.md) for production-focused work.

### Researcher Track
Follow the Comprehensive track but focus deeply on [Architectures](learning/architectures.md), [Interpretability](learning/interpretability.md), [Advanced](learning/advanced.md), and your area of interest.

### Engineer Track
Prioritize [Language Models](learning/language-models.md), [Attention](learning/attention.md), [Interpretability](learning/interpretability.md), [Safety](learning/safety.md), and [Hardware](learning/hardware.md).

### Security Specialist Track
[Foundations](learning/foundations.md) and [Language Models](learning/language-models.md) for basics, then deep dive into [Safety](learning/safety.md). Add [Interpretability](learning/interpretability.md) and [Policy](learning/policy.md) for full coverage.

---

## 📖 Notes on Learning

- **Start with the abstract and the "Why" annotation**: Understand the core contribution and its context before diving into the paper
- **Check the [📖 Glossary](learning/glossary.md)** whenever you hit an unfamiliar term
- **Don't read linearly**: Papers build on each other, so refer back to earlier papers as needed
- **Implement as you learn**: Try to implement key concepts from papers
- **Join study groups**: Discuss papers with others
- **Take notes**: Summarize key insights and connections between papers
- **Focus on intuition first**: Understand the "why" before diving into mathematical details
- **Revisit papers**: Papers reveal more insights on second or third readings

---

## 🔗 Additional Resources

- **[📖 Glossary](learning/glossary.md)** - Comprehensive definitions of terms, concepts, and acronyms
- **Full Chronological List**: [by-date.md](by-date.md)
- **Topical Summary**: [README.md](README.md)
- **Academic Conference Deadlines**: [AI Deadlines](https://aideadlin.es/?sub=ML,CV,CG,NLP,RO,SP,DM,AP,KR,HCI)

---

## 🚀 Quick Start

**New to AI/ML?** → Start with [Foundations](learning/foundations.md)

**Have ML background?** → Jump to [Large Language Models](learning/language-models.md)

**Looking for specific topics?** → Use the TOC above to navigate by area

**Want to build agents?** → Focus on [Reasoning & Agents](learning/reasoning.md)

**Interested in safety?** → Head to [Security, Safety & Robustness](learning/safety.md)
