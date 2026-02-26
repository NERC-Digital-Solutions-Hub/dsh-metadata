# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

- Purpose and outputs
  - Provides UK maps of baseline prior uncertainty (UQ) for greenhouse gas fluxes of CO2 and CH4.
  - Outputs three UK uncertainty quantile maps (5%, 50%, 95%) at 20 km × 20 km resolution for CO2 and CH4.
  - Intended as baseline prior UQ against which future UK maps of uncertainty can be compared (DARE-UK use).

- Data and inputs
  - Flux model: simple linear combination of sector fluxes with sector-specific alpha coefficients from inventories.
  - Sectors for CO2: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
  - Sectors for CH4: energy production, domestic combustion, industrial combustion, industrial processes, offshore, road transport, other transport, waste, agriculture, biogenic.
  - Units: CO2 fluxes in micro moles per m2 per second; CH4 fluxes in nano moles per m2 per second.
  - Temporal coverage: CO2 maps for 2014-03 to 2015-02; CH4 maps for 2015 (year-long).

- Modelling approach
  - Bayesian framework with a linear model combining sector fluxes and sector-specific calibration multipliers (betas).
  - Spatial dependence modelled via a nearest-neighbor Gaussian process (NNGP) to represent model discrepancy with spatial structure.
  - Spatial priors and hyperparameters (sigma, phi, etc.) specified and calibrated.

- Priors and calibration
  - Priors for calibration multipliers (beta parameters) are independent Beta distributions to enforce bounds and allow asymmetry.
  - CO2 priors: sector-specific min, mode, max values drawn from UK NAEI uncertainty factsheets; used to derive Beta parameters.
  - CH4 priors: sector-specific ranges based on table references; where not available, a general 20% uncertainty applied.
  - Calibration data: created by disaggregating lower-resolution (100 km) flux maps to 20 km, introducing a smeared calibration dataset with large uncertainty to mimic independent flux datasets; calibration data assigned large datasd to minimize impact on posterior (posterior close to prior).

- Data processing and NNGP setup
  - Resolution and data handling: disaggregate flux data from 100 km to 20 km; aggregate sector data to annual means.
  - Nearest neighbors: set M = 6 for NNGP (balance between spatial dependency capture and computational cost).
  - Stan-based calibration: input data prepared (Y, sector fluxes, NN structures, priors) and passed to Stan; three MCMC chains run, total iterations typically 4800 for convergence.
  - Outputs include posterior samples for beta parameters and spatial w term; posterior summaries produced for prior vs. posterior comparison.

- Model structure and computation
  - Core model: detMod is a linear combination of sector flux multipliers and sector baselines; Y is modeled as detMod plus spatially structured w plus calibration noise.
  - Stan code uses non-spatial bias, NNGP-based spatial term, and Gaussian observation error.
  - Data interfaces include: N, M, sector vectors (energyprod, domcom, indcom, indproc, roadtrans, othertrans, waste, offshore, agric, biogenic), NN structures (NN_ind, NN_dist, NN_distM), priors (ss, st, ap, bp), calibration variance (datasd).

- Outputs and products
  - Uncertainty maps for CO2 and CH4: 5th, 50th, and 95th quantiles of calibrated model output, rasterized to 20 × 20 km grid.
  - GeoTIFF outputs generated for each quantile (e.g., CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif; CH4-2015-5Q.tif, CH4-2015-50Q.tif, CH4-2015-95Q.tif).
  - Plots include trace plots and marginal histograms for MCMC convergence; posterior vs. prior comparisons show minimal shifts due to calibration uncertainty.

- Reproducibility and workflow notes
  - Methodology implemented via R Markdown for CO2 and CH4 uncertainty maps; Stan code implements the NNGP-based spatial model.
  - Calibration data preparation includes processing steps to read UKGHG inputs, compute annual sector means, and apply large data uncertainty to calibration to reflect data limitations.
  - Outputs support future updates (e.g., DARE-UK) by providing a baseline against which new maps can be compared.

- Application and context
  - Baseline UQ for UK maps of CO2 and CH4 fluxes to benchmark future updates and assessments.
  - Serves as a methodological exemplar for combining sectoral flux data with spatially structured model discrepancy.

- References
  - Finley et al. 2019 on Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes (NNGP).
  - DARE-UK project and related UKSCAPE work package 1.1.
  - UK NAEI sectoral uncertainty factsheets and uncertainty guidance.