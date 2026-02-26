# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- Dataset of electrical resistance measurements for trees and soils in the Ankasa Conservation Area, southwestern Ghana.
- Includes measurements from 20 trees (various species) and one liana, collected in 2019 across wet and dry seasons.
- Part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics? (Grant NE/P001564/1).

## Data files and structure
- TreeResistanceGhana2019.csv
  - Columns include: Species_name, Field_ID, D (diameter at 130 cm), Resistance to ground at 1.4 m and 0.7 m (wet/dry), Trunk Resistance, Root Resistance, with descriptive notes for each.
- SoilResistanceGhana2019.csv
  - Columns include: Point, date, Hour, Hectare, Subplot, Landcover, Direction, Spike_spacing, Spike_depth, Resistance (Low_current, High_current), Resistivity, Moisture_1, Moisture_2, Moisture_3.
- Both files provide detailed field-collected measurements and unit descriptions.

## Data collection methods
- Tree resistance to ground
  - Measured with a Digital Earth Tester DET2/2 using a Fall of Potential approach around the tree.
  - Eight nails placed around the trunk at two heights (1.40 m and 0.70 m); multiple configurations (eight nails, four, two) to estimate intercept, stem, and root resistivity.
- Soil resistance
  - Measured with DET2/2 using a Wenner array in a line traverse configuration.
  - Four electrodes along a line; outer electrodes provide current, inner electrodes measure potential to derive soil resistivity.
  - Depth of electrode spikes = 1/20 of spike spacing; resistivity is an approximately depth-proxy value.
- Soil moisture
  - Measured with an SM150T sensor at 5 cm depth along measurement lines; recorded as volumetric moisture at 2 m and 3 m spacings (and possibly other spacings when time allowed).

## Metadata and data structure considerations
- Species names provided as binomial nomenclature; field codes for tree IDs.
- Measurements cover both wet and dry seasons in 2019.
- Clear documentation of measurement heights, configurations, and sensor methods to enable reproducibility.
- Units are specified for each field in the column descriptions.

## Quality control and provenance
- Quality control: field-recorded values only; no post-collection QC performed.
- Data attributed to multiple authors and linked to the NERC project on lightning and tree mortality.

## Governance, sharing, and reuse considerations for Data Stewards
- Data governance: rich methodological metadata supports reuse, cross-study comparability, and replication of the measurement approach.
- Sharing implications: dataset comprises two CSV files; ensure clear licensing, data access permissions, and persistent identifiers if distributing widely.
- Maintenance and updates: dataset appears to be a one-off 2019 field campaign; consider adding an accompanying data availability note, method calibration details, and versioning if updates occur.
- Data quality risk: absence of post-field QC suggests users should assess measurement uncertainty and consider documenting any data cleaning steps if performed later.
- Usability guidance: maintain and share the data dictionary and metadata to aid discoverability and interoperability with similar soil–root resistance datasets.