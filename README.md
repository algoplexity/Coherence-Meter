# The Coherence Meter

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An AIT-MDL framework for detecting systemic regime shifts in complex systems by measuring local rule incoherence.

This repository contains the full computational narrative and all code required to reproduce the findings of the paper:

**"The Coherence Meter: A Hybrid AIT-MDL Framework for Structural Break Detection in Complex Financial Systems"**

**[Read the full paper on arXiv (Link to be added upon publication)]**

---

## Abstract

Detecting structural breaks in non-stationary, multivariate time series remains a central challenge in time-series analysis, particularly under distribution shift and channel dependency. This paper presents a falsification-driven investigation into algorithmic information-theoretic (AIT) approaches to market regime detection. 

We begin by testing a direct predictive analogy: can an Elementary Cellular Automata (ECA) solver, trained on binary-encoded asset returns, forecast market dynamics? This hypothesis is cleanly falsified, revealing fundamental limits of domain transfer and encoding fidelity. 

Pivoting to Minimum Description Length (MDL) as a robust segmentation framework, we compare high-resolution multivariate analysis ("Microscope") against intelligent aggregation ("Stethoscope"), finding the latter consistently superior—validating a "less is more" principle. 

We then synthesize these insights into the **Coherence Meter**: a hybrid diagnostic that repurposes ECA predictive error as a proxy for *systemic rule incoherence*, analyzed via MDL/Gaussian change-point detection. 

In a head-to-head test on the Q4 2018 U.S. equity downturn, the Coherence Meter detects the regime collapse with **23.9 bits** of MDL evidence—**twice** that of the Stethoscope (11.7 bits)—and pinpoints the exact trough of maximum incoherence (Dec 10, 2018). 

Our core contribution is not complexity for its own sake, but a **refined "less is more"**: the *final decision framework* must be simple and robust, yet powerfully **informed by sophisticated diagnostics**.

---

## Reproducing the Results

All key findings of the paper can be reproduced by running a single Google Colab notebook.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/Coherence-Meter/blob/main/computational_narrative.ipynb) 
*(Note: You will need to replace `YOUR_USERNAME` with your actual GitHub username after you create the repo).*

**Instructions:**
1. Click the "Open in Colab" badge above.
2. In the Colab notebook, click `Runtime` -> `Run all`.
3. The entire experimental pipeline, including all falsified prototypes and the final successful result, will execute in approximately 2-3 minutes. All tables and figures from the paper will be generated as output.

---

## Citation

If you find this work useful in your research, please consider citing our paper:

```bibtex
@article{mak2025coherence,
  title   = {The Coherence Meter: A Hybrid AIT-MDL Framework for Structural Break Detection in Complex Financial Systems},
  author  = {Yeu Wen Mak},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2025}
}
