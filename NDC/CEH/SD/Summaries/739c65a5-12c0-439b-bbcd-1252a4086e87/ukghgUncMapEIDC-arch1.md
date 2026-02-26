# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

- Purpose
  - Provide UK maps of baseline prior uncertainty in CO2 and CH4 fluxes to quantify spatial uncertainty in annual emissions maps.
  - Uses sector uncertainty data from NAEI to propagate uncertainty to total emissions spatially via Monte Carlo.

- Context and origin
  - Demonstrates methodology from the UKSCAPE project (exemplar for uncertainty quantification with spatial dependence).
  - Method adapted from Nearest Neighbor Gaussian Process (NNGP) as described by Finlay et al. (2019) and Zhang (2018).
  - Aims to support ongoing work in DARE-UK for updating UK maps of uncertainty.

- Data and inputs
  - Fluxes by sector (CO2 and CH4) sourced from UK government NAEI inventories.
  - Sectors (CO2 model) include: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
  - CH4 model uses a similar structure with sectoral uncertainties; CH4 generally more uncertain than CO2.
  - Calibration data: downscaled calibration datasets created by reducing 100 km maps to 20 km to mimic independent flux data, with a large calibration uncertainty.
  - Temporal coverage for maps:
    - CO2: March 2014 to February 2015
    - CH4: January 2015 to December 2015
  - Output grid: 20 km by 20 km UK grid.

- Modelling approach
  - Structure: simple linear combination of sector fluxes with alpha coefficients to capture interannual variation, using NAEI inventory alphas.
  - Model parameters: 10 sector-specific multipliers (betas) for CO2; similar set for CH4 with beta priors.
  - Priors:
    - Independent Beta priors for each sector multiplier (constrained min, mode, max derived from sector uncertainty tables).
    - Prior ranges reflect UK sector uncertainty factsheets; different ranges for CO2 and CH4 (with CH4 typically wider, e.g., min=0.50, max=1.50 for some sectors).
  - Calibration/likelihood:
    - Calibration data treated with large uncertainty to keep posterior close to prior.
    - Likelihood includes a non-spatial bias term, a spatial GP term (NNGP), and Gaussian residuals.
    - DetMod computes the deterministic flux from sector multipliers and alpha terms and the spatial discrepancy w is modeled via NNGP.
  - Spatial dependence:
    - Nearest Neighbor Gaussian Process (NNGP) to model spatially structured discrepancy.
    - Number of nearest neighbors M set to 6 (M = 6 found to be sufficient; increases computation if larger).
  - Computational setup:
    - Stan-based calibration with three MCMC chains; total iterations about 4800 per chain.
    - Data assembly includes coordinates, neighbor indices, and distance matrices for NNGP.
  - Outputs from calibration:
    - Posterior distributions for sector multipliers (beta parameters) and GP hyperparameters (sigma, phi) and spatial parameters (tau).
    - Posterior vs prior comparison to assess information gain from calibration data.

- Implementation details (reproducibility)
  - Software: R (for data prep and generation of inputs), Stan (for Bayesian calibration with NNGP), Python in parts for data handling.
  - Data preparation steps:
    - Obtain sectoral fluxes and convert to annual means at 20 km resolution.
    - Create calibration dataset by downscaling 100 km maps to 20 km and assigning large uncertainty.
    - Assemble input data for Stan: N, M, sector vectors, NN indices/distances, and priors.
  - Model code references:
    - Stan model implements the NNGP-based spatially-discrepant linear model with detMod and w terms.
    - Data block includes all sector vectors and calibration inputs; parameters include 10 sector betas and GP hyperparameters.
  - Outputs:
    - UK uncertainty maps for CO2 and CH4 at 20 km resolution, with 5th, 50th, and 95th percentile maps.
    - GeoTIFF files written for submission (e.g., CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif; CH4 equivalents for 2015).

- Outputs and interpretation
  - Uncertainty maps (5%, 50%, 95%) quantify baseline prior uncertainty in UK GHG fluxes for CO2 and CH4.
  - Maps are intended as baselines for comparison with future UK maps of uncertainty (e.g., in DARE-UK work).
  - Outputs also serve to illustrate the spatial structure of uncertainty and how sectoral uncertainties propagate across the domain.

- Outputs and accessibility
  - Three quantile maps per gas (5%, 50%, 95%) at 20 km resolution.
  - GeoTIFFs prepared for data submission to EIDC.
  - Documentation includes methodology, priors, calibration approach, and NNGP details to enable reproduction and adaptation.

- References and resources
  - Finley et al., 2019: Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes.
  - Zhang, 2018: Nearest Neighbor Gaussian Processes (NNGP) in Stan.
  - UKSCAPE work package 1.1 and UKSCAPE exemplar methods.
  - National Atmospheric Emissions Inventory (NAEI) sector uncertainty summaries.
  - DARE-UK project for ongoing updates to UK GHG maps.