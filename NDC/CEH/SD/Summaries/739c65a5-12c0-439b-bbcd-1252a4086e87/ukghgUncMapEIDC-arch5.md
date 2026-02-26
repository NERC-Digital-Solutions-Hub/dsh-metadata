# UK maps representing baseline uncertainty in CO2 and CH4 fluxes: Supporting documentation.

## Overview
- Provides UK maps of baseline prior uncertainty (UQ) in fluxes of greenhouse gases CO2 and CH4.
- Supports modeling of UK emissions for climate projections; uncertainty informs future map updates.
- Builds baseline UQ using sectoral uncertainty data from the National Atmospheric Emissions Inventory (NAEI) and propagates uncertainty via a Monte Carlo approach.
- Methodology uses a nearest-neighbour Gaussian Process (NNGP) for spatial dependence to keep computation affordable.
- An exemplar derived from UKSCAPE work-packages; intended to inform DARE-UK updates and future UK maps.

## Data content and scope
- Spatial grids: 20 km by 20 km resolution UK maps.
- GHGs: CO2 and CH4 fluxes.
- Time frames:
  - CO2: March 2014 to February 2015.
  - CH4: January 2015 to December 2015.
- Units:
  - CO2: micromol per square metre per second.
  - CH4: nanomol per square metre per second.
- Model uses a simple linear combination of sector fluxes (energy production, domestic and industrial combustion, offshore, road and other transport, waste, agriculture, biogenic), with sector-specific alpha coefficients from the inventory to capture interannual variation.
- Uncertainty sources are drawn from sectoral uncertainty ranges (Beta priors) and propagated to total emissions via the model and a spatial GP term.

## Methodology and modeling framework
- Baseline prior uncertainty is defined for 10 Beta-distributed parameters corresponding to sectoral contributions.
- Spatial structure:
  - Nearest-neighbour Gaussian Process (NNGP) to model spatial discrepancy with parameters:
    - sigmasq (variance), phi (spatial range), and NN configuration (M = 6 nearest neighbours).
- Calibration data:
  - Starts from 100 km resolution maps, disaggregated to 20 km to create a calibration dataset that mimics independent flux data.
  - Calibration data given large uncertainty to minimize its influence on posterior estimates.
- Likelihood and model:
  - Y ~ normal(detModel + w, datasd), where w is the NNGP spatial term.
  - detModel is the linear combination of sector fluxes with calibrated beta coefficients.
- Priors and hyperparameters:
  - Independent Beta priors for the 10 sectoral betas, with min/mode/max informed by UK government uncertainty tables.
  - Gamma prior for phi; normal priors for sigma and tau (through ss, st).
- Data inputs to Stan:
  - N (points), M (nearest neighbours), Y and sectoral inputs aligned to NN indices, NN distances, and prior hyperparameters.
- Calibration and inference:
  - Three MCMC chains, total iterations 4800, to assess convergence.
  - Outputs include posterior samples for w (spatial effect) and calibrated beta parameters.
- Output generation:
  - Compute posterior means for sector contributions and produce uncertainty maps for CO2 and CH4 (5th, 50th, 95th quantiles).
  - GeoTIFFs are written for submission to the EIDC.
- Reproducibility:
  - Code and methodology provided via R markdown and Stan, with references to relevant literature and UKSCAPE/DARE-UK projects.

## Data processing and pipeline
- Calibration data preparation:
  - UK flux data at 100 km resolution read and aggregated to annual means, then disaggregated to 20 km; large datasd applied to reflect calibration uncertainty.
  - Spatial aggregation uses country masks (Scotland, Northern Ireland, England, Wales).
- Data inputs:
  - Flux data for each sector (per time period) and aggregated sector composites used to form input vectors for Stan.
  - UK countries shapefile used for region-level aggregation.
- Stan inputs:
  - Data blocks include N, M, Y, sector vectors, NN indices/distances, priors for beta parameters, and spatial parameters.
- Model outputs:
  - Posterior summaries for sectoral multipliers, and maps of the calibrated total uncertainty (CO2 and CH4).
  - Prior vs. posterior comparisons for model outputs to assess calibration impact.

## Outputs and data products
- Uncertainty maps for CO2 and CH4:
  - 5th, 50th, and 95th quantile maps produced at 20 km grid resolution.
  - GeoTIFFs written for submission (e.g., CO2-2014-5Q.tif, CO2-2014-50Q.tif, CO2-2014-95Q.tif; CH4 equivalents for 2015).
- Visualizations:
  - Trace plots and posterior histograms for Beta parameters to assess convergence.
  - Prior vs. posterior comparisons of the model output.
- Code and workflow:
  - R, Stan, and Python components provided, enabling replication of calibration, inference, and map generation.

## Governance, provenance, and reproducibility
- Provenance:
  - Submissions are rooted in UKSCAPE exemplar work and tied to UK-wide emissions inventories (NAEI) and UKSCAPE/DARE-UK programs.
- Data sharing and submission:
  - Outputs prepared for EIDC submission; GeoTIFFs are part of the data products.
- Reproducibility:
  - Detailed methodological descriptions, parameter settings, priors, and data processing steps are documented, with code blocks and references to the Stan model and NNGP implementation.

## Practical considerations for Data Stewards
- Data governance and metadata:
  - Clear lineage from NAEI sector uncertainties to the resulting UQ maps; documentation of priors, calibration approach, and spatial modeling choices.
  - Metadata should include time frames, spatial resolution, units, input data sources, and processing steps (downscaling from 100 km to 20 km).
- Data availability and updates:
  - Maps are prepared for baseline UQ; future updates tied to UKSCAPE/DARE-UK workflows and subsequent model developments.
  - Outputs are designed to be reused for benchmarking future UK maps of uncertainty.
- System interoperability:
  - Use of 20 km raster outputs and standard formats (GeoTIFF); code relies on R, Stan, and Python components with explicit inputs and parameters.
- Data quality and limitations:
  - Calibration dataset intentionally given large uncertainty to minimize influence on posterior; the approach acknowledges potential limitations due to downscaling and calibration data sparsity.
- Compliance and references:
  - Methodology aligns with published work on NNGP (Finley et al. 2019; Zhang 2018) and UKSCAPE/DARE-UK project frameworks; references included for traceability.

## References
- Finley, Datta, Cook, Morton, Andersen & Banerjee (2019) on Efficient Algorithms for Bayesian Nearest Neighbor Gaussian Processes.
- Detection and attribution of regional greenhouse gas emissions in the UK (DARE-UK).
- Zhang (2018) Nearest Neighbor Gaussian Processes (NNGP) in Stan.
- National Atmospheric Emissions Inventory (NAEI) sector and uncertainty summaries.
- UKSCAPE work package 1.1 and related methodologies.