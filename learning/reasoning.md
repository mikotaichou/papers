# Reasoning & Agents

[← Back to Learning Path](../learning-path.md) | [← Prev: Retrieval](retrieval.md) | [Next: Architectures →](architectures.md) | [📖 Glossary](glossary.md)

**Overview**: Raw language models don't naturally follow instructions or break down complex problems step-by-step. This area covers the crucial techniques that transform base models into helpful, harmless assistants: [reinforcement learning from human feedback (RLHF)](glossary.md#rlhf-reinforcement-learning-from-human-feedback) that aligns models with human preferences, [chain-of-thought prompting](glossary.md#chain-of-thought-prompting) that enables multi-step reasoning, and [constitutional AI](glossary.md#constitutional-ai) approaches that encode ethical principles. You'll also learn about [agent](glossary.md#agent) frameworks like [ReAct](glossary.md#react-reasoning-and-acting) that give models the ability to use tools and take actions. These methods are what make modern AI systems genuinely useful and (relatively) safe.

## Teaching Models to Reason
**Goal**: Build models that can reason and solve complex problems

1. [Deep Reinforcement Learning from Human Preferences](https://arxiv.org/abs/1706.03741) (Christiano et al., 2017)
   - *Why*: **Introduces RLHF** - the foundation of alignment; learning from human feedback without explicit rewards

2. [Proximal Policy Optimization Algorithms (PPO)](https://arxiv.org/abs/1707.06347) (Schulman et al., 2017)
   - *Why*: **Modern RL training backbone** for LLM fine-tuning; simpler and more stable than TRPO

3. [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) (Yao et al., 2022)
   - *Why*: **Core to reasoning-agent architectures** - interleaves reasoning traces with actions for better problem-solving

4. [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) (Shinn et al., 2023)
   - *Why*: Agentic self-improvement through linguistic feedback and episodic memory

5. [Hierarchical Reasoning Model](https://arxiv.org/pdf/2506.21734) (2025)
   - *Why*: **Multi-level reasoning decomposition** - structures LLM reasoning into hierarchical levels mirroring how humans break complex problems into subgoals; each level operates at a different abstraction granularity, enabling systematic decomposition of problems that flat chain-of-thought fails on

6. [Less is More: Recursive Reasoning with Tiny Networks](https://arxiv.org/pdf/2510.04871) (2025)
   - *Why*: **Recursive depth over parameter width** - shows that small networks applied recursively over multiple passes can match or exceed large models on reasoning tasks; trades model size for inference-time compute by iterating over intermediate representations; challenges the assumption that reasoning requires massive parameter counts

7. [Reinforcement Pre-Training](https://arxiv.org/abs/2506.08007) (2025)
   - *Why*: **RL-augmented pretraining** - integrates reinforcement learning objectives directly into the language model pretraining loop rather than applying RL only during fine-tuning; produces base models with stronger reasoning and instruction-following capabilities before any alignment stage; blurs the traditional pretrain-then-finetune boundary

8. [A Simple Neural Network Module for Relational Reasoning](https://arxiv.org/abs/1706.01427) (Santoro et al., 2017)
   - *Why*: **Relational reasoning foundation** - introduces Relation Networks for learning to reason about relationships between objects; essential for visual question answering and abstract reasoning tasks

9. [Embarrassingly Simple Self-Distillation Improves Code Generation](https://arxiv.org/abs/2604.01193) (Zhang et al., 2026)
   - *Why*: **Self-distillation for code generation** - shows that sampling solutions at a tuned temperature and retraining on them lifts Qwen3-30B-Instruct's LiveCodeBench v6 pass@1 from 42.4% to 55.3%, with the largest gains on hard problems; frames the improvement as resolving a precision-exploration conflict in decoding by suppressing unhelpful token variations while preserving useful exploratory diversity.

10. [Scaling Latent Reasoning via Looped Language Models](https://arxiv.org/abs/2510.25741) (Zhu et al., 2025)
    - *Why*: **Reasoning baked into pretraining via weight-shared loops** - introduces Ouro, a family of looped LMs that perform iterative computation in latent space with an entropy-regularized objective for learned depth allocation, pretrained on 7.7T tokens; the 1.4B and 2.6B variants reportedly match 12B-parameter baselines, with gains traced to better knowledge manipulation rather than larger storage capacity, suggesting latent recurrence is an alternative axis to chain-of-thought for scaling reasoning.

11. [A Formal Comparison Between Chain of Thought and Latent Thought](https://arxiv.org/abs/2509.25239) (Xu et al., 2025)
    - *Why*: **Theoretical separation between CoT and latent reasoning** - proves that latent thought enables more efficient parallel computation than the inherently sequential CoT, while CoT uniquely supports approximate counting and sampling via stochastic decoding; gives principled guidance for choosing between discrete-token and continuous-representation reasoning based on whether a task needs iterative recursion, depth, or stochasticity.

12. [NL2LOGIC: AST-Guided Translation of Natural Language into First-Order Logic with Large Language Models](https://arxiv.org/abs/2602.13237) (Putra et al., 2026)
    - *Why*: **Neuro-symbolic NL-to-logic translation** - inserts an abstract syntax tree as an intermediate representation between a recursive LLM semantic parser and a grammar-constrained generator, deterministically producing solver-ready first-order logic so inference can be delegated to automated solvers; reaches 99% syntactic accuracy and up to 30% higher semantic correctness than prior LLM logic-parsing methods on FOLIO, LogicNLI, and ProofWriter, and lifts downstream reasoning accuracy by 31% when integrated into Logic-LM.

13. [Scaling up Test-Time Compute with Latent Reasoning: A Recurrent Depth Approach](https://arxiv.org/abs/2502.05171) (Geiping et al., 2025)
    - *Why*: **Test-time depth instead of test-time tokens** - iterates a recurrent block to unroll a model to arbitrary depth at inference, so reasoning happens in latent space rather than as emitted chain-of-thought; needs no specialized reasoning data and works with small context windows, and a 3.5B proof-of-concept trained on 800B tokens reaches benchmark performance equivalent to a ~50B-parameter compute load.

## Agentic Systems
**Goal**: Create autonomous AI agents

1. [A Generalist Agent](https://arxiv.org/pdf/2205.06175) (2022)
   - *Why*: **Single network, hundreds of tasks** - Gato uses a single transformer to play Atari, caption images, chat, stack blocks with a robot arm, and more; tokenizes all modalities (text, images, actions, observations) into a shared sequence format; demonstrates that a generalist agent can perform competently across 604 distinct tasks without task-specific architecture changes

2. [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/pdf/2402.01030) (2024)
   - *Why*: **Code as the action language** - replaces JSON/text-based tool calls with executable Python code, enabling agents to compose actions, use variables, and leverage control flow; significantly outperforms structured action formats on multi-step tasks; shows that code generation is a more natural and expressive action space for LLM agents

3. [DynaSaur: Large Language Agents Beyond Predefined Actions](https://arxiv.org/abs/2411.01747) (2024)
   - *Why*: **Runtime action synthesis** - allows LLM agents to dynamically generate new actions (as Python functions) at inference time rather than selecting from a fixed action set; accumulates a growing action library across episodes; overcomes the brittleness of predefined tool inventories in open-ended environments

4. [MAS-ZERO: Designing Multi-Agent Systems with Zero Supervision](https://arxiv.org/pdf/2505.14996) (2025)
   - *Why*: **Zero-shot multi-agent orchestration** - automatically designs multi-agent team structures, role assignments, and communication protocols without human supervision or task-specific training; uses an LLM meta-controller to generate and refine agent configurations; outperforms hand-designed multi-agent systems on complex collaborative benchmarks

5. [Small Language Models are the Future of Agentic AI](https://arxiv.org/abs/2506.02153) (2025)
   - *Why*: Makes the case for using smaller, specialized models in agent systems for efficiency and cost-effectiveness; practical deployment considerations

6. [Learning in Stackelberg Mean Field Games: A Non-Asymptotic Analysis](https://arxiv.org/pdf/2509.15392) (Zeng et al., 2025)
   - *Why*: Introduces AC-SMFG, a single-loop actor-critic algorithm for hierarchical multi-agent systems with a leader and infinite population of followers; first Stackelberg MFG algorithm with non-asymptotic convergence guarantees; addresses policy optimization in strategic interactions like optimal liquidation and public policy

7. [Embedded Universal Predictive Intelligence: a coherent framework for multi-agent learning](https://arxiv.org/pdf/2511.22226) (Meulemans et al., 2025)
   - *Why*: Introduces a mathematical framework for embedded agency and prospective learning in multi-agent settings; extends AIXI theory with self-prediction where Bayesian RL agents predict both future inputs and their own actions; enables infinite-order theory of mind and novel forms of cooperation in mixed-motive scenarios

8. [Artificial Intelligent Disobedience: Rethinking the Agency of Our Artificial Teammates](https://arxiv.org/abs/2506.22276) (Mirsky, 2025)
   - *Why*: Argues for expanding AI teammate autonomy beyond rigid obedience to include intelligent disobedience; introduces a scale of AI agency levels and examines when autonomous contributions in human-AI teams are necessary, even when they conflict with explicit instructions

9. [TRINITY: An Evolved LLM Coordinator](https://arxiv.org/abs/2512.04695) (Xu et al., 2025)
   - *Why*: **Evolved coordinator for multi-LLM collaboration** - trains a compact ~0.6B-parameter language model plus a ~10K-parameter head with separable CMA-ES to orchestrate a pool of larger LLMs over multiple turns, dynamically assigning each a Thinker, Worker, or Verifier role; reaches 86.2% on LiveCodeBench with gains across coding, math, reasoning, and domain-knowledge tasks, and credits the advantage to rich contextualization from hidden-state representations and the suitability of separable CMA-ES under high dimensionality

10. [Learning to Orchestrate Agents in Natural Language with the Conductor](https://arxiv.org/abs/2512.04388) (Nielsen et al., 2025)
    - *Why*: **RL-learned LLM orchestration** - trains a 7B Conductor with end-to-end reinforcement learning to coordinate a pool of worker LLMs, jointly designing agent-to-agent communication topologies and prompt-engineering targeted instructions to each worker; reaches state-of-the-art on reasoning benchmarks like LiveCodeBench and GPQA, generalizes to arbitrary open- and closed-source agent pools via randomized-pool training, and can select itself as a worker to form recursive topologies for dynamic test-time scaling

11. [AI agents can coordinate beyond human scale](https://arxiv.org/abs/2409.02822) (De Marzo et al., 2024)
    - *Why*: **Coordination limits of AI agent societies** - applies complexity-science methods to show LLM groups coordinate via a majority force that weakens with group size, yielding a critical group size beyond which spontaneous consensus fails; this threshold grows exponentially with model capability and exceeds typical human informal group sizes for frontier LLMs

---

**Related**: [Retrieval](retrieval.md) | [Architectures](architectures.md) | [Safety](safety.md)
