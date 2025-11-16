# The Coherence Meter

[![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An AIT-inspired framework for detecting systemic regime shifts in complex systems by measuring local rule incoherence.

This repository contains the full computational appendices and all code required to reproduce the findings of the paper:

**"The Coherence Meter: A Hybrid AIT-Inspired Framework for Early Warning of Structural Breaks in Complex Systems"**

**[Read the full paper on arXiv (Link to be added upon publication)]**

---

### Abstract

> Detecting structural breaks in non-stationary, multivariate time series remains a central challenge, particularly under distribution shift. This paper presents a falsification-driven investigation into AIT-inspired approaches to market regime detection. We begin by testing a direct predictive analogy: can an Elementary Cellular Automata (ECA) solver, trained on binary-encoded asset returns, forecast market dynamics? This hypothesis is cleanly falsified, revealing fundamental limits of domain transfer and encoding fidelity. Pivoting to Minimum Description Length (MDL) as a robust segmentation framework, we compare high-resolution multivariate analysis ("Microscope") against intelligent aggregation ("Stethoscope"), finding the latter consistently superior—validating a "less is more" principle. We then synthesize these insights into the **Coherence Meter**: a hybrid diagnostic that repurposes ECA predictive error as a proxy for *systemic rule incoherence*. In a case study on the Q4 2018 U.S. equity downturn, the Coherence Meter detects the regime collapse with **23.9 bits** of MDL evidence—**twice** that of the Stethoscope (11.7 bits). To test for generalizability, we conducted a systematic validation on a large, labeled dataset, revealing a more profound capability: the Coherence Meter functions as a powerful **early-warning system**, detecting the genesis of instability with a mean lead time of **31.21%** relative to the pre-break period. Our core contribution is not complexity for its own sake, but a refined "less is more": the final decision framework must be simple and robust, yet powerfully informed by sophisticated, second-order diagnostics.

---

### Reproducing Our Findings

All key findings of the paper can be reproduced by running the three Google Colab notebooks provided in this repository. Each notebook corresponds to a specific stage of our research journey.

#### 1. Main Narrative: The Q4 2018 Case Study (Section 3 & 4)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/computational_narrative.ipynb)

Click the badge above to run the main `computational_narrative.ipynb`. This notebook tells the primary story of the paper, from the "Stethoscope vs. Microscope" showdown to the definitive "Final Showdown" victory of the Coherence Meter.

**Instructions:**
1.  Click the "Open in Colab" badge.
2.  In the Colab notebook, click `Runtime` -> `Run all`.
3.  The entire pipeline will execute in approximately **2-3 minutes**.

#### 2. Definitive Proof: The Early-Warning System (Section 5)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/systematic_validation.ipynb)

Click the badge above to run `systematic_validation.ipynb`. This notebook contains the large-scale validation experiment on the CrunchDAO dataset, providing the definitive proof of the Coherence Meter's capability as a highly sensitive, early-warning system.

**Instructions:**
1.  Click the "Open in Colab" badge.
2.  In the Colab notebook, click `Runtime` -> `Run all`.
3.  The entire pipeline will execute in approximately **5-10 minutes**.

#### 3. Foundational Experiments & Full Audit (Section 2 & 3)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/supplementary_evidence.ipynb)

Click the badge above to run `supplementary_evidence.ipynb`. This notebook contains the "full audit trail" for our foundational experiments, including the code to generate the conceptual figures ("Rule 37 Delusion," "Cost of Complexity") and the complete, computationally intensive "Microscope" scans.

**Instructions:**
1.  Click the "Open in Colab" badge.
2.  In the Colab notebook, run cells individually to reproduce specific figures or tables.
3.  The full "Microscope" scans may take **20-30 minutes** to complete.

---

### Citation

If you find this work useful in your research, please consider citing our paper and this repository.

```bibtex
@article{mak2025coherence,
  title   = {The Coherence Meter: A Hybrid AIT-Inspired Framework for Early Warning of Structural Breaks in Complex Systems},
  author  = {Mak, Yeu Wen},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2025}
}

@misc{mak2025coherence_code,
  author = {Mak, Yeu Wen},
  title  = {The Coherence Meter: Code and Computational Appendices},
  year   = {2025},
  url    = {https://github.com/algoplexity/Coherence-Meter},
  doi    = {10.5281/zenodo.XXXXXXX}
}
```

---
