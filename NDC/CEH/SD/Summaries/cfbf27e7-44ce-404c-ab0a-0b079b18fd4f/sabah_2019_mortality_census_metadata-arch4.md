# Collection methods

## Overview
- Data collection aimed at confirming alive/dead status of large trees (>30 cm stem diameter) in permanent field plots.
- For dead trees, record mode of death (mostly standing dead or uprooted/snapped).
- If uprooted or snapped, record direction of fall and the size of the canopy gap (small, medium, large).

## Data captured and units
- Alive_2019 status is recorded as a logical value (dead or alive).
- Direction_of_fall recorded as degrees from North.
- Gap_size recorded qualitatively as small, medium, or large.

## Sites and data structure
- Danum Valley
  - Entire contiguous 50 ha plot covered.
  - CSV fields: Tag (tree ID), Species, Dbh (stem diameter at breast height, ~1.3 m), Hom (measurement height when 1.3 m not possible), Alive_2019, Direction_of_fall, Gap_size, Notes.
- Sepilok Reserve
  - 9 unique 4 ha plots with hierarchical subplots: PlotID_4ha, Forest, PlotID_1ha, Subplot, Quadrat, TreeNo, Tno, IDNo2, Species, Diameter_1 (approx. 2010), Remarks_1, Diameter_2 (approx. 2015), Remarks_2, Remarks_2019, Mode_of_death, Direction_of_fall, GapSize.

## Data quality and governance
- No formal quality control applied; data are provided exactly as recorded in the field.
- Each site yields a single CSV file, with site-specific column naming.

## Data mapping and harmonization
- Column names and structure differ between sites (e.g., Danum vs. Sepilok), implying a need for mapping to a common schema if integrating datasets.

## Practical notes
- Data support mortality status, decay/decline history, and canopy impact analyses.
- Field-recorded descriptions (Remarks) can indicate additional context for diameter measurements and mortality status.

## Implications for data leadership
- Consider harmonizing schemas across sites to improve interoperability and discovery.
- Document metadata and data provenance to enable traceability from field collection to analyses.
- Implement minimal quality checks and standards for key fields (e.g., units, categorical codes) to improve reliability.
- Ensure clear data updates and versioning practices to track changes over time.
- Promote discoverability by maintaining consistent, well-described CSV files and an accessible data catalog for these datasets.