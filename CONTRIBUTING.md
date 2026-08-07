# Contributing to AI/ML Papers Collection

Thank you for your interest in contributing! This document describes how the repo is organized, the exact formats in use, and the validation that keeps everything consistent.

## 📋 Table of Contents

- [How This Repo Stays Consistent](#how-this-repo-stays-consistent)
- [Ways to Contribute](#ways-to-contribute)
- [Paper Selection Criteria](#paper-selection-criteria)
- [How to Add a Paper](#how-to-add-a-paper)
- [Entry Format Reference](#entry-format-reference)
- [Glossary Contributions](#glossary-contributions)
- [How to Fix Issues](#how-to-fix-issues)
- [Code of Conduct](#code-of-conduct)

---

## 🔒 How This Repo Stays Consistent

The repo validates itself — all machinery lives in the repo, nothing external:

- **`scripts/validate.py`** is the single source of truth for every invariant: papers listed in both a topic file and `by-date.md`, chronological ordering, entry format, emoji rules, resolvable anchors, and derived counts. Run it any time:

  ```bash
  python3 scripts/validate.py          # report problems (file:line + fix hint)
  python3 scripts/validate.py --fix    # apply mechanical fixes (counts, ordering,
                                       # numbering, back-links, README coverage block)
  python3 scripts/validate.py --links  # on-demand external link-rot check (network)
  ```

- **Git pre-commit hook** (`githooks/pre-commit`): every commit is blocked until the validator passes. Activation is automatic — the validator sets `git config core.hooksPath githooks` on any run, so a fresh clone converges on its own. Escape hatch: `git commit --no-verify`.
- **Claude Code hooks** (`.claude/settings.json`, tracked): after any edit to an index file, and before an agent finishes, the validator runs and feeds failures back to the agent. Hook config is snapshotted at session start — a new session picks up changes.

**Never hand-edit counts.** The README badges, the per-area table numbers, the totals, the Coverage-by-Topic block, and the `by-date.md` footer stats are all derived. Run `python3 scripts/validate.py --fix` instead.

---

## 🎯 Ways to Contribute

1. **Suggest new papers** — open an issue with the [paper suggestion template](../../issues/new?template=paper-suggestion.yml)
2. **Fix broken links** — [report one](../../issues/new?template=broken-link.yml) or submit a PR (`python3 scripts/validate.py --links` finds them)
3. **Improve annotations** — better "Why" explanations are always welcome
4. **Add glossary terms** — [suggest a term](../../issues/new?template=glossary-term.yml)
5. **Report errors** — typos, wrong dates, miscategorizations

---

## 📚 Paper Selection Criteria

### Must Have
- [ ] **Influential or foundational** — highly cited, introduced key concepts, or represents a significant advance
- [ ] **Accessible** — available via arXiv, proceedings, or author's website (open access preferred)
- [ ] **Relevant** — fits within the AI/ML research landscape

### Strong Preference
- [ ] **Pedagogically valuable** — clear writing that teaches concepts effectively
- [ ] **Well-scoped** — focused contribution that's digestible
- [ ] **Reproducible** — methods described in enough detail to replicate

### Area Fit

The 15 areas (names match each file's title):

| Area file | Canonical name | Example papers |
|-----------|----------------|----------------|
| `learning/classics.md` | Classics: The Historical Roots of Neural Networks | McCulloch-Pitts, Perceptron, Hopfield 1982 |
| `learning/foundations.md` | Foundations (Start Here) | LeNet, AlexNet, Word2Vec |
| `learning/language-models.md` | Large Language Models | BERT, GPT-3, Transformers |
| `learning/attention.md` | Attention Mechanisms & Context | FlashAttention, RetNet |
| `learning/retrieval.md` | Retrieval & Knowledge Systems | RAG, Dense Passage Retrieval |
| `learning/reasoning.md` | Reasoning & Agents | ReAct, RLHF, PPO |
| `learning/architectures.md` | Novel Architectures & Theory | Mamba, KAN, Neural Turing Machines |
| `learning/interpretability.md` | Interpretability & Evaluation | LIME, Integrated Gradients |
| `learning/safety.md` | Security, Safety & Robustness | Prompt injection, red teaming, alignment |
| `learning/advanced.md` | Advanced Topics & Applications | AI Scientist, TabPFN |
| `learning/probabilistic.md` | Probabilistic & Bayesian Approaches | Probabilistic programming, diffusion theory |
| `learning/vision.md` | Vision & Multimodal Systems | ViT, CLIP, SAM |
| `learning/hardware.md` | Hardware & Systems | GPU optimization, photonics, VLSI |
| `learning/human-ai-interaction.md` | Human-AI Interaction & Cognition | Automation bias, cognitive offloading |
| `learning/policy.md` | Policy, Safety & Societal Impact | GDPR, EU AI Act, NIST AI RMF |

---

## 📝 How to Add a Paper

### Option 1: GitHub Issue (easiest)

1. Go to [Issues → New Issue](../../issues/new/choose) and pick "Paper Suggestion"
2. Fill in title, link (arXiv preferred), authors, year, suggested area, and a 1–2 sentence "Why read this?"

### Option 2: Claude Code `/add-paper` (maintainer workflow)

Run `/add-paper <url>` in Claude Code. It fetches metadata, proposes an area and section, and after confirmation edits the topic file and `by-date.md`, runs the validator (`--fix` updates all derived counts), and lands the change via a branch + PR.

### Option 3: Pull Request by hand

1. Fork and branch: `git checkout -b add-paper-<short-name>`
2. Append the paper as the **next numbered entry** in the best-fit section of the area file (format below)
3. Add a bullet to `by-date.md` under `## YYYY` / `### YYYY.MM` (newest first, arXiv submission month is authoritative) **including the area back-link**
4. Run `python3 scripts/validate.py --fix`, then confirm `python3 scripts/validate.py` reports 0 errors
5. Commit (the pre-commit hook re-validates) and open a PR

---

## 🎨 Entry Format Reference

These are the formats actually used by every entry in the repo — the validator enforces them.

### Topic file entry (`learning/*.md`)

```markdown
7. [Full Paper Title](https://arxiv.org/abs/XXXX.XXXXX) (Authors et al., YYYY)
   - *Why*: One or two concise sentences on why the paper matters and what the reader learns.
   - *Note*: Optional extra context, cross-listing, or caveats.
```

- Numbering is sequential within each `##` section (the validator can renumber via `--fix`)
- Continuation bullets are indented to align under the title (3 spaces for 1-digit numbers, 4 for 2-digit); deeper nesting is fine
- Policy documents (in `learning/policy.md` only) prefix the link with `📄 `; they may also carry `- *Status*:` lines for legal status
- Paywalled papers prefix the link with `🔒 `
- Cross-listing: a paper gets **one** numbered entry per file; a second section references it with an unnumbered `*See also*:` line

### by-date.md bullet

```markdown
- [Full Paper Title](https://arxiv.org/abs/XXXX.XXXXX) (Authors et al., YYYY) — [Area](learning/area.md)
- 📄 [Policy Document Title](https://example.gov/...) (Jurisdiction, YYYY) — [Policy & Governance](learning/policy.md)
- 🔒 [Paywalled Title](https://journal...) (Authors, YYYY) - *Paywalled* — [Area](learning/area.md)
```

- Every bullet ends with an **area back-link** to the topic file that lists the paper (`--fix` adds these)
- arXiv entries are filed under their submission month (`### YYYY.MM`); undated policy documents sit directly under the `## YYYY` heading

### Emoji key

| Emoji | Meaning |
|-------|---------|
| 📄 | Policy/governance document (policy area only) |
| 🔒 | Paywalled content (also gets the ` - *Paywalled*` suffix in by-date.md) |

Research papers carry **no** emoji.

### Link preference

1. arXiv abstract page: `https://arxiv.org/abs/XXXX.XXXXX` (preferred — stable, un-versioned)
2. Conference proceedings page
3. Direct PDF (last resort; avoid versioned URLs like `...v3.pdf`, they rot)

### "Why" annotations

- **Concise**: 1–2 sentences
- **Specific**: what will the reader learn?
- **Contextual**: how does this relate to other papers?

Good: *Introduces the Transformer architecture that became the foundation for modern LLMs; essential for understanding attention mechanisms.*
Too vague: *An important paper about neural networks.*

---

## 📊 Glossary Contributions

Glossary terms in `learning/glossary.md` use the format every existing term uses:

```markdown
### Term Name
One to three sentences of plain-prose definition, with context on where the term
shows up and how it relates to nearby concepts.
```

- Place terms in alphabetical order within the appropriate `##` category
- Acronyms also go in the (alphabetized) Acronyms Quick Reference table
- Topic files link to terms as `glossary.md#term-name` — the validator checks these anchors resolve

---

## 🔧 How to Fix Issues

### Broken links
1. Confirm with `python3 scripts/validate.py --links`
2. Find the correct URL: [arXiv](https://arxiv.org), [Semantic Scholar](https://semanticscholar.org), author/institutional pages
3. Open an issue or submit a PR (update the topic file **and** `by-date.md` — the validator checks both)

### Typos and corrections
Small fixes: edit directly on GitHub and submit a PR. Larger changes: open an issue first.

---

## 🤝 Code of Conduct

**Our standards**: be respectful and constructive; focus on the technical merits of papers; welcome newcomers; acknowledge different perspectives on paper importance.

**Not acceptable**: dismissive or rude comments; personal attacks; spam or self-promotion; off-topic discussions.

---

## ❓ Questions?

- **General questions**: open a [Discussion](../../discussions)
- **Bug reports**: open an [Issue](../../issues)
- **Paper debates**: use Discussions to debate inclusion/classification

Thank you for helping make this resource better for the AI/ML learning community! 🚀
