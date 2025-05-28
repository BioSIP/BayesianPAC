# BayesianPAC
Bayesian estimation of Phase-Amplitude Coupling
# BayesianPAC

This repository contains the core implementation of the **Bayesian Phase-Amplitude Coupling (PAC)** model presented in our manuscript on EEG-based analysis of reading difficulties in children. The approach uses probabilistic modeling to estimate directional connectivity between EEG channels while accounting for uncertainty in both data and inference.

The method has been developed and tested using EEG data collected under controlled auditory stimulation at 4.8, 16, and 40 Hz, with the aim of identifying functional coupling differences between typically developing children and those with reading difficulties.

> 🔗 **If the associated manuscript is published, a citation and DOI will be added here.**

---

## 📂 Included Notebooks

### `BPAC_OneSubject.ipynb`

This notebook performs the full analysis pipeline for a **single subject**:
- Loads PAC values and time fragments.
- Computes conditional probabilities using non-parametric Kernel Density Estimation (KDE).
- Applies Bayesian inference to estimate directed PAC connections.
- Outputs a subject-level probability matrix for directional connectivity.

### `BPAC_GroupsComparison.ipynb`

This notebook takes individual probability matrices (from multiple subjects) and:
- Compares connectivity patterns between two groups (e.g., controls vs. dyslexia).
- Performs statistical testing (e.g., z-scores, permutation tests).
- Outputs group-level summary figures and statistical results.

---

## 📌 Why Jupyter Notebooks?

We chose Jupyter Notebooks to ensure transparency, reproducibility, and accessibility. This format allows users to:
- Read and execute the analysis step-by-step.
- Modify parameters interactively.
- Visualize results directly within the workflow.

Researchers can adapt the pipeline to their own EEG datasets by editing and running the notebooks in any standard Python environment.

---

## 🚀 How to Run the Code

1. Clone or download the repository:

   ```bash
   git clone https://github.com/BioSIP/BayesianPAC.git
   ```

2. Create a Python environment with the following recommended packages:

   - `numpy`  
   - `scipy`  
   - `pandas`  
   - `matplotlib`  
   - `seaborn`  
   - `scikit-learn`  
   - `statsmodels`  
   - `jupyter`

3. Launch Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open and run one of the following notebooks:
   - `BPAC_OneSubject.ipynb`: to compute subject-level PAC connectivity.
   - `BPAC_GroupsComparison.ipynb`: to perform statistical comparisons between two groups.

---

## 📄 License

This work is licensed under a **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

You are free to:
- **Share** — copy and redistribute the material in any medium or format.
- **Adapt** — remix, transform, and build upon the material.

Under the following terms:
- **Attribution** — You must give appropriate credit.
- **NonCommercial** — You may not use the material for commercial purposes.

For full details, see the license description here:  
[https://creativecommons.org/licenses/by-nc/4.0/](https://creativecommons.org/licenses/by-nc/4.0/)

---

## 👥 Authors & Contact

This repository is maintained by the **BioSIP research group**, University of Málaga.

If you have questions, comments, or would like to collaborate, please contact us at:  
📧 **biosip@uma.es**
