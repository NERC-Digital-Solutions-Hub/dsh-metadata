# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Overview
- Excerpt of a 2013 study detailing methods, results, and quality control for habitat suitability modelling of Rhododendron ponticum (an emergent reservoir host for Phytophthora pathogens) across Scotland.
- Aims to map potential habitat suitability to assess risk of pathogen spread to vulnerable habitats and inform monitoring and management.

## Data sources and dataset composition
- Eleven datasets compiled for R. ponticum presence in Scotland (1950–2008).
  - Nine datasets from Local Record Centres (LRCs), largely volunteer-generated (≈70% of records).
  - One dataset from the National Biodiversity Network Gateway (NBN) downloaded Feb 2009.
  - A dataset for Argyll and Bute region collated by Edwards and Taylor (2008).
- Data represented at original resolutions (1 km or finer) and summarized to 1 km x 1 km grid cells across Scotland:
  - 82,690 grid cells with environmental data; 17,25 grid cells with presence.
  - 1,725 unique grid cells with R. ponticum presence used for modelling.
- Presence data complemented by environmental predictors derived from multiple sources (forest cover, NDVI/EVI, elevation, soil carbon content, soil pH).

## Data preparation and management
- Presence data aggregated to 1 km grid cells; predictor data calculated as mean values per grid cell (for those at finer resolution).
- Predictor variables used:
  - Broad-leaf forest cover (BLWOOD)
  - Conifer forest cover (CWOOD)
  - Elevation (ELEV)
  - Enhanced Vegetation Index (EVI)
  - Normalised Difference Vegetation Index (NDVI)
  - Soil carbon content (Carbon)
  - Soil pH (PH)
- Data processing and analysis conducted in ArcGIS 9.3; predictions produced as continuous habitat-suitability surfaces and binary maps.

## Modelling approach
- Species distribution modelling (SDM) using Maxent (version 3.3.3e).
- Approaches to address typical invasive-species data issues:
  - Upweighting records with few geographic neighbours (bias grid) to counteract clustering and recent-invasion imprint.
  - Testing three background-area options to reflect sampling effort:
    - ALL: entire study area as background.
    - MCP: minimum convex polygon around each presence dataset (regional).
    - REACH: reachable area defined by roads, railways, and urban landcover.
  - Six Maxent models total (combinations of background option and weighting).
- Model construction details:
  - 25 iterations with 30% of data withheld for cross-validation.
  - Included linear and quadratic predictor terms to capture non-linear relationships.
  - Models projected across Scotland; produced maps of mean predicted suitability, standard deviation across iterations, and average clamping (predictor-range extrapolation) across iterations.
- Model evaluation and selection:
  - Binary maps thresholded to maximize test-set sensitivity plus specificity.
  - Performance metrics included AUC for training and test sets, predicted-to-expected (P/E) ratios, and correlation with habitat suitability (Boyce et al. 2002).
  - Relationship between predicted habitat suitability and observed R. ponticum cover tested using Spearman rank correlation (Argyll & Bute region).

## Key results and interpretation
- Best model: ALL background with presence data unweighted or weighted, averaged across 25 iterations.
  - ALL background model achieved strong balance between training and test accuracy.
  - MCP background performed worst; upweighting did not improve accuracy.
  - P/E ratios indicated good discrimination between suitable and unsuitable habitat; monotonic increase with habitat suitability.
- Predictor importance (best model ALL):
  - Broad-leaved woodland (BLWOOD) was the most influential predictor (approx. 56% contribution).
  - Other important predictors (≈10% each): EVI (annual mean), soil carbon content, elevation.
  - Elevation and soil carbon content generally reduced suitability at extreme values; high/low moisture indicated by EVI also influenced suitability.
- Spatial patterns:
  - Scotland-wide predicted suitable habitat: 24% of 1 km grid cells (20,021 of 82,960).
  - Contiguous areas of suitable habitat identified in regions such as the Great Glen, central belt, Fife, Perthshire, and parts of the east and southeast coasts.
  - All-absence model (ALL background) produced the most contiguous suitable-habitat predictions with the least clamping (predictor-range extrapolation).
- Validation and ecological relevance:
  - Positive correlation between predicted habitat suitability and local R. ponticum cover in Argyll & Bute (Spearman’s ρ ≈ 0.58; p < 0.00001).
  - Premises for Phytophthora infection (P. kernoviae and P. ramorum) were disproportionately located within R. ponticum-suitable habitats:
    - 71% of all inspected premises and 73% of non-trade (garden) premises fell in suitable grid cells.
    - Among non-trade garden premises, 23% occurred in highly suitable habitat (compared with 13% for all inspected premises).
  - Larix kaempferi (Japanese larch) distributions overlapped with suitable habitat for R. ponticum (64% of observed L. kaempferi populations in FC sub-compartments fell within suitable areas).
- Overlaps with vulnerable habitats:
  - Core native woodland overlapped with 54% of predicted suitable habitat; 10% within highly suitable areas.
  - Heathlands largely lay outside predicted suitable habitat in the study area, though some fringe zones exist where woodland, heathland, and potential host plants intersect.
  - Areas with mosaics of vulnerable habitats and potential infection sources (nurseries, gardens, and garden centers) highlighted as priority for monitoring and biosecurity.

## Data governance, use, and implications
- The study demonstrates how heterogeneous data sources (volunteer-based, institutional datasets, and national gateways) can be harmonised into a shared grid for modelling and risk assessment.
- It underscores the importance of metadata, provenance, and documentation when integrating multiple datasets with varying resolutions and scales.
- Findings support targeted surveillance and management by identifying landscapes where R. ponticum habitat suitability and infection-source premises co-occur, informing resource allocation for monitoring and control efforts.
- Governance considerations include handling background sampling biases, avoiding over-interpretation in extrapolated areas (clamping), and ensuring transparency about model assumptions (e.g., equilibrium with environment) and data limitations.