# Field level headings: 1m, GMT = °C at 1 metre. 3m, GMT = °C at 3metre. 5m, GMT = °C at 5 metre. 7m, GMT = °C at 7 metre. 9m, GMT = °C at 9 metre. 11m, GMT = °C at 11 metre. 13m, GMT = °C at 13 metre. 15m, GMT = °C at 15 metre. 17m, GMT = °C at 17 metre. 19m, GMT = °C at 19 metre

- Temperature sensing setup
  - 10 Labfacility platinum resistance thermometers (PRTs) encapsulated in a stainless steel sheath
  - Temperature range for thermometers: -5 to +40°C
  - Sensor type and enclosure described as part of the temperature string

- Depth and temperature data
  - Temperatures reported at multiple depths: 1 m, 3 m, 5 m, 7 m, 9 m, 11 m, 13 m, 15 m, 17 m, 19 m
  - Each depth provides GMT timestamped °C readings

- Timeframe
  - Date range: 03/11/2006 00:00 to 15/12/2008 14:00

- Location and positioning
  - Grid reference: SH 77961 46465
  - Latitude: 53.001555
  - Longitude: -3.8200267
  - Elevation: 460 m

- Data acquisition
  - Data logger: Campbell Scientific CR10X

- Data interpretation and usage notes
  - Data are structured to allow depth-resolved temperature profiling over time
  - Metadata includes sensor type, depth, time standard (GMT), and precise location
  - “Location” field shows placeholders in the snippet; ensure complete geolocation is captured in the full metadata

- How this supports data work for the Data Support archetype
  - Provides a concrete, multi-depth time series that can be explored to identify temperature patterns with depth and over time
  - Enables creation of self-serve data products (e.g., depth-specific time series, heatmaps, and cross-depth comparisons)
  - Useful for policy or operations: environmental monitoring, climate studies, or site-specific thermal profiling

- Potential data products and visualisations
  - Depth-wise temperature time series by depth
  - Temperature profile heatmaps across depths and dates
  - Summary statistics (min, max, mean) by depth over the date range
  - exports to CSV for downstream analysis

- Data quality and management considerations
  - Ensure complete and consistent metadata (exact location, deployment details, sensor IDs)
  - Validate time stamps are in GMT and aligned across all depths
  - Handle any missing readings due to logger downtime or sensor issues
  - Confirm temperature range suitability for all sensors (-5 to +40°C) and document any excursions

- Suggested next steps for data support
  - Create a data dictionary including field names, units, and depths
  - Produce a starter dashboard with depth-aggregated temperature visualisations
  - Document data provenance: sensor model, installation date, maintenance notes, and logger configuration