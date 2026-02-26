# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Overview
- Study location: three estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal: Ujung Tanjung, Kandista, Libo).
- Experimental setup: 18 plots established in 2013 within a 50 x 50 m area per plot.
- Plant material and stand status: mature/over-mature oil palm in Ujung Tanjung and Kandista; replanted plots in Libo in 2014.
- Measurement periods: granivory assessed once in 2014 (mature) and five times in 2016–2017 (both mature and replanted).
- Experimental units and procedure: ten shelled sunflower seeds on a paper disc, exposed for ~24 hours; tests conducted under four treatments (cage + grease, cage only, grease only, open) across three sampling positions per plot.
- Data purpose: quantify granivory under different microhabitats and management histories.

## Experimental design and sampling regime
- Plots and positions: 3 sampling positions per plot at 45°, 165°, and 285° from compass north.
- Treatments: 
  - remain_cage
  - remain_open
  - remain_cage_grease
  - remain_open_grease
- Sampling cadence:
  - 2014: data from mature stands (one observation per plot)
  - 2016–2017: data from mature and replanted stands (five observations per plot)
- Exclosures and context: ant poison exclosure experiments (2016–2017) with distance measurements (SAFE_distance) in certain records; rain data captured for the 24-hour exposure period.

## Data files and structure
- Three CSV data files:
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (mature stands)
  - SunflowerSeedPredationRates_replants.csv (replanted stands)
- Format: thin (one observation per line)
- Key columns (described below)

## Data fields and definitions
- Estate_abbrev: short estate code (KNDE for Kandista, UTNE for Ujung Tanjung, LIBE for Libo)
- Triplet: grouping of plots in sets of three
- Plot_no: three-character plot identifier (e.g., C01)
- Treatment: management status since Feb 2014 (reduced, normal, enhanced)
- Period: discrete sampling period identifier
- Position: compass heading where the seed disc intercepted the plot boundary
- Date_set / Time_set: date and time seeds were placed in the field
- Date_coll / Time_coll: date and time seeds remaining were recorded
- seedstreat: seed treatment category (remain_cage, remain_open, remain_cage_grease, remain_open_grease)
- seedsremaining: number of seeds remaining out of ten (decimal values possible)
- dayrain: rainfall over the 24 hours from 8am to 8am at the nearest station
- allnotes: field or data-entry observations and any changes during data checking
- SAFE_distance: distance metric used for BEFTA 2016–2017 exclosure data (only present in SunflowerSeedPredationRates_2016_2017.csv); values suggest records that should likely be excluded

## Data quality, provenance, and governance
- Quality checks: basic validation for implausible values; 50% of data entry cross-checked against original field sheets with an error rate <1%; any changes documented and retained with the dataset.
- Data provenance: funded under NE/P00458X/1; datasets comprise BEFTA core plots (2016–2017) and replanted plots.
- Documentation scope: includes field methods, unit definitions, and dataset structure to support reproducibility and cross-study comparability.

## Miscellaneous and notes for data governance
- The dataset includes coordinates and additional miscellaneous notes relevant to plotting and sampling schemes.
- Two datasets cover core BEFTA plots (2016–2017) and replanted plots; researchers should note potential differences in sampling intensity and stand history when integrating datasets.

## Considerations for data leadership and strategy
- Data discoverability and interoperability: three clearly named CSV files with consistent field definitions enable cross-site analyses; consider consolidating into a unified data catalog entry with explicit lineage.
- Metadata completeness: ensure consistent interpretation of Period, Position, and Treatment across files; standardize units and naming conventions (e.g., period intervals, plot identifiers) to facilitate cross-dataset analyses.
- Data quality management: maintain the <1% error rate evidence and extend data validation to automate integrity checks for future updates; clearly flag SAFE_distance-related records for exclusion where applicable.
- Usability and governance: document data usage constraints (exclosure influence, weather context) and provide guidance on filtering by maturity status, period, or treatment to support targeted analyses.