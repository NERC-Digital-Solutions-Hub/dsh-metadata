# Dendrometer_Cantium_Caryoarbiria_Symplocus.csv

## Overview
- High-resolution dendrometer data from trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Location: 14.49 N, 74.75 E; altitude 538 m.
- Data cover Jan 2020 to May 2021.
- Measurements include minute-interval data for Cantium, Caryoarbiria, SymplocusBeddomii and 15-minute interval data for Terminalia, Oleadioica, Mymocylon.

## Datasets and Filenames
- Dendrometer_Cantium_Caryoarbiria_Symplocus.csv
- Dendrometer_Terminalia_Oleadioica_Mymocylon.csv

## Sampling and Instruments
- Instrument: High-resolution dendrometer (Ecomatik, D25) installed at breast height.
- Purpose: Measures diameter changes relative to the sensor’s initial position (D_plus_Dref_mm_speciesX).
- Temporal resolution:
  - Minute intervals for Cantium, Caryoarbiria, SymplocusBeddomii.
  - 15-minute intervals for Terminalia, Oleadioica, Mymocylon.

## Data Details
- Time format: Date in DD/MM/YY; Time in HH:MM:SS; AM/PM indicator provided.
- Measurements: D_plus_Dref_mm_species1, D_plus_Dref_mm_species2, D_plus_Dref_mm_species3 (all in millimeters).
- Units: Diameter changes relative to a reference diameter (mm).

## Data Quality and Processing
- Raw data scaled by a factor of 4 to convert from volts (V) to millimeters (mm).

## GIS and Data Use Considerations
- Suitable for map-based visualizations of tree growth dynamics and spatial patterns in a local orchard/forest setting.
- Can be integrated with spatial coordinates to map growth responses across trees and relate to environmental variables.
- Important to account for data alignment across species due to different sampling intervals (minute vs. 15-minute).