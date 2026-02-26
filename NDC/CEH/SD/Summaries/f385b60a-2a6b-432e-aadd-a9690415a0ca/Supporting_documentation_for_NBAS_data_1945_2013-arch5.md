# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013.

## Overview
- Long-term monitoring dataset from the North Basin of Windermere, Cumbria, England, covering 1945–2013 for multiple variables: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sampling frequency: weekly or fortnightly for most variables; depth integration changes over time (0–5 m, 0–10 m, 0–7 m).
- Origin and custody: data initially collected by the Freshwater Biological Association; since 1989 collected by the Centre for Ecology & Hydrology (CEH) and its predecessor Institute of Freshwater Ecology.
- Data are provided as downloadable CSV files with clearly described variables and units; includes examples of how data have been used in recent publications.

## Sampling regime and collection methods
- Measurements taken from a boat at a marked location (buoy) at the deepest part of the lake.
- Water samples are integrated by depth according to historical period: 0–5 m (1945–1962), 0–10 m (1962–1964), and 0–7 m (1964 onwards).
- Variables and units are specified to support comparability across time, with explicit handling of detection limits.

## Quality control and data provenance
- The dataset consists of raw measurements and has not undergone formal quality control or calibration, with exceptions only for double entries from 2005 onward.
- Data have been visually checked for consistency.
- A detection-limit indicator is included as sign_if_LT_LOD to flag values below detection limits.

## Data structure and metadata
- Data format: comma-separated values (CSV).
- Core columns:
  - sdate, Description = Date of measurement.
  - variable, Description = Name of the measurement (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value, Description = Measured value for each variable (with units as described).
  - sign_if_LT_LOD, Description = Indicator (< if below detection limit).
- Variables include temperature (C), oxygen saturation (%), Secchi depth (m), alkalinity (µg CaCO3 per L), pH, and nutrient/phyto-chemical concentrations (µg per L).

## Accessibility and reuse
- The dataset is available to download and can be used for long-term ecological analyses, comparisons, and model validation.
- Documented usage in recent peer-reviewed publications demonstrates ongoing applicability and relevance.

## Considerations for data stewardship and governance
- Ensure timely transfer of data from data creators and maintain alignment with metadata standards (units, depth-integrated sampling regimes, QC flags).
- Maintain and document provenance, including changes in sampling depth protocols and data custodianship (Freshwater Biological Association → CEH).
- Preserve raw data while continuing to implement quality control, calibration, and documented transformations where appropriate.
- Implement and communicate clear update/versioning processes, including any corrections or reprocessing and associated changelogs.
- Maintain data access controls and disclosure of any limitations or caveats (e.g., raw data status, detection-limit handling) to support responsible data discovery and reuse.

## Publications and impact
- Dataset has been used in multiple recent studies, illustrating its value for long-term ecological and climate-related research (examples include work on early warning indicators, perch ecology, pathogen-driven ecosystem forcing, phytoplankton phenology, and climate-change impacts on lake systems).