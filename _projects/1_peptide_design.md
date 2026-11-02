---
layout: page
title: Generative AI for peptide binder design
description: De novo design of peptide binders for immunotherapy, using BoltzGen and Boltz. Undergraduate thesis at the Purdue Institute for Drug Discovery.
img: assets/img/projects/peptide_design.png
importance: 1
---

<div class="project-facts">
  <p><strong>Where:</strong> Madduri Lab, Purdue Institute for Drug Discovery, Purdue University</p>
  <p><strong>When:</strong> August 2026 – present</p>
  <p><strong>Supervisors:</strong> Dr. Madduri Srinivasarao (Purdue) · Dr. Raviprasad Aduri (BITS Pilani, Goa)</p>
  <p><strong>Tools:</strong> BoltzGen, Boltz-2, AlphaFold, RFpeptides, Python, HPC</p>
</div>

My undergraduate thesis, *Computational Strategies for the Discovery and Optimization of Novel Therapeutic Candidates*, asks whether recent generative and structure-prediction models can produce peptide binders for immunotherapy targets that are good enough to synthesize and test.

**Approach**

- **Generate** candidate peptides, mini-binders and nanobody scaffolds against therapeutically relevant immune targets, using generative models including BoltzGen and RFpeptides.
- **Predict** the peptide–target complexes with structure models such as Boltz-2 and AlphaFold.
- **Rank** designs by refolding agreement, interface confidence and predicted affinity, then shortlist the strongest candidates for chemical synthesis and wet-lab validation.

The goal is an end-to-end *in silico* workflow — generation, structure prediction, and candidate prioritisation — that turns a target into a small, testable set of designs. I'm also preparing a compute-grant application to scale the generation and triage stages.

*This is ongoing thesis work; details and results will be added as they mature.*
