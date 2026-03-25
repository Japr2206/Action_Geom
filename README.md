# 📘 Geometry of Learning — Computational README

## 🔬 What this repository contributes

This repository is the **computational realization** of the paper’s main claim:

> **observable learning trajectories are not exhausted by endpoint metrics; they also contain internal temporal and structural organization that can be detected, summarized, and analyzed computationally.**

The code is therefore not a numerical appendix or a visualization add-on.  
It implements a **reproducible structural-analysis pipeline** grounded in the mathematical objects introduced in the manuscript and translated into executable procedures.

In practical terms, the repository shows that the paper’s formal layer can be turned into a usable computational workflow that can:

- localize trajectory structure through centered windows,
- compute interpretable local observables,
- build temporal structural profiles,
- detect boundaries and transitions,
- recover macro-regimes,
- compare trajectory families beyond endpoint summaries,
- and validate the framework on both synthetic and public external cases.

That is the repository’s central scientific role.

---

## 🧠 Core message of the project

The main computational idea is simple:

**two runs can end with similar final loss or final accuracy and still differ meaningfully in their internal temporal organization.**

This repository studies that internal organization through mathematically motivated descriptors rather than ad hoc feature engineering.

The code is built from the paper’s structural language:

1. **local windows** as discrete analogues of local jets,
2. **admissible observables** on those windows,
3. **structural profiles** along time,
4. **structural mass** as an integrated summary of mesoscopic activity,
5. **superlevel geometry** to isolate structurally active zones,
6. **corrected multiscale boundary parsing** to detect changes,
7. **event and regime extraction** to recover large-scale temporal organization.

This means the mathematics is not only providing notation.  
It determines **what is computed, how it is computed, and why the resulting quantities are meaningful**.

---

## 🧭 Scope of the repository

This repository is focused on **structural analysis of observable learning trajectories**.

It is **not** an early-stopping rule and **not** a learning-rate selection criterion.  
Its purpose is different:

- to define stable structural descriptors for trajectory organization,
- to operationalize them in a reproducible computational pipeline,
- and to evaluate whether they recover nontrivial temporal information beyond terminal summaries.

That distinction matters both scientifically and editorially.

---

## 🧩 From theory to executable objects

### 1. Local jets become centered discrete windows

The manuscript studies local behavior through local trajectory structure.  
In the code, that becomes a centered window extracted around each admissible iteration.

This creates a localized view of the trajectory instead of collapsing the entire run into a single scalar.  
That move preserves temporal information and enables the later structural layers.

### 2. Local observables become measurable descriptors

The code computes three central local observables:

- **oscillation**,
- **triangular excess**,
- **second-order window mass**.

These are structurally meaningful quantities.  
They measure complementary aspects of local shape:

- spread inside the window,
- non-geodesicity or non-flatness,
- and second-order bending / acceleration.

This is where the formal layer becomes computationally useful: the method compresses local geometry into finite-dimensional descriptors that remain interpretable.

### 3. Structural profiles convert local geometry into temporal signals

Once local observables are computed over valid centers, they are assembled into **profiles along time**.

These profiles are mesoscopic signals.  
They indicate where the trajectory is locally smooth, curved, structurally active, or unstable.

This is one of the key computational steps of the repository:

- a high-dimensional trajectory becomes a small number of informative temporal signals,
- those signals can be compared across runs,
- and they can be summarized statistically across seeds and conditions.

### 4. Structural mass bridges local and global description

The code integrates profiles into quantities such as **structural mass**.

This matters because it links:

- local behavior,
- mesoscopic activity,
- and global trajectory characterization.

The result is a useful balance:

- profiles remain available for interpretation,
- while compact scalar summaries remain available for tables and classification experiments.

### 5. Superlevel geometry isolates structurally active zones

Thresholding structural energy into **superlevel sets** turns a temporal signal into a geometric object:

- a mask,
- connected components,
- and candidate boundaries.

This lets the method quantify not only *how much* structural activity exists, but also its **location**, **persistence**, and **fragmentation**.

### 6. Corrected multiscale boundary parsing turns structure into temporal intelligence

A major contribution of the computational layer is the **corrected multiscale boundary parser**.

Instead of treating raw peaks of activity as transitions, the parser combines:

- left/right contrast in structural profiles,
- residual-energy contrast,
- and fine-scale shape information.

This is important because **activity is not automatically the same as change**.

The parser therefore sharpens the temporal story:

- it proposes boundary candidates,
- it distinguishes persistent zones from transition points,
- and it supports the recovery of events and regimes.

### 7. Events and regimes make the output explanatory

The final outputs of the pipeline are not only classification scores.  
The repository can also recover:

- boundary peaks,
- event intervals,
- transition zones,
- macro-regimes,
- and regime-level summaries.

That matters because the framework is explanatory rather than merely predictive: it tries to say **where** changes happen and **how** the trajectory is organized over time.

---

## 🧪 Synthetic study: controlled identifiability environment

The synthetic layer is not meant to claim benchmark leadership.  
Its role is to provide a **controlled laboratory** in which temporal organization is partially known in advance.

The code generates structured families such as:

- homogeneous dynamics,
- oscillatory dynamics,
- pulse dynamics,
- regime-change dynamics,
- three-phase dynamics.

This makes the synthetic experiment mathematically useful: the descriptors can be tested against settings where different types of temporal organization are deliberately present.

