# Elter_dissolved_oxygen_2018-2019.txt

- What this dataset contains
  - Daily average dissolved oxygen concentration (DO_conc, μg L-1) measured at the deepest point of Elterwater Inner basin.
  - Time period: May 2018 through December 2019.
  - Depths: measurements at 3 m and 5 m below the surface.
  - Measurement approach: PME miniDOT oxygen sensors using a fluorescence method; sensors include anti-fouling wipers.
  - Sensor specification: accuracy stated as 0.3 mg L-1.
  - Data processing: raw data collected every 15 minutes; these were daily averaged. Some small gaps in the QCed data were linearly interpolated if gaps were under 3 hours.

- Data collection specifics
  - Location: deepest point of Elterwater Inner basin (Latitude 54.4287°, Longitude -3.0350°).
  - Data structure implies a two-depth time series with a single DO_conc value per depth per day.

- Data structure
  - Columns: Date (yyyy-mm-dd), Depth (m), DO_conc (μg L-1).

- Data quality and provenance
  - Data are described as QCed with gaps interpolated for small (<3 hour) missing intervals.
  - Measurements rely on fluorescence-based DO sensors (miniDOT) with anti-fouling features, contributing to data reliability.
  - The description provides explicit measurement method, sensor type, and location, supporting traceability.

- Considerations for data governance and reuse (as relevant for Data Leaders)
  - Metadata completeness: confirm and document units, depth references, method details, and sensor calibration dates to support reproducibility.
  - Discoverability and standards: ensure clear naming conventions and add a data dictionary for DO_conc units and the interpretation of depths.
  - Data quality management: maintain QC flags, justify interpolation decisions, and record any remaining gaps or sensor maintenance events.
  - Data integration: align with broader datasets by standardizing timestamp formats, depth notation, and units to enable cross-dataset analysis.
  - Data stewardship: preserve versioning of the dataset and provide provenance so future users can trace data processing steps from raw 15-minute data to daily averages.