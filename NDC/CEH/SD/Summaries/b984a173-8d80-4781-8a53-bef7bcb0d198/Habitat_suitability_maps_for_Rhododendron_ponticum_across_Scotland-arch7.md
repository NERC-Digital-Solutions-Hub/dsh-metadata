# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Overview
- Objective: Map habitat suitability for Rhododendron ponticum (R. ponticum) across Scotland to assess potential reservoirs for Phytophthora ramorum and Phytophthora kernoviae.
- Data scope: Eleven presence datasets (1950–2008), largely volunteer-sourced; presence records summarized to 1 km x 1 km grid cells (82690 cells with environmental data; 1725 cells with presence).
- Output: Maxent-based habitat suitability maps, including mean suitability, variability, and projection reliability (clamping).

## Data sources and preparation
- Presence datasets (11 total) collected from Local Record Centres, NBN Gateway, and targeted surveys (Argyll and Bute region).
- Spatial resolution: Original records at 1 km or finer, aggregated to 1 km grid cells.
- Environmental predictors (per 1 km cell): 
  - Broad-leaf forest cover (BLWOOD) – primary predictor
  - Conifer forest cover (CWOOD)
  - Elevation (ELEV)
  - Annual mean Enhanced Vegetation Index (EVI)
  - Annual mean Normalised Difference Vegetation Index (NDVI)
  - Dominant soil carbon content (Carbon)
  - Dominant soil pH (PH)
- Predictor data sources include UK Land Cover Map 2000, MODIS (EVI/NDVI), SRTM elevation, and soil data.

## Modelling approach
- Species distribution modelling using Maxent (version 3.3.3e).
- Core modelling assumptions: Equilibrium with environment; addressed sampling biases due to clustered citizen science data.
- Methods to address biases (Elith et al. 2010):
  - Upweight records with few geographic neighbours (bias grid) to mitigate clustering.
  - Test different background areas for background samples:
    - ALL: whole Scotland
    - REACH: reachable areas (roads/railways/urban)
    - MCP: minimum convex polygon around presence datasets
- Model configurations: Six Maxent models (three background options × with/without upweighting), each with 25 iterations and 30% withheld data for cross-validation.
- Predictor terms: Both linear and quadratic terms included to capture non-linear relationships.
- Output maps per model: mean predicted habitat suitability, standard deviation across iterations, and average clamping (extrapolation) risk.

## Model evaluation and selection
- Evaluation metrics: 
  - Area Under the Curve (AUC) for training and test sets
  - Predicted-to-expected (P/E) ratios across habitat suitability classes
  - Spearman correlation between predicted habitat suitability and observed R. ponticum cover (Argyll and Bute)
- Key findings:
  - ALL background with no upweighting (unweighted ALL) produced the best overall performance; MCP background performed worst.
  - Upweighting did not improve model accuracy and sometimes worsened independence between training and test sets.
  - High correlation between predicted suitability and observed local cover (Spearman r ≈ 0.58 in Argyll and Bute).
  - Predicted distributions indicated substantial, contiguous suitable areas when using ALL background.

## Key spatial results
- Extent of suitable habitat: About 24% of Scotland (≈20,021 of 82,960 1 km cells) predicted to be suitable for R. ponticum.
- Geographic hotspots of suitability: Great Glen, central belt (Edinburgh–Lothians–Glasgow corridor), Fife, Perthshire, and parts of the southeast and northeast coasts.
- Model uncertainty: Regions with higher elevation showed greater clamping (extrapolation) in some projections.
- Background choice impact: ALL background yielded the most contiguous suitable areas and fewer extrapolation warnings; MCP produced fragmented predictions.

## Implications for risk assessment and management
- Premises linked to P. kernoviae and P. ramorum infections were disproportionately located in regions predicted to be suitable for R. ponticum:
  - 71% of inspected premises and 73% of non-trade garden premises fell within suitable habitat cells.
  - Among non-trade garden premises, 23% occurred in highly suitable areas (>0.65) versus 13% for all premises.
- Co-location with vulnerable habitats:
  - 54% of core native woodland coincided with suitable habitat; 10% of core woodland fell in highly suitable areas.
  - 64% of Larix kaempferi populations occurred in suitable habitat; 14% in highly suitable areas.
  Heathland largely outside suitable habitat in southwest Scotland, but some fringe overlaps exist where vulnerable habitats coincide with garden sources and L. kaempferi.
- Management focus: Highest risk areas are mosaics where broad-leaved woodland, Larix kaempferi, and garden premises overlap; these areas warrant intensified surveillance and biosecurity measures.

## GIS outputs and methodological notes
- Outputs suitable for policy and public-facing maps: 
  - Mean habitat suitability maps for Scotland
  - Uncertainty/variability maps (standard deviation)
  - Clamping maps to identify extrapolation risk
  - Binary presence/absence maps using a threshold maximizing test sensitivity + specificity
- Spatial workflow considerations:
  - Aggregation from multiple data sources to a single 1 km grid
  - Use of NDVI/EVI as proxies for soil moisture and vegetation activity
  - Cautious interpretation where data coverage is patchy or biased by citizen science
  - Overlay analyses in ArcGIS to assess overlaps with habitats, woodlands, nurseries, and Larix kaempferi distributions

## Limitations and considerations for future GIS work
- Data heterogeneity and potential sampling biases inherent in volunteer-collected records
- Resolution constraints: predictors and presence data at 1 km (finer data not uniformly available)
- Spatial autocorrelation concerns; model validation indicates dependence between training and test sets can affect results if not properly mitigated
- Extrapolation risk in higher-elevation or novel environmental spaces highlighted by clamping maps
- Need for ongoing data updates and validation as new occurrences and environmental layers become available