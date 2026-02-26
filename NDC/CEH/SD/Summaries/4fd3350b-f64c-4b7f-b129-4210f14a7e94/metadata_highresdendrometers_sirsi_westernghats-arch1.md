# Dendrometer_Cantium_Caryoarbiria_Symplocus.csv; Dendrometer_Terminalia_Oleadioica_Mymocylon.csv

- Location and context
  - Farm near Sirsi, Karnataka, Western Ghats, India
  - Coordinates: 14.49 N, 74.75 E; altitude 538 m

- Datasets and species
  - Dendrometer data for Cantium, Caryoarbiria, SymplocusBeddomii (minute-interval data)
  - Dendrometer data for Terminalia, Oleadioica, Mymocylon (15-minute interval data)

- Time period and sampling cadence
  - January 2020 to May 2021
  - Cantium, Caryoarbiria, SymplocusBeddomii: measurements at 1-minute intervals
  - Terminalia, Oleadioica, Mymocylon: measurements at 15-minute intervals

- Instrumentation and measurement type
  - High-resolution dendrometers (Ecomatik D25)
  - Installed at approximately breast height
  - Measure diameter changes relative to the sensor’s initial position (Dref)

- Data structure and fields
  - Date format: DD/MM/YY
  - Time format: HH:MM:SS (with AM/PM indicator)
  - D_plus_Dref_mm_species1 / D_plus_Dref_mm_species2 / D_plus_Dref_mm_species3: diameter changes expressed in millimeters relative to a non-specified reference Dref
  - Each dataset uses per-species D_plus_Dref columns indicating diameter plus a constant reference

- Data quality and notes
  - Raw data have been multiplied by 4 to convert from volts (V) to millimeters (mm)

- Considerations for analysis
  - Data at different temporal resolutions require alignment if combined
  - Dref values are not specified, which may affect interpretation of absolute diameters
  - Time stamps include AM/PM; ensure consistent time interpretation when merging datasets
  - Files indicate separate species groups; plan to join data by time and species where appropriate

- Potential uses
  - Analyze short-term and long-term diameter fluctuations
  - Explore patterns of growth and shrinkage at fine temporal scales
  - Assess responses to environmental factors if combined with external data (not provided in this document)