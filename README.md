# S2 coursework - Raunaq Rai
### rsr45@cam.ac.uk

# Bayesian Inference for the Antikythera Mechanism Calendar Ring

The Antikythera mechanism is an ancient Greek mechanical device, dating back to around 100 BC, believed to be one of the earliest known astronomical calculators. Recovered from a shipwreck in 1901, it contains a complex system of gears that modeled celestial motions. Among its components, the calendar ring — a fragmented structure with evenly spaced holes — has been a subject of debate regarding its original purpose.

Historically, it was assumed that the full ring contained 365 holes, corresponding to a solar calendar. However, recent studies suggest that it may instead  align with a lunar calendar (approx. 354 days). The goal of this project is to apply Bayesian inference and Hamiltonian Monte Carlo (HMC) to estimate the original number of holes in the complete ring, based on available fragmentary data.

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
'''


