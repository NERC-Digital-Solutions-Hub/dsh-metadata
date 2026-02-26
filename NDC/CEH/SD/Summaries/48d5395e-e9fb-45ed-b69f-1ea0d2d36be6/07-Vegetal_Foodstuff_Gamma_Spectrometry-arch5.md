# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Overview
- Describes metadata and measurement data for vegetal foodstuff spectrometry dataset.
- Contains sample metadata (Sample_Code, Sample_Type, Location, Sample_Description, Collection_Date, Sample_size) and radionuclide measurements for Ra-226, Ra-228, Cs-137, and K-40.
- Concentrations are on a dry mass basis (Bq/kg_dm); for olive oil and wine, units may be Bq/L.
- Collection date format: dd-mm-yyyy. Sample_size: kg fresh matter or L for olive oil and wine.
- Data quality indicators include uncertainties (Unc_*) and detection limits (Detection_Limit_*); blanks indicate concentrations below detection limits.
- Detection limits are calculated according to ISO 11929. Some notes indicate radioactive equilibrium conditions (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).

## Fields and data types
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of sample (foodstuff group).
- Location: Name of the collection location.
- Sample_Description: Part of the plant analysed (e.g., section of plant).
- Collection_Date: Date of sample collection (dd-mm-yyyy).
- Sample_size: Amount analyzed (kg fresh matter or L for olive oil and wine).
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 on a dry mass basis.
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 concentration.
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929).
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137 on a dry mass basis.
- Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration.
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929).
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228 on a dry mass basis.
- Unc_Ra-228_Bq/kg_dm: Uncertainty of Ra-228 concentration.
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929).
- K-40_Bq/kg_dm: Activity concentration of K-40 on a dry mass basis.
- Unc_K-40_Bq/kg_dm: Uncertainty of K-40 concentration.
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929).
- Notes: Additional remarks (e.g., equilibrium relations or detection-limit implications).

## Measurement details, normalization, and notes
- Nuclides reported on a dry mass basis; olive oil and wine may have conversions to Bq/L.
- Equilibrium context noted for Ra-226 (Pb-214 and Bi-214) and Ra-228 (Ac-228).
- Below-detection-limit values may be left blank; clearly indicates concentrations were not detected above ISO 11929 limits.
- Some field name inconsistencies or typographical issues exist (e.g., stray spaces in certain Detection_Limit field names); requires data curation to ensure consistent naming.

## Quality, provenance, and standards
- Detection limits computed per ISO 11929; ensures comparability across samples.
- Metadata supports reproducibility: sample description, collection date, location, and sample size documented.
- Clear indication of when data represent measurements above or below detection limits through presence/absence of values.
- Matrix-specific considerations documented (dry mass vs. liquid equivalents for olive oil and wine).

## Data governance and stewardship actions
- Ensure dataset is stored with complete metadata and versioned provenance.
- Validate unit consistency across records (Bq/kg_dm vs. Bq/L for certain matrices).
- Normalize and fix any field-name inconsistencies during curation.
- Publish and catalog data in appropriate portals; document processing steps and any transformations.
- Establish update and embargo procedures for new samples or revised measurements.
- Align dataset with user needs by maintaining clear definitions and notes on equilibrium and detection limits.

## Practical considerations for users
- Interpreting blanks: blank Detection_Limit fields imply values below detection capability.
- Be mindful of matrix effects: olive oil and wine may require Bq/L reporting, unlike other matrices.
- Use documented Collection_Date and Sample_size to contextualize activity concentrations.
- Reference ISO 11929 for detection-limit interpretation and reporting conventions.