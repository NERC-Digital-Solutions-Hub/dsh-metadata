# Supporting documentation for 02-Sample_List.csv

## Overview
- Defines the metadata schema for the 02-Sample_List.csv dataset.
- Captures core attributes of each sample to support data integration, analysis, and reporting.
- Documents the types of analyses available (Gamma spectrometry; ICP-MS for stable elements).

## Fields and their metadata
- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: n/a
- Sample_Type
  - Explanation: General description of sample (e.g., foodstuff group).
  - Units: n/a
  - Notes: n/a
- Location
  - Explanation: Name of the sampling location.
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Further description of the sample (e.g., when organism/foodstuff was divided and analysed separately).
  - Units: n/a
  - Notes: n/a
- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mm-yyyy
  - Notes: n/a
- Coordinates_of_the_Sample
  - Explanation: Latitude, longitude coordinates of sampling location.
  - Units: decimal degrees and minutes
  - Notes: n/a
- Analysis
  - Explanation: Analyses carried out (Gamma = gamma spectrometry; Stable = stable elements by ICP-MS).
  - Units: n/a
  - Notes: n/a
- Notes
  - Explanation: Additional comments (where applicable).
  - Units: n/a
  - Notes: n/a

## Data quality and standardisation considerations
- Date format specified as dd-mm-yyyy for consistency.
- Coordinates are in decimal degrees and minutes (standardise across records).
- Units are largely n/a except for Collection_Date and Coordinates; ensure consistent interpretation across analyses.
- Several fields may be left as n/a in Notes or other columns, indicating optional data.

## How to use for analysis
- Use Sample_Code as a unique key to join with other datasets (e.g., results, provenance).
- Filter by Sample_Type, Location, or Collection_Date to build time- or location-specific analyses.
- Parse Analysis to distinguish datasets from Gamma spectrometry vs. ICP-MS (Stable elements) for modeling and correlation studies.
- Leverage Sample_Description and Notes to understand sub-sample partitioning and context for analyses.

## Data provenance and accessibility
- The document serves as metadata guidance for documenting samples and analyses.
- Emphasises structured description to aid discovery, reproducibility, and cross-dataset integration.