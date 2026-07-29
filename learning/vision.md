# Vision & Multimodal Systems

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Probabilistic](probabilistic.md) | [Hardware](hardware.md)

**Overview**: The transformer revolution didn't stop at text—it transformed computer vision too. This area explores how [attention mechanisms](glossary.md#attention-mechanism) replaced [convolutional neural networks](glossary.md#cnn-convolutional-neural-network) as the dominant paradigm in vision, how [CLIP](glossary.md#clip-contrastive-language-image-pre-training) bridges vision and language through contrastive learning, and how models like [SAM](glossary.md#sam-segment-anything-model) achieve unprecedented zero-shot image segmentation. You'll see how the same principles that power ChatGPT enable models to understand and generate images, paving the way for truly [multimodal](glossary.md#multimodal-learning) AI systems that can seamlessly work with text, images, and video together.

## Vision Transformers
**Goal**: Understand how transformers replaced CNNs as the dominant vision paradigm

1. [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale (Vision Transformer/ViT)](https://arxiv.org/abs/2010.11929) (Dosovitskiy et al., 2021)
   - *Why*: **The Vision Transformer paper** - applies pure transformers to image recognition by treating patches as tokens; connects vision and language model architectures and underpins modern multimodal models

2. [Learning Transferable Visual Models From Natural Language Supervision (CLIP)](https://arxiv.org/abs/2103.00020) (Radford et al., 2021)
   - *Why*: **The bridge to multimodal AI** - learns vision-language alignment from 400M image-text pairs; enables zero-shot transfer

3. [Segment Anything (SAM)](https://arxiv.org/abs/2304.02643) (Kirillov et al., 2023)
   - *Why*: **Pivotal open foundation model** - promptable segmentation with 1B masks; demonstrates vision foundation model capabilities

4. [Visualizing and Understanding Convolutional Networks (DeconvNet)](https://arxiv.org/abs/1311.2901) (2013)
   - *Why*: **Peering inside CNN layers** - introduces deconvolutional network visualization that maps activations back to pixel space, revealing what each layer and feature map has learned; shows early layers learn edges and textures while deeper layers learn object parts and compositions; guided the design of better architectures by making learned representations inspectable

5. [Striving for Simplicity: The All Convolutional Net](https://arxiv.org/abs/1412.6806) (2015)
   - *Why*: **Eliminating pooling layers entirely** - shows that replacing max-pooling with strided convolutions matches or improves accuracy while making the network fully differentiable and learnable at every layer; simplifies architecture design by using a single operation type; provides cleaner gradient flow for visualization and interpretability

6. [Semantic Segmentation using Adversarial Networks](https://arxiv.org/abs/1611.08408) (2016)
   - *Why*: **GAN-based structured prediction** - uses an adversarial discriminator to enforce higher-order spatial consistency in segmentation maps, catching implausible label configurations that per-pixel losses miss; demonstrates that adversarial training can improve any dense prediction task by learning to distinguish realistic outputs from artifacts

## Multimodal & Speech
**Goal**: Connect vision, language, and audio in unified models

1. [Visual Instruction Tuning (LLaVA)](https://arxiv.org/abs/2304.08485) (Liu et al., 2023)
   - *Why*: **Pioneering vision-language instruction following** - connects vision encoder with LLM for multimodal conversations; demonstrates that instruction tuning works across modalities; foundation for many open-source multimodal models

2. [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](https://arxiv.org/abs/1512.02595) (Amodei et al., 2016)
   - *Why*: **End-to-end speech recognition** - demonstrates deep learning for speech without hand-engineered features; scales to multiple languages; foundational for modern speech systems

## Vision Interpretability
**Goal**: Understand what vision models learn and how they decide

1. [Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps](https://arxiv.org/abs/1312.6034) (2013)
   - *Why*: **Gradient-based saliency maps** - introduces backpropagation-based visualization to highlight which input pixels most influence a CNN's classification decision; one of the earliest methods for explaining individual predictions in vision models; foundational technique that led to Grad-CAM, Integrated Gradients, and modern attribution methods

2. [Visualizing Deep Neural Network Decisions: Prediction Difference Analysis](https://arxiv.org/abs/1702.04595) (2017)
   - *Why*: **Occlusion-based decision explanations** - systematically measures how removing or altering each input region changes the prediction, producing fine-grained maps of which areas support or oppose each class; provides model-agnostic explanations that do not require access to gradients; complements gradient-based methods by capturing nonlinear feature interactions

3. [Synthesizing the Preferred Inputs for Neurons via Deep Generator Networks](https://arxiv.org/abs/1605.09304) (2016)
   - *Why*: **Activation maximization via learned generators** - uses a pre-trained deep generator network to synthesize high-quality natural images that maximally activate specific neurons; produces dramatically more realistic and interpretable visualizations than direct pixel-space optimization; reveals what individual neurons and layers have learned to detect in a human-understandable way

---

**Related**: [Probabilistic](probabilistic.md) | [Hardware](hardware.md) | [Interpretability](interpretability.md)
