# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

## Overview
- Provides UK-wide maps of baseline prior uncertainty (UQ) for CO2 and CH4 fluxes, derived from sectoral uncertainty data in the National Atmospheric Emissions Inventory (NAEI).
- Aims to quantify spatial uncertainty in annual UK emissions maps to support climate modelling and future uncertainty assessments.
- Maps are created at 20 km x 20 km resolution and intended as a baseline for comparison with future UK maps (e.g., in DARE-UK work).

## Data and model structure
- Fluxes decomposed into a simple linear combination of sector fluxes:
  - Sectors for CO2: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
  - CH4 mirrors a similar sector-based structure with corresponding coefficients.
- Anthropogenic fluxes and sectoral alphas come from the UK government NAEI inventories.
- Model outputs are annual flux maps (CO2: 2014/03–2015/02; CH4: 2015 calendar year).

## Uncertainty quantification approach
- Uncertainty in total emissions is propagated from sectoral uncertainties using a Monte Carlo framework.
- Spatial dependence in model discrepancy is represented with a Nearest Neighbor Gaussian Process (NNGP).
- The NNGP uses M = 6 nearest neighbours to balance spatial dependency with computational affordability.
- Outputs are UK uncertainty maps for CO2 and CH4, including 5th, 50th, and 95th percentiles.

## Calibration data and likelihood
- Calibration data are created by downsampling from 100 km resolution ( ukghg ) and disaggregating back to 20 km, yielding a “smeared” calibration dataset to mimic independent flux datasets.
- Calibration data are given large uncertainty to ensure the posterior remains similar to the prior (the prior dominates the calibration).
- Likelihood structure (for completeness) includes:
  - Y ~ Normal(detModel + bias + GP_w + epsilon, datasd)
  - detModel is the linear combination of sector fluxes with calibrated beta-like coefficients.
  - GP_w is the spatial NNGP component; the rest captures bias and Gaussian noise.

## Spatial modelling and priors
- Priors for the spatial term:
  - sigma and phi (NNGP hyperparameters) with normal and gamma-type priors.
  - Phi controls spatial correlation length; sigma controls the variance of the spatial discrepancy.
- Ten Beta-distributed priors correspond to the ten sectoral coefficients (ensuring non-negativity and soft bounds around unity).
- Prior ranges for CO2 sectors derived from UK sector uncertainty summaries; CH4 priors broadened due to higher CH4 uncertainty (often up to 1.5x or 0.5x the baseline).

## Implementation workflow
- Data processing and setup:
  - Read sectoral flux data and create 20 km resolution inputs from 100 km calibration data.
  - Assemble input vectors for Stan: sector fluxes, calibration Y, NN indices, distances, and priors.
- Stan model:
  - Implements the linear combination of sector fluxes plus a spatially structured discrepancy term via an NNGP.
  - Includes 10 beta-like parameters (one per sector), plus spatial hyperparameters (sigma, phi) and a scale parameter for the calibration noise.
- Computation:
  - Three MCMC chains run with ~4800 iterations to assess convergence.
  - Outputs include posterior samples for the spatial term w and the sector coefficients, plus diagnostic plots (trace plots and marginal histograms).
- Diagnostics and reporting:
  - Convergence assessed via trace plots and histograms of posterior beta parameters.
  - Posterior mean model outputs compared against prior means to illustrate data influence (typically small changes due to large calibration uncertainty).

## Outputs and data products
- UK uncertainty maps for CO2 and CH4:
  - CO2: 5th, 50th, and 95th quantile maps at 20 km resolution for 2014/2015 period; GeoTIFF outputs written as part of data submission (examples include CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif).
  - CH4: analogous 5th, 50th, and 95th quantile maps for 2015; GeoTIFF outputs such as CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif.
- Code and methodological documentation:
  - R, Stan, and helper scripts demonstrating how to reproduce the maps and uncertainty estimates.
  - Reference materials including the NNGP methodology (Finley et al. 2019; Zhang 2018) and relevant UKSCAPE and NA E I sources.

## Relevance to environmental monitoring and future work
- Provides a standardized baseline UQ framework to assess spatial uncertainty in UK GHG flux maps, enabling:
  - Temporal comparisons of uncertainty and model discrepancy over time.
  - Integration with other datasets and cross-sector analyses to increase dataset value beyond single-use.
  - Transparent data sharing through established portals and EIDC submissions.
- The baseline UQ maps serve as a reference point for future updates (e.g., in DARE-UK) to evaluate improvements in uncertainty quantification and spatial modelling.

## References
- Finley et al. 2019. Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes.
- Zhang 2018. Nearest Neighbor Gaussian Processes (NNGP) in Stan.
- UKSCAPE work package 1.1 and related UKNAEI/NAEI uncertainty resources.
- National Atmospheric Emissions Inventory (NAEI) sector uncertainty factsheets.