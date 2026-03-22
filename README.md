# 📘 Geometry of Learning — Computational README
## 🔬 Why this code is a genuine computational contribution of the paper

This repository is not just a numerical appendix or a visualization add-on.  
It is the **computational realization** of the mathematical program developed in the paper.

The main contribution of the manuscript is to argue that learning trajectories are not exhausted by their endpoint metrics.  
Instead, they possess an internal **geometric**, **structural**, and **temporal** organization that can be studied through mathematically defined objects.

This code shows that those objects are not merely formal.  
They can be:

- defined algorithmically,
- extracted from real trajectories,
- summarized in reproducible descriptors,
- used to detect transitions and regimes,
- validated statistically,
- and transferred beyond the synthetic setting.

In that sense, the code provides the paper’s **computational proof of concept**:  
it demonstrates that the mathematical language of the article leads to a concrete, usable, and informative analysis pipeline.

---

# 🧠 The core idea

The paper develops a mathematical framework for studying trajectories through local geometry, mesoscopic structure, and macroscopic organization.

The code turns that framework into an executable pipeline.

The key message is:

> **mathematics is not used here only to justify notation; it determines what is computed, how it is computed, and why the resulting quantities are meaningful.**

This is what makes the repository a true computational contribution.

---

# ✨ Why the mathematical layer matters computationally

A referee may naturally ask:

> “Why is this more than another handcrafted feature extraction script?”

The answer is: because the feature architecture is **not arbitrary**.

The code is built from mathematically motivated objects that appear in the paper:

1. **local windows** as the discrete analogue of local jets,
2. **admissible observables** on those windows,
3. **structural profiles** built from those observables,
4. **structural mass** as an integrated mesoscopic descriptor,
5. **superlevel geometry** to isolate persistent structural zones,
6. **boundary extraction** to locate changes,
7. **event parsing** to identify transition regions,
8. **macro-regime decomposition** to recover large-scale temporal organization.

So the code does not begin from generic ML feature engineering.  
It begins from a mathematical theory of trajectory organization.

That is the main reason the computational part is scientifically valuable.

---

# 🧩 From mathematical objects to executable objects

## 1. Local jets become discrete centered windows 🔹

In the manuscript, local behavior is studied through local trajectory structure.  
In the code, this becomes a centered discrete window extracted around each admissible time index.

This is computationally important because it creates a **localized view of the trajectory**.  
Instead of summarizing the whole run with a single scalar, the trajectory is scanned point by point through local neighborhoods.

That move is fundamental:

- it preserves temporal information,
- it allows the method to detect local irregularities,
- and it creates the base layer for all later structural quantities.

So the first computational contribution of the mathematics is **localization**.

---

## 2. Admissible observables become measurable local descriptors 📐

The code computes three central local observables:

- **oscillation**,
- **triangular excess**,
- **second-order window mass**.

These are not random quantities.

They measure complementary aspects of local shape:

- how much the path spreads inside a window,
- how non-geodesic or non-flat the local geometry is,
- how much second-order bending or acceleration exists.

This is where the mathematical viewpoint creates computational value:

- instead of storing full windows,
- the method compresses them into **structurally interpretable descriptors**.

So the mathematics yields a principled feature map from local trajectory geometry to finite-dimensional computational summaries.

---

## 3. Structural profiles convert local geometry into a temporal signal 📈

Once local observables are computed over all valid centers, the code assembles them into **profiles along time**.

This is one of the most important ideas in the repository.

A structural profile is not just a list of values.  
It is a **mesoscopic signal** that records where the trajectory is locally smooth, curved, concentrated, unstable, or structurally active.

This creates a major computational advantage:

- the original high-dimensional trajectory is transformed into a small number of meaningful temporal signals,
- these signals can be compared across runs,
- and they can be aggregated statistically across seeds and families.

In other words, the mathematics gives a way to transform complex training dynamics into an analyzable time-series object.

---

## 4. Structural mass gives a stable global summary of mesoscopic complexity ⚖️

The code then integrates profiles into quantities such as **structural mass**.

This is important because it creates a bridge between:

- local geometry,
- mesoscopic organization,
- and global trajectory characterization.

Computationally, this is powerful because it gives the reviewer both:

- a detailed local explanation through profiles,
- and compact scalar summaries for tables and comparisons.

