# Supporting documentation for 12-Feedstuff_Stable.csv

## Overview
- Documentation for a dataset detailing stable element concentrations in feedstuff samples.
- Provides both measurement values and associated metadata to enable data exploration and reuse.
- Intended to support data users in understanding what is measured, where it comes from, and how to interpret results (including uncertainties and detection limits).

## Key data model and structure
- Sample identifiers and description:
  - Sample_Code: unique sample identifier.
  - Sample_Type: general description of the feedstuff group.
  - Location: location where the sample was collected.
  - Sample_Description: part of the organism analysed (e.g., tissue/section).
  - Collection_Date: date of sample collection (dd-mm-yyyy).
  - Sample_size: amount analyzed (g fresh matter).
- Analyte measurements (reported on a dry mass basis, mg/kg_dm):
  - Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm.
- Uncertainty and detection limits:
  - Unc_<element>_mg/kg_dm: combined uncertainty for the element concentration (mg/kg dry mass).
  - Detection_Limit_<element>_mg/kg_dm: detection limit for the element concentration (mg/kg dry mass).
- Data interpretation notes:
  - If a concentration field is blank, it indicates the concentration was below the detection limit for that element.
  - Some lines show formatting inconsistencies (e.g., Na and Unc_Na_mg/kg_dm) that should be treated as data quality notes during cleaning.

## Variables, units, and conventions
- Units:
  - All concentrations and uncertainties are in mg/kg_dm (dry mass basis).
  - Detection limits share the same units (mg/kg_dm).
- Handling below-detection values:
  - Blank values for concentration fields imply values below the detection limit.
  - Documentation explicitly notes this convention for interpretation.

## Data quality and preparation considerations
- The documentation includes formatting irregularities (typos and inconsistent suffixes for some elements), requiring cleaning during ingestion.
- Critical to consistently apply the below-detection rule across all analytes (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th).
- Ensure date parsing for Collection_Date and unit checks for Sample_size (g fresh matter) when integrating with other datasets.

## Practical guidance for data use
- Enables end users to self-serve data through dashboards or pivot reports by providing:
  - Transparent sample metadata (identifier, location, collection date, sample description, and size).
  - Quantitative results for multiple elements with uncertainties and detection limits.
- When combining with other datasets, align on Sample_Code and ensure consistent handling of below-detection values.
- For reporting, clearly indicate concentrations and upper-bound implications where values are below detection limits.