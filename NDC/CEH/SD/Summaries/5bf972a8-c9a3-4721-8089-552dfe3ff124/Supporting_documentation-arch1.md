# Global inequities and political borders challenge nature conservation under climate change

## Overview
- Outputs from ensemble Species Distribution Models (SDMs) examining how socio-political factors influence bird and mammal biodiversity under climate change.
- National-level insights for 189 countries on projected changes in species richness to 2070 and associations with governance quality, per-capita GDP, and per-capita CO2 emissions.
- Border-focused analyses estimating how many species’ ranges currently intersect or are projected to cross each political border, highlighting transboundary conservation challenges under climate change.

## Datasets included
- Climate_impacts_by_country.csv
  - National-level metrics for 189 countries (31 columns).
  - Columns encode climate scenario, taxonomic group (bird, mammal, or both), and measure (SR = species richness; pctChange = percentage change).
  - Last column provides a governance score (mean of World Bank governance indicators; range -2.5 to 2.5).
- Transboundary_richness.csv
  - 327 rows; each row corresponds to a political border.
  - Columns: border, transboundary_richness (current number of intersecting species), transboundary_richness_threatened (threatened intersecting species).
- Transboundary_range_shifts.csv
  - 6 columns including border and projected transboundary range shifts.
  - Breakdown by taxonomic group (mammals or birds) and climate scenario (RCP 4.5 and RCP 8.5).
  - Barrier_species column: number of non-flying mammals projected to cross fortified borders under high-emission scenario (NA for borders without barriers).

## Data generation and modeling methods
- Data sources: IUCN Red List of Threatened Species and BirdLife International/BHOW data for species distributions.
- Modeling approach: ensemble SDMs using GAMs, GLMs, Random Forests, and Boosted Regression Trees.
- Predictors: five climatic variables (mean annual temperature, temperature seasonality, precipitation in wettest/driest months, and precipitation seasonality).
- Climate projections: 2070 projections under four IPCC scenarios (RCP 2.6, 4.5, 6.0, 8.5) using three GCMs (HadGEM2-ES, CCSM4, MIROC-ESM-CHEM).
- Spatial approach: data split into ten blocks to enable 10-fold cross-validation with blockTools; blocks chosen to balance area and bioclimatic variation.
- Model evaluation: performance via ROC-AUC, weighting the ensemble by each model’s AUC; final species distribution projections used to compute grid-cell and national-level richness.
- Aggregation: national-level percentage changes in richness calculated by averaging grid-cell projections across each country.
- Governance measure: mean of six World Bank Governance Indicators (based on 2018 data).

## Data structure and content details

- Climate_impacts_by_country.csv
  - 189 rows (one per country) and 31 columns.
  - Column 1: ISO3 country code.
  - Last column: governance score (-2.5 to 2.5).
  - Intermediate columns: named as <scenario>_<taxon>_<measure> (e.g., rcp85_bird_SR, current_mammal_pctChange).
  - Scenarios include current, rcp26, rcp45, rcp60, rcp85; taxonomic groups: bird, mammal, or both; measures: SR or pctChange.

- Transboundary_richness.csv
  - 327 rows (each border between two ISO3 countries).
  - Columns:
    - border: border identifier (ISO3 code pair).
    - transboundary_richness: number of bird/mammal species whose ranges intersect the border currently.
    - transboundary_richness_threatened: number of threatened intersecting species (VU/EN/CR).

- Transboundary_range_shifts.csv
  - 6 columns.
  - border: border identifier (ISO3 code pair).
  - Four columns: projected transboundary range shifts across the border, broken down by taxonomic group (mammals or birds) and climate scenario (RCP 4.5 or RCP 8.5).
  - barrier_species: number of non-flying mammals projected to cross fortified borders under high-emission scenario (RCP 8.5); NA where no physical barrier exists.

## How to use the data
- Analyze correlations between governance/wealth indicators and projected biodiversity losses at the national level (Climate_impacts_by_country.csv).
- Assess regional and continental patterns in climate-driven biodiversity change across species groups and scenarios.
- Explore how climate change may alter cross-border biodiversity connectivity by examining transboundary richness and projected range shifts.
- Identify borders with high numbers of crossing species or many threatened species to inform transboundary conservation priorities.
- Compare impacts under different climate scenarios (e.g., RCP 4.5 vs. 8.5) to understand potential mitigation benefits.

## Context and limitations
- Data are model-based projections with inherent uncertainties from SDMs, scenario selection, and GCMs.
- Ensemble weighting by model performance (AUC) helps but does not remove uncertainty.
- Species distributions rely on IUCN/BirdLife data and may not capture all local dynamics or recent changes.
- Governance metric uses 2018 data and represents a mean across indicators, which may not reflect current conditions.

## Reference
- Materials and Methods provide full methodological details; base publication: Titley M.A., Butchart S.H.M., Jones, V.R., Whittingham M.J., Willis, S.G. Global inequities and political borders challenge nature conservation under climate change, Proceedings of the National Academy of Sciences, USA (2021, in press).