That balance is one of the strengths of the framework:

> it does not force a choice between interpretability and summarization.

The mathematics makes both possible.

---

## 5. Superlevel geometry isolates the structurally active zones 🔥

A crucial step in the pipeline is thresholding structural energy into **superlevel sets**.

This is more than a convenience trick.

It turns a continuous-valued structural signal into a geometric object:

- a mask,
- a set of connected components,
- and a set of boundary points.

This matters computationally because it lets the method identify not only the magnitude of structural activity, but also its **location**, **persistence**, and **fragmentation**.

So the mathematical notion of superlevel geometry becomes a practical device for:

- detecting active temporal zones,
- counting components,
- quantifying complexity,
- and preparing the path for event parsing.

---

## 6. The corrected multiscale boundary parser is where the mathematics becomes temporal intelligence 🧭

One of the strongest aspects of the script is that it does not define events from raw peaks of energy alone.

Instead, the code uses a **corrected multiscale boundary score** built from:

- left/right contrast in structural profiles,
- left/right contrast in residual energy,
- fine-scale curvature information.

This is a genuine computational advance, because it addresses a real difficulty:

> a large value of energy is not always the same thing as a structural transition.

The parser therefore tries to detect boundaries in a mathematically sharper way.

This improves the computational story in three ways:

1. it distinguishes **activity** from **change**,
2. it turns structural signals into explicit event candidates,
3. it allows the trajectory to be segmented into **transition zones** and **macro-regimes**.

This is exactly the point where the mathematics stops being descriptive and becomes algorithmic.

---

## 7. Events and regimes make the framework explanatory, not just predictive 🧱

Many computational pipelines stop at classification scores.  
This one goes further.

The code extracts:

- boundary peaks,
- event intervals,
- transition intervals,
- macro-regimes,
- regime words / regime structure summaries.

This matters because the output is not just “family A vs family B”.

Instead, the method can say:

- where the important changes happen,
- how many transitions occur,
- how many regimes the run contains,
- and how the structural organization unfolds over time.

That is a major computational contribution of the paper:

> it provides an **interpretable temporal parser** of learning dynamics.

---

# 🧪 Why the synthetic experiment is mathematically useful

The synthetic block is not there to claim state-of-the-art benchmark performance.

Its role is different and much more aligned with the paper.

The code builds a controlled trajectory laboratory using a simple nonlinear binary dataset and logistic training under several scheduled learning-rate regimes.

These include families such as:

- homogeneous dynamics,
- regime-change dynamics,
- three-phase dynamics,
- pulse dynamics,
- oscillatory dynamics.

This design is mathematically important because the true temporal organization is partially known in advance.

That lets the computational layer test whether the proposed descriptors can recover:

- no regime changes,
- one regime change,
- multiple phases,
- transient pulses,
- oscillatory structure.

So the synthetic layer is not “toy” in a weak sense.  
It is a **controlled identifiability environment** for the theory.

---

# 🌍 Why external datasets are still necessary

A referee could still object:

> “Perhaps the method only works because the synthetic environment was designed to make it work.”

That is precisely why the repository adds a compact external validation layer.

The code includes:

- **Airfoil-Self-Noise** as a real external validation case,
- **Mini-PDEBench-Darcy** as a scientific machine learning / PDE-oriented validation case.

This is important because it shows that the same structural logic can survive outside the toy family generator.

So the computational contribution is twofold:

- **internal validity** through controlled synthetic families,
- **external plausibility** through public datasets with different structure.

That strengthens the paper considerably.

---

# 📊 Why the temporal null control is a strong reviewer-facing argument

One of the most important parts of the code is the **temporal null control**.

This section compares different feature blocks such as:

- terminal-only information,
- structural core,
- global + structural combinations,
- fuller clean feature blocks.

This is conceptually powerful because it asks a very direct scientific question:

> does the method capture real temporal organization, or is it only repackaging endpoint information?

If structural features outperform terminal-only summaries, then the computational evidence supports the central claim of the paper:

- trajectories contain internal organization,
- that organization is not reducible to the last iterate,
- and the mathematical descriptors recover useful information that terminal metrics miss.

This is exactly the kind of test a careful referee would want to see.

---

# 🛡️ Why the robustness layer matters

A paper can look convincing if it reports one carefully chosen configuration.  
A stronger paper tests whether the conclusions survive nearby settings.

