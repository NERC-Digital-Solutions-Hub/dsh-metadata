# Global inequities and political borders challenge nature conservation under climate change

## Overview
- Outputs from ensemble Species Distribution Models (SDMs) assess how climate change and socio-political factors affect bird and mammal biodiversity.
- National-level data for 189 countries projecting changes in species richness to 2070 (dataset: Climate_impacts_by_country.csv).
- Cross-border biodiversity metrics: number of species whose ranges intersect political borders (transboundary_richness.csv) and projected cross-border range shifts under climate change (transboundary_range_shifts.csv).
- Global scope across >12,700 terrestrial birds and mammals (about 80%), excluding species with highly restricted ranges.
- Governance context included via a national-level governance score derived from World Bank indicators (2018 baseline).

## Datasets included
- Climate_impacts_by_country.csv
  - 189 rows (one per country), 31 columns.
  - Columns: ISO3 country code (first column); governance score (last column; mean of six World Bank Governance Indicators; range -2.5 to 2.5).
  - Intervening columns encode a three-part structure: climate scenario (current, rcp26, rcp45, rcp60, rcp85), taxonomic group (mammal, bird, or both), and measurement (SR for species richness; pctChange for percentage change in richness).
  - Example: rcp85_bird_SR = bird species richness under RCP 8.5 for each country.
- Transboundary_richness.csv
  - 327 rows (one per border), 3 columns.
  - Border identifier (ISO3 country code pair).
  - transboundary_richness: number of bird/mammal species whose ranges intersect the border.
  - transboundary_richness_threatened: number of threatened species (VU/EN/CR) intersecting the border.
- Transboundary_range_shifts.csv
  - 6 columns.
  - Border identifier (ISO3 country code pair).
  - Four columns: projected transboundary range shifts broken down by taxonomic group (mammals or birds) and climate scenario (moderate RCP 4.5 or high RCP 8.5).
  - barrier_species: number of non-flying mammals projected to cross fortified borders under high emissions (RCP 8.5); NA where no barrier exists.

## Data collection and model methods
- Data sources: IUCN Red List (species distributions), BirdLife International, Handbook of the World (HBW).
- SDM ensemble: Generalised Additive Models (GAMs), Generalised Linear Models (GLMs), Random Forests (RFs), Boosted Regression Trees (BRTs).
- Predictors: five climate variables (mean annual temperature, temperature seasonality, precipitation in wettest/driest months, precipitation seasonality).
- Projections: 2070 under four climate scenarios (RCP 2.6, 4.5, 6.0, 8.5) using three GCMs (HadGEM2-ES, CCSM4, MIROC-ESM-CHEM).
- Spatial blocking for independence: non-contiguous sampling units (ecoregions) divided into ten blocks; 10-fold cross-validation (block left out as test set).
- Model performance: assessed with AUC (area under the ROC curve); ensemble projections per species: 4 model types × 10 blocks × 3 GCMs × 4 scenarios (total 120 projections) weighted by each model’s AUC.
- Outputs: grid-cell species richness projections, aggregated to national level by averaging grid cells within each country; national richness change and governance score computed accordingly.

## Data structure and fields
- Climate_impacts_by_country.csv
  - 189 country rows, 31 columns.
  - Column 1: ISO3 country code.
  - Column 31: governance score (mean of six World Bank indicators; range -2.5 to 2.5).
  - Column naming: climate scenario_taxon_measurement (e.g., rcp85_bird_SR or current_mammal_pctChange).
  - Measurement types: SR (species richness, count) or pctChange (percentage change relative to current richness).
- Transboundary_richness.csv
  - 327 border rows, 3 columns.
  - border: border identifier (country code pair).
  - transboundary_richness: current number of intersecting species.
  - transboundary_richness_threatened: number of threatened intersecting species.
- Transboundary_range_shifts.csv
  - 6 columns.
  - border: border identifier.
  - Four columns for projected shifts by taxon (mammals or birds) and scenario (RCP 4.5 or RCP 8.5).
  - barrier_species: non-flying mammals projected to cross fortified borders (RCP 8.5); NA if no barrier.

## Usage, interpretation, and governance considerations
- Purpose: provide standardized, geographically extensive datasets to assess biodiversity under climate change and the influence of governance and political borders.
- For data stewards:
  - Standardization: consistent use of ISO3 codes and a clear, repeatable column-naming scheme enabling programmatic access and interoperability.
  - Provenance: explicit data sources (IUCN, BirdLife, HBW) and transparent SDM methodology (model types, predictors, GCMs, scenarios, cross-validation approach).
  - Metadata richness: detailed description of file structures, units, and calculation methods, facilitating reproducibility and audit trails.
  - Reproducibility: ensemble workflow and weighting by model performance documented; national and cross-border metrics derived through specified aggregation steps.
  - Data updates: governance-based sharing and updates are anticipated; governance score is based on 2018 World Bank indicators, indicating the need to document any future updates or versioning.
  - Limitations and caveats: excludes restricted-range species; global-scale aggregation may mask regional data quality differences; border and barrier metrics depend on geopolitical and infrastructural details (e.g., barriers are NA where none exist).
- Access and interoperability:
  - Three CSV data files with explicit schemas support integration into data portals and catalogues.
  - Open-access publication cited for context and methodological details (useful for methodological reproducibility and extension).

## Practical notes for data stewards
- Ensure ongoing metadata maintenance, including versioning of the three CSV files and any future updates to climate projections or species lists.
- Maintain clarity on data licensing and access terms to align with open-access publication status.
- Consider establishing a data release schedule aligned with updates to climate scenarios, governance indicators, or species distribution data.
- Document any changes to border definitions or administrative boundaries that could affect cross-border metrics.