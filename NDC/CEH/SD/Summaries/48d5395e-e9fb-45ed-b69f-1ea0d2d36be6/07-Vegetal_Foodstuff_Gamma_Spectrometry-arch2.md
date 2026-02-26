# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Overview
- Provides the metadata and measurement definitions for a dataset measuring radionuclide activity in vegetal foodstuffs.
- Aimed at enabling standardized data collection, validation, transformation, and downstream reporting for environmental monitoring.

## Data fields and metadata
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (e.g., foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the plant analyzed (e.g., specific plant portion).
- Collection_Date: Date of sample collection (format dd-mm-yyyy).
- Sample_Size: Amount of sample analyzed (units: kg fresh matter, or L for olive oil and wine).
- Radionuclide concentrations (measured on a dry mass basis unless specified):
  - Ra-226_Bq/kg_dm
  - Cs-137_Bq/kg_dm
  - Ra-228_Bq/kg_dm
  - K-40_Bq/kg_dm
- Uncertainties:
  - Unc_Ra-226_Bq/kg_dm
  - Unc_Cs-137_Bq/kg_dm
  - Unc_Ra-228_Bq/kg_dm
  - Unc_K-40_Bq/kg_dm
- Detection limits:
  - Detection_Limit_Ra-226_Bq/kg_dm
  - Detection_Limit_Cs-137_Bq/kg_dm
  - Detection_Limit_Ra-228_Bq/kg_dm
  - Detection_Limit_K-40_Bq/kg_dm
- Special notes on units for olive oil and wine:
  - For olive oil and wine, activity concentration is given in Bq/L instead of Bq/kg_dm where applicable.
- Equilibrium references:
  - Ra-226 is in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is in equilibrium with Ac-228.

## Measurement specifics
- Measurements follow ISO 11929 guidance for detection limits (where noted).
- Some fields indicate “where blank” meaning the concentration was below the detection limit.
- K-40, Ra-226, Cs-137, and Ra-228 are reported on a dry mass basis unless olive oil/wine contexts require L-based reporting.

## Data quality, standardization, and workflow
- Data are prepared to support quality assurance, cleaning, and transformation for standardized reporting.
- Clear metadata and units support cross-study comparability and reuse in environmental health assessments.
- Data are intended to be stored and uploaded to appropriate data portals, supporting long-term monitoring and traceability.

## Data provenance and use for monitoring
- Aligns with monitoring responsibilities to demonstrate environmental health and policy performance over time.
- Enables categorization and assessment of radiological measurements in vegetal foodstuffs against standards.
- Supports transparency by documenting detection limits, uncertainties, and equilibrium assumptions.

## Challenges and considerations
- Enhancing dataset value by integrating radionuclide data with other relevant environmental datasets.
- Ensuring accessible underlying data to support analyses and policy scrutiny.