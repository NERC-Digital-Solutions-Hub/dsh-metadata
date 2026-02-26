# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

- Purpose: Provide UK maps of baseline prior uncertainty (UQ) for CO2 and CH4 fluxes to quantify uncertainty in annually produced NAEI emissions maps. Supports UKSCAPE exemplar work and future updates (e.g., DARE-UK) with a baseline UQ for model discrepancy that has spatial dependence.

- Key outputs:
  - Baseline prior uncertainty maps for CO2 and CH4 at 20 km × 20 km resolution.
  - UK maps showing 5th, 50th, and 95th percentile (5Q/50Q/95Q) of the model discrepancy uncertainty.
  - GeoTIFF files written for submission (CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif; CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif).

- Data sources and inputs:
  - Sectoral GHG fluxes (from UK government NAEI inventories) for:
    - CO2 sectors: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
    - CH4 sectors: similar set with broader uncertainty ranges.
  - Baseline annual fluxes:
    - CO2: March 2014 to Feb 2015.
    - CH4: Jan 2015 to Dec 2015.
  - Calibration data:
    - Start with 100 km-resolution maps disaggregated to 20 km to create a calibration dataset (simulated “smeared” flux data) with large uncertainty to mimic independent flux datasets.
  - Spatial framework:
    - 20 km × 20 km grid across the UK; subset to Scotland, Northern Ireland, England, Wales.
    - Resolution grid yields N = 69 × 41 = 2829 cells.
  - Ad hoc data handling:
    - NaNs replaced; data stored in arrays/vectors for Stan. 
    - Masked rasters and country boundaries used for UK-wide aggregation.

- Statistical model and methodology:
  - Simple linear model: total flux is a weighted sum of sector fluxes, with sector-specific coefficients (alphas) to capture interannual variation and inventory-derived scaling.
  - Spatial discrepancy: represented with a nearest-neighbour Gaussian Process (NNGP) to capture spatial dependence in model discrepancy across grid cells.
  - Priors:
    - Ten Beta-distributed priors for sector coefficients (hard bounds with asymmetric shapes to resemble a Gaussian-like prior).
    - Hyperpriors for spatial terms:
      - sigma (variance of the discrepancy), phi (range/length-scale), with priors defined via ss, st, ap, bp.
    - Prior parameter values set per sector (min, mode, max) to reflect expert uncertainty ranges from UK sources.
  - Calibration and likelihood:
    - Calibration data given large uncertainty (datasd) to keep posterior close to prior, reflecting limited constraint from calibration data.
    - Likelihood includes calibration data, a spatial GP term (NNGP), a bias term, and measurement error.
  - Nearest neighbors:
    - Number of nearest neighbors, M, fixed at 6 for computational efficiency and adequate spatial representation.
  - Computational framework:
    - Implementation via Stan with an NNGP formulation; three MCMC chains; 4800 iterations to ensure convergence.
    - Data and parameters prepared in R/Python-like pseudo-structures; NN matrix built for Stan input.
  - Outputs included for diagnostics:
    - Trace plots and posterior histograms of Beta parameters.
    - Comparison of prior vs posterior means of sector contributions.

- CO2 uncertainty maps specifics:
  - Flux units: CO2 in micromol per square meter per second (μmol m⁻² s⁻¹).
  - Calibration setup leads to baseline UQ maps (5%, 50%, 95%) at 20 km resolution.
  - Model parameters calibrated for 10 CO2 sector coefficients (Beta priors) plus spatial parameters.
  - Prior-to-posterior behavior: minimal shift observed due to deliberately large calibration uncertainty.

- CH4 uncertainty maps specifics:
  - Flux units: CH4 in nanomol per square meter per second (nmol m⁻² s⁻¹).
  - Similar modeling approach and calibration as CO2, with larger sector uncertainties reflecting CH4’s higher baseline uncertainty.
  - Outputs include 5Q/50Q/95Q maps and corresponding GeoTIFFs.

- Outputs and data products:
  - UK maps of baseline prior uncertainty for CO2 and CH4 (20 km resolution).
  - Quantile maps:
    - CO2: 5th, 50th, 95th percentiles for 2014/2015 maps.
    - CH4: 5th, 50th, 95th percentiles for 2015 maps.
  - GeoTIFF exports for data submission to EIDC (as part of UKSCAPE deliverables).

- Implementation details and reproducibility:
  - Code and methodology documented within an R Markdown workflow; includes:
    - Data preprocessing (disaggregation from 100 km to 20 km, aggregation to 20 km grid, country masking).
    - Stan data preparation (N, M, sector vectors, priors, calibration data uncertainty).
    - Stan model implementing the NNGP-based spatial discrepancy and linear flux model.
    - Post-processing for prior vs posterior comparisons and generation of mean/quantile maps.
  - Key modeling choices:
    - M = 6 nearest neighbors.
    - Three MCMC chains, 4800 iterations for convergence.
    - Independent Beta priors for ten sector coefficients to enforce bounds and plausible asymmetry.

- Context and references:
  - Methodology grounded in Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes (Finley et al., 2019) and Zhang (2018) for NNGP in Stan.
  - Data sources include UKSCAPE work package 1.1, UKSCAPE exemplar methodology, NAEI sector uncertainty factsheets, and UK Defra uncertainty guidelines.
  - Relevance to ongoing projects: DARE-UK (for updating UK maps of CO2/CH4 uncertainty).

- Access and usage notes for data supporters:
  - The deliverable provides a baseline UQ framework to compare future UK maps against, enabling assessment of uncertainty propagation in national inventories.
  - Outputs are designed for data reuse in policy analysis and visualization pipelines, with explicit 20 km spatial resolution and standardized GeoTIFF exports for external sharing.