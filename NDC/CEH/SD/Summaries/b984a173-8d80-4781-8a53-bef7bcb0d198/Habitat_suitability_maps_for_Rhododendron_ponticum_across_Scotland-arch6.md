# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Overview
- Study models habitat suitability for Rhododendron ponticum as a reservoir host for Phytophthora ramorum and Phytophthora kernoviae in Scotland.
- Uses multiple presence datasets and environmental predictors to generate Maxent-based habitat maps and assess infection risk to vulnerable habitats.

## Data sources
- Presence data: eleven datasets (1950–2008) for R. ponticum in Scotland.
  - Nine datasets from Local Record Centres (LRCs), ~70% of records volunteer-generated.
  - A dataset from the National Biodiversity Network Gateway (NBN) accessed Feb 2009.
  - Edwards and Taylor (2008) dataset for Argyll and Bute region (driven from field surveys and maps).
- Spatial resolution: original records at 1 km or finer, summarized to 1 km × 1 km grid cells; 82,690 grid cells in Scotland with environmental data; 1,725 grid cells with R. ponticum presence.
- Environmental predictors (seven): 
  - Broad-leaved forest cover (BLWOOD)
  - Coniferous forest cover (CWOOD)
  - Elevation (ELEV)
  - Enhanced Vegetation Index (EVI)
  - Normalised Difference Vegetation Index (NDVI)
  - Soil carbon content (Carbon)
  - Soil pH (PH)
- Data sources for predictors: UK Land Cover Map 2000, forest cover data, MODIS EVI, NDVI datasets, SRTM elevation, soil datasets; analysis performed in ArcGIS 9.3.

## Data preparation and predictors
- Presence data summarized to 1 km grid cells; calculated proportion of 1 km cells in Argyll and Bute with dense, scattered, or cleared R. ponticum stands.
- Predictors derived as mean values per 1 km cell (or percent cover) where data resolution differed.
- Background areas tested to address sampling biases (see Modeling Approach).

## Modeling approach
- Species distribution modeling with Maxent (version 3.3.3e).
- Addressing non-equilibrium and sampling bias:
  - Three background options to reflect survey effort and accessibility:
    - ALL: whole study area (all 1 km cells with data available)
    - MCP: minimum convex polygons around presence datasets per region
    - REACH: reachable areas defined by road/rail networks and urban land cover
  - For each background option, models run with and without upweighting of records having few geographic neighbours (bias grid approach).
- Model setup:
  - 25 iterations with 30% of data withheld for cross-validation.
  - Included linear and quadratic predictor terms.
  - Projections produced across Scotland; generated mean predicted suitability, standard deviation, and average clamping maps.
  - Binary presence/absence maps produced using the threshold that maximizes test-set sensitivity plus specificity.
- Model evaluation:
  - AUC (training and test) to assess discrimination.
  - Predicted-to-expected (P/E) ratio for model calibration.
  - Spearman correlation between predicted habitat suitability and observed R. ponticum cover (Argyll and Bute).
  - Spatially cross-validated checks to assess independence of test vs training data.
- Integration with risk data:
  - Spatial overlap of predicted suitable habitat with:
    - Premises subject to routine inspections (Scottish Government Horticulture and Marketing Unit)
    - Forest Habitat Networks (Core Woodlands)
    - CEH CEH 2000 heathland map
    - Larix kaempferi (Japanese larch) distribution in Forestry Commission Scotland compartments
  - Premises categorized as trade vs non-trade (gardens, parks, hotels, etc., vs nurseries/garden centres).

## Key predictors and model performance
- Most important predictor: Broad-leaved woodland (BLWOOD) with average contribution ~55.8%.
- Other contributors (approximate across models): EVI (~9.1%), soil carbon content (~11.6%), elevation (~10.7%); NDVI and soil pH contributed modestly.
- Background and weighting effects:
  - ALL background without upweighting yielded the best performance.
  - MCP background performed worst.
  - Upweighting records with few neighbours did not improve model accuracy and, in weighted ALL, worsened test performance due to potential clustering.
- Validation metrics:
  - Best model (ALL background, unweighted): training AUC ≈ 0.83; test AUC ≈ 0.83.
  - Predicted-to-expected ratio indicates good model discrimination across suitability classes; monotonic increase with habitat suitability.
  - Omission rates on test data aligned with predictions for unweighted ALL model; weighted models showed poorer omission match.
  - Correlation between predicted habitat suitability and observed R. ponticum cover in Argyll and Bute: Spearman ρ ≈ 0.58 (p < 0.00001).

## Results: spatial patterns and risk implications
- Scotland-wide predictions:
  - 24% of 1 km grid cells predicted to be suitable habitat for R. ponticum (20,021 of 82,960 cells).
  - Most contiguous high-suitability areas located in: Great Glen, central belt (Edinburgh–Glasgow corridor), Fife, Perthshire, and parts of the SE and NE coasts.
  - Prediction uncertainty higher on fringe areas near high elevations.
- Premises and potential infection risk:
  - 71% of all inspected premises and 73% of non-trade garden premises fell in predicted suitable habitat cells.
  - Of non-trade garden premises, 23% occurred in highly suitable habitat (predicted presence probability > 0.65).
  - Larix kaempferi populations: 64% in suitable habitat; 14% in highly suitable habitat.
- Interaction with vulnerable habitats:
  - 54% of core native woodland coincided with predicted suitable habitat for R. ponticum; 11% of dwarf shrub heath and 7% of open shrub heath occur within predicted suitable habitat.
  - In the SW Scotland study area, mosaics where native woodland, gardens, and Larix kaempferi co-occur identified areas with elevated risk for rapid spread of P. kernoviae and P. ramorum.
- Practical outputs:
  - Binary suitability maps and clamping information provided to identify areas where predictor ranges extend beyond training data.
  - Overlay with habitat networks, heathland, and larch distributions to prioritize surveillance and management.

## Data quality, limitations, and considerations
- Data limitations:
  - Sampling biases inherent in volunteer and varied source datasets; addressed via background options and bias correction attempts.
  - Equilibrium assumption for SDMs challenged by ongoing invasion; multiple background schemes used to mitigate this.
- Validation caveats:
  - Potential spatial autocorrelation between training and test sets; cross-validation performed to gauge robustness.
- Implications for data support practice:
  - Demonstrates integration of heterogeneous presence data and diverse environmental layers into a coherent predictive framework.
  - Highlights importance of background selection, bias correction, and multi-faceted validation when building data products for monitoring invasive reservoir hosts.

## Takeaways for data support practice
- Combining multiple, heterogeneous data sources requires careful alignment to a common grid and consistent predictor definitions.
- Explicitly test multiple background definitions and weighting schemes to mitigate sampling bias in presence-only SDMs.
- Use cross-validation and multiple performance metrics (AUC, P/E, correlation with observed abundance) to assess model reliability.
- Produce interpretable data products (mean maps, uncertainty maps, and clamping) and integrate with other risk layers to support surveillance and management decisions.