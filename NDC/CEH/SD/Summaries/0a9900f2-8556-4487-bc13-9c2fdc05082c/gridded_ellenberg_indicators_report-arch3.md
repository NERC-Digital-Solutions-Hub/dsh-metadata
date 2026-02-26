# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

- Aim: Provide a consistent spatial estimate of four vegetation indicators (Ellenberg N, R, F, L) by integrating three datasets (Countryside Survey, Natural England’s Long Term Monitoring Network, and the National Plant Monitoring Scheme) to support environmental health monitoring, policy scrutiny, and decision-making. Produce 2015-2019 snapshots and comparisons with 1990.

## Background and rationale
- Integrated model combines CS, LTMN, and NPMS data to estimate spatial patterns of Ellenberg indicators across GB.
- Purpose: include datasets with varying spatial coverage and design, enabling a representative map while leveraging all available data.
- Indicators focus: Ellenberg N (nutrient/wetness/control), R (soil/wetness), F (moisture), and L (light).
- 2015-2019 maps serve as a current snapshot; 1990 maps explore potential changes over time (1990 maps derived from CS only).

## Data sources and indicators
- Datasets:
  - Countryside Survey (CS) 1990 and 2015-2019: 2 m x 2 m plots; representative GB coverage (random within CS stratified design).
  - Natural England Long Term Monitoring Network (LTMN): 2 m x 2 m plots; site-based, stratified grid; limited GB representativeness.
  - National Plant Monitoring Scheme (NPMS): 5 m x 5 m plots; community-science data with regionally weighted sampling to cover habitats.
- Indicators computed per plot:
  - Plot-average Ellenberg values and cover-weighted Ellenberg values (converted to Domin scale for comparability).
  - Bryophyte indicators considered but excluded due to large scheme-specific recording differences.
- Covariates considered to explain spatial patterns:
  - Habitat (plot-level Biodiversity Action Plan Broad Habitat classification)
  - Nitrogen and sulfur deposition (mean over preceding 10 years in 5 km squares, CBED model)
  - Climate: annual precipitation, July maximum temperature, January minimum temperature (HadUK-Grid 1 km)

## Data processing and standardisation
- Data harmonisation across schemes:
  - Convert cover values to Domin scale; use midpoints for calculation of cover-weighted indicators.
  - Taxon matching via vegtaxon R package to align taxa across datasets.
- Time periods:
  - 2015-2019: data from CS, LTMN, NPMS combined (2,375 plots in total: CS 445, LTMN 1,287, NPMS 643).
  - 1990: data from CS only (2,282 plots).
- Spatial and sampling considerations:
  - CS: randomly located 2m x 2m X plots.
  - LTMN: 2m x 2m VC plots on stratified grid.
  - NPMS: 5m x 5m plots on grid intersections; Inventory surveys used.
- Modelling units:
  - Indicators computed per plot; covariates and spatial terms linked to plot coordinates.

## Modelling approach
- Objective: estimate a shared spatial pattern of indicators while accounting for non-representative dataset coverage.
- Model structure (conceptual):
  - Additive effects: covariates + random effects + spatial terms shared across datasets + NPMS-specific uptake term.
  - Random effects: plot nested within site nested within scheme.
  - Spatial effects: shared across all datasets; additional NPMS-specific spatial term.
- Formal modelling considerations:
  - Includes cubic regression splines for spatial smooths and smooth terms for covariates.
  - NPMS uptake modeled with a dataset-specific spatial term (dummy variable) to capture complex uptake patterns.
  - LTMN and NPMS down-weighted to reflect non-representative coverage; NPMS uptake modeled directly rather than via covariates.
- Weighted likelihood:
  - Observations are weighted to balance information across schemes; incorporates NPMS and LTMN considerations.

## Predictions and outputs
- Spatial scale and targets:
  - Predictions generated for every 1 km cell across GB to capture broad spatial patterns (not local guidance).
  - 2015-2019 using the 1 km Land Cover Map (LCM) dominant class; 1990 using the 1990 LCM.
- Output formats:
  - Three sets of 2-band TIFF files per time period for each indicator:
    - [variable]_90.tif: mean and SE for 1990
    - [variable]_15-19.tif: mean and SE for 2015-2019
    - [variable]_difference.tif: mean difference and SE between periods
  - Variables include EBERGN, EBERGR, EBERGF, EBERGL with options for non-cover weighted ('_site') and cover weighted ('_cwt') indicators.
  - Total of 24 files.

## Quality control and validation
- Model fit assessment:
  - RMSE evaluated primarily on CS data (highest weighting and representative coverage).
  - Overall RMSE indicates good predictive performance (generally < 1 for many indicators); cover-weighted indicators show higher RMSE due to cross-dataset recording differences.
- Key recommendations:
  - Use non-cover weighted indicator values unless cover weighting is specifically required.
  - Provide and interpret uncertainty maps: standard errors show higher uncertainty in northern Scotland; treat such regions with caution.
- Limitations acknowledged:
  - Despite accounting for scheme differences, residual biases may remain; maps reflect best use of available data and may differ from a single high-coverage unbiased dataset.
  - Plans to update maps as new data become available.

## Data structure and accessibility
- File naming and structure:
  - 24 TIFF files per variable/time period with naming pattern:
    - [variable]_90.site.tif or [variable]_90.cwt.tif
    - [variable]_15-19.site.tif or [variable]_15-19.cwt.tif
    - [variable]_difference.site.tif or [variable]_difference.cwt.tif
  - Each file contains two bands: band 1 mean, band 2 standard error.
- Data availability:
  - Open Government Licence.
  - Citation required: Jarvis et al. (2022) for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain, 1990 and 2015-2019.
  - Reproducibility: scripts to replicate modelling available on request; data sources publicly available; CS plot locations available on request.

## Acknowledgements and funding
- Acknowledgements to NPMS contributors and NPMS weights; Nature of collaboration with Pescott et al. for NPMS sampling weights; interpretation support from Ed Rowe.
- Funded by Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme delivering National Capability.

## Considerations for monitoring frameworks
- Demonstrates how to integrate heterogeneous monitoring datasets with different designs to produce unified spatial indicators.
- Shows practical handling of data gaps and biases via weighting and dataset-specific spatial terms.
- Provides a clear pathway for uncertainty quantification and communication (uncertainty maps, RMSE-based validation).
- Highlights governance aspects relevant to monitoring: data provenance, metadata standardisation, data sharing openness, and reproducibility (scripts available, data licensing).
- Emphasizes scalable output (1 km grids) suitable for policy-level monitoring and comparative analyses over time.