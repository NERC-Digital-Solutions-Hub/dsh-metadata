# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Overview
- SDM-based study using Maxent to map habitat suitability for Rhododendron ponticum across Scotland to assess risks for Phytophthora ramorum and Phytophthora kernoviae.
- Integrated 11 presence datasets (1950–2008) with environmental predictors to produce 1 km grid-scale habitat suitability maps.

## Data sources and data structuring
- Presence data compiled from 11 sources, dominated by Local Record Centres (LRCs, ~70% of records) and National Biodiversity Network (NBN) gateway; Edwards & Taylor (2008) contributed Argyll and Bute region data.
- Data aggregated to 1 km grid squares across Scotland (82,690 cells); 17,25 grid cells recorded as Rhododendron ponticum present.
- Habitat category coding where possible in Argyll and Bute: dense, scattered, or cleared cover.
- Predictors included: broad-leaved and coniferous forest cover; elevation; Enhanced and Normalised Vegetation Indices (EVI, NDVI); soil carbon content; soil pH; data derived from MODIS, Landsat-based sources, UK Land Cover Map 2000; ArcGIS 9.3 used for processing.

## Modelling approach and considerations
- Addressed SDM assumptions (equilibrium with environment) and sampling biases (clustering) using:
  - Upweighting records with few geographic neighbours (bias grid) to counteract first-appearance clustering.
  - Three background definitions for Maxent: ALL (whole study area), MCP-based (region-specific convex polygons), REACH (areas reachable via roads/rail/urban land cover).
- For each background option, models were run with and without upweighting (six total Maxent models).
- Modeling setup: 25 iterations with 30% of data withheld for cross-validation; included both linear and quadratic predictor terms.
- Outputs included: mean predicted habitat suitability, standard deviation across iterations, and clamping maps to show predictor value ranges beyond training data.
- Model evaluation metrics included: AUC for training/testing, predicted-to-expected (P/E) ratios, and Spearman correlations between predicted suitability and observed R. ponticum cover.

## Key predictors and model insights
- Most important predictor: broad-leaved woodland cover (average contribution ~55.8%).
- Additional influential predictors: annual mean EVI (~9.1%), soil carbon content (~11.6%), elevation (~10.7%); soil moisture indicators (via EVI) also influential.
- Relationship patterns: suitability increases with broad-leaved woodland; suitability declines with higher elevation and high/low extremes of EVI (soil moisture proxy).
- Background choice impact: ALL background provided the strongest, most contiguous predictions; MCP background performed worst; upweighting records did not improve accuracy.

## Results and spatial implications
- Best model (ALL background, unweighted) showed good discrimination (training and test AUC ≈ 0.83); P/E ratios aligned with model expectations across suitability classes.
- About 24% of Scotland’s 1 km grid cells predicted to be suitable habitat for R. ponticum.
- Premises data alignment: 71% of inspected premises and 73% of non-trade garden premises fell within R. ponticum suitable habitat cells.
- Co-location with vulnerable habitats and potential infection sources:
  - 54% of core native woodland overlapped with predicted suitable habitat; 10% within highly suitable zones.
  - Some heathland types and Larix kaempferi distributions overlapped with suitable areas, indicating potential hotspots for rapid pathogen spread if introduction occurs.
- Regional patterns highlighted: contiguous suitable areas around the Great Glen, central belt, coastal zones; exposure uncertain at fringe high-elevation cells due to clamping.

## Data governance, quality, and limitations
- Data provenance spans multiple organizations and volunteer contributions; 1 km grid aggregation aids comparability but may obscure fine-scale patterns.
- Sampling bias and background selection significantly influence model outcomes; the ALL background with unweighted records yielded the most robust results.
- Limitations include reliance on presence-only data, potential under-sampling in some areas, and extrapolation indicated by clamping in high-elevation fringes.
- Underlying uncertainties in predicting actual occupancy versus suitability; explicit use of multiple validation diagnostics (AUC, P/E, Spearman correlations) to support interpretation.

## Implications for data leaders
- Demonstrates the value of integrating diverse data sources (volunteer, governmental, and institutional datasets) for landscape-scale risk mapping.
- Highlights the importance of explicit bias handling (background selection, spatial weighting) and robust cross-validation in presence-only SDMs.
- Emphasizes data interoperability and metadata clarity to enable reproduction and reuse across agencies (policy units, habitat networks, and infection surveillance).
- Shows how linked data layers (habitat networks, garden/premises data, and pathogen sources) can inform targeted monitoring and management decisions.