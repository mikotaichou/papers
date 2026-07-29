# AI/ML Glossary

[← Back to Learning Path](../learning-path.md)

A comprehensive glossary of terms, concepts, and acronyms used throughout the learning path. Terms are organized alphabetically within categories for easy reference.

---

## Table of Contents

- [Core Concepts](#core-concepts)
- [Architectures & Models](#architectures--models)
- [Training & Optimization](#training--optimization)
- [Attention Mechanisms](#attention-mechanisms)
- [Natural Language Processing](#natural-language-processing)
- [Interpretability & Evaluation](#interpretability--evaluation)
- [Security & Safety](#security--safety)
- [Systems & Hardware](#systems--hardware)
- [Applications & Domains](#applications--domains)
- [Acronyms Quick Reference](#acronyms-quick-reference)
- [Cross-References](#cross-references)

---

## Core Concepts

### Activation Function
A mathematical function applied to a neuron's output that introduces non-linearity into neural networks. Common examples include ReLU, sigmoid, and tanh. Without activation functions, neural networks would just be linear transformations.

### Backpropagation
The fundamental algorithm for training neural networks by computing gradients of the loss function with respect to each weight. Uses the chain rule to efficiently propagate errors backward through the network.

### Batch Normalization
A technique that normalizes layer inputs by re-centering and re-scaling, making training faster and more stable. Introduced in the Foundations area, it enables training much deeper networks by reducing internal covariate shift.

### Deep Learning
A subset of machine learning using neural networks with multiple layers (hence "deep"). Excels at automatically learning hierarchical representations from raw data without manual feature engineering.

### Distributional Hypothesis
The linguistic principle that "words that occur in similar contexts tend to have similar meanings." Foundation of word embedding methods like Word2Vec and GloVe.

### Dual Encoder
An architecture using two separate encoders (typically transformers) to encode queries and documents into dense vectors that can be compared via similarity metrics. Foundation of modern dense retrieval systems like DPR.

### Embeddings
Dense, continuous vector representations of discrete objects (words, tokens, images). Convert discrete symbols into points in high-dimensional space where semantic similarity corresponds to geometric proximity.

### Feature Map
The output of a convolutional layer, representing detected features at different spatial locations. Early layers detect edges; deeper layers detect complex patterns.

### Gradient Descent
The optimization algorithm that iteratively adjusts model parameters in the direction that reduces the loss function. Variants include SGD, Adam, and AdamW.

### Hidden Layer
Any layer in a neural network between the input and output layers. Where the network learns intermediate representations and transformations.

### Hyperparameter
A parameter set before training begins (e.g., learning rate, batch size, number of layers). Distinct from model parameters learned during training.

### Inference
The process of using a trained model to make predictions on new data. Contrasts with training.

### Loss Function
A mathematical function that measures how far the model's predictions are from the true values. Training aims to minimize this function. Also called objective function or cost function.

### Overfitting
When a model learns the training data too well, including noise and outliers, leading to poor generalization on new data. Addressed through regularization, dropout, or more training data.

### Regularization
Techniques to prevent overfitting by constraining model complexity. Examples: L1/L2 weight penalties, dropout, early stopping.

### Underfitting
When a model is too simple to capture the underlying patterns in the data, performing poorly on both training and test sets.

---

## Architectures & Models

### AlexNet
2012 convolutional neural network that sparked the deep learning revolution by winning ImageNet with a large margin. First to successfully use ReLU, dropout, and GPU training at scale.

### Autoencoder
A neural network that learns to compress data into a lower-dimensional representation and then reconstruct it. Used for dimensionality reduction, denoising, and unsupervised learning.

### BERT (Bidirectional Encoder Representations from Transformers)
A transformer-based model that learns contextual word representations by predicting masked words in both directions. Revolutionized NLP fine-tuning in 2019.

### CLIP (Contrastive Language-Image Pre-training)
A multimodal model that learns aligned representations of images and text by training on 400M image-text pairs. Enables zero-shot image classification using natural language descriptions.

### CNN (Convolutional Neural Network)
A neural network architecture designed for processing grid-like data (images). Uses convolutional layers to detect local patterns and pooling layers to reduce spatial dimensions.

### Diffusion Model
A generative model that learns to gradually denoise random noise into coherent outputs (images, audio, etc.). Powers systems like Stable Diffusion and DALL-E.

### Encoder-Decoder Architecture
A model structure with two components: an encoder that compresses input into a fixed representation, and a decoder that generates output from that representation. Foundation of Seq2Seq models.

### GAN (Generative Adversarial Network)
A framework where two networks compete: a generator creates fake data, and a discriminator tries to distinguish real from fake. The competition improves both networks.

### GloVe (Global Vectors for Word Representation)
A word embedding method that learns vectors by factorizing word co-occurrence statistics. Alternative to Word2Vec that captures global corpus statistics.

### GoogLeNet
A 2014 CNN architecture introducing Inception modules, which use parallel convolutions of different sizes to capture multi-scale features efficiently.

### GPT (Generative Pre-trained Transformer)
An autoregressive language model trained to predict the next token. GPT-3 demonstrated remarkable few-shot learning abilities; GPT-4 powers ChatGPT.

### KAN (Kolmogorov-Arnold Network)
A neural network architecture using learnable activation functions on edges instead of fixed activations on nodes. Explores alternatives to traditional MLPs.

### LeNet
The pioneering 1998 convolutional neural network for handwritten digit recognition. Introduced the basic CNN pattern still used today.

### LSTM (Long Short-Term Memory)
A recurrent neural network architecture with gates that control information flow, enabling learning of long-range dependencies in sequences. Addresses vanishing gradient problem in vanilla RNNs.

### Mamba
A state-space model offering an alternative to transformers with linear-time inference. Part of the search for more efficient sequence modeling architectures.

### ResNet (Residual Network)
A CNN architecture using skip connections that allow gradients to flow directly through the network. Enabled training of very deep networks (100+ layers) and won ImageNet 2015.

### RNN (Recurrent Neural Network)
A neural network architecture with loops, allowing information to persist across sequence steps. Processes sequential data like text or time series.

### RWKV
A parallelizable RNN that combines efficient training like transformers with O(1) inference cost like RNNs. Alternative architecture to transformers.

### SAM (Segment Anything Model)
A vision foundation model capable of zero-shot image segmentation from prompts. Trained on 1 billion masks, demonstrating powerful generalization.

### Seq2Seq (Sequence to Sequence)
An architecture using encoder-decoder pattern to map input sequences to output sequences. Foundation for machine translation and laid groundwork for modern transformers.

### State-Space Model
A class of models based on continuous-time dynamical systems. Recently adapted for deep learning as efficient alternatives to transformers (e.g., Mamba).

### Transformer
The dominant neural architecture for sequential data, using self-attention mechanisms instead of recurrence. Introduced in "Attention Is All You Need" (2017).

### U-Net
An architecture with an encoder-decoder structure and skip connections, originally for image segmentation. Recently connected to probabilistic inference.

### Vision-Language Model (VLM)
A model that can understand and reason about both images and text together. Examples include CLIP (contrastive), LLaVA (generative), and GPT-4V. Key for multimodal AI applications.

### ViT (Vision Transformer)
Applies pure transformer architecture to image classification by treating images as sequences of patches. Showed transformers aren't just for text.

### Word2Vec
A foundational word embedding method using shallow neural networks to predict context words (Skip-gram) or target words from context (CBOW). Sparked the embeddings revolution in 2013.

---

## Training & Optimization

### Adam (Adaptive Moment Estimation)
An optimization algorithm combining momentum and adaptive learning rates. The most popular optimizer for training deep learning models.

### Batch Size
The number of training examples processed together in one forward/backward pass. Larger batches are more stable but require more memory.

### BPE (Byte Pair Encoding)
A tokenization algorithm that iteratively merges the most frequent character or subword pairs. Used by GPT and many modern LLMs to handle rare words and new languages.

### Checkpoint
A saved snapshot of model parameters during training, allowing resumption if training is interrupted or selection of the best model.

### Constitutional AI
An approach to AI safety where models are trained to follow explicit constitutional principles through AI feedback (RLAIF), reducing need for human oversight.

### Data Augmentation
Artificially expanding the training dataset by applying transformations (rotations, crops, noise) to existing data. Improves generalization and reduces overfitting.

### Dropout
A regularization technique that randomly drops neurons during training, preventing co-adaptation and improving generalization.

### Early Stopping
Stopping training when validation performance stops improving, even if training loss continues to decrease. Prevents overfitting.

### Epoch
One complete pass through the entire training dataset. Models are typically trained for multiple epochs.

### Fine-tuning
Continuing to train a pre-trained model on a specific task or dataset. Adapts general knowledge to specialized applications.

### Gradient Clipping
Limiting the magnitude of gradients during training to prevent exploding gradients, especially in RNNs and transformers.

### Knowledge Distillation
Transferring knowledge from a large "teacher" model to a smaller "student" model, maintaining performance while reducing size.

### Learning Rate
A hyperparameter controlling how much model weights change in response to gradients. Too high causes instability; too low causes slow training.

### Megatron-LM
A framework for training massive language models using model parallelism and distributed computing across multiple GPUs.

### Model Parallelism
Splitting a model across multiple devices when it's too large to fit on one. Contrasts with data parallelism where the model is replicated.

### Neural Tangent Kernel
A kernel that describes how an infinitely wide neural network's predictions evolve during gradient descent training. Connects deep learning to kernel methods and explains convergence and generalization behavior of very wide networks in theory.

### Pre-training
Initial training phase on large, general datasets before fine-tuning on specific tasks. Foundation of transfer learning.

### Quantization
Reducing the precision of model weights (e.g., from 32-bit to 8-bit or even 1-bit) to save memory and increase inference speed.

### RLHF (Reinforcement Learning from Human Feedback)
Training models using human preferences as rewards. Core technique for aligning LLMs with human values, used in ChatGPT.

### SGD (Stochastic Gradient Descent)
An optimization algorithm that updates parameters using gradients computed on small random batches of data. Foundation of modern neural network training.

### Transfer Learning
Using knowledge learned from one task to improve learning on a different but related task. Especially powerful in deep learning.

### Vanishing Gradient Problem
Issue in deep networks where gradients become extremely small during backpropagation, preventing effective learning in early layers. Addressed by skip connections, LSTM, careful initialization.

### Xavier Initialization
A weight initialization method that keeps signal variance consistent across layers, enabling training of deep networks without gradient explosion or vanishing.

### ZeRO (Zero Redundancy Optimizer)
A memory optimization technique for training large models by partitioning optimizer states, gradients, and parameters across devices.

---

## Attention Mechanisms

### Attention Mechanism
A mechanism that allows models to focus on relevant parts of the input when producing each output. Core innovation enabling transformers to outperform RNNs.

### Attention Sink
A phenomenon where attention weights concentrate on initial tokens regardless of relevance. Understanding this helps with streaming/infinite context.

### Cross-Attention
Attention between two different sequences (e.g., between encoder and decoder outputs). Used in machine translation and multimodal models.

### FlashAttention
An IO-aware attention algorithm that's 3x faster than standard attention by optimizing memory access patterns. Critical for training modern LLMs efficiently. FlashAttention-2 further improves performance with better parallelism and is the de facto standard in production systems.

### Infini-attention
An attention mechanism enabling infinite context windows by compressing information from earlier tokens, allowing processing of arbitrarily long sequences.

### Multi-Head Attention
Running multiple attention operations in parallel with different learned projections. Allows the model to attend to different aspects simultaneously.

### Query, Key, Value (Q, K, V)
The three components of attention: queries search for relevant information, keys represent what information is available, values contain the actual information to be retrieved.

### RetNet (Retentive Network)
An alternative to transformers that achieves efficient training like transformers but O(1) inference cost like RNNs by combining attention with recurrence.

### Self-Attention
Attention mechanism where queries, keys, and values all come from the same sequence. Allows each position to attend to all positions in the sequence.

### Sparse Attention
Attention patterns that only attend to a subset of positions rather than all positions. Reduces complexity from O(n²) to near-linear, enabling longer sequences.

### Speculative Decoding
A technique to accelerate LLM inference by using a smaller "draft" model to propose multiple tokens, then verifying them in parallel with the larger model. Can achieve 2-3x speedups without changing output distribution.

---

## Natural Language Processing

### Autoregressive Model
A model that generates sequences one token at a time, where each token depends on previous tokens. GPT models are autoregressive.

### BLEU Score
A metric for evaluating machine translation quality by comparing generated text to reference translations. Measures n-gram overlap.

### CBOW (Continuous Bag of Words)
A Word2Vec training objective that predicts a target word from its surrounding context words. Contrasts with Skip-gram.

### Contextual Embeddings
Word representations that vary based on context. BERT and GPT produce contextual embeddings, unlike static embeddings (Word2Vec/GloVe).

### Few-Shot Learning
The ability to learn new tasks from just a few examples. GPT-3 demonstrated remarkable few-shot abilities via in-context learning.

### In-Context Learning
The ability of large language models to learn tasks from examples provided in the prompt, without updating parameters. Emergent ability of large models.

### Induction Head
A specific attention pattern in transformers that copies tokens that appeared after similar tokens earlier in the sequence. Key mechanistic interpretability finding that explains how models perform in-context learning. A circuit composed of a "previous token head" and an "induction head" working together.

### kNN-LM (k-Nearest Neighbors Language Model)
Augmenting language models with retrieval: at each step, retrieve similar contexts from a database and use them to improve predictions.

### Masked Language Modeling (MLM)
BERT's training objective: predict randomly masked words in a sentence using bidirectional context. Contrasts with autoregressive prediction.

### Perplexity
A metric for evaluating language models: the inverse probability of the test set normalized by sequence length. Lower is better.

### Prompt Engineering
Crafting input prompts to elicit desired behaviors from language models. Crucial for getting good results from models like GPT-4.

### RAG (Retrieval-Augmented Generation)
Combining language generation with information retrieval: the model retrieves relevant documents before generating responses, grounding outputs in factual sources.

### REALM (Retrieval-Augmented Language Model)
First major approach to integrate retrieval into language model pre-training with backpropagation through millions of documents.

### SentencePiece
A language-agnostic tokenizer that works directly on raw Unicode without pre-tokenization. Implements BPE and Unigram algorithms.

### Skip-gram
A Word2Vec training objective that predicts context words from a target word. Often works better than CBOW for word embeddings.

### Static Embeddings
Word representations that are fixed regardless of context (Word2Vec, GloVe). Contrasts with contextual embeddings from transformers.

### Tokenization
Converting text into discrete units (tokens) that models can process. Critical preprocessing step affecting model performance, vocabulary size, and multilingual capabilities.

### Vocabulary
The set of all tokens a model can understand. Larger vocabularies handle rare words better but increase computational cost.

### WordPiece
A tokenization algorithm similar to BPE but optimizes for likelihood. Used by BERT and many Google models.

### Zero-Shot Learning
Performing a task without any task-specific training examples. CLIP enables zero-shot image classification; large LLMs can do zero-shot text tasks.

---

## Interpretability & Evaluation

### Adversarial Example
An input crafted with small, imperceptible perturbations that causes a model to make incorrect predictions. Reveals model vulnerabilities.

### Attribution Method
A technique for explaining model predictions by assigning importance scores to input features. Examples: Integrated Gradients, LIME.

### Calibration
How well a model's confidence scores match actual accuracy. A well-calibrated model's predicted 80% confidence means it's correct 80% of the time. Critical for safety-critical applications where understanding prediction reliability is essential.

### Gradient-based Attribution
Explanation methods using gradients to identify which input features most influence the output. Includes vanilla gradients, Integrated Gradients, SmoothGrad.

### H-Neurons (Hallucination-Associated Neurons)
A sparse subset of feedforward network (FFN) neurons whose activations reliably predict when an LLM will produce hallucinated rather than faithful outputs. Identified via sparse linear probing on contribution metrics (e.g., CETT); typically &lt;0.1% of model neurons. Causal interventions show they drive over-compliance behaviors (invalid premises, misleading context, sycophancy, harmful instructions). They originate in pre-training rather than alignment. Enables neuron-level hallucination detection and potential intervention points. See [H-Neurons (Gao et al., 2025)](https://arxiv.org/abs/2512.01797).

### Hallucination
When language models generate plausible-sounding but factually incorrect information. A major challenge for deploying LLMs in production.

### Influence Functions
A method from robust statistics adapted to deep learning for understanding how individual training examples affect predictions.

### Integrated Gradients
An attribution method that computes the path integral of gradients from a baseline to the actual input. Satisfies desirable axioms for explanations.

### LIME (Local Interpretable Model-agnostic Explanations)
A technique that explains individual predictions by fitting an interpretable model locally around the prediction.

### Mechanistic Interpretability
Reverse-engineering neural networks to understand the algorithms they've learned at a mechanistic level. Goes beyond just finding important features. Essential for safety as it enables detection of deceptive or misaligned behavior in models.

### MLE-bench
A benchmark for evaluating machine learning agents on practical ML engineering tasks, testing end-to-end capabilities.

### Saliency Map
A visualization highlighting which parts of an input are most important for a model's prediction. Common in computer vision interpretability.

### SmoothGrad
An attribution method that reduces noise in gradient-based explanations by averaging gradients of noisy versions of the input.

### TruthfulQA
A benchmark measuring whether language models generate truthful answers, revealing that larger models can be less truthful due to learning human falsehoods. Critical safety evaluation tool for assessing model reliability.

### Truthfulness
The property of generating factually correct information. A key safety concern as language models may generate plausible-sounding but false information, especially on topics where training data contains human falsehoods.

---

## Security & Safety

### Adversarial Attack
Deliberately crafted inputs designed to fool machine learning models. Includes adversarial examples, poisoning attacks, and backdoor attacks.

### Adversarial Training
Training models on adversarial examples to improve robustness. A defense against adversarial attacks.

### AI Alignment
Ensuring AI systems behave in accordance with human values and intentions. A central challenge in AI safety.

### Constitutional Principles
Explicit rules or values that guide AI behavior, used in Constitutional AI to train models to be helpful, harmless, and honest.

### Data Poisoning
Corrupting training data to manipulate model behavior. A serious security concern for models trained on web-scraped data.

### Jailbreaking
Crafting prompts that bypass safety guardrails to make models produce harmful content. An ongoing cat-and-mouse game in LLM deployment.

### Prompt Injection
Attacks where malicious instructions hidden in user input override the system's intended behavior. Major security concern for LLM applications.

### Red Teaming
Testing AI systems by deliberately trying to find failures, vulnerabilities, or harmful outputs. Essential for identifying weaknesses before deployment.

### RLAIF (Reinforcement Learning from AI Feedback)
Using AI systems to provide feedback for training instead of humans. Potentially more scalable than RLHF.

### Robust Machine Learning
Developing models that maintain performance under adversarial conditions, distribution shifts, or corrupted inputs.

### Algorithmic Bias
Systematic and unfair discrimination in AI systems, often reflecting biases in training data or model design. Can manifest as demographic disparities, unfair treatment of protected groups, or unequal outcomes.

### Bias Detection
Methods for identifying when AI systems exhibit biased behavior, including statistical tests, fairness metrics, and demographic analysis.

### Fairness
Ensuring AI systems treat different groups equitably. Common definitions include demographic parity (equal positive rates), equalized odds (equal true/false positive rates), and calibration (equal prediction accuracy across groups).

### Demographic Parity
A fairness criterion requiring that the rate of positive predictions is equal across different demographic groups. Also known as statistical parity or group fairness.

### Equalized Odds
A fairness criterion requiring that true positive rates and false positive rates are equal across different demographic groups. Stronger than demographic parity as it accounts for actual outcomes, not just predictions.

### Harmful Content
AI-generated content that is toxic, offensive, discriminatory, or otherwise harmful. Includes hate speech, misinformation, and content that could cause real-world harm.

### Toxicity
Language or content that is harmful, offensive, or inappropriate. Toxicity detection is crucial for safety in text generation systems, as models can generate toxic content even when not explicitly prompted.

### Misinformation
False or misleading information that is spread, often unintentionally by AI systems. A major safety concern as language models can generate plausible-sounding but factually incorrect information.

### Long-term Safety
Research addressing safety challenges for advanced AI systems, including AGI safety, scalable oversight, corrigibility, and control problems. Focuses on ensuring safety as AI systems become more capable than humans.

### Safety Evaluation
Systematic assessment of AI systems for safety risks, including red teaming, safety benchmarks, and evaluation frameworks. Essential for identifying harmful behaviors before deployment.

### Scalable Oversight
The challenge of supervising AI systems that may become more capable than their human supervisors. Research explores techniques like debate, recursive reward modeling, and amplification to maintain control.

### Corrigibility
The property of an AI system that allows it to be corrected or shut down even if doing so conflicts with its training objectives. Important for maintaining human control over advanced AI systems.

---

## Systems & Hardware

### Arithmetic Intensity
The ratio of compute operations (FLOPs) to memory accesses (bytes). High arithmetic intensity operations are compute-bound; low intensity operations are memory-bound. Critical concept for understanding GPU performance and why optimizations like FlashAttention work.

### Checkpoint Sharding
Splitting model checkpoints across multiple files to enable distributed saving/loading of very large models.

### Distributed Training
Training a model across multiple devices (GPUs, TPUs) by parallelizing computation. Essential for training large models.

### Flash Memory
High-speed memory used in modern GPUs. FlashAttention is named for optimizing use of this memory hierarchy.

### GPU (Graphics Processing Unit)
Specialized hardware for parallel computation, originally for graphics but now dominant for deep learning training and inference.

### IO-Aware Algorithm
An algorithm designed with memory access patterns in mind, minimizing expensive data transfers between different memory levels. FlashAttention is IO-aware.

### Mixed Precision Training
Using lower precision (e.g., FP16) for most operations while keeping some in higher precision (FP32) to speed up training without sacrificing accuracy.

### Photonic Computing
Using light instead of electricity for computation. Promising for extremely fast, low-power AI inference in the future.

### Tensor Core
Specialized hardware in modern GPUs for accelerating matrix multiplications, the core operation in deep learning.

### TPU (Tensor Processing Unit)
Google's custom ASIC designed specifically for deep learning workloads. Offers high performance for training and inference.

### VLSI (Very Large Scale Integration)
Technology for creating integrated circuits with millions of components. Relevant for custom AI hardware implementations.

---

## Applications & Domains

### Agent
An AI system that can take actions in an environment to achieve goals. Modern LLM agents can use tools, make decisions, and interact with external systems.

### Agentic System
A framework where AI agents autonomously plan, execute tasks, and potentially collaborate with other agents to achieve objectives.

### Automation Bias
The human tendency to over-rely on automated systems and accept their outputs uncritically, even when contradictory evidence is available. A central concern in human-AI interaction: it drives both misuse (following wrong AI advice) and complements automation-induced complacency in monitoring tasks.

### Chain-of-Thought Prompting
Encouraging models to show step-by-step reasoning in their outputs, improving performance on complex reasoning tasks.

### DynaSaur
A system enabling language agents to dynamically generate new actions beyond predefined options, increasing flexibility.

### Federated Learning
Training models across decentralized devices without centralizing data. Preserves privacy by keeping data local.

### Foundation Model
A large-scale model trained on broad data that can be adapted to many downstream tasks. Examples: GPT-3, CLIP, SAM.

### Gato
A "generalist agent" that can perform hundreds of different tasks (text, images, robotics control) with a single model.

### Multimodal Learning
Training models on multiple types of data (text, images, audio) simultaneously. Enables richer understanding and cross-modal tasks.

### ReAct (Reasoning and Acting)
A framework where language models alternate between reasoning (thinking) and acting (using tools), improving problem-solving.

### Reflexion
An agent framework using linguistic feedback and episodic memory to enable self-improvement through trial and error.

### Reinforcement Learning (RL)
Training agents through trial and error using reward signals. Different from supervised learning which uses labeled examples.

### Tabular Data
Data organized in rows and columns (spreadsheets, databases). TabPFN specializes in learning from small tabular datasets.

### Test-Time Compute
Using additional computation during inference (e.g., generating multiple solutions, extended reasoning) to improve output quality. Also known as inference-time scaling or "thinking longer."

### Test-Time Training
Adapting model parameters during inference on the specific input, as opposed to fixed weights. Enables models to dynamically improve on individual examples.

### Time Series
Data points indexed in time order. Require specialized models (LSTM, MOMENT) that can capture temporal dependencies.

---

## Acronyms Quick Reference

| Acronym | Full Name | Category |
|---------|-----------|----------|
| AGI | Artificial General Intelligence | Concepts |
| ASIC | Application-Specific Integrated Circuit | Hardware |
| BERT | Bidirectional Encoder Representations from Transformers | Models |
| BLEU | Bilingual Evaluation Understudy | Metrics |
| BPE | Byte Pair Encoding | Tokenization |
| CBOW | Continuous Bag of Words | Embeddings |
| CLIP | Contrastive Language-Image Pre-training | Models |
| CNN | Convolutional Neural Network | Architectures |
| GAN | Generative Adversarial Network | Architectures |
| GPT | Generative Pre-trained Transformer | Models |
| GPU | Graphics Processing Unit | Hardware |
| KAN | Kolmogorov-Arnold Network | Architectures |
| kNN-LM | k-Nearest Neighbors Language Model | NLP |
| LIME | Local Interpretable Model-agnostic Explanations | Interpretability |
| LLM | Large Language Model | Models |
| LSTM | Long Short-Term Memory | Architectures |
| MCP | Model Context Protocol | Systems |
| MLM | Masked Language Modeling | Training |
| NLP | Natural Language Processing | Domain |
| PPO | Proximal Policy Optimization | Training |
| RAG | Retrieval-Augmented Generation | Techniques |
| REALM | Retrieval-Augmented Language Model | Models |
| RL | Reinforcement Learning | Training |
| RLAIF | Reinforcement Learning from AI Feedback | Training |
| RLHF | Reinforcement Learning from Human Feedback | Training |
| DPR | Dense Passage Retrieval | Retrieval |
| LLaVA | Large Language and Vision Assistant | Models |
| RNN | Recurrent Neural Network | Architectures |
| RWKV | Named after its components (receptance, weight, key, value) | Architectures |
| SAM | Segment Anything Model | Models |
| Seq2Seq | Sequence to Sequence | Architectures |
| SGD | Stochastic Gradient Descent | Optimization |
| TPU | Tensor Processing Unit | Hardware |
| ViT | Vision Transformer | Models |
| VLM | Vision-Language Model | Models |
| VLSI | Very Large Scale Integration | Hardware |
| ZeRO | Zero Redundancy Optimizer | Training |

---

## Cross-References

### If you're reading about...
- **Attention mechanisms** → See also: Transformer, Self-Attention, Multi-Head Attention, FlashAttention
- **Embeddings** → See also: Word2Vec, GloVe, Tokenization, Static vs Contextual Embeddings
- **LLMs** → See also: GPT, BERT, Transformer, Pre-training, Fine-tuning, RLHF
- **Training** → See also: Backpropagation, SGD, Adam, Batch Normalization, Dropout
- **Interpretability** → See also: LIME, Integrated Gradients, Attribution Methods, Saliency Maps
- **Security & Safety** → See also: Adversarial Examples, RLHF, Constitutional AI, Jailbreaking, Red Teaming, Bias Detection, Fairness, Safety Evaluation, Long-term Safety

---

[← Back to Learning Path](../learning-path.md) | [→ Browse Papers by Date](../by-date.md)

*Last updated: December 2025*
