# Supporting documentation for Sample_list.csv

## Overview
- This document provides a data dictionary for Sample_list.csv, detailing each field’s purpose, the expected units, and any notes.
- It is intended to support GIS workflows by clarifying how sample attributes map to spatial data and further analysis.

## Field definitions (explanation, units, notes)

- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: .

- RAP
  - Explanation: ICRP Reference Animals and Plant (RAP) into which the sampled species can be attributed.
  - Units: n/a
  - Notes: .

- Sample_Description
  - Explanation: Part of the organism analysed (e.g., where the whole organism was divided and analysed separately).
  - Units: n/a
  - Notes: .

- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mmm-yy
  - Notes: .

- Dry/Fresh_Ratio
  - Explanation: Dry to fresh weight ratio.
  - Units: unitless
  - Notes: .

- Coordinates_of_the_Sample
  - Explanation: Grid reference of sampling location.
  - Units: decimal degrees and minutes
  - Notes: .

- Sample_Association
  - Explanation: Unique sample identifier of soil which was sampled at the same site.
  - Units: n/a
  - Notes: .

- Notes
  - Explanation: Additional comments (where applicable).
  - Units: n/a
  - Notes: .

## GIS considerations
- Coordinates_of_the_Sample enables spatial plotting of samples; ensure coordinates are in a consistent coordinate reference system (CRS) for mapping.
- The field includes grid references and specifies coordinates in decimal degrees and minutes, so standardize to a single format/CRS before integration.
- Sample_Association can be used to group samples sampled at the same location for aggregation or site-level analyses.
- RAP provides a categorical attribute for thematic mapping by species or biological reference groups.

## Data quality and workflow implications
- Data may come from multiple sources; plan for data cleaning and standardization, especially for dates and coordinate formats.
- Check for completeness in essential fields (Sample_Code, Coordinates_of_the_Sample, Collection_Date) to enable reliable GIS analysis.
- Ensure consistency between RAP classifications and sample descriptions during data validation.
- When integrating with other datasets, align resolutions and units, and document any transformations applied to coordinates or dates.