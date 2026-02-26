# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2019 to 2020

## Overview
- Part of an ongoing fortnightly monitoring dataset for the South Basin of Windermere, Cumbria, England.
- Timeframe: January 2019 through the end of 2020.
- Data types included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), phytoplankton chlorophyll a (TOCA).
- Data are provided to support understanding of lake water quality and phytoplankton dynamics.

## Sampling regime and collection methods
- Sampling frequency: fortnightly.
- Location and depth: water samples collected from a boat at a marked buoy location in the deepest part of the lake.
- Water column integration: samples drawn from 0 to 7 m.
- Measurement units:
  - TEMP: degrees Celsius
  - OXYG: % air saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - pH: pH units
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: µg per litre (with <LOD indicated by a "<" sign in the Sign column)

## Data structure and metadata
- Data format: comma-separated values (CSV).
- Core columns:
  - Date
  - Variable (description of measurement)
  - Value (measurement)
  - Sign (if below detection limit)
- Variable descriptions align with the measured parameters listed above.
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Quality control and data readiness
- Raw data: not yet quality controlled or calibrated.
- Data integrity checks: double entered and visually checked.
- Data gaps: caused by weather conditions, COVID-19 restrictions, or staff shortages.
- Ongoing quality control status implies readiness for initial use with caution; users should apply appropriate QC/calibration steps before downstream analyses.

## Provenance and funding
- Source publication: Feuchtmayr et al. (2024) describing the dataset.
- Funding/support: NERC award NE/R016429/1, UK-SCaPE programme.

## Data availability and stewardship considerations
- Availability: CSV dataset with clearly defined variables and units; includes a field to denote values below detection limits.
- Stewardship actions to consider:
  - Maintain and update metadata to reflect QC status, calibration details, and any reprocessing.
  - Preserve the 0–7 m integrated sampling depth specification and deepest-location collection point for reproducibility.
  - Track and document any updates, corrections, or reprocessing of raw data.
  - Ensure proper handling of <LOD values via the Sign column to preserve data interpretation.
  - Align with repository or portal standards for metadata completeness and discoverability.
  - Consider linking this dataset to related Windermere time series and related environmental datasets for interoperability.

## Temporal and spatial coverage
- Temporal: 2019-01 to 2020-12.
- Spatial: South Basin of Windermere, Cumbria, England; sampling at the deepest part of the lake from a buoy location.