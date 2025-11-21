# The Coherence Meter

[![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Data: Hugging Face](https://img.shields.io/badge/Data-Hugging%20Face-FFD21E.svg)](https://huggingface.co/datasets/algoplexity/computational-phase-transitions-data)

An AIT-inspired framework for detecting systemic regime shifts in complex systems by measuring local rule incoherence.

This repository contains the full computational appendices and all code required to reproduce the findings of the paper:

**"The Coherence Meter: A Hybrid AIT-Inspired Framework for Early Warning of Structural Breaks in Complex Systems"**

**[Read the full paper on arXiv (Link to be added upon publication)]**

---

### Abstract

Detecting structural breaks in non-stationary, multivariate time series remains a central challenge, particularly under distribution shift. This paper presents a falsification-driven investigation into AIT-inspired approaches to market regime detection. We begin by testing a direct predictive analogy: can an Elementary Cellular Automata (ECA) solver, trained on binary-encoded asset returns, forecast market dynamics? This hypothesis is cleanly falsified, revealing fundamental limits of domain transfer and encoding fidelity. Pivoting to Minimum Description Length (MDL) as a robust segmentation framework, we compare high-resolution multivariate analysis ("Microscope") against intelligent aggregation ("Stethoscope"), finding the latter consistently superior—validating a "less is more" principle. We then synthesize these insights into the **Coherence Meter**: a hybrid diagnostic that repurposes ECA predictive error as a proxy for *systemic rule incoherence*. In a case study on the Q4 2018 U.S. equity downturn, the Coherence Meter detects the regime collapse with **23.9 bits** of MDL evidence—**twice** that of the Stethoscope (11.7 bits). To test for generalizability, we conducted a systematic validation on a large, labeled dataset, revealing a more profound capability: the Coherence Meter functions as a powerful **early-warning system**, detecting the genesis of instability with a mean lead time of **31.21%** relative to the pre-break period. Our core contribution is not complexity for its own sake, but a refined "less is more": the final decision framework must be simple and robust, yet powerfully informed by sophisticated, second-order diagnostics.

---

### 📊 Datasets & Experimental Design

To ensure robust validation, this research employs a **dual-track data strategy**, combining real-world historical case studies with large-scale systematic benchmarks.

#### 1. Historical Case Study: The Q4 2018 U.S. Equity Downturn
*   **Purpose:** Qualitative validation, falsification of "Microscope" (multivariate) approaches, and "mechanism" demonstration.
*   **Source:** **Yahoo Finance** (Public API).
*   **Assets:** Daily closing prices for a representative basket of US Blue Chips (`AAPL`, `MSFT`, `BA`, `CAT`, `DIS`, `GE`, `IBM`, `TSLA`).
*   **Usage:** Used in `computational_narrative.ipynb` to demonstrate the Coherence Meter's detection logic on a known, real-world crisis.

#### 2. Systematic Benchmark: The CrunchDAO Structural Break Dataset
*   **Purpose:** Quantitative validation, statistical significance testing, and measurement of the **-31.21% Early-Warning Lead Time**.
*   **Source:** **Hugging Face** (Immutable Scientific Artifact).
*   **Assets:** 
    *   `X_train.parquet`: 1,000+ continuous financial time series with non-stationary regimes.
    *   `y_train.parquet`: Ground-truth labels for precise structural break timing.
*   **Usage:** Used in `systematic_validation.ipynb`.
*   **Access:** Hosted permanently at [algoplexity/computational-phase-transitions-data](https://huggingface.co/datasets/algoplexity/computational-phase-transitions-data).

---

### Foundational Work

The research in this paper is a direct extension of the foundational work completed in the author's Master's capstone thesis. The thesis establishes the core principle that financial markets possess discoverable algorithmic structure, providing the theoretical and empirical bedrock for the "Coherence Meter." The full thesis and its accompanying code are publicly available:

*   **[📄 Read the full foundational thesis on ResearchGate]**
    (https://www.researchgate.net/publication/397662822_Discovering_Hidden_Structures_in_Stock_Market_Data_using_Algorithmic_Generative_Modeling)

*   **[💻 Access the thesis source code on GitHub]**
    (https://github.com/algoplexity/High-Order-Stocks-Dependencies/blob/main/MScFE_690_G3614_2n1R%20ules.ipynb)

---

### Reproducing Our Findings

All key findings of the paper can be reproduced by running the three Google Colab notebooks provided in this repository.

#### 1. Main Narrative: The Q4 2018 Case Study (Section 3 & 4)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/computational_narrative.ipynb)

Click the badge above to run the main `computational_narrative.ipynb`. This notebook tells the primary story of the paper, from the "Stethoscope vs. Microscope" showdown to the definitive "Final Showdown" victory of the Coherence Meter.
*   **Data Source:** Yahoo Finance (Live/Public API).
*   **Execution Time:** ~2-3 minutes.

#### 2. Definitive Proof: The Early-Warning System (Section 5)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/systematic_validation.ipynb)

Click the badge above to run `systematic_validation.ipynb`. This notebook performs the large-scale validation on the **CrunchDAO Structural Break Benchmark**, proving the early-warning capability.
*   **Data Source:** Hugging Face (Cloud Artifact).
*   **Experiments:** In-Sample Validation (-31% Lag) & Out-of-Sample Generalization (-39% Lag).
*   **Execution Time:** ~5-10 minutes.

#### 3. Foundational Experiments & Full Audit (Section 2 & 3)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/algoplexity/Coherence-Meter/blob/main/supplementary_evidence.ipynb)

Click the badge above to run `supplementary_evidence.ipynb`. This notebook contains the "full audit trail" for our foundational experiments, including the code to generate the conceptual figures ("Rule 37 Delusion," "Cost of Complexity") and the complete, computationally intensive "Microscope" scans.

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
