# Elter_chlorophyll_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of chlorophyll a collected from May 2018 to December 2019.
- Location: deepest point of Elterwater inner basin (Lat 54.4287, Long -3.0350).

## Sampling details
- Water samples: 500 mL per sample.
- Depths sampled: 0.5, 1, 2, 3, 4, 5, and 6 m.
- Frequency: weekly to monthly throughout the study period.

## Sample processing and analysis
- Filter: 5.5 cm GF/C filter paper.
- Post-collection handling: filter papers frozen; analysis within one month.
- Chlorophyll a extraction: heated methanol.
- Instrumentation: spectrophotometer.

## Measurement and calculation
- Wavelengths: 750 nm (background turbidity) and 665 nm (chlorophyll a).
- Corrected absorbance: A_corr665 corrected for turbidity by subtracting A_corr750.
- Concentration formula: Chlorophyll a concentration = (13.9 * A_corr665 * (1/d)) * (v/V)
  - 13.9 = reciprocal of the specific absorption coefficient at 665 nm for chlorophyll a in this solvent.
  - d = cuvette pathlength (cm).
  - v = volume of extract (mL).
  - V = volume of sample filtered (mL).
- Units: μg L^-1.

## Data structure
- Columns: Date (yyyy-mm-dd), Depth (m), Concentration (μg L^-1).

## Temporal and spatial coverage
- Timeframe: May 2018 – December 2019.
- Spatial focus: deepest point in Elterwater inner basin; single-site time-series by depth.

## Documentation and provenance
- Method reference: Talling (1974).
- Coordinates provided for sampling location.

## Data quality and interpretation (Data Support considerations)
- Variable sampling frequency (weekly to monthly) may affect continuity.
- Single-site, depth-resolved time series; limited spatial generalization.
- Processing involves chemical extraction and spectrophotometry; potential batch effects if multiple runs occur.
- Consider capturing QA details (calibration, blanks, detection limits) if available for robust analysis.

## Potential uses
- Time-series analysis of chlorophyll a by depth.
- Dashboards or pivot-table views for self-serve data exploration.
- Compare seasonal and depth-specific chlorophyll dynamics within Elterwater.