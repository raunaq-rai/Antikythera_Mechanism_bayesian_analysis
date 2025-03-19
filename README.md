# S2 coursework - Raunaq Rai
### rsr45@cam.ac.uk

# Bayesian Inference for the Antikythera Mechanism Calendar Ring

## Introduction

The Antikythera mechanism is an ancient Greek mechanical device, dating back to around 100 BC, believed to be one of the earliest known astronomical calculators. Recovered from a shipwreck in 1901, it contains a complex system of gears that modeled celestial motions. Among its components, the calendar ring — a fragmented structure with evenly spaced holes — has been a subject of debate regarding its original purpose.

Historically, it was assumed that the full ring contained 365 holes, corresponding to a solar calendar. However, recent studies suggest that it may instead  align with a lunar calendar (approx. 354 days). The goal of this project is to apply Bayesian inference and Hamiltonian Monte Carlo (HMC) to estimate the original number of holes in the complete ring, based on available fragmentary data.

## Approach

1. **Data Processing**  
   - The dataset containing measured hole positions is loaded and preprocessed.  
   - The fractured ring sections are identified and grouped.

2. **Mathematical Modeling**  
   - Hole positions are modeled as lying on a circular ring with an unknown number of original holes.  
   - The surviving sections are assumed to be misaligned due to fragmentation, with independent **translations** and **rotations**.

3. **Likelihood Function**  
   - A **Gaussian likelihood** is used to model measurement uncertainties.  
   - Two covariance structures are considered:  
     - **Isotropic model**: A single uncertainty parameter for x and y errors.  
     - **Anisotropic model**: Separate uncertainty parameters for **radial** and **tangential** directions.

4. **Parameter Estimation**  
   - The log-likelihood function is implemented using **JAX** for automatic differentiation.  
   - The parameters are optimized using **gradient-based methods** to find the maximum likelihood estimate (MLE).

5. **Bayesian Inference via HMC**  
   - **Hamiltonian Monte Carlo (HMC)** is used to sample the posterior distribution of the model parameters.  
   - The posterior predictive distribution of hole locations is visualized.

6. **Model Comparison**  
   - The role of the covariance structure is analyzed by comparing the isotropic and anisotropic models.  
   - The model predictions are validated against the observed hole positions.
