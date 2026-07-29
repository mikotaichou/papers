# Human-AI Interaction & Cognition

[← Back to Learning Path](../learning-path.md) | [← Prev: Hardware](hardware.md) | [Next: Policy →](policy.md) | [📖 Glossary](glossary.md)

**Overview**: AI systems don't just produce outputs—they reshape how humans think, decide, and act. This area examines the human side of the human-AI equation: how people calibrate trust in automated systems, when they over-rely on or reject algorithmic advice, and how sustained AI use may alter cognition itself. Building on decades of research in [automation bias](glossary.md#automation-bias), dual-process theory, and human factors, these papers are essential for anyone designing AI systems that humans actually interact with—or studying what happens when they do.

## Trust, Reliance & Automation Bias
**Goal**: Understand when and why humans trust, distrust, or blindly follow AI systems

1. [Thinking, Fast and Slow](https://us.macmillan.com/books/9780374533557/thinkingfastandslow) (Kahneman, 2011)
   - *Why*: Foundational synthesis of dual-process theory (System 1/System 2) underpinning all research on human judgment heuristics and AI over-reliance
   - *Note*: Book, not a paper; essential background for understanding cognitive surrender and automation bias

2. 🔒 [Humans and Automation: Use, Misuse, Disuse, Abuse](https://journals.sagepub.com/doi/10.1518/001872097778543886) (Parasuraman & Riley, 1997)
   - *Why*: Seminal framework defining how humans interact with automation—overreliance, underutilization, and misuse; foundational taxonomy still used in modern AI interaction research

3. 🔒 [Trust in Automation: Designing for Appropriate Reliance](https://journals.sagepub.com/doi/10.1518/hfes.46.1.50_30392) (Lee & See, 2004)
   - *Why*: Introduces the calibrated trust model explaining why people adjust confidence in automated systems; directly applicable to designing AI assistants that foster appropriate (not blind) reliance

4. 🔒 [Algorithm Aversion: People Erroneously Avoid Algorithms After Seeing Them Err](https://psycnet.apa.org/record/2014-48748-001) (Dietvorst et al., 2015)
   - *Why*: Demonstrates the paradox where people reject statistically superior algorithms after observing single errors while tolerating worse human forecasters; the flip side of automation bias

## Cognitive Effects of AI
**Goal**: Understand how AI reshapes human thinking, memory, and reasoning

1. 🔒 [The Extended Mind](https://academic.oup.com/analysis/article-abstract/58/1/7/153111) (Clark & Chalmers, 1998)
   - *Why*: Philosophical foundation arguing that cognition extends beyond the brain into external tools and artifacts; essential grounding for understanding AI as a functional component of human thought

2. 🔒 [Cognitive Offloading](https://www.cell.com/trends/cognitive-sciences/abstract/S1364-6613(16)30098-5) (Risko & Gilbert, 2016)
   - *Why*: Foundational review of how people use external tools to reduce cognitive demand; distinguishes strategic offloading from the deeper abdication of judgment that AI enables

3. [Your Brain on ChatGPT: Accumulation of Cognitive Debt when Using an AI Assistant for Essay Writing Task](https://arxiv.org/abs/2506.08872) (Kosmyna et al., 2025)
   - *Why*: Neuroimaging study showing LLM users display weaker brain connectivity than search-engine or traditional learners; introduces "cognitive debt"—short-term cognitive relief creating long-term mental atrophy

4. [Thinking—Fast, Slow, and Artificial: How AI is Reshaping Human Reasoning and the Rise of Cognitive Surrender](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6097646) (Shaw & Nave, 2026)
   - *Why*: Introduces Tri-System Theory extending dual-process cognition with System 3 (artificial cognition); demonstrates "cognitive surrender"—adopting AI outputs with minimal scrutiny—across three preregistered experiments (N=1,372), showing AI access increases both accuracy and confidence even when the AI errs

## Human-AI Decision-Making
**Goal**: Learn how human-AI teams actually perform and how to improve collaboration

1. [The Principles and Limits of Algorithm-in-the-Loop Decision Making](https://dl.acm.org/doi/10.1145/3359152) (Green & Chen, 2019)
   - *Why*: Empirical study showing humans fail to accurately evaluate algorithmic reliability and don't calibrate reliance on system performance; reveals fundamental limits of algorithm-in-the-loop approaches

2. [Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance](https://arxiv.org/abs/2006.14779) (Bansal et al., 2021)
   - *Why*: Shows AI explanations increase human reliance regardless of correctness without improving complementary team performance; challenges the assumption that transparency alone fixes over-reliance

3. [To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI in AI-Assisted Decision-Making](https://arxiv.org/abs/2102.09692) (Buçinca et al., 2021)
   - *Why*: Demonstrates that cognitive forcing functions (requiring humans to commit to an answer before seeing AI advice) reduce over-reliance, though at cost of user satisfaction; practical intervention design for human-AI systems

---

**Related**: [Reasoning](reasoning.md) | [Safety](safety.md) | [Policy](policy.md)
