# The Coherence Meter

[![DOI](https://img.shields.io/badge/DOI-10.13140/%2FRG.2.2.30347.55847-blue.svg)](https://doi.org/10.13140/RG.2.2.30347.55847) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Data: Hugging Face](https://img.shields.io/badge/Data-Hugging%20Face-FFD21E.svg)](https://huggingface.co/datasets/algoplexity/computational-phase-transitions-data)

**Horizon 0 of the Algoplexity Research Program: Statistical Detection of Regime Shifts.**

An AIT-inspired framework for detecting systemic regime shifts in complex systems by measuring local rule incoherence. This repository contains the full computational appendices and code required to reproduce the findings of the paper:

**"The Coherence Meter: A Hybrid AIT-MDL Framework for Early-Warning Structural Break Detection in Complex Financial Systems"**

---

### Abstract

Detecting structural breaks in non-stationary, multivariate time series remains a central challenge, particularly under distribution shift. This paper presents a falsification-driven investigation into Algorithmic Information Theory (AIT) inspired approaches to market regime detection. We begin by testing a direct predictive analogy: can an Elementary Cellular Automata (ECA) solver, trained on binary-encoded asset returns, forecast market dynamics? This hypothesis is cleanly falsified, revealing fundamental limits of domain transfer and encoding fidelity. Pivoting to Minimum Description Length (MDL) as a robust segmentation framework, we compare high-resolution multivariate analysis ("Microscope") against intelligent aggregation ("Stethoscope"), finding the latter consistently superior—validating a "less is more" principle. We then synthesize these insights into the Coherence Meter: a hybrid diagnostic that repurposes ECA predictive error as a proxy for systemic rule incoherence. In a case study on the Q4 2018 U.S. equity downturn, the Coherence Meter detects the regime collapse with 23.9 bits of MDL evidence—twice that of the Stethoscope (11.7 bits). To test for generalizability, we conducted a systematic validation on the Algoplexity Structural Break Benchmark (hosted on Hugging Face). This dual-phase experiment revealed a profound capability: the Coherence Meter functions as a powerful early-warning system, detecting instability with a mean lead time of 31.21% in-sample and 39.37% on unseen, out-of-sample data. Our core contribution is not complexity for its own sake, but a refined "less is more": the final decision framework must be simple and robust, yet powerfully informed by sophisticated, second-order diagnostics.

---

### 📊 Datasets & Experimental Design

To ensure robust validation, this research employs a **dual-track data strategy**, combining real-world historical case studies with large-scale systematic benchmarks.

#### 1. Historical Case Study: The Q4 2018 U.S. Equity Downturn
*   **Purpose:** Qualitative validation, falsification of "Microscope" (multivariate) approaches, and "mechanism" demonstration.
*   **Source:** **Yahoo Finance** (Public API).
*   **Assets:** Daily closing prices for a representative basket of US Blue Chips (`AAPL`, `MSFT`, `BA`, `CAT`, `DIS`, `GE`, `IBM`, `TSLA`).
*   **Usage:** Used in `computational_narrative.ipynb` to demonstrate the Coherence Meter's detection logic on a known, real-world crisis.

#### 2. Systematic Benchmark: The Algoplexity Structural Break Dataset
*   **Purpose:** Quantitative validation of **Generalization Capability**. We measure Early-Warning Lead Time on both In-Sample (**-31.21%**) and Out-of-Sample (**-39.37%**) data.
*   **Source:** **Hugging Face** (Immutable Scientific Artifact).
*   **Assets:** 
    *   `X_train.parquet`: 1,000+ continuous financial time series (In-Sample Training).
    *   `y_train.parquet`: Ground-truth labels for precise structural break timing.
    *   `X_test.reduced.parquet`: Unseen series from the Falcon competition (Out-of-Sample Generalization).
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

If you find this work useful in your research, please cite the permanent DOI:

```bibtex
@misc{mak2025coherence,
  title   = {The Coherence Meter: A Hybrid AIT-MDL Framework for Early-Warning Structural Break Detection in Complex Financial Systems},
  author  = {Mak, Yeu Wen},
  year    = {2025},
  publisher = {ResearchGate},
  doi     = {10.13140/RG.2.2.19275.25122},
  url     = {https://doi.org/10.13140/RG.2.2.19275.25122}
}

@misc{mak2025coherence_code,
  author = {Mak, Yeu Wen},
  title  = {The Coherence Meter: Code and Computational Appendices},
  year   = {2025},
  url    = {https://github.com/algoplexity/Coherence-Meter}
}