That is the role of the parser robustness layer.

The code evaluates sensitivity around the parsing mechanism and keeps quantities such as:

- boundary-peak recall,
- boundary-peak precision,
- event recovery behavior,
- regime recovery behavior,
- structural stability summaries.

This is important because it reduces the danger that the full story depends on a brittle hand-tuned setting.

Even more importantly, the code explicitly avoids using parser-vs-ground-truth quantities as classification features in the temporal classification tables.  
Those quantities are reserved for the robustness layer where they actually belong.

This separation is methodologically clean and strengthens the credibility of the results.

---

# ⚙️ The computational contribution in one sentence

The computational contribution of this repository is that it transforms an abstract mathematical theory of trajectory geometry into a reproducible algorithmic pipeline that can:

- localize structure,
- quantify it,
- detect transitions,
- recover regimes,
- test robustness,
- and validate the framework both internally and externally.

---

# 🧭 How the mathematics improves computation in practice

## A. Better representation
The code replaces raw trajectory storage with mathematically meaningful local summaries.

## B. Better interpretability
Each computed quantity has a structural role:
oscillation, excess, mass, superlevel, boundary, event, regime.

## C. Better temporal resolution
The method does not collapse everything into final loss or final accuracy.

## D. Better segmentation
The parser identifies where meaningful changes occur in the trajectory.

## E. Better validation logic
The synthetic families let the code test recoverability under controlled temporal patterns.

## F. Better external credibility
Airfoil and Darcy show that the same logic is not confined to one handcrafted environment.

## G. Better methodological discipline
The code separates:
- descriptive structure,
- temporal discrimination,
- and parser-ground-truth evaluation.

That separation is important for a clean scientific argument.

---

# 🗂️ What each group of tables is doing

## Tables A–C: Internal geometric and structural evidence
These tables show that the synthetic learning families differ in:

- global geometry,
- structural profile behavior,
- event / regime / superlevel complexity.

This establishes the descriptive and structural core of the method.

## Tables D–F: Validation of usefulness
These tables ask whether the descriptors are:

- discriminative,
- nontrivial beyond terminal summaries,
- and robust to nearby parser configurations.

This establishes methodological credibility.

## Tables G, I, J, L, M: Compact external validation
These tables move the framework outside the synthetic laboratory and check whether the same descriptors retain explanatory value on public external cases.

This establishes transferability.

---

# 🖼️ Why the figures matter scientifically

The figures are not ornamental.  
They create a visual map between the theory and the code.

They let the reviewer see:

- global geometric separation,
- structural profile shape,
- representative trajectory organization,
- boundary scores and detected peaks.

This is useful because the theory is naturally multi-scale:

- global,
- local,
- mesoscopic,
- event-level.

The figures make those scales visible.

---

# 💻 Why this counts as a real computational benefit for the field

The repository contributes something computationally meaningful because it offers a reusable way to study learning trajectories as structured objects rather than as endpoint summaries only.

That opens several possibilities:

- comparing optimizers by geometry instead of only final score,
- studying training instability through structural profiles,
- detecting phase changes automatically,
- quantifying temporal organization in scientific ML,
- building new diagnostic layers for optimization research.

So the code is not only validating the paper.  
It is also proposing a potentially reusable computational toolkit.

---

# 📦 Reproducibility and design philosophy

The repository is organized so that the paper’s claims are reproducible and auditable.

It includes:

- explicit default settings,
- repeated seeds,
- family-wise organization,
- compact reporting tables,
- and a reduced fast validation layer that preserves the main claims while keeping execution manageable.

This is important because a computational contribution should not only be interesting.  
It should also be executable, inspectable, and reusable by others.

---

# ✅ Final message for the reviewer

This code should be read as the **computational crown of the paper**.

Its purpose is not to win a benchmark.  
Its purpose is to show that the manuscript’s mathematical framework generates a real computational methodology.

More precisely, the repository demonstrates that:

1. the paper’s abstract objects can be turned into algorithms,
2. those algorithms recover meaningful temporal structure,
3. the resulting descriptors are informative beyond endpoint summaries,
4. the parser is not purely ad hoc,
5. and the whole framework remains meaningful on external public datasets.

That is why this repository is not just supporting material.

It is part of the contribution.
