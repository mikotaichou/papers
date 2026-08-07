# Classics: The Historical Roots of Neural Networks

[← Back to Learning Path](../learning-path.md) | [Next: Foundations →](foundations.md) | [📖 Glossary](glossary.md)

**Overview**: This area tells the story of how the field arrived at trainable feedforward networks — the seventy-year lineage behind everything else in this collection. You'll follow the thread from Turing's universal machines and the McCulloch-Pitts formal neuron, through Rosenblatt's perceptron and the first AI winter, to the quiet independent inventions of [backpropagation](glossary.md#backpropagation) and [stochastic gradient descent](glossary.md#sgd-stochastic-gradient-descent), the associative memories of Amari and Hopfield, the connectionist revival of the 1980s, and the [vanishing gradient](glossary.md#vanishing-gradient-problem) wall whose eventual circumvention in 2006 launched modern [deep learning](glossary.md#deep-learning). These papers are history rather than prerequisites — but reading them explains *why* [CNNs](glossary.md#cnn-convolutional-neural-network), [RNNs](glossary.md#rnn-recurrent-neural-network), and gradient training look the way they do, and how often the field forgot and reinvented its own ideas.

## Computation & the First Neurons
**Goal**: Understand the theoretical bedrock — universal computation and the neuron as a logical unit

1. [On Computable Numbers, with an Application to the Entscheidungsproblem](https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf) (Turing, 1936)
   - *Why*: **Universal computation** - defines the Turing machine and the boundary between computable and uncomputable; the premise that a machine can in principle compute anything a brain computes underlies the entire field

