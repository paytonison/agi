# **Conscious Models as a Necessary Step Toward AGI**

**Tagline:**
> _Bigger models aren’t enough. AGI needs a world-and-self model that knows it’s the thing doing the thinking._

This repo holds the LaTeX source for the paper:
> **Conscious Models as a Necessary Step Toward Artificial General Intelligence**  
> Author: **Payton Ison — Lead Architect and Designer of the Singularity**

The paper argues that **conscious models**—globally accessible, self-referential, temporally deep world-and-self models that sit in the control loop—are not a nice-to-have on the way to AGI. They’re a **necessary architectural ingredient**.

---
## **1. Quick Orientation**
- **What this is:**
    A publication-ready LaTeX paper that makes the case that you **cannot** get robust, open-ended AGI in realistic environments without something functionally equivalent to machine consciousness.
    
- **What it is not (yet):**
    - No code implementation of the architecture (you can add that here).
    - No simulation benchmarks (also a natural fit for this repo).
    
- **Audience:**    
    - AGI researchers and architects
    - Alignment / safety people
    - Cognitive science/philosophy of mind folks interested in machine consciousness

---
## **2. Repo Layout**
Suggested structure (adapt names as needed to match your actual files):

```
.
├── README.md
├── paper/
│   ├── main.tex      # Main LaTeX source
│   └── figures/                      # (Optional) figures
│       └── ...
├── build/                            # (Optional) compiled outputs (gitignored)
│   └── conscious-models-agi.pdf
└── experiments/                      # (Optional) code for future toy agents
    └── ...
```
---
## **3. Building the Paper**
### **3.1 Requirements**

Install any modern LaTeX distribution, e.g.:
- **TeX Live** (Linux/macOS/Windows) 
- **MacTeX** (macOS)
- **MiKTeX** (Windows)

The paper uses only standard packages:
- geometry
- amsmath, amssymb, amsthm
- graphicx
- enumitem
- microtype
- hyperref

No BibTeX/BibLaTeX setup is required in the current version; citations are defined with thebibliography.
### **3.2 Build commands**
From the repo root (adjust for your actual file path):

```
pdflatex main.tex
pdflatex main.tex
```

Or with latexmk:

```
latexmk -pdf main.tex
```

The main output will be:

```
main.pdf
```

You can move or copy it into build/ if you want a clean separation of source vs. artifacts.

---
## **4. Core Thesis**
### **4.1 One-sentence version**  
> **To get real AGI in an open-ended world, you need an internal conscious model: a globally accessible, self-referential, temporally deep world-and-self model that lives in the control loop.**
### **4.2 Slightly longer version**
The paper defines a **conscious model** in strictly functional/architectural terms (no metaphysical commitments):
- A **limited-capacity global workspace** whose contents are available to perception, memory, planning, language, and motor systems.
- An explicit **self-model**: the agent’s body/interface, capabilities, limitations, goals, and identity over time.
- An egocentric, **situated perspective** that supports indexicals like “I, here, now, this action”.
- **Temporally deep simulation**: counterfactual futures, uncertainty, and value estimates.
- Direct **control relevance**: what is “in” this model systematically shapes deliberate, value-laden decisions.

The central claim (the **Conscious Model Thesis**) is:
> Any artificial system that robustly satisfies the functional criteria for AGI in an open-ended, partially observed, stochastic environment must implement at least one such conscious model (or an architecture functionally equivalent in all relevant respects).

---
## **5. Conceptual Map of the Paper**

This section is a high-level guide so you can jump around the TeX file intelligently.
### **5.1 Introduction**
- Frames the gap between current foundation models and genuine AGI.    
- Sets up the question: is more scale enough, or is a new architectural ingredient required?
- Answers: that ingredient is a **conscious model**.
### **5.2 Background: AGI and Consciousness**
- Defines AGI as **embedded, autonomous, open-ended general intelligence** (not just benchmark scores).    
- Distinguishes:
    - **Phenomenal consciousness** (subjective feeling)
    - **Access consciousness** (globally available information)
    
- Summarizes key scientific theories:
    - Global Workspace / Global Neuronal Workspace
    - Higher-order / self-model theories
    - Predictive processing / active inference
    - Attention schema
    
- Shows how these converge on similar architectural motifs: global broadcast, self-models, temporally deep control.
### **5.3 The Conscious Model Thesis**
- Gives a precise definition of a **conscious model** in an artificial agent (global accessibility, self-modeling, situatedness, temporally deep simulation, control relevance).    
- Argues the thesis along four main axes:
    1. **Global coherence and cross-domain integration**
    2. **Self-modeling and indexical reasoning**
    3. **Temporally deep, value-sensitive control**
    4. **Alignment, value grounding, and interpretability**

### **5.4 Requirements for Conscious Models in AGI**

Specifies design constraints:
- **Representational**:
    - Multimodal integration
    - Hierarchical abstraction
    - Egocentric + allocentric coordinate frames
    - Uncertainty and counterfactuals
    
- **Dynamical**:
    - Workspace bottleneck + competition
    - Broadcast + feedback loops
    - Persistent but revisable context
    - Self-monitoring and meta-control
    
- **Formal sketch**:
    - World model M_t
    - Self-model S_t
    - Workspace W_t
    - Actions A_t
    - Simple update equations showing how these interact.
