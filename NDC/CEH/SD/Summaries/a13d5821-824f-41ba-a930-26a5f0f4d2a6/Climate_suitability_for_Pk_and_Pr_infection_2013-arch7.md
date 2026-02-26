# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

## Overview
- Study refining climate-suitability models for Phytophthora spp. to predict infection risk across the UK, with a focus on Scotland and broader UK applicability.
- Distinguishes species-specific responses to temperature and humidity; expands spatial resolution to reduce coastal data gaps.
- Aims to support risk assessments and guidance by providing GIS-ready layers of climatically suitable conditions.

## Modelling objectives
- Incorporate updated epidemiological data and literature.
- Develop separate models for Pk and Pr reflecting species-specific responses to temperature and humidity.
- Improve spatial resolution to minimize data gaps, especially near coasts.

## Data inputs
- Environmental data: hourly temperature and relative humidity (RH) at 4 km grid resolution across the UK (2007–2011; 360 × 288 grid; 23,246 land squares).
- Data sources: Met Office climate data provided for model inputs.
- Output preparation: model layers reprojected to Ordnance Survey GB National Grid and resampled to a 5.5 grid square resolution for overlay with other risk factors.

## Modelling approach
- Temporal window: assesses climate suitability in 4 km squares over 48-hour periods (two consecutive days) to reflect infection processes that can require up to ~32 hours.
- Core mechanism: for each day and grid cell, compute hourly infection completion rates based on lab-derived temperature–infection relationships; infection is deemed successful over a 48-hour period if rates sum to one.
- Species-specific rules (see Table 1 in the report):
  - Pk (Phytophthora kernoviae): infection occurs between approximately 3°C and 27°C; upper bound and low-temperature behaviour include stricter conditions (e.g., potential failure if extended below 2°C).
  - Pr (Phytophthora ramorum): infection occurs between approximately 2°C and 29°C; higher probability of success at lower temperatures (i.e., broader suitability at cold ends).
  - Relative humidity: infection requires RH ≥ 85% for at least 10 hours on both days.
  - Some partial-success probabilities apply for temperatures near upper bounds (e.g., 1/3 probability between 28–29°C for Pr).
- Output metric: for each square, the predicted number of days per year suitable for infection, averaged across years (2007–2011).

## Spatial/Temporal resolution and outputs
- Initial spatial scale: 4 km grid square resolution (Scotland-focused in original development; extended UK coverage).
- Temporal scale: 2007–2011 data year-by-year, with annual and monthly summaries.
- Outputs include:
  - Annual average days suitable per square (UK-wide and Scotland-focused).
  - Spatial maps showing variation in suitability (highlights along west and some southern coasts in Scotland; broader UK patterns).
  - Standard deviation across years to indicate inter-annual variability.
  - Yearly and multi-year profiles of monthly days suitable for Pr and Pk (seasonality).

## GIS data processing and compatibility
- Reprojection and resampling: climate layers reprojected to OS GB National Grid; resampled to 5.5 grid square resolution for overlay with risk factors.
- Outputs designed as layers that can be combined with other GIS risk indicators and used in decision-making and policy contexts.
- The modelling framework was implemented in R and designed to support map-based data products for end users (policy colleagues, clients, public).

## Model validation
- Data sources for validation (presence/absence of infection):
  - (i) Wild and established plantings in England and Wales (2002–2009).
  - (ii) Scottish non-trade premises (2007–2012).
  - (iii) Larch fragments (Forestry Commission Scotland and others; 25791 samples).
- Validation approach: binary logistic regression to test whether observed infection status is predicted by climate-suitability values from the model; separate tests for Pr, Pk, or both where species identification varied.
- Key validation results:
  - All datasets showed climate-suitability values as significant predictors of infection status.
  - AUC (area under the ROC curve) values indicate reasonable discriminatory ability:
    - Dataset (i): Pr ~0.63; Pk ~0.72 (with Pr and Pk distinguishable per site data).
    - Dataset (ii): Pr ~0.65.
    - Dataset (iii): Pr ~0.81.
  - Relative differences: squares positive for a pathogen typically have more suitable days per year than negative squares; stronger discrimination in larch (Pk-associated) data.
- Implications: the climate-suitability models provide meaningful predictors of onward transmission in the field, though other factors influence actual spread.

## Key findings
- Scotland shows markedly higher suitability for Pr than for Pk; across Scotland, Pr generally yields many more suitable days per year than Pk.
- UK-scale patterns indicate Pr has broader and higher suitability across years than Pk.
- Seasonal peaks differ:
  - Pr: tends to peak between November and February.
  - Pk: tends to peak between June and August.
- Geographic patterns:
  - High Pr suitability along west coast (Argyll and Bute, Ayrshire) and parts of the south coast and central belt; some variability year-to-year, especially in southern Scotland.
  - Pk suitability, while present in western and central regions, remains relatively low compared with Pr, with notable but smaller regional maxima (e.g., Argyll and Bute, Ayrshire, central Highlands).

## Practical implications for GIS specialists
- Provides GIS-ready layers showing annual and monthly climate-suitability for Pr and Pk infection, suitable for risk mapping, overlay with land-use data, and informing surveillance or management decisions.
- Supports scenario analysis and prioritization by visualizing spatial patterns of climatically suitable conditions across Scotland and the UK.
- Demonstrates an approach to integrate species-specific epidemiological data with high-resolution climate rasters to produce actionable map products.

## Notes and limitations
- Validation with field data is ongoing; seasonality patterns require further field validation to confirm observed timings.
- Actual infection and transmission depend on additional ecological and operational factors beyond climate suitability (hosts, pathways, land management, etc.).
- While broader than Scotland, coastal and region-specific data gaps were addressed by increasing spatial resolution, though residual gaps may persist in some areas.