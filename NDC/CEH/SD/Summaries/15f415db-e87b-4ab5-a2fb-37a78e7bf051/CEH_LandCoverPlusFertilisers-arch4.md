# CEH Land Cover plus: Fertilisers 2010-2015 (England)

## Overview
- A set of 1 km x 1 km resolution maps showing predicted average annual application rates of nitrogen (N), phosphorus (P), and potassium (K) fertilisers in England for 2010–2015, with accompanying uncertainty.
- Created to enable exploration of environmental impacts of agrochemical use, supporting farmers and policymakers in adopting sustainable practices.
- Data assets are intended to be reusable, with clear provenance and uncertainty estimates to support risk-informed decision making.

## Data content
- Three fertilisers covered: N, P, and K.
- For each fertiliser and for the study period, two-band raster tiles at 1 km resolution:
  - Band 1: Predicted average annual application rate (kg/km^2).
  - Band 2: Uncertainty associated with the predicted rate (percentage).
- Final maps reflect only non-zero application rates (0 kg/ha values excluded or treated as non-spatially-predictable).
- Accompanied by a crop typology layer derived from CEH Land Cover plus: Crops (averaged 2015–2017) used to weight application by crop area.

## Collection and processing (data provenance)
- Raw data from Defra’s British Survey of Fertiliser Practice (BSFP), 2010–2015:
  - Yearly surveys with georeferenced farm-level fertiliser rates (kg/ha), crop type (66 classes), soil type, farm-level IDs.
  - Participation is voluntary; surveys are nationally representative but subject to data gaps (including 0 values).
- Methodology:
  - Interpolation via Ordinary Kriging (OK) to produce prediction and variance (uncertainty) surfaces.
  - Crops map from Land Cover plus: Crops used to allocate predicted rates to crop areas; results summed across crops to yield total per 1 km cell (kg/km^2).
  - ArcGIS default parameters used for OK; a variable search radius of 12 input points was applied to account for small sample sizes per crop group.
- Quality controls:
  - Kriging variance overlaid with crop-area extents to produce a per-fertiliser uncertainty surface.
  - Uncertainty per cell computed as U = 2 * sqrt(V) / P * 100, representing approximate 95.5% confidence limits.

## Methods and technical notes
- Interpolation approach: OK chosen for performance, agricultural-data familiarity, and ability to generate variance surfaces.
- Supplementary data: CEH Land Cover plus: Crops ( Sentinel-based crop identification across England).
- Calculation workflow:
  - Link fertiliser records to crop typology, multiply by crop-area per 1 km cell, sum across crops to obtain total per fertiliser.
  - Produce per-fertiliser, per-cell surfaces for prediction and uncertainty (kg/km^2 and %).
- Data are stored as two-band TIFF rasters per fertiliser, covering all of England:
  - fertiliser_n_prediction_uncertainty
  - fertiliser_p_prediction_uncertainty
  - fertiliser_k_prediction_uncertainty

## Data structure and access
- Format: Two-band raster TIFFs at 1 km resolution.
- Bands:
  - Band 1: Predicted average annual fertiliser application rate (kg/km^2).
  - Band 2: Uncertainty (percentage).
- Data access and citation:
  - Access via Environmental Information Data Centre: https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051
  - Required citation when using the data: Osório et al. (2019). CEH Land Cover plus: Fertilisers 2010-2015 (England). NERC Environmental Information Data Centre. https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051

## Uses and applications
- Modelling nutrient fate and potential runoff changes under different farming practices (intensification/extensification).
- Estimating greenhouse gas emissions associated with fertiliser use and linking to air-quality impacts.
- Assessing historical and potential future effects on ecosystems (e.g., arable plants, farmland birds, pollinators) and eutrophication.
- Linking nutrient data to crop-growth models to identify opportunities for yield improvements via better nutrient management.
- Informing policies aimed at reducing fertiliser-related environmental impacts (e.g., catchment-sensitive farming).

## Limitations and considerations for data leaders
- Data are based on voluntary BSFP surveys; zero-value records may reflect missing data or actual non-use and are excluded from spatial predictions, which may affect completeness at fine scales.
- Spatial resolution is fixed at 1 km; finer-scale patterns and within-farm heterogeneity are not captured.
- Uncertainty is provided per cell, but aggregation across crops can introduce approximation errors if fertiliser use is correlated across crops.
- Interpolation relies on crop-area weighting; accuracy depends on the quality of the crop map and its temporal alignment (2015–2017 averages used for weighting).

## Acknowledgements and provenance
- Funded by NERC national capability to CEH and the ASSIST programme (with BBSRC/Defra contributions) to advance sustainable agriculture.
- BSFP data contributions acknowledged (e.g., David Fernall and Alison Wray).