# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Overview
- Provides metadata and measurement fields for a gamma spectrometry dataset focused on animal foodstuffs.
- Defines identifiers, sample characteristics, collection details, and radiological measurements with associated uncertainties and detection limits.

## Key fields and purpose
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analysed (e.g., specific tissue or whole organism).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Sample_size: Amount analyzed; units typically kg fresh matter or L for milk.

## Measurement fields and meaning
- Ra-226_Bq/kg_fm: Activity concentration of Ra-226 on a fresh mass basis (Bq/kg_fm); notes indicate equilibrium with Pb-214 and Bi-214; blank values indicate concentrations below detection limit.
- Unc_Ra-226_Bq/kg_fm: Uncertainty of Ra-226 concentration (same unit and equilibrium context).
- Detection_Limit_Ra-226_Bq/kg_fm: Detection limit for Ra-226 (per ISO 11929); indicates non-detects when blank.
- Cs-137_Bq/kg_fm: Activity concentration of Cs-137 (Bq/kg_fm); blank indicates non-detects.
- Unc_Cs-137_Bq/kg_fm: Uncertainty for Cs-137 concentration.
- Detection_Limit_Cs-137_Bq/kg_fm: Detection limit for Cs-137 (per ISO 11929).
- Ra-228_Bq/kg_fm: Activity concentration of Ra-228 (Bq/kg_fm); notes indicate it was below detection limit or in equilibrium with Ac-228.
- Unc_Ra-228_Bq/kg_fm: Uncertainty for Ra-228 concentration.
- Detection_Limit_Ra-228_Bq/kg_fm: Detection limit for Ra-228 (per ISO 11929).
- K-40_Bq/kg_fm: Activity concentration of K-40 (Bq/kg_fm); notes indicate below detection limit when blank.
- Unc_K-40_Bq/kg_fm: Uncertainty for K-40 concentration.
- Detection_Limit_K-40_Bq/kg_fm: Detection limit for K-40 (per ISO 11929).

## Standards and interpretation notes
- Detection limits are calculated according to ISO 11929.
- Some concentration values are described as being in equilibrium with daughter nuclides (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).
- Blank values for measurements indicate concentrations below the detection limit.

## Data quality and governance considerations for Data Stewards
- Metadata clarity: Each field is defined with explanation, units, and notes to support discoverability and reuse.
- Standardization: Units (Bq/kg_fm, dd-mm-yyyy) and terminology should be consistently applied across datasets.
- Handling non-detects: Blank values indicate concentrations below detection limits; ensure consistent treatment in analyses and reporting.
- Provenance and auditability: Documentation links measurements to ISO 11929 detection limits and equilibrium assumptions for traceability.
- Interoperability: Be aware of potential formatting inconsistencies or typographical issues (e.g., spacing in unit names) that should be cleaned for interoperability across systems.
- Updating and sharing: Ensure that any embargoes, updates, or provenance changes are reflected in metadata and accessible through the designated data portals.