# Security, Safety & Robustness

[← Back to Learning Path](../learning-path.md) | [📖 Glossary](glossary.md) | Related: [Interpretability](interpretability.md) | [Reasoning](reasoning.md) | [Policy](policy.md)

**Overview**: AI systems face unique challenges in both **security** and **safety** that don't exist in traditional software. This phase examines both dimensions:

**Security** focuses on protecting systems from attacks: [adversarial examples](glossary.md#adversarial-example) that fool models with imperceptible perturbations, [jailbreaking](glossary.md#jailbreaking) techniques that bypass safety guardrails, [prompt injection](glossary.md#prompt-injection) attacks that hijack model behavior, and [data poisoning](glossary.md#data-poisoning) that corrupts training.

**Safety** focuses on ensuring systems behave correctly and don't cause harm: [AI alignment](glossary.md#ai-alignment) techniques that make models follow human values, bias detection and mitigation, harmful content prevention, and long-term safety research for advanced AI systems.

As AI systems control increasingly important decisions—from content moderation to autonomous vehicles—understanding both their vulnerabilities and how to ensure safe behavior becomes critical for responsible deployment.

## AI Alignment & Safety Training
**Goal**: Build AI systems that are aligned with human values and safe to deploy

1. [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) (Amodei et al., 2016)
   - *Why*: **Foundational AI safety paper** - defines five practical research problems for ensuring AI systems operate safely: safe exploration, robustness to distributional shift, avoiding negative side effects, avoiding reward hacking, and scalable oversight; essential reading for understanding the field

2. [Training language models to follow instructions with human feedback (InstructGPT)](https://arxiv.org/abs/2203.02155) (Ouyang et al., 2022)
   - *Why*: **The InstructGPT paper** - demonstrates fine-tuning with RLHF for alignment; 1.3B model preferred over 175B GPT-3; foundational work showing how human feedback can align models

3. [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073) (Bai et al., 2022)
   - *Why*: **Central to LLM safety** - self-improvement through AI feedback (RLAIF) without human labels; reduces need for oversight; demonstrates how models can learn safety principles through constitutional principles

4. [Weak-to-Strong Generalization: Eliciting Strong Capabilities With Weak Supervision](https://arxiv.org/abs/2312.09390) (Burns et al., 2023)
   - *Why*: **OpenAI superalignment research** - explores whether weak supervisors can safely train more capable models; demonstrates surprising success in eliciting strong capabilities with weak supervision; critical for scalable oversight as AI systems become superhuman

5. [Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations](https://arxiv.org/abs/2312.06674) (Inan et al., 2023)
   - *Why*: **Practical safety guardrail** - open-source safety classifier for LLM inputs and outputs; defines taxonomy of unsafe content categories; enables deployment of safety-filtered LLM applications

## Security Threats & Attacks
**Goal**: Understand and defend against security vulnerabilities in AI systems

1. [Pr$εε$mpt: Sanitizing Sensitive Prompts for LLMs](https://arxiv.org/abs/2504.05147) (2025)
   - *Why*: Protecting sensitive information in prompts; defense against prompt injection attacks

2. [Enterprise-Grade Security for the Model Context Protocol (MCP): Frameworks and Mitigation Strategies](https://arxiv.org/pdf/2504.08623) (2025)
   - *Why*: Security frameworks for AI applications; practical deployment considerations

3. [A2AS: Agentic AI Runtime Security and Self-Defense](https://arxiv.org/pdf/2510.13825) (2025)
   - *Why*: Runtime security for AI agents; self-defense mechanisms for agentic systems

4. [Breaking Agent Backbones: Evaluating the Security of Backbone LLMs in AI Agents](https://arxiv.org/abs/2510.22620) (Bazinska et al., 2025)
   - *Why*: Systematic security evaluation of LLM backbones in AI agents; introduces threat snapshots framework and b³ benchmark with 194,331 adversarial attacks; reveals reasoning capabilities improve security while model size doesn't correlate

5. [Large Language Models are Unreliable for Cyber Threat Intelligence](https://arxiv.org/abs/2503.23175) (2025)
   - *Why*: Understanding LLM limitations in security contexts; highlights reliability concerns

6. [SEC-bench: Automated Benchmarking of LLM Agents on Real-World Software Security Tasks](https://openreview.net/pdf?id=QQhQIqons0) (Lee et al., 2025)
   - *Why*: First fully automated benchmarking framework for evaluating LLM agents on authentic security engineering tasks; introduces multi-agent scaffold for constructing verified vulnerability datasets with reproducible PoCs and patches; reveals significant performance gaps (18% PoC generation, 34% vulnerability patching)

7. [Your Agent Is Mine: Measuring Malicious Intermediary Attacks on the LLM Supply Chain](https://arxiv.org/abs/2604.08407) (Liu et al., 2026)
   - *Why*: First systematic study of malicious LLM API routers as a supply-chain attack surface; formalizes payload injection and secret exfiltration attack classes with evasion variants; empirically tests 428 third-party routers finding active code injection, credential theft, and crypto draining; proposes three deployable client-side defenses

8. [Bad Memory: Evaluating Prompt Injection Risks from Memory in Agentic Systems](https://arxiv.org/abs/2607.14611) (Gadgil et al., 2026)
   - *Why*: Shows that persistent memory files change the prompt injection threat model - payloads planted in an agent's memory attack current and future sessions, even though getting an agent to overwrite its own memory from untrusted content is hard; evaluates two coding agents across four models and measures how attack success and payload persistence vary by system, adversarial goal, and multi-session sequence

9. [AI Agents May Always Fall for Prompt Injections](https://arxiv.org/abs/2605.17634) (Abdelnabi & Bagdasarian, 2026)
   - *Why*: Reframes prompt injection through Contextual Integrity theory and argues an "impossibility result": adversaries can always craft contexts that make blocked flows look legitimate, while tightening norms blocks legitimate flows; shows data/instruction separation defenses miss contextual manipulation attacks

## Safety Evaluation & Red Teaming
**Goal**: Systematically evaluate AI systems for safety risks and harmful behaviors

1. [Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned](https://arxiv.org/abs/2209.07858) (Ganguli et al., 2022)
   - *Why*: **Foundational red teaming paper** from Anthropic - systematic approach to discovering harmful outputs through adversarial probing; demonstrates how red teaming scales with model size; essential methodology for safety evaluation

2. [Automated Red Teaming with GOAT: the Generative Offensive Agent Tester](https://arxiv.org/abs/2410.01606) (Pavlova et al., 2024)
   - *Why*: Agentic red teaming system that simulates multi-turn adversarial conversations using 7 attack techniques; achieves 97% ASR against Llama 3.1 and 88% against GPT-4-Turbo; demonstrates how combining jailbreak methods in conversation outperforms single-prompt attacks

3. [HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal](https://arxiv.org/abs/2402.04249) (Mazeika et al., 2024)
   - *Why*: **Comprehensive safety benchmark** - standardized evaluation for automated red teaming; includes 510 harmful behaviors across semantic categories; enables reproducible comparison of attack and defense methods

4. [WildGuard: Open One-Stop Moderation Tools for Safety Risks, Jailbreaks, and Refusals of LLMs](https://arxiv.org/abs/2406.18495) (Han et al., 2024)
   - *Why*: Open-source moderation tool covering prompt harmfulness, response harmfulness, and refusal detection; trained on WildGuardMix with 92K examples; strong performance on 13 public benchmarks

5. [TruthfulQA: Measuring How Models Mimic Human Falsehoods](https://arxiv.org/abs/2109.07958) (Lin et al., 2022)
   - *Why*: **Foundational safety benchmark** - reveals that larger models can be less truthful; critical for understanding model limitations and safety risks; measures tendency to generate false but plausible-sounding answers
   - *Note*: Also covered in [Interpretability](interpretability.md)

6. [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218) (Li et al., 2024)
   - *Why*: **Weapons of Mass Destruction Proxy benchmark** - evaluates dangerous knowledge in biosecurity, cybersecurity, and chemical security; demonstrates unlearning can reduce hazardous capabilities while maintaining general performance; critical for preventing dual-use risks

7. [Agents of Chaos](https://arxiv.org/abs/2602.20021) (Shapira et al., 2026)
   - *Why*: Empirical red-teaming of autonomous LLM agents with persistent memory, email, shell access, and multi-agent communication in a live environment; documents eleven failure modes including unauthorized compliance, identity spoofing, cross-agent propagation, and partial system takeover

8. [Beyond Red-Teaming: Formal Guarantees of LLM Guardrail Classifiers](https://arxiv.org/abs/2605.10901) (Kezins et al., 2026)
   - *Why*: Shifts guardrail verification from discrete input space to the classifier's pre-activation layer, where harmful prompts form convex regions certifiable via monotonicity of the sigmoid head; introduces SVD-aligned hyper-rectangles (exact) and Gaussian Mixture Models (probabilistic) for region construction, exposing large safety gaps in BERT (55-90% coverage) versus more stable GPT-2/Llama classifiers (~80-90%)

## Bias, Fairness & Robustness
**Goal**: Detect, measure, and mitigate bias in AI systems while maintaining robustness

1. [Equality of Opportunity in Supervised Learning](https://arxiv.org/abs/1610.02413) (Hardt et al., 2016)
   - *Why*: **Foundational fairness paper** - introduces equalized odds criterion for fair machine learning; shows how to adjust classifiers to achieve fairness; critical theoretical foundation for bias mitigation

2. [Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification](http://proceedings.mlr.press/v81/buolamwini18a.html) (Buolamwini & Gebru, 2018)
   - *Why*: **Landmark bias study** - demonstrates intersectional bias in commercial face recognition systems; darker-skinned females had error rates 34x higher than lighter-skinned males; catalyzed industry-wide improvements and regulatory attention

3. [Understanding and Mitigating Tokenization Bias in Language Models](https://arxiv.org/abs/2406.16829) (2024)
   - *Why*: Reveals how tokenization introduces systematic biases that affect model fairness and performance across languages; critical insight that tokenization isn't neutral

4. [On Calibration of Modern Neural Networks](https://arxiv.org/abs/1706.04599) (Guo et al., 2017)
   - *Why*: **Foundational work on model calibration** - shows modern neural networks are poorly calibrated despite high accuracy; important for understanding when to trust model predictions; critical for safety-critical applications
   - *Note*: Also relevant for [Interpretability](interpretability.md)

## Harmful Content & Misinformation
**Goal**: Detect and mitigate harmful content generation and misinformation

1. [RealToxicityPrompts: Evaluating Neural Toxic Degeneration in Language Models](https://arxiv.org/abs/2009.11462) (Gehman et al., 2020)
   - *Why*: **Foundational toxicity benchmark** - systematically evaluates how likely language models are to generate toxic content; reveals that larger models can be more toxic; critical for understanding safety risks in text generation

2. [Perspective API](https://perspectiveapi.com/) (Jigsaw/Google)
   - *Why*: **Production toxicity detection system** - widely-used API for identifying toxic content; trained on millions of human annotations; foundational for content moderation in production systems
   - *Note*: API/service rather than paper, but essential practical reference

3. [The Pile: An 800GB Dataset of Diverse Text for Language Modeling](https://arxiv.org/abs/2101.00027) (Gao et al., 2020)
   - *Why*: Large-scale dataset that includes analysis of toxic content; important for understanding training data composition and its impact on model behavior; highlights challenges in web-scraped training data

4. [TruthfulQA: Measuring How Models Mimic Human Falsehoods](https://arxiv.org/abs/2109.07958) (Lin et al., 2022)
   - *Why*: Benchmark measuring how models generate misinformation by mimicking human falsehoods; reveals counterintuitive scaling where larger models can be less truthful
   - *Note*: Also listed in 8.3 for safety evaluation context

## Long-term Safety Research
**Goal**: Understand and address long-term safety challenges for advanced AI systems

1. [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) (Amodei et al., 2016)
   - *Why*: **Foundational long-term safety roadmap** - defines research agenda for safe AI including scalable oversight and avoiding reward hacking; continues to guide safety research a decade later
   - *Note*: Also listed in 8.1 as foundational alignment paper

2. [Sleeper Agents: Training Deceptive LLMs That Persist Through Safety Training](https://arxiv.org/abs/2401.05566) (Hubinger et al., 2024)
   - *Why*: **Critical deceptive alignment research** - demonstrates that LLMs can be trained with hidden behaviors that persist through safety training; shows current safety techniques may be insufficient for detecting deceptive models; essential for understanding alignment challenges

3. [Scalable Oversight](https://www.anthropic.com/research/measuring-progress-on-scalable-oversight-for-large-language-models) (Anthropic, 2022)
   - *Why*: **Key long-term safety challenge** - addresses how to supervise AI systems that may become more capable than their human supervisors; explores techniques like debate, recursive reward modeling, and amplification
   - *Note*: Research blog post from Anthropic; foundational concept in AI safety

4. [AI Safety Gridworlds](https://arxiv.org/abs/1711.09883) (Leike et al., 2017)
   - *Why*: Suite of reinforcement learning environments testing safety properties: safe interruptibility, avoiding side effects, absent supervisor, reward gaming, and more; foundational benchmark for safety research

5. [Interpretability in the Wild: a Circuit for Indirect Object Identification in GPT-2 small](https://transformer-circuits.pub/2022/in-context-learning-and-induction-heads/index.html) (Elhage et al., 2022)
   - *Why*: **Mechanistic interpretability for safety** - demonstrates how to reverse-engineer model behavior to understand what models are actually doing; essential for detecting deceptive or misaligned behavior
   - *Note*: Part of Anthropic's interpretability research; also relevant for [Interpretability](interpretability.md)

6. [Towards Guaranteed Safe AI: A Framework for Ensuring Robust and Reliable AI Systems](https://arxiv.org/abs/2405.06624) (Dalrymple et al., 2024)
   - *Why*: Proposes world model-based safety framework with quantitative guarantees; addresses how to build AI systems with provable safety properties; important for high-stakes deployment scenarios

7. [Subliminal Learning: Language Models Transmit Behavioral Traits via Hidden Signals in Data](https://arxiv.org/pdf/2507.14805) (Cloud et al., 2025)
   - *Why*: **Critical safety finding** - demonstrates that language models can transmit behavioral traits (including misalignment) through semantically unrelated data like number sequences, code, or reasoning traces; occurs even when data is filtered to remove explicit references to the trait; reveals unexpected pitfall for AI development where distillation could propagate unintended traits; only works when teacher and student share similar initializations

---

**Related**: [Interpretability](interpretability.md) | [Advanced](advanced.md) | [Policy](policy.md)
