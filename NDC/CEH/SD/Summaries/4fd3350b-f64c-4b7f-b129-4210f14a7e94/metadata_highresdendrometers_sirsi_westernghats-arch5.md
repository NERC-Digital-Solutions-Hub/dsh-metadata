# Dendrometer_Cantium_Caryoarbiria_Symplocus.csv and Dendrometer_Terminalia_Oleadioica_Mymocylon.csv – Dendrometer measurements from a farm near Sirsi, Karnataka, India (Jan 2020–May 2021)

## Overview
- Two CSV datasets containing high-resolution dendrometer measurements from trees on a farm near Sirsi, Western Ghats, India.
- Measurements cover January 2020 to May 2021 with differing sampling frequencies by species groups.

## Data collection details
- Site: Farm near Sirsi, Karnataka; latitude 14.49 N, longitude 74.75 E; altitude 538 m.
- Instrument: High-resolution dendrometers (Ecomatik, D25) installed at approximately breast height.
- Measurement approach: Diameter changes recorded relative to the sensor’s initial position (D_plus_Dref_mm_speciesN).
- Sampling frequencies by species group:
  - Minute intervals for Cantium, Caryoarbiria, SymplocusBeddomii.
  - 15-minute intervals for Terminalia, Oleadioica, Mymocylon.

## Datasets and variables
- Filenames indicate dataset boundaries:
  - Dendrometer_Cantium_Caryoarbiria_Symplocus.csv
  - Dendrometer_Terminalia_Oleadioica_Mymocylon.csv
- Core variables are diameter changes expressed as D_plus_Dref_mm_species1/2/3 (in mm); Dref is a non-specified constant.
- Time metadata:
  - Date format: DD/MM/YY
  - Time format: HH:MIN:SEC with AM/PM indicator
- Data are aligned with measurements taken at breast height and reflect changes relative to the initial sensor position.

## Data quality and processing notes
- Raw data were multiplied by 4 to convert from voltage (V) to millimeters (mm).

## Governance, accessibility, and documentation
- Datasets were uploaded to relevant portals and catalogued.
- Metadata provides:
  - Sensor model and placement details
  - Spatial-temporal coverage
  - Unit conventions and time formatting
- Implicit data availability considerations, such as potential embargoes or proprietary issues, should be reviewed during sharing decisions.

## Considerations for Data Stewards
- Temporal and spatial coverage are well-defined, but ensure future updates capture any recalibrations or sensor changes.
- Standardize species naming conventions across datasets to improve interoperability (current names show inconsistencies in spelling/formatting).
- Clarify the Dref constant specification and provide a data dictionary for D_plus_Dref_mm_speciesN variables.
- Validate unit consistency and provide explicit timezone information if timestamps are used in cross-dataset analyses.
- Prepare for data transfer and storage considerations given high-frequency, large-volume time-series data.