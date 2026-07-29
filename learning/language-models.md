# Large Language Models

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Foundations](foundations.md) | [Attention](attention.md)

**Overview**: This area traces the explosive evolution of language models from [BERT](glossary.md#bert-bidirectional-encoder-representations-from-transformers)'s bidirectional pretraining breakthrough to [GPT](glossary.md#gpt-generative-pre-trained-transformer)-3's massive scale demonstration. You'll learn how the field discovered that [pre-training](glossary.md#pre-training) on vast amounts of text data creates models with remarkable [few-shot learning](glossary.md#few-shot-learning) abilities, and how different pretraining objectives (masked language modeling vs. autoregressive) lead to different capabilities. This progression from BERT to GPT-3 to instruction-tuned models forms the backbone of modern NLP and sets the stage for understanding today's ChatGPT-style systems.

## LLM Foundations
**Goal**: Understand transformer architecture and pre-training

1. [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473) (Bahdanau et al., 2014)
   - *Why*: **Introduces attention mechanism** - the foundational paper that introduced attention for sequence-to-sequence models; paved the way for transformers

2. [Attention Is All You Need](https://arxiv.org/abs/1706.03762) (Vaswani et al., 2017)
   - *Why*: **THE foundational transformer paper** - introduces self-attention, multi-head attention, and the transformer architecture that powers all modern LLMs

3. [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) (Devlin et al., 2019)
   - *Why*: Introduces masked language modeling and bidirectional pre-training; revolutionized NLP fine-tuning

4. [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361) (Kaplan et al., 2020)
   - *Why*: **Empirical scaling laws** - establishes predictable relationships between model size, dataset size, compute, and performance; foundational for understanding how to scale LLMs effectively

5. [Language Models are Few-Shot Learners (GPT-3)](https://arxiv.org/abs/2005.14165) (Brown et al., 2020)
   - *Why*: Demonstrates emergent abilities at scale; introduces in-context learning and few-shot prompting

6. [ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators](https://arxiv.org/abs/2003.10555) (2020)
   - *Why*: Efficient alternative to masked language modeling; achieves BERT-level performance with less compute

7. [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783) (2024)
   - *Why*: State-of-the-art open-source LLMs; demonstrates continued scaling benefits and instruction-tuning techniques

8. [OpenELM: An Efficient Language Model Family with Open-source Training and Inference Framework](https://arxiv.org/pdf/2404.14619) (2024)
   - *Why*: **Fully open LLM pipeline** - releases training code, data, weights, and evaluation logs for complete reproducibility; uses layer-wise scaling to allocate parameters non-uniformly across transformer layers for better accuracy per FLOP

9. [EuroLLM: Multilingual Language Models for Europe](https://arxiv.org/pdf/2409.11741) (2024)
   - *Why*: **Multilingual-first pretraining** - trains LLMs on all official EU languages plus additional high-resource languages with carefully curated data mixtures; demonstrates that balanced multilingual pretraining avoids the "curse of multilinguality" capacity dilution seen in English-centric models with multilingual fine-tuning

## Training at Scale
**Goal**: Learn how to train massive models efficiently

1. [GPipe: Easy Scaling with Micro-Batch Pipeline Parallelism](https://arxiv.org/abs/1811.06965) (Huang et al., 2019)
   - *Why*: **Pipeline parallelism foundation** - enables training of very large models by splitting across devices with micro-batching; essential for scaling beyond single-device memory limits

2. [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053) (2019)
   - *Why*: **Intra-layer model parallelism** - partitions transformer attention heads and MLP columns across GPUs without requiring new communication primitives; achieves 76% scaling efficiency at 8.3B parameters on 512 GPUs; established the practical blueprint for distributed LLM training

3. [ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/abs/1910.02054) (2019)
   - *Why*: **Eliminating memory redundancy in data parallelism** - partitions optimizer states, gradients, and parameters across data-parallel ranks to reduce per-device memory by up to 8x; enables training models with over 100B parameters without model parallelism; foundational technique used in DeepSpeed and most modern training frameworks

4. [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473) (2021)
   - *Why*: **3D parallelism at trillion scale** - combines tensor, pipeline, and data parallelism into a unified framework; analyzes interaction effects between parallelism strategies on communication overhead and memory; achieves 52% compute efficiency training a 1T-parameter model across thousands of GPUs

5. [The Potential of Second-Order Optimization for LLMs: A Study with Full Gauss-Newton](https://arxiv.org/pdf/2510.09378) (2025)
   - *Why*: **Second-order methods revisited for LLMs** - makes full Gauss-Newton optimization tractable at LLM scale through careful implementation; shows curvature-aware updates converge in fewer steps than Adam on language modeling tasks; quantifies the gap between first- and second-order methods to motivate future optimizer research

6. [MegaTrain: Full Precision Training of 100B+ Parameter Large Language Models on a Single GPU](https://arxiv.org/abs/2604.05091) (Yuan et al., 2026)
   - *Why*: Stores parameters and optimizer states in host memory and treats the GPU as a transient compute engine, using pipelined double-buffered execution across CUDA streams and stateless layer templates in place of a persistent autograd graph; trains up to 120B parameters full precision on a single H200 and achieves 1.84× the throughput of DeepSpeed ZeRO-3 with CPU offloading at 14B.

## Memory & Efficiency Optimizations
**Goal**: Make models faster and more memory-efficient

1. [Cut Your Losses in Large-Vocabulary Language Models](https://arxiv.org/abs/2411.09009) (2024)
   - *Why*: **Chunked cross-entropy loss** - eliminates the massive logit matrix that dominates memory in large-vocabulary models by computing loss in small chunks; reduces peak memory by up to 7x for vocabularies of 128K+ tokens with no accuracy loss; directly enables longer sequences and larger batch sizes on existing hardware

2. [Scalable MatMul-free Language Modeling](https://arxiv.org/pdf/2406.02528) (2024)
   - *Why*: **Removing matrix multiplications entirely** - replaces all MatMul operations in transformers with ternary weight operations and element-wise Hadamard products; matches transformer quality at billion-parameter scale while drastically reducing compute and memory requirements; demonstrates a viable path toward hardware-efficient LLMs on custom accelerators

3. [The Era of 1-bit LLMs: All Large Language Models are in 1.58 Bits](https://arxiv.org/pdf/2402.17764) (2024)
   - *Why*: **Ternary weight LLMs from scratch** - trains BitNet b1.58 with weights constrained to {-1, 0, 1}, matching full-precision LLM perplexity and task performance at 3B parameters; reduces memory footprint by 3.5x and increases throughput by 2.7x; replaces multiplication with addition for energy-efficient inference

4. [TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate](https://arxiv.org/abs/2504.19874) (Zandieh et al., 2025)
   - *Why*: **Near-optimal data-oblivious vector quantization** - achieves within ~2.7× of information-theoretic distortion limits using randomized rotations and optimal scalar quantizers per coordinate; preserves KV cache quality at 3.5 bits per channel and outperforms product quantization for nearest neighbor search, providing a principled low-bit compression primitive for inference.

5. [Do LLMs Benefit From Their Own Words?](https://arxiv.org/abs/2602.24287) (Huang et al., 2026)
   - *Why*: Shows that omitting prior assistant responses in multi-turn context often preserves quality while cutting context length; identifies context pollution and motivates selective context filtering.

6. [DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation](https://arxiv.org/abs/2607.05147) (Cheng et al., 2026)
   - *Why*: **Load-aware speculative decoding** - couples a parallel drafter with a lightweight sequential module (semi-autoregressive) to add intra-block dependencies and slow acceptance decay, then confidence-schedules verification length per request; deployed in DeepSeek-V4 serving, it lifts per-user generation speed 60–85% at matched throughput.

---

**Related**: [Foundations](foundations.md) | [Attention](attention.md) | [Retrieval](retrieval.md)
