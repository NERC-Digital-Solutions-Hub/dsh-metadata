# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

## Aim
- Refine climate suitability models for Pr and Pk infection.
- Incorporate updated epidemiological data and literature; develop separate models for each pathogen.
- Improve spatial resolution to reduce data gaps and extend from Scotland to the UK.
- Validate model outputs against field datasets on onward transmission to assess predictive relevance.

## Data inputs and provenance
- Climate inputs: hourly temperature and relative humidity at 4 km resolution, 2007–2011, across the UK (360 × 288 grid; 23,246 land squares); provided by the Met Office.
- Processing: reprojected to OSGB National Grid at 5.5 grid square resolution; outputs used in a UK risk framework.
- Code and modelling: algorithm implemented in R.
- Validation data: field datasets (England/Wales plantings; Scottish non-trade premises; larch plantations) with infection status; pathogen species sometimes not consistently recorded.

## Approach and model design
- Uses 48-hour windows to reflect the infection process duration (up to 32 hours at 2°C).
- Inverts laboratory time-to-infection curves to derive hourly infection rates per pathogen across temperatures.
- For each 48-hour period, infection is predicted if cumulative hourly rates sum to 1, with species-specific temperature and humidity rules.
- Temperature thresholds and rules:
  - Pk: infection between 3°C and 27°C; lower bound details include a fail condition if dips below 2°C for long periods.
  - Pr: infection between 2°C and 29°C, with broader tolerance.
  - Relative humidity: infection requires ≥85% RH for at least 10 hours on both days.
- Outputs: predicted number of days suitable for infection per 4 km grid cell per year; reprojected to OSGB 5.5 grid for overlays with risk factors.
- Geographic and seasonal emphasis: detailed Scotland-focused analysis; UK extension.

## Outputs and interpretation
- Spatial maps of annual days suitable for Pr and Pk infection per square.
- Scotland: Pr shows much higher suitability than Pk; Pk typically has low suitability (median ~17–18 days; max ~30 days across cells).
- Pr suitability highest along west and south coasts and central belt; Pk highest in limited western/highland areas, overall far lower.
- Temporal patterns: Pr infection peaks Nov–Feb; Pk peaks Jun–Aug.
- Inter-annual variability: Pr suitability can vary by tens of days between years; Pk also variable but overall lower.
- Outputs emphasize relative (not absolute) suitability and note differing color scales between pathogens.

## Validation and model performance
- Datasets and method:
  - (i) Wild and established plantings in England/Wales (2002–2009).
  - (ii) Scottish non-trade premises (2007–2012).
  - (iii) Larch plantations across Scotland (FC and commercial).
- Analysis: binary logistic regression predicting infection status from climate suitability; performance measured by AUC.
- Results:
  - All datasets showed significant predictions; AUC values ranged (e.g., ~0.63 for Pr in England/Wales; up to ~0.81 for Pr in larch plantations).
  - Infected squares generally had higher predicted suitability (e.g., +20 days/year for Pr in some datasets; +40 days/year for Pr in larch plantations).
  - In England/Wales, Pk predictions sometimes outperformed Pr, suggesting pathogen-specific predictability can vary by dataset.
- Conclusion: climate suitability is a meaningful predictor of onward infection across diverse datasets.

## Key findings and implications
- Pr has a much broader and higher climate suitability footprint in the UK than Pk, especially in Scotland.
- Pr infection is predicted year-round, with strongest emphasis in winter; Pk is largely restricted to April–October.
- Model outputs align with field observations to a degree, supporting their use in risk assessment and biosecurity planning.
- Seasonal and geographic patterns can inform targeted monitoring and management strategies.

## Data governance and stewardship considerations
- Provenance and reproducibility:
  - Met Office climate inputs; epidemiological data from multiple sources; R-based modelling code; derived outputs with accompanying metadata.
- Data sharing and stewardship:
  - Outputs suitable for risk mapping and decision support; consider archiving in a data centre (e.g., ENDC/NERC DCI) with clear licensing and versioning.
  - Maintain data lineage from input climate data through processing steps to final risk layers.
- Metadata and documentation:
  - Capture temporal and spatial resolutions, processing steps (reprojection/resampling), model thresholds, validation datasets, and performance metrics.
- Reusability and updates:
  - Framework can be updated with new years or refined input data; ensure reproducibility through scripts and parameter records.

## Limitations and challenges
- Validation data sometimes lack consistent pathogen identification (Pr vs Pk), affecting species-specific assessment.
- Outcomes are relative measures of suitability, not absolute risk; cross-pathogen comparisons are limited by differing color scales.
- Spatial resolution and coastal data gaps pose interpretation challenges; ongoing need for field validation of seasonality and distribution patterns.