### **5.5 Non-Conscious vs Conscious Architectures**

Compares:
- **Scaled LLM-style models** (feedforward/autoregressive):
    - No durable self, no grounded world model, no explicit control interface.
    
- **Purely modular RL agents** without a global workspace:
    - Coordination overhead, fragmented self-representation, poor meta-cognition.
    
- **Conscious-model architectures**:
    - Global integrative hub.
    - Coherent self-model.
    - Natural home for meta-cognition and alignment machinery.
### **5.6 Design Patterns for Conscious Models**

Sketches several families of architectures:
1. **Global workspace over foundation models**
    - Workspace + routing + self-model supervising multiple specialized models (language, vision, code, motor control).
    
2. **Predictive processing with explicit self-latents**
    - Hierarchical generative models with self-variables at the top; conscious state ≈ posterior over world + self-latents.
    
3. **Simulation-based meta-controllers**
    - Conscious model as the locus for internal rollouts, value evaluation, and final action selection.
### **5.7 Evaluating Machine Consciousness for AGI**

Proposes multi-layer evaluation:

- **Behavioral**:    
    - Coherent reporting of internal states,
    - Error awareness and correction,
    - Self-directed learning and goal formation.
    
- **Structural / information-theoretic**:
    - Evidence of global broadcast and bottlenecks,
    - Localized self-model,
    - Measurable temporally deep simulation processes.
    
- **Safety-oriented**:
    - How values, norms, and corrigibility are represented within the conscious model itself.
### **5.8 Objections and Replies**

Addresses:

- “Intelligence doesn’t require consciousness.”    
- “Consciousness will emerge automatically at scale.”
- “Conscious AGI is too dangerous or unethical; avoid it.”
- “This doesn’t solve the hard problem.”

The replies lean heavily on **engineering constraints** (resource-bounded, learnable, maintainable architectures) instead of metaphysics.
### **5.9 Implications, Roadmap, and Conclusion**

- Architecture matters more than pure scale.    
- Embodiment, continual interaction, and meta-cognition should be central design targets.
- Conscious models may **improve safety** by making internal states more interpretable.
- Outlines a roadmap:
    1. Formalization
    2. Toy architectures
    3. Integration with large models / richer embodiments
    4. Evaluation + governance

---
## **6. How to Use This Repo**
### **6.1 If you’re a reader / theorist**

Build the PDF and use it as:

- **Position paper** in AGI discussions.
- Reference when arguing that “just scale it” is likely insufficient.
- Conceptual scaffold for comparing architectures (does this design have a conscious model or not?)
### **6.2 If you’re an implementer**

Extend the repo along these lines:

```
experiments/
  ├── toy_gridworld_conscious_vs_baseline/
  ├── workspace_over_llm/
  └── predictive_self_latents/
src/
  ├── workspace/
  ├── self_model/
  ├── world_model/
  └── meta_controller/
notebooks/
  ├── workspace-dynamics.ipynb
  ├── self-model-consistency.ipynb
  └── simulation-depth-vs-performance.ipynb
```

Possible experiment ideas directly inspired by the paper:

- Compare agents **with vs. without** a global workspace on tasks that require long-horizon credit assignment and cross-modal integration. 

- Study how an explicit **self-model** affects:
    - catastrophic failure modes,
    - calibration of uncertainty,
    - and consistency in self-referential reporting.
    
- Implement a simple **simulation-based meta-controller** and measure whether explicitly representing counterfactual futures in a workspace improves safety and performance. 
### **6.3 If you’re doing alignment / safety work**

Use the conscious model as a **natural alignment interface**:

- Define constraints and value structures **inside the conscious model**, not scattered across opaque weights.    

- Design tools that:
    - Probe and visualize W_t (the workspace state),
    - Inspect and modify S_t (the self-model),
    - Audit how these drive A_t (actions) in high-stakes scenarios.

---
## **7. Extending the Paper**

Future extensions you can track as issues / milestones:

- **More formal theory**    
    - Full probabilistic / decision-theoretic treatment of M_t, S_t, W_t, A_t.
    - Links to free energy, expected utility, and multi-objective optimization.
    
- **Case studies**
    - Analyze real architectures (LLM agents, RL agents with memory, classical cognitive architectures) under the conscious-model lens.
    - Concrete “upgrade plans” that show what adding a conscious model would look like.
    
- **Deeper safety analysis**
    - Formalization of “conscious corrigibility” and “value reflection”.
    - Protocols for safe interventions in the conscious model (forcing functions, oversight hooks, etc.).
    
- **Benchmark suite**
    - Tasks that are specifically hard without:
        - self-awareness,
        - counterfactual simulation from the agent’s own POV,
        - and explicit value modeling in the control loop.

---
## **8. Citation**

```
@misc{payton_conscious_models_agi_2025,
  title  = {Conscious Models as a Necessary Step Toward Artificial General Intelligence},
  author = {Payton Ison},
  year   = {2025},
  note   = {Manuscript},
}
```

---
## **9. License**

> This repository is licensed under **MIT** for all code and **CC BY 4.0** for the paper text.

---
## **10. Contact / Links**

Add whatever you want here:

- Contact email
	- isonpayton@gmail.com
- Project page / personal site
	- https://x.com/p8on_
