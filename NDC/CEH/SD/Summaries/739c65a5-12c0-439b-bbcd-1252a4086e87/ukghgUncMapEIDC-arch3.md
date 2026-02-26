# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation

## Overview
- Provides UK maps of baseline prior uncertainty (UQ) in greenhouse gas fluxes for CO2 and CH4.
- Aims to quantify spatial uncertainty in annual emissions maps used for climate modelling.
- Builds UK-wide 20 km × 20 km resolution uncertainty maps by propagating sectoral uncertainties from the National Atmospheric Emissions Inventory (NAEI) using a Monte Carlo framework.
- Employs a computationally affordable nearest-neighbour Gaussian Process (NNGP) approach to model spatial dependence in model discrepancy.
- Outputs three UK uncertainty quantile maps (5%, 50%, 95%) and accompanies R, Stan, and Python code to enable reproducibility and future updates (e.g., for DARE-UK).

## Model and data inputs
- Simple linear model combining sectoral fluxes with alpha coefficients to capture interannual variation; anthropogenic fluxes and alphas are sourced from the UK NAEI inventory.
- CO2 sectors (10 total): energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
- CH4 sectors (summary provided; more extensive uncertainty treatment mirrors CO2).
- Calibration data prepared by transforming higher-level resolution maps (100 km) to the target 20 km grid, introducing large calibration uncertainty to mimic independent flux datasets.
- Prior uncertainty for model parameters derived from UK government sources; priors implemented as independent Beta distributions per sector to enforce plausible bounds and allow asymmetry.
- Prior variance and spatial terms set to reflect expected discrepancy structure; a baseline prior UQ is established to benchmark future maps.

## Priors and calibration data
- CO2 priors (Beta distribution per sector) defined by min, mode, max ranges taken from NAEI sector factsheets; used to derive Beta parameters for sector multipliers (alpha-like coefficients).
- CH4 priors (Beta distributions) reflect generally higher uncertainty; where sector uncertainties are missing, a default ~20% uncertainty is applied.
- Calibration dataset consists of smeared 100 km flux maps down to 20 km to emulate typical independent GHG flux datasets; calibration uncertainty is intentionally set large to keep posterior close to prior.

## Nearest Neighbour Gaussian Process (NNGP)
- Uses NNGP to model spatially structured model discrepancy with a spatial dependence that is computationally tractable for large grids.
- Number of nearest neighbours (M) set to 6 (M = 6) as a balance between performance and cost.
- NN structure (NN_matrix) built on grid coordinates; distances and neighbor indices passed to Stan for the spatial term w.

## Data preparation and Stan integration
- Data preparation workflow implemented in R and Python:
  - CO2: flux_20 and flux_100 generation, disaggregation to 20 km grid, and extraction of country-level data for calibration.
  - CH4: analogous workflow post CO2, with sectoral data prepared similarly.
- Key input data for Stan includes:
  - N (grid points), M (NNs), Y (calibration data), sectoral covariates (energyprod, domcom, indcom, indproc, roadtrans, othertrans, waste, offshore, agric, biogenic), NN_ind, NN_dist, NN_distM.
  - Priors: ss (sigma prior scale), st (tau prior scale), ap, bp (phi prior shape/rate), and sector-specific Beta prior endpoints (min, mode, max) converted into Beta parameters.
  - Datasd (calibration data uncertainty) set to a large value to minimize calibration influence.
- Stan data block and model block implemented to incorporate:
  - Simple linear detMod of sector contributions.
  - Spatial random effect w modeled via nngp_w(sigma^2, phi, NN_dist, NN_distM, NN_ind, N, M).
  - Likelihood: Y ~ normal(detMod(...) + w, datasd).

## Stan model and run configuration
- Stan model mirrors an NNGP-based spatial error framework atop the linear sector model.
- Model parameters include calibrated sector betas (10 Beta parameters for CO2 sectors), sigma (measurement error), tau (nugget-like term), phi (spatial range), and w (spatial random effects).
- Three MCMC chains run for convergence assessment; total iterations set to 4800 (with consensus on convergence via trace plots and marginal posteriors).

## Outputs and visualization
- Uncertainty maps for CO2 and CH4 produced at 20 km × 20 km resolution; output maps correspond to 5th, 50th (median), and 95th percentiles of calibrated model outputs.
- GeoTIFFs written for EIDC submission:
  - CO2: 2014-2015 period maps for 5Q, 50Q, 95Q (CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif).
  - CH4: 2015 period maps for 5Q, 50Q, 95Q (CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif).
- Demonstrates minimal posterior shift from prior due to high calibration uncertainty; compares prior-mean versus posterior-mean UKGHG model outputs.
- Includes plots and overlays with UK coastlines and regional boundaries to contextualize spatial uncertainty.
- CH4 workflow mirrors CO2 with sectoral priors and calibration similar in structure.

## CH4 uncertainty maps
- CH4 uncertainty maps follow the CO2 methodology: calibration data preparation, priors, NNGP setup, Stan run, posterior analysis, and generation of 5th/50th/95th quantile maps.
- Outputs similarly include GeoTIFFs for 5Q, 50Q, 95Q and visualization with regional boundaries.

## Reproducibility and governance
- Methodology and code are provided in R Markdown and Stan; exemplar code and results are aligned with UKSCAPE and DARE-UK initiatives.
- Outputs are intended for submission to the EIDC, with clearly documented data structures and modeling steps to support transparency and reuse in monitoring frameworks.
- The approach foregrounds the need for baseline uncertainty quantification to benchmark future updates, enabling consistent monitoring and decision-support.

## Implications for monitoring frameworks
- Demonstrates how to quantify spatial uncertainty in national emission maps using a scalable spatial model, anchored in official sectoral uncertainties.
- Provides a replicable workflow for constructing baseline uncertainty maps, including data preparation, priors informed by authoritative sources, and integration with Stan for Bayesian calibration.
- Highlights the balance between prior information and calibration data, showing how larger calibration uncertainty can preserve prior characteristics while still yielding spatially explicit uncertainty estimates.
- Emphasizes open, auditable workflows suitable for monitoring authorities seeking to inform policy decisions and future monitoring upgrades.

## References
- Finley et al., Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes, J. of Computational and Graphical Statistics (2019).
- DARE-UK project: Detection and attribution of regional greenhouse gas emissions in the UK.
- Zhang, Lu (2018): Nearest Neighbor Gaussian Processes (NNGP) in Stan.
- National Atmospheric Emissions Inventory (NAEI) sector uncertainty factsheets.
- UKSCAPE WP1.1: UK Status, Change and Projections of the Environment.