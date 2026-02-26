# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

## Overview
- Integrated model producing gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain.
- Combines three vegetation datasets: Countryside Survey (CS), Natural England's Long Term Monitoring Network (LTMN), and the National Plant Monitoring Scheme (NPMS).
- Time periods: 1990 (CS only) and 2015–2019 (integrated CS, LTMN, NPMS).
- Aims to provide consistent spatial patterns while leveraging varying scheme coverage and biases.

## Data sources and scope
- CS: random 2m x 2m plots; primary representative coverage of GB.
- LTMN: 2m x 2m plots on a stratified grid; not fully representative of GB.
- NPMS: 5m x 5m plots on a fixed grid; community-science data with regionally weighted sampling.
- Indicators computed: Ellenberg N (nitrogen), Ellenberg R (soil reaction/acidity), Ellenberg F (moisture), Ellenberg L (light).
- Focus on vascular plants only (bryophytes excluded due to recording differences across schemes).

## Data processing and indicator construction
- Calculated both plot-average and cover-weighted Ellenberg scores per plot.
- Standardized cover data to the Domin scale; used midpoints for cover-weighted indicators.
- Taxon matching across schemes with vegtaxon R package.
- Covariates considered: broad habitat (matched to Biodiversity Action Plan classes), nitrogen and sulfur deposition (CBED model; 5 km mean over preceding 10 years), annual precipitation, maximum July temperature, minimum January temperature (HadUKGrid 1 km; 10-year means).

## Modelling approach
- Hierarchical model: indicators as additive functions of covariates, random effects (plot within site within scheme), shared spatial effects, and NPMS-specific uptake effects.
- Spatial components modeled with cubic regression splines in East/North coordinates.
- NPMS uptake modeled with a NPMS-only spatial term via a dummy variable to separate from shared spatial patterns.
- LTMN and NPMS data down-weighted relative to CS due to non-representative GB coverage; NPMS weights derived from habitat layer as part of the likelihood.
- Special handling for sampling structure: sites nested within schemes and plots within sites.
- 1990 predictions use CS data only; 2015–2019 predictions combine all three schemes.

## Weighting and bias handling
- Addressed non-representative sampling by incorporating observation weights and separate NPMS uptake term.
- To account for LTMN bias (site locations tied to reserves), applied a down-weighting scheme based on National Nature Reserve (NNR) presence/absence.
- NPMS uptake estimated directly from NPMS data to capture complex regional patterns.

## Predictions and output resolution
- Predictions produced for every 1 km grid cell in GB, using consistent climate and deposition inputs and a 1 km Land Cover Map dominant class.
- Separate predictions and uncertainty maps for each indicator and time period.
- Both non-cover weighted (site-level, “_site”) and cover-weighted (cwt, “_cwt”) indicators provided.

## Quality control and validation
- Model fit assessed using RMSE, with emphasis on CS data (highest weighting, best spatial representation, available in both time periods).
- Overall RMSE generally < 1 unit for most non-cover weighted indicators; cover-weighted indicators showed higher RMSE due to cross-scheme recording differences.
- Uncertainty maps accompany predictions; higher uncertainty in northern Scotland regions; users should interpret these areas with caution.
- Acknowledges potential residual differences compared to a single unbiased dataset, and notes plans for future updates as new data become available.

## Data structure and files
- Output consists of three sets of 2-band TIFF files per indicator:
  - [variable]_90.tif: 1990 predicted mean (band 1) and standard error (band 2)
  - [variable]_15-19.tif: 2015–2019 predicted mean (band 1) and standard error (band 2)
  - [variable]_difference.tif: difference between 2015–2019 and 1990 (band 1) and SE (band 2)
- Variables include EBERGN, EBERGR, EBERGF, EBERGL; and options for non-cover weighted (_site) or cover weighted (_cwt) indicators.
- Total of 24 TIFF files.

## Data availability and licensing
- Open Government Licence; data citation required:
  Jarvis, S.G.; Risser, H.; Smart, S.M.; Monteith, D.; Henrys, P.A. (2022). Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain, 1990 and 2015-2019. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/0a9900f2-8556-4487-bc13-9c2fdc05082c
- Scripts to replicate modelling available on request; repository: https://github.com/NERC-CEH/T1.1-indicatormaps
- Input data are publicly available; CS plot locations require request; NPMS/other sources list DOIs and access details.
- Data provenance and citation are essential for reuse.

## Reproducibility and updates
- Version 1.0, dated 12 August 2022.
- Reproducibility facilitated by the vegtaxon R package for taxon matching and by provided scripts (on request).
- Authors note potential updates as new data become available; aim to maintain currentness and improve bias handling over time.

## Data stewardship considerations (for Data Stewards)
- Provenance: multi-source integration with explicit handling of sampling design differences and biases.
- Metadata completeness: maintain detailed metadata including data sources, plot types, time periods, weighting schemes, and covariates used.
- Accessibility: ensure licensing, citation requirements, and access constraints (e.g., CS plot locations on request) are clearly documented.
- Versioning and updates: track versions of input data and models; plan for future updates when new data are released.
- Usability: provide uncertainty measures and guidance on interpretation, particularly where uncertainty is high (e.g., northern Scotland) or where cover-weighted indicators underperform.
- Governance: document data processing steps, model structure, and assumptions to support auditability and stakeholder trust.

## Contact and acknowledgments
- Acknowledges NPMS weights, interpretation support, and NERC/National Capability funding.
- Contact for replication: susjar@ceh.ac.uk; NPMS weights and data usage references provided.
- Data producers and supporting organizations listed, with links to data sources and licensing.