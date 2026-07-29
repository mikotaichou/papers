# Attention Mechanisms & Context

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Language Models](language-models.md) | [Retrieval](retrieval.md)

**Overview**: While [transformers](glossary.md#transformer) are powerful, their quadratic memory and compute complexity with sequence length creates significant bottlenecks. This area explores ingenious solutions to make [attention](glossary.md#attention-mechanism) more efficient—from [FlashAttention](glossary.md#flashattention)'s IO-aware algorithms that dramatically speed up training, to architectural innovations like linear attention and state-space models that achieve sub-quadratic scaling. These advances are critical for processing long documents, reducing costs, and enabling real-time applications, representing some of the most active areas of current research.

## Efficient Attention
**Goal**: Understand and optimize the core attention mechanism

1. [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/abs/2205.14135) (Dao et al., 2022)
   - *Why*: **Foundational for modern efficient training** - IO-aware attention algorithm that's 3x faster and enables longer context

2. [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://arxiv.org/abs/2307.08691) (Dao, 2023)
   - *Why*: **The production standard** - 2x faster than FlashAttention through improved parallelism and reduced non-matmul FLOPs; de facto attention implementation in modern LLM training and inference

3. [Retentive Network: A Successor to Transformer for Large Language Models](https://arxiv.org/abs/2307.08621) (Sun et al., 2023)
   - *Why*: **Triple-paradigm sequence modeling** - introduces retention, a mechanism that supports parallel training (like transformers), recurrent O(1) inference (like RNNs), and chunked hybrid computation; achieves training parallelism and low-cost autoregressive decoding simultaneously, addressing the fundamental efficiency-quality tradeoff in sequence models

4. [Efficient streaming language models with attention sinks](https://arxiv.org/pdf/2309.17453.pdf) (2023)
   - *Why*: **Attention sink discovery** - reveals that LLMs allocate disproportionate attention to initial tokens regardless of semantic relevance, causing failures when those tokens leave the KV cache window; fixes this by retaining a few "sink" tokens alongside the sliding window, enabling stable generation over arbitrarily long sequences with bounded memory

5. [Leave No Context Behind: Efficient Infinite Context Transformers with Infini-attention](https://arxiv.org/pdf/2404.07143v1.pdf) (2024)
   - *Why*: **Compressive memory for unbounded context** - augments standard attention with a compressive memory that accumulates information from discarded KV cache segments; blends local fine-grained attention with a global compressed summary using a learned gating mechanism; enables processing of million-token inputs with bounded memory and compute

6. [Native Sparse Attention: Hardware-Aligned and Natively Trainable Sparse Attention](https://arxiv.org/abs/2502.11089) (2025)
   - *Why*: **Trainable sparse attention aligned to GPU hardware** - designs sparsity patterns that map directly to GPU memory hierarchies and tensor core operations, avoiding the overhead of unstructured sparse kernels; trains the sparsity pattern end-to-end rather than applying it post-hoc; maintains dense-attention quality at a fraction of the compute cost for long sequences

7. [SSA: Sparse Sparse Attention by Aligning Full and Sparse Attention Outputs in Feature Space](https://arxiv.org/abs/2511.20102) (Shen et al., 2025)
   - *Why*: **Bridges the sparse/full attention divide** - diagnoses the *attention gap* (sparse inference on full-attention-trained models degrades quality) and the *capability gap* (pure sparse training loses gradient signal), then jointly trains both modes with bidirectional output alignment in feature space; theory bounds the approximation error linearly in the dropped attention mass, and a single trained model adapts to variable sparsity levels at inference, excelling on long-context inputs

## Long Context & Compression
**Goal**: Handle longer sequences efficiently

1. [TriForce: Lossless Acceleration of Long Sequence Generation with Hierarchical Speculative Decoding](https://arxiv.org/pdf/2404.11912v1.pdf) (2024)
   - *Why*: **Hierarchical speculative decoding** - uses a two-level draft-verify pipeline where a lightweight model proposes tokens and a retrieval-based system verifies against the full KV cache; achieves lossless (identical output) speedups of up to 2.3x on long-context generation by reducing the number of full-model forward passes

2. [DeepSeek-OCR: Contexts Optical Compression](https://arxiv.org/pdf/2510.18234) (2025)
   - *Why*: **2D optical context compression** - maps sequential token representations into 2D image-like structures and applies vision-style compression to reduce context length; preserves semantic content while drastically cutting the number of tokens the LLM must attend over; bridges techniques from image compression and language modeling for efficient long-context processing

3. [Agentic Context Engineering: Evolving Contexts for Self-Improving Language Models](https://arxiv.org/abs/2510.04618) (2025)
   - *Why*: **Evolutionary context optimization** - treats the LLM's context (system prompts, few-shot examples, instructions) as a mutable artifact that an agent iteratively refines through evaluation and selection; demonstrates self-improving performance without weight updates by evolving the prompt environment; formalizes context engineering as an optimization problem

4. [Recursive Language Models](https://arxiv.org/abs/2512.24601) (Zhang et al., 2025)
   - *Why*: **Scales context beyond model limits** - treats long prompts as external environment, allowing LLMs to programmatically examine and recursively call themselves over snippets; handles inputs up to two orders of magnitude beyond context windows while maintaining quality

---

**Related**: [Language Models](language-models.md) | [Retrieval](retrieval.md) | [Architectures](architectures.md)
