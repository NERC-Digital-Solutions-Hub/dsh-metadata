# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Overview
- Metadata and definitions for a dataset of radionuclide activity concentrations in vegetal foodstuffs.
- Includes general sample information (identifier, type, location, description, collection date, sample size) and a set of isotope-specific measurements.

## Data structure and fields
- Sample_Code: unique sample identifier.
- Sample_Type: general description of the sample (foodstuff group).
- Location: name of the collection site.
- Sample_Description: part of the plant analyzed (e.g., specific plant tissue).
- Collection_Date: date of sample collection (dd-mm-yyyy).
- Sample_size: amount analyzed (kg fresh matter or L for olive oil and wine).
- Isotope measurement fields (each with Explanation, Units, Notes):
  - Ra-226_Bq/kg_dm
  - Unc_Ra-226_Bq/kg_dm
  - Detection_Limit_Ra-226_B q/kg_dm
  - Cs-137_Bq/kg_dm
  - Unc_Cs-137_Bq/kg_dm
  - Detection_Limit_Cs-137_B q/kg_dm
  - Ra-228_Bq/kg_dm
  - Unc_Ra-228_Bq/kg_dm
  - Detection_Limit_Ra-228_B q/kg_dm
  - K-40_Bq/kg_dm
  - Unc_K-40_Bq/kg_dm
  - Detection_Limit_K-40_Bq/ kg_dm
- Notes common to isotope fields indicate equilibrium with progeny (e.g., Pb-214/Bi-214 for Ra-226; Ac-228 for Ra-228) and that blanks mean concentrations below detection limits.

## Measurement specifics
- All activity concentrations are on a dry mass basis; for olive oil and wine, values may be reported per liter (Bq/L).
- Detection limits are calculated per ISO 11929 (where applicable) or as described for Cs-137.
- Equilibrium relationships with progeny isotopes are documented where relevant.

## Data quality considerations
- Non-detect values are represented as blanks in the concentration and sometimes related Unc_ or Detection_Limit_ fields.
- The documentation text contains some formatting irregularities and truncations (e.g., incomplete phrases in detection limit descriptions), which may require data cleaning during ingestion.
- Some fields reference two unit conventions (dry mass vs. Bq/L for certain matrices).

## Practical use and guidance
- Purpose: enable assessment of radionuclide content in vegetal foods and support data-driven decision making.
- Supports self-serve data exploration through dashboards or reports after harmonizing units (dry mass vs liquid basis) and handling non-detects via detection limits.
- Useful for quality assurance, comparisons across samples, and interpretation with explicit uncertainties (Unc_ columns) and equilibrium notes.

## End notes
- This document defines the metadata schema and measurement definitions for the 07-Vegetal_Foodstuff_Spectrometry dataset, ensuring traceability, correct interpretation, and consistent use of units, uncertainties, and detection limits.