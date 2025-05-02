### rsr45@cam.ac.uk

# Bayesian Inference for the Antikythera Mechanism Calendar Ring


The Antikythera Mechanism is an ancient Greek device, often regarded as the world’s first analog computer. Dating back to ~100 BCE, it used a sophisticated system of gears to track celestial events. A key component is the calendar ring, a fragmented bronze disk believed to have once featured an evenly spaced set of holes.

While traditionally thought to encode a 365-day solar calendar, recent research suggests the ring more likely followed a **354-day lunar cycle**. In this project, we apply Bayesian inference and Hamiltonian Monte Carlo to reconstruct the original structure of the ring and estimate the total number of holes using surviving fragment data.

This work replicates and extends the statistical framework developed by Woan & Bayley (2024), comparing isotropic and anisotropic error models to assess measurement uncertainty.

## Key work:

- **Two Error Models:**  
  Comparison of isotropic (circular uncertainty) vs. anisotropic (radial–tangential) uncertainty.

- **Bayesian Model Comparison:**  
  - **Savage–Dickey Bayes Factor** decisively favours the anisotropic model.  
  - **Nested Sampling** confirms this with a log-evidence difference of **Δ log Z ≈ 239**.

- **Final Estimate:**  
  Using the anisotropic HMC model: Total number of holes = **355.1 ± 1.26**, supporting a 354-day lunar calendar hypothesis.


## Contents

- Report directory contains report.tex and report.pdf along with all relevant plots
- main_notebook.ipynb is the notebook where all analysis was done
- dataverse_files contains relevant data and images with a description
- pyproject.toml defines the project's metadata, dependencies and build system.
- requirements.txt contains all libraries required for analysis

## Usage
pip:

```bash
pip install -r requirements.txt
```

conda:
```bash
conda env create -f environment.yaml
conda activate s2_coursework
python -m ipykernel install --user --name=s2_coursework --display-name "Python (S2 Coursework)"
```


