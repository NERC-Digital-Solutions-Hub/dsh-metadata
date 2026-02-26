# Dendrometer_Cantium_Caryoarbiria_Symplocus.csv; Dendrometer_Terminalia_Oleadioica_Mymocylon.csv

## Overview
- High-resolution dendrometer data collected from trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Site coordinates: 14.49 N, 74.75 E; altitude 538 m.
- Measurement period: January 2020 to May 2021.
- Sampling frequency: minute intervals for Cantium, Caryoarbiria, and SymplocusBeddomii; 15-minute intervals for Terminalia, Oleadioica, and Mymocylon.
- Instrument: high-resolution dendrometer (Ecomatik, D25) installed at breast height.
- Measurements: diameter changes relative to the sensor’s initial position (D_plus_Dref_mm_species1/2/3).

## Data structure and metadata
- Filenames indicate two datasets:
  - Dendrometer_Cantium_Caryoarbiria_Symplocus.csv
  - Dendrometer_Terminalia_Oleadioica_Mymocylon.csv
- Columns representing diameter changes:
  - D_plus_Dref_mm_species1, D_plus_Dref_mm_species2, D_plus_Dref_mm_species3 (all in mm)
- Date and time formatting:
  - Date format: DD/MM/YY
  - Time format: HH:MM:SS
  - Time indicator: AM/PM
- Explanation for data columns:
  - D_plus_Dref_mm_speciesX represents the diameter plus a non-specified constant Dref for species X.
- Data quality note:
  - Raw data were multiplied by 4 to convert from volts (V) to millimeters (mm).

## Spatial and temporal context
- The data cover multiple tree species on a single farm site adjacent to Sirsi, Karnataka.
- Time series span across 2020–2021 with high temporal resolution, enabling fine-scale growth and diameter-change analyses.

## Practical considerations for data leaders
- Data discovery and usability:
  - Clear metadata describing date/time formats, units, and the meaning of each D_plus_Dref column.
  - Two separate files align with species groupings, aiding cross-species analyses.
- Data gaps and granularity:
  - Mixed sampling intervals (minute vs 15 minutes) by species require harmonization for joint analyses.
  - The Dref term is not explicitly defined; interpretation requires careful handling during analyses.
- Data quality and standardization:
  - The 4x scale factor to convert from V to mm must be consistently applied across the dataset.
  - Metadata provides essential context for sensor placement and measurement baseline (breast height, initial sensor position).
- Potential use cases:
  - Growth dynamics and diurnal/seasonal diameter changes.
  - Inter-species comparisons of diameter variability.
  - Integration with environmental data (e.g., climate records) for broader ecological or agronomic insights.