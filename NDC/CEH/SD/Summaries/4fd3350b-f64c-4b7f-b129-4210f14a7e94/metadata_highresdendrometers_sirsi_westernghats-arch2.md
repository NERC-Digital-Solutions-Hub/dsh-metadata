# Dendrometer datasets from trees on a farm near Sirsi, Karnataka, India (Jan 2020–May 2021)

- Overview
  - High-resolution dendrometer data from trees on a farm near Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
  - Measurements collected from January 2020 to May 2021.

- Data resources and structure
  - Filenames:
    - Dendrometer_Cantium_Caryoarbiria_Symplocus.csv
    - Dendrometer_Terminalia_Oleadioica_Mymocylon.csv
  - Species groups by file:
    - First file: Cantium, Caryoarbiria, SymplocusBeddomii
    - Second file: Terminalia, Oleadioica, Mymocylon
  - Instrument: High-resolution dendrometer (Ecomatik, D25) installed at breast height.
  - Measurement concept: Diameter changes relative to the sensor’s initial position (D_plus_Dref_mm_speciesX).

- Time resolution and coverage
  - Cantium, Caryoarbiria, SymplocusBeddomii: minute-interval measurements.
  - Terminalia, Oleadioica, Mymocylon: 15-minute interval measurements.
  - Time format: Date as DD/MM/YY; Time as HH:MM:SS; AM/PM indicated.

- Data content and variables
  - D_plus_Dref_mm_species1, D_plus_Dref_mm_species2, D_plus_Dref_mm_species3 (mm): diameter plus a non-specified constant Dref (offset).
  - Values reflect changes from the initial sensor position rather than absolute diameter at breast height.

- Data quality and processing notes
  - Raw data have been multiplied by 4 to convert from volts (V) to millimeters (mm), indicating a units conversion step.
  - Measurements are relative to baseline, not raw DBH; Dref offsets present per species.

- Location context
  - Site: Farm near Sirsi, Karnataka, Western Ghats, India.
  - Coordinates: 14.49 N, 74.75 E; Elevation: 538 m.

- Relevance for environmental monitoring
  - Supports consistent, time-series monitoring of tree diameter fluctuations as indicators of growth dynamics, water status, and environmental stress.
  - Standardized format (DD/MM/YY, time, species-specific Dref-augmented diameter) facilitates cross-temporal analysis and policy-relevant reporting.

- Considerations for data integration and reuse
  - Different sampling frequencies across species require harmonization for combined analyses.
  - Dref offsets are not individually specified, which may necessitate clarification during downstream synthesis.
  - Data are suitable for augmentation with other environmental datasets to increase analytical value and reuse across monitoring initiatives.