2. [A Logical Calculus of the Ideas Immanent in Nervous Activity](https://www.cs.cmu.edu/~./epxing/Class/10715/reading/McCulloch.and.Pitts.pdf) (McCulloch & Pitts, 1943)
   - *Why*: **The founding abstraction** - models the neuron as a binary threshold logic unit and proves networks of them can compute any propositional-logic expression; every artificial neuron since is a descendant, and von Neumann cited it in the EDVAC report

3. [Intelligent Machinery](https://weightagnostic.github.io/papers/turing1948.pdf) (Turing, 1948)
   - *Why*: **The first learning-machine proposal** - describes "unorganised machines," randomly connected networks of NAND-like units trained by interference rather than programmed; dismissed by Turing's supervisor as a "schoolboy essay" and unpublished for 20 years

4. [The Organization of Behavior](https://archive.org/details/in.ernet.dli.2015.97836) (Hebb, 1949)
   - *Why*: **"Cells that fire together wire together"** - the first concrete, biologically grounded learning rule (activity-dependent synaptic strengthening) and the cell-assembly idea; direct ancestor of the perceptron rule and Hopfield's storage prescription
   - *Note*: Chapter 4 carries the learning rule; the full book is optional

## Perceptrons & the First Winter
**Goal**: See machine learning become an empirical discipline — and hit its first wall

1. [The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain](https://www.ling.upenn.edu/courses/cogs501/Rosenblatt1958.pdf) (Rosenblatt, 1958)
   - *Why*: **The first trainable classifier** - an error-correction rule with a convergence guarantee and a physical implementation (the Mark I Perceptron); machine learning becomes engineering rather than formalism, and the target of the critique that defined the next fifteen years

2. [Adaptive Switching Circuits](https://isl.stanford.edu/~widrow/papers/c1960adaptiveswitching.pdf) (Widrow & Hoff, 1960)
   - *Why*: **ADALINE and the LMS/delta rule** - least-mean-squares [gradient descent](glossary.md#gradient-descent) on a continuous error surface, in working hardware; the direct precursor of backprop's per-unit weight update and the most-deployed adaptive algorithm in history via adaptive filters

3. [Principles of Neurodynamics: Perceptrons and the Theory of Brain Mechanisms](https://gwern.net/doc/ai/nn/1962-rosenblatt-principlesofneurodynamics.pdf) (Rosenblatt, 1962)
   - *Why*: **The full perceptron theory** - multi-layer "cross-coupled" perceptrons, the convergence theorem, and Rosenblatt's own attempts at training hidden layers; reading it shows Minsky & Papert's target was narrower than the field remembers

4. [A Theory of Adaptive Pattern Classifiers](https://people.idsia.ch/~juergen/amari1967.pdf) (Amari, 1967)
   - *Why*: **SGD for multilayer nets, twenty years early** - stochastic gradient descent on non-separable pattern distributions, including (with his student Saito) a trained five-layer network with modifiable hidden layers learning a non-linearly-separable problem

5. 🔒 [Perceptrons: An Introduction to Computational Geometry](https://archive.org/details/perceptronsintro0000mins) (Minsky & Papert, 1969)
   - *Why*: **The book blamed for the first AI winter** - a rigorous geometric analysis of what single-layer perceptrons cannot represent (parity, connectedness, XOR); its reception collapsed neural network funding until multi-layer training became practical in the mid-1980s
   - *Note*: Paywalled - archive.org controlled digital lending (borrow required)

## Backprop's Prehistory & Associative Memory
**Goal**: Watch the core algorithms of deep learning get invented — outside the spotlight

1. [The Representation of the Cumulative Rounding Error of an Algorithm as a Taylor Expansion of the Local Rounding Errors](https://people.idsia.ch/~juergen/linnainmaa1970thesis.pdf) (Linnainmaa, 1970)
   - *Why*: **Reverse-mode automatic differentiation** - the first publication of the algorithm now called [backpropagation](glossary.md#backpropagation), derived for rounding-error analysis on arbitrary computation graphs, with working FORTRAN code; everything from `loss.backward()` to JAX's `grad` is this algorithm
   - *Note*: Master's thesis in Finnish; the readable English version is [Linnainmaa 1976](https://papers.baulab.info/papers/also/Linnainmaa-1976.pdf)

2. [Polynomial Theory of Complex Systems](https://www.gmdh.net/articles/history/polynomial.pdf) (Ivakhnenko, 1971)
   - *Why*: **The first working deep networks** - the Group Method of Data Handling grows and prunes layers of polynomial units by validation error, reporting a trained 8-layer network; deep learning's earliest working instance, from Soviet cybernetics

3. [Learning Patterns and Pattern Sequences by Self-Organizing Nets of Threshold Elements](https://people.idsia.ch/~juergen/amari1972hopfield.pdf) (Amari, 1972)
   - *Why*: **Associative memory a decade before Hopfield** - shows that recurrent nets of threshold elements can store patterns and pattern sequences as stable equilibrium states and recall them under noise; the earliest formulation of what later became known as the Hopfield network

4. [Beyond Regression: New Tools for Prediction and Analysis in the Behavioral Sciences](https://gwern.net/doc/ai/nn/1974-werbos.pdf) (Werbos, 1974)
   - *Why*: **Backprop proposed for learning** - derives ordered-derivative chain-rule differentiation for arbitrary nonlinear systems and proposes applying it to modelling; the thesis the 1986 backprop paper is standardly credited with rediscovering
   - *Note*: Whether the NN-specific efficient form dates to this thesis or to Werbos's 1982 paper is disputed (Schmidhuber vs. Werbos); his readable [1990 backprop-through-time overview](https://www.cs.cmu.edu/~bhiksha/courses/deeplearning/Fall.2016/pdfs/Werbos.backprop.pdf) states the history explicitly

5. 🔒 [Cognitron: A Self-Organizing Multilayered Neural Network](https://link.springer.com/article/10.1007/BF00342633) (Fukushima, 1975)
   - *Why*: **Unsupervised multilayer self-organization** - develops progressively larger receptive fields in deeper layers without a teacher; the direct predecessor of the Neocognitron
   - *Note*: Paywalled - Springer, Biological Cybernetics

## Attractors & Self-Organization
**Goal**: See memory and representation emerge from network dynamics rather than supervision

1. [Neocognitron: A Self-Organizing Neural Network Model for a Mechanism of Pattern Recognition Unaffected by Shift in Position](https://www.cs.princeton.edu/courses/archive/spr08/cos598B/Readings/Fukushima1980.pdf) (Fukushima, 1980)
   - *Why*: **The CNN's architectural ancestor** - alternating S-cell/C-cell layers give local receptive fields, weight sharing, and shift invariance, built explicitly on Hubel & Wiesel's visual cortex findings; LeNet is this structure plus backprop

2. [Neural Networks and Physical Systems with Emergent Collective Computational Abilities](https://pmc.ncbi.nlm.nih.gov/articles/PMC346238/) (Hopfield, 1982)
   - *Why*: **Attractor dynamics as memory** - recurrent symmetric networks as an energy-minimizing dynamical system with content-addressable memory as attractors; made connectionism respectable to physicists and earned half the 2024 Nobel Prize in Physics

3. [Self-Organized Formation of Topologically Correct Feature Maps](https://www.cnbc.cmu.edu/~tai/nc19journalclubs/Kohonen1982_Article_Self-organizedFormationOfTopol.pdf) (Kohonen, 1982)
   - *Why*: **Self-organizing maps** - topology-preserving representation learning with no teacher and no gradient; the canonical unsupervised branch of the revival and the counterweight to the backprop lineage

## The Connectionist Revival
**Goal**: Understand how hidden representations became learnable — and the field came back to life

1. [A Learning Algorithm for Boltzmann Machines](https://www.cs.toronto.edu/~hinton/absps/cogscibm.pdf) (Ackley, Hinton & Sejnowski, 1985)
   - *Why*: **Hidden units get a learning rule** - takes Hopfield's energy formulation stochastic and derives learning for hidden units; where "learn internal representations" becomes a stated goal, and the direct ancestor of the RBM that reappears in 2006

2. [Learning Representations by Back-Propagating Errors](https://www.cs.toronto.edu/~hinton/absps/naturebp.pdf) (Rumelhart, Hinton & Williams, 1986)
   - *Why*: **The paper that ended the perceptron winter** - not the first derivation of backprop (see Linnainmaa 1970, Werbos 1974) but the one that showed it learns useful hidden representations and convinced the field; short enough to read in a sitting
   - *Note*: The full-length version with the XOR experiments and mechanics is [PDP Vol. 1, Chapter 8](https://www.cs.toronto.edu/~hinton/absps/pdp8.pdf)

3. [Backpropagation Applied to Handwritten Zip Code Recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-89e.pdf) (LeCun et al., 1989)
   - *Why*: **The first deployed neural network** - Fukushima's architecture plus Rumelhart's algorithm plus real USPS data; introduces weight sharing as an architectural prior rather than a biological analogy, and leads directly to LeNet in the Foundations area

4. [Approximation by Superpositions of a Sigmoidal Function](https://web.njit.edu/~usman/courses/cs675_fall18/10.1.1.441.7873.pdf) (Cybenko, 1989)
   - *Why*: **The universal approximation theorem** - a single hidden layer suffices in principle (Hornik et al. 1989 generalizes to broader activations); the theoretical license for the enterprise, and the setup for the field's later realization that representability is not learnability

5. [Finding Structure in Time](https://gwern.net/doc/ai/nn/rnn/1990-elman.pdf) (Elman, 1990)
   - *Why*: **Recurrence discovers structure** - context units feeding hidden state back to itself let a network discover lexical categories and constituent structure from raw sequences; the conceptual origin of every recurrent language model

## Limits, Winter, and the Way Out
**Goal**: Understand why deep nets didn't train — and the 2006 breakthrough that changed it

1. [Untersuchungen zu dynamischen neuronalen Netzen](https://people.idsia.ch/~juergen/SeppHochreiter1991ThesisAdvisorSchmidhuber.pdf) (Hochreiter, 1991)
   - *Why*: **The vanishing gradient identified** - the first formal analysis of the [vanishing/exploding gradient problem](glossary.md#vanishing-gradient-problem), the reason deep and recurrent nets did not train and thus the reason the second winter happened
   - *Note*: Diploma thesis in German; the readable English statement is the next entry

2. [Learning Long-Term Dependencies with Gradient Descent is Difficult](https://www.comp.hkbu.edu.hk/~markus/teaching/comp7650/tnn-94-gradient.pdf) (Bengio, Simard & Frasconi, 1994)
   - *Why*: **The theorem behind the second winter** - proves the trade-off between robustly latching information and efficient gradient-based learning; directly motivates the [LSTM](glossary.md#lstm-long-short-term-memory) (see Foundations), gating, residual connections, and ultimately attention

3. [A Fast Learning Algorithm for Deep Belief Nets](https://www.cs.toronto.edu/~hinton/absps/fastnc.pdf) (Hinton, Osindero & Teh, 2006)
   - *Why*: **The paper that restarted the field** - greedy layer-wise unsupervised pretraining with stacked RBMs makes deep networks trainable for the first time, sidestepping the vanishing-gradient wall, and gives "deep learning" its name

4. [Reducing the Dimensionality of Data with Neural Networks](https://www.cs.toronto.edu/~hinton/absps/science.pdf) (Hinton & Salakhutdinov, 2006)
   - *Why*: **Deep learning goes public** - deep [autoencoders](glossary.md#autoencoder) beating PCA, in Science, with pictures; together with deep belief nets this is the hinge between this historical area and the modern era covered in Foundations

## Guides & Retrospectives
**Goal**: Get the map of the whole lineage — including the credit disputes

1. [Annotated History of Modern AI and Deep Neural Networks](https://arxiv.org/abs/2212.11279) (Schmidhuber, 2022)
   - *Why*: **The link-rich narrative of this whole area** - the reason Ivakhnenko, Amari, and Linnainmaa are known to the modern field at all; accurate on dates and citations, but Schmidhuber is a partisan in most of the priority disputes he describes, so read it as an opinionated brief

2. [Deep Learning in Neural Networks: An Overview](https://arxiv.org/abs/1404.7828) (Schmidhuber, 2015)
   - *Why*: **The reference map** - 88 pages and ~900 references organized by credit-assignment path depth; sections 5.1-5.5 cover the pre-1980 story told in this area

3. [On the Origin of Deep Learning](https://arxiv.org/abs/1702.07800) (Wang & Raj, 2017)
   - *Why*: **The neutral survey** - a pedagogical walk through the same lineage (McCulloch-Pitts → Hebb → perceptron → Hopfield → Boltzmann → backprop → modern) with actual derivations; a good counterweight to Schmidhuber's framing

---

**Related**: [Foundations](foundations.md) | [Architectures](architectures.md) | [Human-AI Interaction](human-ai-interaction.md)
