# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

## Overview
- Provides UK-wide maps of baseline prior uncertainty for CO2 and CH4 fluxes.
- Quantifies spatial uncertainty in National Atmospheric Emissions Inventory (NAEI) maps using sectoral uncertainty data.
- Uses Monte Carlo propagation of sector uncertainties to obtain spatial uncertainty in total emissions.
- Methodology adapted from UKSCAPE exemplar; employs Nearest Neighbor Gaussian Process (NNGP) for scalable spatial dependence.
- Aims to establish baseline prior uncertainty for UK maps to compare future updates (e.g., DARE-UK).

## Data and scope
- Flux model: simple linear combination of sectoral GHG fluxes with sector-specific alpha coefficients from the NAEI inventory.
  - Sectors: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
- Years and units:
  - CO2 maps: 2014/03–2015/02 (monthly data aggregated to annual mean).
  - CH4 maps: 2015 (annual mean; 2015 calendar year).
  - Units: CO2 in micro mol per m2 per second; CH4 in nano mol per m2 per second.
- Output resolution: 20 km × 20 km UK grid (with UK country-scale masking during processing).
- Output products: UK maps of baseline prior uncertainty for CO2 and CH4, at 5%, 50%, and 95% quantiles.

## Methodology (statistical modeling)
- Uncertainty propagation approach
  - Treat sectoral alpha coefficients as uncertain quantities; calibrate priors from UK government uncertainty tables.
  - Use Monte Carlo sampling to propagate sector uncertainties into total flux uncertainty.
- Spatial dependence
  - Model discrepancy with a spatially dependent term using Nearest Neighbor Gaussian Process (NNGP).
  - Neighbors: 6 nearest points (M = 6) found to be sufficient; increases in M raise compute cost.
  - Parameters for spatial term: sigma (variance proxy), phi (correlation length); priors set to be broad but informative.
- Model structure
  - Y (calibration data) modeled as detModel(θ) + bias + GP_w + epsilon.
  - detModel is a linear combination of sector fluxes with calibrated coefficients.
  - GP_w is the NNGP-based spatial discrepancy term.
- Priors and calibration
  - Priors for sector alphas are independent Beta distributions with hard bounds around 1.0 (to reflect multiplicative scaling of sector contributions).
  - For CO2, sector-specific min/mode/max values drawn from UK NAEI uncertainty factsheets.
  - For CH4, similar Beta priors with generally larger uncertainty (often broader ranges, reflecting higher CH4 uncertainty).
  - Calibration dataset: created by upscaling from 100 km to 20 km and disaggregating, with intentionally large calibration uncertainty to keep posterior close to prior, mimicking independent flux datasets.
- Likelihood (summary)
  - Y ~ Normal(detModel + bias + GP_w, datasd), with datasd set large to reflect calibration uncertainty.
- Computation and software
  - Stan-based Bayesian calibration with three MCMC chains (total iterations ~ 4800 per chain) to assess convergence.
  - Data assembled for Stan include sector arrays, NN indices/distances, hyperpriors, and calibration data uncertainty.
  - Outputs include trace plots, posterior distributions for sector coefficients, and posterior mean model outputs.

## Data inputs and processing workflow
- UKGHG data preparation
  - Read flux data at 100 km, disaggregate to 20 km for calibration.
  - Compute annual means for 2014/2015 CO2 and 2015 CH4 with large datasd to reflect high calibration uncertainty.
  - Mask by country (England, Scotland, Wales, Northern Ireland) to extract relevant regional data.
- Stan data setup
  - N = number of 20 km grid points; M = 6 nearest neighbors.
  - Y and sector vectors aligned to NN indices; NN_ind, NN_dist, NN_distM encoded for NNGP.
  - Priors: ss, st, ap, bp; sector-specific a/b parameters for calculating Beta priors; the dataset uncertainty datasd.
- Model inputs for CH4 follow the CO2 structure with CH4-specific priors and sector bounds.
- Outputs
  - Quantile maps: 5th, 50th, and 95th percentile maps for CO2 and CH4 uncertainty.
  - GeoTIFFs written for submission (examples: CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif; CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif).

## Outputs and GIS relevance
- Produces spatially explicit uncertainty maps at 20 km resolution suitable for map-based GIS analyses.
- Maps show baseline prior uncertainty for UK CO2 and CH4 fluxes, enabling comparisons with future map updates (e.g., DARE-UK projections).
- Outputs include:
  - 5th, 50th, and 95th percentile uncertainty maps for CO2 (CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif).
  - 5th, 50th, and 95th percentile uncertainty maps for CH4 (CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif).
- Methodology and code
  - R and Stan code snippets provided to reproduce data preparation, calibration, and map generation.
  - Includes details on NNMatrix construction, data packaging for Stan, priors specification, and interpretation of posterior outputs.

## Reproducibility and references
- Provides explicit references for the NNGP approach and the UKSCAPE/DARE-UK framework:
  - Finley et al. (2019) on Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes.
  - Zhang (2018) on NNGP-based models in Stan.
  - National Atmospheric Emissions Inventory (NAEI) sector uncertainty factsheets.
  - UKSCAPE and DARE-UK project documentation.
- Data submission and future use
  - Baseline uncertainty maps intended for comparison against future UK maps of CO2 and CH4 uncertainty (DARE-UK updates).
  - Outputs suitable for EIDC submission; GeoTIFFs written for data dissemination.

## Notes for GIS practitioners
- The dataset emphasizes transparent propagation of sectoral uncertainty into spatial uncertainty, enabling map-based decision support with quantified risk.
- The 20 km grid and OSGB projection are used in processing; GIS users should ensure consistent projection when importing the GeoTIFF outputs.
- The approach focuses on baseline priors; users should be aware that calibration data were intentionally given large uncertainty, limiting the posterior’s departure from the prior.