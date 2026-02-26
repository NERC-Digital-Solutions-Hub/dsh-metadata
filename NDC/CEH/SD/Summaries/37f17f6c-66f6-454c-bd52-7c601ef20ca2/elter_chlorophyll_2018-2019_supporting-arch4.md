# Elter_chlorophyll_2018-2019.txt

- Overview
  - Weekly to monthly vertical profiles of chlorophyll a collected from May 2018 to December 2019.
  - Location: deepest point of Elterwater inner basin (latitude 54.4287°, longitude -3.0350°).
  - Purpose: measure chlorophyll a concentrations across depth to understand phytoplankton biomass dynamics.

- Sampling Design and Procedures
  - Water samples (volume: 500 mL) collected at depths of 0.5, 1, 2, 3, 4, 5, and 6 meters.
  - Sampling frequency ranged from weekly to monthly within the study period.
  - Filtration: a known volume of each sample filtered immediately on a 5.5 cm GF/C filter.
  - Sample handling: filter papers frozen; samples analyzed within one month.

- Laboratory Analysis and Calculations
  - Chlorophyll a extraction: heated methanol extraction.
  - Measurement: spectrophotometer with wavelengths set at 750 nm for background turbidity and 665 nm for chlorophyll a.
  - Concentration calculation: Chlorophyll a concentration = (13.9 × A_corr665 × 1/d) × (v/V)
    - A_corr665 = corrected absorbance at 665 nm (A_corr665 = A_corr750 subtracted from A_corr665)
    - d = cuvette pathlength (cm)
    - v = volume of extract (mL)
    - V = volume of sample filtered (mL)
  - The constant 13.9 represents the reciprocal of the specific absorption coefficient at 665 nm for chlorophyll a in the solvent used.

- Data Structure and Units
  - Data fields: Date (formatted as yyyy-mm-dd), Depth (m), Concentration (μg L^-1).

- Data Quality, Standards, and Metadata Considerations
  - Transparent remediation of turbidity and background correction via A_corr750.
  - Clear documentation of sample volume, extract volume, cuvette pathlength, and filtration volume supports reproducibility and recalculation if needed.
  - Data are organized in a simple, tidy structure enabling straightforward aggregation across dates and depths.

- Implications for Data Management and Use
  - Provides a time-series, depth-resolved chlorophyll a dataset suitable for tracking phytoplankton biomass trends in Elterwater.
  - Useful for integration with other lake-water quality datasets and for assessing seasonal or episodic blooms.
  - Potential limitations include the weekly-to-monthly cadence and focus on a single deepest point, which may affect representativeness for wider lake conditions.

- Access and Reuse Considerations
  - Core fields and procedural notes are captured for reproducibility and re-analysis.
  - Consider linking to broader metadata (sampling protocols, QA/QC records, and instrument calibration) to enhance discoverability and cross-study comparability.