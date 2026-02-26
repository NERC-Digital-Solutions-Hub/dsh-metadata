# Dendrometer_Cantium_Caryoarbiria_Symplocus.csv and Dendrometer_Terminalia_Oleadioica_Mymocylon.csv Dataset from Farm near Sirsi, Karnataka

## Overview
- High-resolution dendrometer time series from trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Two CSV datasets covering different species with different sampling intervals.
- Data collected to measure diameter changes over time using a dendrometer installed at breast height.

## Dataset structure and contents
- Filenames:
  - Dendrometer_Cantium_Caryoarbiria_Symplocus.csv
  - Dendrometer_Terminalia_Oleadioica_Mymocylon.csv
- Location and site:
  - Farm near Sirsi, Karnataka, Western Ghats, India
  - Coordinates: 14.49 N, 74.75 E
  - Altitude: 538 m
- Time period:
  - January 2020 to May 2021
- Species and sampling intervals:
  - Cantium, Caryoarbiria, SymplocusBeddomii: measurements at minute intervals
  - Terminalia, Oleadioica, Mymocylon: measurements at 15-minute intervals

## Measurements and instrumentation
- Instrument: High-resolution dendrometer (Ecomatik, D25)
- Installation: Mounted at breast height
- What is measured: Diameter changes relative to the sensor’s initial position (Dref)
- Data fields (per species group):
  - Date: DD/MM/YY
  - Time: HH:MM:SS
  - AM/PM indicator
  - D_plus_Dref_mm_species1, D_plus_Dref_mm_species2, D_plus_Dref_mm_species3 (diameter plus a non-specified constant Dref; units in mm)

## Data formatting and units
- Date format: DD/MM/YY
- Time format: HH:MM:SS with AM/PM indicator
- Units: millimeters (mm) for diameter changes
- Field explanations indicate diameter values are relative to an initial reference position (Dref)

## Data quality and preprocessing notes
- Raw data have been multiplied by 4 to convert from voltage (V) to millimeters (mm); the dataset reflects this scaling.
- The D_plus_Dref_mm fields represent diameter plus an unspecified constant Dref; users should account for this Dref when interpreting absolute diameters.
- Metadata on data provenance beyond what is described is limited; users may need to verify sensor calibration and exact Dref values for precise analyses.

## Usage and considerations for data support
- Suitable for analyses of short- and long-term diameter changes, diurnal cycles, and growth patterns across species.
- Can be used to create self-serve dashboards or time-series visualizations by species and sampling interval.
- Important considerations:
  - Apply or reverse the 4x scaling as needed depending on analysis approach.
  - Clarify or estimate the Dref constant when comparing across species or datasets.
  - Be mindful of time zone and any potential daylight-saving adjustments if integrating with external environmental data.

## Provenance and access notes
- Data are provided as two CSV files with explicit filenames, location details, and species groupings.
- Site metadata includes exact coordinates and altitude to support spatial analyses or site-level comparisons.