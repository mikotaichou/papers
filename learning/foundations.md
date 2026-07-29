# Foundations (Start Here)

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Language Models](language-models.md)

**Overview**: This area establishes the essential groundwork for understanding modern AI systems. You'll explore the fundamental principles of [deep learning](glossary.md#deep-learning), from basic neural network architectures to the revolutionary [transformer](glossary.md#transformer) model that underpins nearly all current LLMs. By mastering these foundational concepts—including training dynamics, [attention mechanisms](glossary.md#attention-mechanism), and the shift from convolutional to attention-based architectures—you'll build the technical vocabulary and intuition needed for everything that follows. Think of this as learning the alphabet before reading literature.

## Deep Learning Basics
**Goal**: Understand the fundamental building blocks of modern deep learning

1. 🔒 [Deep Learning (Nature Review)](https://www.nature.com/articles/nature14539) (LeCun, Bengio, Hinton, 2015)
   - *Why*: The canonical overview of deep learning principles - start here for the big picture
   - *Note*: Paywalled - Nature journal article
   
2. [Understanding the Difficulty of Training Deep Feedforward Neural Networks](https://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf) (Glorot & Bengio, 2010)
   - *Why*: Introduces [Xavier initialization](glossary.md#xavier-initialization) and explains training challenges; foundational for understanding why deep networks are hard to train

3. [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://arxiv.org/abs/1502.03167) (Ioffe & Szegedy, 2015)
   - *Why*: Essential technique for stable, fast training; enables much deeper networks

4. [Gradient-Based Learning Applied to Document Recognition (LeNet)](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf) (1997)
   - *Why*: **The original convolutional neural network** - introduces learnable convolutional filters, pooling layers, and end-to-end backpropagation training for image recognition; demonstrated real-world deployment reading millions of checks at banks; established the CNN blueprint that every subsequent architecture builds upon

5. [ImageNet Classification with Deep Convolutional Neural Networks (AlexNet)](https://papers.nips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) (2012)
   - *Why*: **Sparked the deep learning revolution** - won ImageNet 2012 by a massive margin (top-5 error 15.3% vs. 26.2%), proving that deep CNNs trained on GPUs dramatically outperform traditional feature engineering; introduced ReLU activations, dropout regularization, and GPU-parallel training that became standard practice
   
6. [Going Deeper with Convolutions (GoogLeNet)](https://arxiv.org/abs/1409.4842) (2014)
   - *Why*: **Inception modules for multi-scale feature extraction** - processes input through parallel convolutions of different kernel sizes (1x1, 3x3, 5x5) and pools results, capturing features at multiple spatial scales simultaneously; achieves state-of-the-art accuracy with 12x fewer parameters than AlexNet through aggressive architectural efficiency

7. [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) (2015)
   - *Why*: **Skip connections that enable extreme depth** - introduces residual learning where layers learn residual functions F(x) + x rather than direct mappings; solves the degradation problem that prevented training networks beyond ~20 layers; won ImageNet 2015 with 152-layer networks and became the default building block for virtually all deep architectures

8. [Identity Mappings in Deep Residual Networks](https://arxiv.org/abs/1603.05027) (He et al., 2016)
   - *Why*: **Refines ResNet architecture** - analyzes and improves residual connections; shows how identity mappings enable training of very deep networks

9. [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122) (Yu & Koltun, 2016)
   - *Why*: **Dilated convolutions for dense prediction** - enables exponential expansion of receptive field without losing resolution; foundational for semantic segmentation and dense prediction tasks

10. [The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks](https://arxiv.org/abs/1803.03635) (Frankle & Carbin, ICLR 2019)
    - *Why*: **Fundamental insight into network initialization and sparsity** - demonstrates that dense networks contain sparse "winning ticket" subnetworks that can train to full accuracy from initialization; reveals the critical importance of weight initialization for trainability; foundational for understanding why pruning works and how to design efficient architectures
    - *Key insight*: Standard pruning naturally uncovers subnetworks whose initializations made them capable of training effectively; these winning tickets are typically 10-20% of the original network size
    - *Impact*: Sparked extensive research into sparse training, initialization strategies, and understanding what makes networks trainable

## Word Embeddings & Representations
**Goal**: Learn how words become vectors - the bridge between discrete symbols and continuous neural networks

**Why this matters**: Before transformers, before tokenization strategies, there was a fundamental question: how do we represent words as numbers that neural networks can process? [Word embeddings](glossary.md#embeddings) revolutionized NLP by learning dense vector representations that capture semantic relationships (e.g., "king" - "man" + "woman" ≈ "queen"). Understanding embeddings is crucial for grasping why modern LLMs work - they're doing something far more sophisticated than simple lookup tables.

1. [Efficient Estimation of Word Representations in Vector Space (Word2Vec)](https://arxiv.org/abs/1301.3781) (Mikolov et al., 2013)
   - *Why*: **THE foundational paper** - introduces Skip-gram and CBOW architectures for learning word embeddings; demonstrates that simple neural models can capture semantic and syntactic relationships through distributed representations
   - *Key insight*: Learn word vectors by predicting context words (Skip-gram) or predicting a word from context (CBOW); resulted in famous analogies like "king - man + woman = queen"
   - *Impact*: Trained on 1.6B words in <1 day; state-of-the-art word similarity performance; sparked the embeddings revolution

2. [GloVe: Global Vectors for Word Representation](https://aclanthology.org/D14-1162/) (Pennington et al., EMNLP 2014)
   - *Why*: Alternative approach that combines global matrix factorization (like LSA) with local context windows (like Word2Vec); often outperforms Word2Vec on certain tasks
   - *Key innovation*: Instead of just predicting context, learn embeddings that directly encode the ratio of word co-occurrence probabilities
   - *Philosophy*: "You shall know a word by the company it keeps" - but capture global statistics rather than just local context

3. [Sequence to Sequence Learning with Neural Networks](https://arxiv.org/abs/1409.3215) (Sutskever et al., 2014)
   - *Why*: Introduces the encoder-decoder architecture that became the template for modern transformers; shows how to map sequences to sequences using neural networks
   - *Key insight*: Use one LSTM to encode the input sequence into a fixed-size vector, then another LSTM to decode the output sequence; reversing input order helps with long sequences
   - *Impact*: Achieved breakthrough results on machine translation (BLEU 34.8 on WMT'14 EN→FR); laid the groundwork for attention mechanisms

4. [Pointer Networks](https://arxiv.org/abs/1506.03134) (Vinyals et al., 2015)
   - *Why*: **Addresses variable-length output sequences** - uses attention to point to input positions rather than generating from vocabulary; essential for tasks like sorting, convex hull, and combinatorial optimization

**Key Concepts to Understand**:
- **[Static vs. Contextual Embeddings](glossary.md#static-embeddings)**: Word2Vec/GloVe produce one vector per word type (static); transformers produce different vectors based on context (contextual)
- **[Skip-gram vs. CBOW](glossary.md#skip-gram)**: Skip-gram predicts context from word; CBOW predicts word from context
- **[Distributional Hypothesis](glossary.md#distributional-hypothesis)**: "Words that occur in similar contexts tend to have similar meanings"
- **[Encoder-Decoder Architecture](glossary.md#encoder-decoder-architecture)**: Pattern of compressing input → fixed representation → generate output
- **Why embeddings matter**: They convert discrete symbols into continuous space where semantic operations become geometric

**The Evolution**:
- **2013**: Word2Vec shows neural embeddings work amazingly well
- **2014**: GloVe and Seq2Seq show different ways to capture meaning
- **2017**: Transformers ([Language Models](language-models.md)) make embeddings contextual via attention
- **2018+**: BERT, GPT show that contextual embeddings are far more powerful

**Bridge to Modern LLMs**: 
The embeddings in GPT-4 or Claude aren't just fancy Word2Vec - they're contextual representations computed through layers of attention. But Word2Vec taught us the fundamental insight: meaning lives in high-dimensional geometry. Every modern LLM starts with an embedding layer that converts tokens to vectors, then transforms those vectors through attention layers.

## Sequence Models
**Goal**: Learn how to model sequential data

1. 🔒 [Long Short-Term Memory (LSTM)](https://www.researchgate.net/publication/13853244_Long_Short-term_Memory) (1997)
   - *Why*: Revolutionary architecture for sequence modeling; still widely used
   - *Note*: Paywalled - MIT Press Neural Computation journal

2. [Recurrent Neural Network Regularization](https://arxiv.org/abs/1409.2329) (Zaremba et al., 2014)
   - *Why*: **Dropout for RNNs** - introduces dropout regularization techniques specifically designed for recurrent networks; essential for training stable RNNs

3. [MOMENT: A Family of Open Time-series Foundation Models](https://arxiv.org/pdf/2402.03885) (2024)
   - *Why*: **Foundation models for time-series** - pre-trains a transformer on diverse public time-series datasets to create a general-purpose representation; achieves strong zero-shot and few-shot performance on forecasting, classification, and anomaly detection without task-specific architectures; demonstrates that the foundation model paradigm transfers from language and vision to temporal data

## Generative Models
**Goal**: Understand how to generate new data

1. [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) (2014)
   - *Why*: **Adversarial training paradigm** - introduces the generator-discriminator game where two networks compete: one generates samples, the other distinguishes real from fake; eliminates the need for explicit density estimation or intractable inference; spawned an entire subfield of generative modeling and is foundational to understanding modern image, video, and audio synthesis

2. [Variational Lossy Autoencoder](https://arxiv.org/abs/1611.02731) (Chen et al., 2016)
   - *Why*: **Connects VAEs and information theory** - shows how variational autoencoders can learn lossy compression; important for understanding generative models and representation learning

3. [Dualscale Diffusion: Adaptive Feature Balancing for Low-Dimensional Generative Models](https://sakana.ai/assets/ai-scientist/adaptive_dual_scale_denoising.pdf) (2024)
   - *Why*: **Dual-scale denoising for low dimensions** - addresses the failure of standard diffusion models on low-dimensional data by adaptively balancing coarse and fine-grained features during denoising; notably one of the first papers generated by the AI Scientist system, demonstrating automated research pipelines producing publishable contributions

## Tokenization & Subword Models
**Goal**: Understand how text is broken into tokens - the bridge between raw text and neural networks

**Why this matters**: Before any language model can process text, it must convert words into tokens. This seemingly simple step profoundly impacts model performance, vocabulary size, and the ability to handle rare words, different languages, and out-of-vocabulary terms. Understanding tokenization is essential for grasping why LLMs behave the way they do with certain inputs.

1. [Neural Machine Translation of Rare Words with Subword Units (BPE)](https://arxiv.org/abs/1508.07909) (Sennrich et al., 2016)
   - *Why*: **The foundational paper** - introduces Byte Pair Encoding (BPE) for NMT; learns to segment words into subword units that balance vocabulary size with representation power. This is the "Rosetta Stone" for understanding how modern LLMs handle text.
   - *Key insight*: Instead of having a fixed word vocabulary, iteratively merge the most frequent character/subword pairs to create a learned vocabulary

2. [SentencePiece: A simple and language independent subword tokenizer and detokenizer](https://arxiv.org/abs/1808.06226) (Kudo & Richardson, 2018)
   - *Why*: Makes tokenization truly language-agnostic by treating text as raw Unicode; implements both BPE and Unigram tokenization; used in T5, ALBERT, XLNet, and many multilingual models
   - *Key innovation*: No need for pre-tokenization (word splitting) - works directly on raw text

3. [Greed is All You Need: An Evaluation of Tokenizer Inference Methods](https://arxiv.org/abs/2403.01289) (2024)
   - *Why*: Modern analysis of how different tokenization inference strategies affect model performance; shows greedy tokenization is surprisingly effective
   - *Practical relevance*: Understanding tokenizer inference helps debug unexpected model behavior

4. [Understanding and Mitigating Tokenization Bias in Language Models](https://arxiv.org/abs/2406.16829) (2024)
   - *Why*: Reveals how tokenization introduces systematic biases that affect model fairness and performance across languages
   - *Critical insight*: Tokenization isn't neutral - it can amplify biases and hurt underrepresented languages

5. [Bytes Are All You Need: Transformers Operating Directly On File Bytes](https://arxiv.org/pdf/2306.00238) (2023)
   - *Why*: Explores byte-level tokenization for truly language-agnostic models; eliminates tokenization entirely by operating on raw bytes

**Key Concepts to Understand**:
- **[Byte Pair Encoding (BPE)](glossary.md#bpe-byte-pair-encoding)**: Bottom-up approach starting from characters
- **[WordPiece](glossary.md#wordpiece)**: Used by BERT; similar to BPE but optimizes likelihood
- **Unigram**: Top-down approach used in [SentencePiece](glossary.md#sentencepiece)
- **[Vocabulary](glossary.md#vocabulary) size tradeoffs**: Larger vocab = longer training but better rare word handling
- **Byte-level BPE**: Used by GPT-2/3/4; ensures any text can be [tokenized](glossary.md#tokenization)

**Common Pitfalls**:
- Same word tokenized differently in different contexts (e.g., "running" vs " running")
- Numbers and code often tokenized suboptimally
- Language-specific issues (agglutinative languages suffer most)
- Whitespace handling varies between tokenizers

---

**Related**: [Language Models](language-models.md) | [Attention](attention.md)
