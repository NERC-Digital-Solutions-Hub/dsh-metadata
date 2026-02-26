# Palm Frond Decomposition Rates

- A dataset documenting decomposition rates of dried oil palm frond litter across three estates in Sumatra, Indonesia, collected between 2013 and 2017 as part of the BEFTA project.
- Purpose aligned with data stewardship: enable discoverability, reuse, and governance of environmental data with clear provenance and quality controls.

## Overview and scope

- Location: Pt Ivo Mas Tunggal estates (Ujung Tanjung, Kandista, Libo) in Riau Province, Sumatra.
- Experimental setup: 18 plots (50 x 50 m) established in 2013 as part of a larger vegetation management experiment; plots include mature/over-mature stands and replanted stands.
- Sampling regime: decomposition measured six times between 2013 and 2017 (with a reduced protocol in May 2016 during ENSO-related drought).
- Litterbags and treatments:
  - Three bag types to isolate effects of invertebrate size:
    - 0.1 mm mesh ( excludes all visible invertebrates)
    - 2 mm mesh ( excludes large invertebrates)
    - 0.1 mm mesh with four 1 cm holes (allows large invertebrates)
  - Each bag contains 4 g of dried palm frond litter.
  - 12 bags per sampling event (3 bag types x 4 bags) placed on soil under litter layer, replicated across 3 plots at 3 sampling positions.
  - Sampling times: 10, 30, 60, 90 days (with a May 2016 reduced protocol using two corners for 30 days).
- Observed variable: grams of litter remaining in each bag.

## Data structure and content

- Format: three separate CSV files in thin format (one observation per line).
  - PalmFrondDecompositionRates_2013_2015.csv (mature plantations, pre-ENSO period)
  - PalmFrondDecompositionRates_2016_2017.csv (mature plantations, during ENSO)
  - PalmFrondDecompositionRates_replants.csv (replanted stands)
- Key fields (selected):
  - Estate_abbrev, Description (estate name), Plot_no (three-character code, e.g., C01), Treatment (reduced, normal, enhanced), Period (discrete sampling periods), Position (compass heading from plot center), Date_set, Time_set, Date_coll, Time_coll, Bag_type, Grammes_remaining, dayrain (rainfall 24h prior to sampling, station-based), allnotes (field/entry observations), SAFE_distance (notes on BEFTA cores proximity; data here may be unsuitable for use), plus miscellaneous notes.
- Data provenance and funding:
  - BEFTA core plots (2013–2014) funded under NE/P00458X/1.
  - BEFTA core plots (2016–2017) funded by NERC.
  - Replanted stands (Libo estate) data funded by NERC.

## Quality control and data stewardship

- Quality checks:
  - Basic validation for impossible values (e.g., dates).
  - 50% of 2016–2017 data entry cross-checked against original field sheets; error rate < 1%; corrections recorded with dataset.
- Documentation and metadata:
  - Comprehensive field descriptions for each column (including data type and meaning).
  - Clear notes on data limitations (e.g., SAFE_distance cautions; exclosure-related data not intended for use in some rows).
- Data management:
  - Data stored as separate, well-labeled CSV files with periodization to distinguish pre-ENSO, during ENSO, and replanted stands.
  - Metadata includes plot, treatment, timing, and environmental context (e.g., rainfall).

## Usage considerations and caveats for data stewards

- Data limitations:
  - The SAFE_distance column contains notes indicating certain observations should probably not be used (related to BEFTA exclosures and potential confounds).
  - Some data reflect special conditions (e.g., ENSO drought period) that may affect decomposition rates and should be accounted for in analyses.
- Interoperability:
  - Thin-format CSVs with explicit column definitions support cleaning, integration, and reuse across platforms.
- Discoverability and sharing:
  - Data are organized by estate, plot, treatment, and period, enabling filter-based discovery and cross-study comparisons.
- Update and provenance:
  - Clear funding sources and replication ensure traceability; any updates should preserve original fields and add versioned notes for corrections.

## Practical notes for researchers and data managers

- Data can support analyses of decomposition rates across treatments, stand types (mature vs replanted), and time since litter introduction, with rainfall context captured per observation.
- When combining the datasets, align on core identifiers (Estate_abbrev, Plot_no, Treatment, Period, Bag_type) and account for the timepoints and sampling dates to ensure consistent time-series analysis.
- Exercise caution with SAFE_distance entries and potential exclosure-related data when interpreting results.