So the synthetic layer is not a weak toy example.  
It is a **controlled identifiability environment** for the theory.

---

## 🔍 Endpoint-matched intervention study

One of the most important additions in the current version of the repository is the **endpoint-matched intervention study**.

Its purpose is to ask a reviewer-facing question very directly:

> **what happens when different trajectory families are forced to end at very similar endpoints?**

This matters because endpoint summaries such as final loss or final accuracy can hide relevant internal differences.

The matched-endpoint study therefore selects runs whose terminal summaries are tightly aligned and then tests whether internal organization remains detectable.

The main takeaway is deliberately modest and careful:

- when endpoint information becomes weak,
- internal temporal organization can still remain informative,
- and structural or geometry-aware descriptors can recover that signal in an interpretable way.

This is a strong computational argument because it shows that the framework is not only repackaging the last iterate.

---

## 🌍 External validation: Airfoil and mini-Darcy

A natural objection is that the method could work only because the synthetic environment was designed for it.

That is why the repository adds compact public external cases:

- **Airfoil Self-Noise**
- **mini-PDEBench Darcy**

These datasets serve a specific purpose: they test whether the same structural logic remains meaningful outside the controlled generator.

This provides two layers of credibility:

- **internal validity** through synthetic identifiability experiments,
- **external plausibility** through public datasets with different structure.

---

## 🛡️ Real-case robustness layer

The repository also includes a **real-case robustness study**.

This layer checks whether the structural extraction and boundary parsing remain informative under moderate configuration perturbations.

That matters for two reasons:

1. it reduces the risk that the main conclusions depend on one brittle hand-tuned setting,
2. it provides a more computer-science-oriented validation story centered on reproducibility and sensitivity analysis.

So the computational contribution is not only “the method works once,” but also “the method remains meaningful under nearby reasonable configurations.”

---

## 📊 Why the temporal discrimination tables matter

Several parts of the repository ask a central scientific question:

> **does the method detect real temporal organization, or is it only repackaging terminal summaries?**

This is tested through comparisons among feature blocks such as:

- terminal-only summaries,
- global geometric summaries,
- structural-core descriptors,
- combined blocks,
- and matched-endpoint variants.

These experiments matter because they evaluate not only descriptive richness, but also **usefulness**.

The goal is not to claim that every structural block dominates every simpler alternative in every setting.  
The goal is more disciplined:

- to show that endpoint summaries are often insufficient,
- to show that internal organization remains detectable,
- and to show that the structural layer provides a principled, interpretable, and theory-aligned representation of that organization.

That is the reviewer-facing value of the computational results.

---

## 🗂️ What is in the paper and what is in the repository

The paper intentionally keeps a **compact subset** of the computational evidence so that the manuscript remains readable and aligned with a computer-science / scientific-computing audience.

Accordingly:

- the manuscript keeps the most informative tables for the main argument,
- while the repository and Colab expose the broader computational record.

When you run the notebook / Colab, the repository makes available:

- the main paper-facing tables,
- additional appendix-style tables,
- extended ablations,
- robustness outputs,
- and full reproducibility artifacts.

This design is deliberate.  
It lets the paper stay compact while still making the broader evidence fully inspectable.

---

## 🖼️ Role of the figures

The figures are not ornamental.  
They help visualize the connection between theory and computation by showing:

- geometric separation,
- structural profile behavior,
- representative temporal organization,
- and boundary-score behavior.

At the same time, the repository is designed so that the paper’s central argument does **not** depend on every figure appearing in the manuscript.  
Several visual or extended outputs can remain in the repository while the paper keeps a tighter main narrative.

---

## 💻 Why this is a real computational contribution

This repository contributes something reusable to the study of learning dynamics.

It offers a way to treat trajectories as **structured temporal objects** rather than as endpoint summaries only.

That opens several computational possibilities:

- comparing training regimes through geometry and structure,
- detecting phase changes automatically,
- studying instability through profiles and regime parsers,
- characterizing learning dynamics in scientific ML,
- and building trajectory-level diagnostic layers that go beyond final metrics.

So the code is not only validating the paper.  
It is also proposing a reusable computational toolkit.

---

## ⚙️ Reproducibility philosophy

The repository is organized so that the manuscript’s claims are reproducible and auditable.

It includes:

- explicit default settings,
- repeated seeds,
- family-wise organization,
- compact paper-facing summaries,
- extended appendix-style outputs,
- and a practical execution path through GitHub / Colab.

This is important because a computational contribution should not only be interesting.  
It should also be executable, inspectable, and reusable.

---

## ✅ Final message for the reviewer

This repository should be read as the **computational counterpart** of the paper.

Its purpose is not to win a benchmark.  
Its purpose is to show that the manuscript’s mathematical framework generates a real computational methodology.

More precisely, the repository demonstrates that:

1. the paper’s abstract objects can be turned into algorithms,
2. those algorithms recover meaningful temporal structure,
3. endpoint summaries are often insufficient to describe trajectory organization,
4. the structural layer provides interpretable and theory-aligned trajectory descriptors,
5. the extraction pipeline remains meaningful on public external datasets,
6. and the broader evidence is fully reproducible through the accompanying GitHub / Colab materials.

That is why this repository is not merely supporting material.

It is part of the contribution.
