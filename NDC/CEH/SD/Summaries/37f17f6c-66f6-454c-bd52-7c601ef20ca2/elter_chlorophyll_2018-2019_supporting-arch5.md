# Elter_chlorophyll_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of chlorophyll a collected from May 2018 to December 2019.
- Sampling location: deepest point of Elterwater inner basin (latitude 54.4287, longitude -3.0350).
- Data intended to quantify chlorophyll a concentration in surface-to-near-surface waters via filtered water extracts.

## Sampling and Analytical Methods
- Water samples of 500 mL collected at depths of 0.5, 1, 2, 3, 4, 5, and 6 meters.
- Frequency: weekly to monthly during the study period.
- Filtration: samples filtered immediately after collection through GF/C filter paper (5.5 cm diameter); filters frozen after filtration.
- Analysis window: samples analysed within one month of collection.
- Chlorophyll a extraction: heated methanol extraction.
- Spectrophotometric measurement:
  - 750 nm used to correct turbidity (A_corr750).
  - 665 nm used for the red absorbance maximum of chlorophyll a (A_corr665).
- Concentration calculation:
  - Chlorophyll a concentration = (13.9 × A_corr665 × (1/d)) × (v/V)
  - A_corr665 is corrected absorbance at 665 nm: A_corr665 − A_corr750.
  - d = cuvette pathlength (cm); V = volume of sample filtered (mL); v = volume of extract (mL).
  - 13.9 approximates the reciprocal of the specific absorption coefficient for chlorophyll a at 665 nm in the solvent used.

## Data Structure and Units
- Data columns: Date (YYYY-MM-DD), Depth (m), Concentration (μg L^-1).

## Provenance and Metadata
- Project/study focus: chlorophyll a profiling in Elterwater inner basin.
- Sampling coordinates provided for the deepest point in the basin.
- Method reference for analysis: described procedure including Talling (1974).
- Data file name: Elter_chlorophyll_2018-2019.txt.

## Quality Assurance and Handling
- Sample handling: immediate filtration, freezing of filters, and analysis within one month to preserve sample integrity.
- Method fidelity: explicit spectrophotometric wavelengths and correction steps to account for turbidity.
- Calculation formula clearly documented to enable reproducibility and re-calculation if needed.

## Sharing, Access, and Updates
- Data are organized as a time-series per depth with a clear data structure; suitable for uploading to data portals and catalogue holdings.
- Documentation provides methodological transparency to support reuse and replication.
- Updates would require maintaining versioned records of the same data along with any methodological clarifications or corrections.

## Governance Considerations for Data Stewards
- Ensure complete metadata accompanies the dataset: sampling location, dates, depths, volume, filter type, extraction solvent, and instrument settings.
- Preserve methodological provenance (Talling 1974 reference) and current calculation formula for concentration.
- Maintain data integrity by validating date formats, depth values, and unit consistency (μg L^-1 and m).
- Consider adding optional metadata fields for instrument model, filtration conditions, and any data gaps or outliers.
- Plan for data stewardship tasks: regular reviews, clear versioning, and timely updates if sampling protocols or locations change.

## Limitations and Usage Notes
- Spatial limitation: single sampling location (deepest point of Elterwater inner basin); may limit spatial representativeness.
- Temporal variability: weekly to monthly sampling cadence may miss short-term fluctuations.
- Data completeness: no explicit QA metrics beyond processing timeline; users may need to inspect raw logs for potential missing values.