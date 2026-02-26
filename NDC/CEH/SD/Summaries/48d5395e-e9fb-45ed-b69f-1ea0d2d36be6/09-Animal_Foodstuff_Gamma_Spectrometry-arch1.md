# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Overview
- Describes the column definitions and metadata for a dataset of gamma spectrometry measurements on animal foodstuff samples.
- Captures sample identity, description, collection details, and radionuclide activity concentrations with uncertainties and detection limits.
- Radionuclides included: Ra-226, Cs-137, Ra-228, and K-40, with measurements on a fresh mass basis (Bq/kg_fm) or milk-specific basis (Bq/L for certain entries).
- Detection limits calculated according to ISO 11929; blanks indicate concentrations below the detection limit.

## Data Structure
- Each row corresponds to a unique sample (Sample_Code) with associated metadata and measurements.
- Core fields:
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (e.g., foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analysed (e.g., whole organism vs. tissue).
  - Collection_Date: Date of sample collection (dd-mm-yyyy).
  - Sample_size: Amount analyzed (kg fresh matter or L for milk).
- Measurement fields for radionuclides are provided alongside uncertainties and detection limits:
  - Ra-226_Bq/kg_fm, Unc_Ra-226_Bq/kg_fm, Detection_Limit_Ra-226_B q/kg_fm
  - Cs-137_Bq/kg_fm, Unc_Cs-137_Bq/kg_fm, Detection_Limit_Cs-137_B q/kg_fm
  - Ra-228_Bq/kg_fm, Unc_Ra-228_Bq/kg_fm, Detection_Limit_Ra-228_B q/kg_fm
  - K-40_Bq/kg_fm, Unc_K-40_Bq/kg_fm, Detection_Limit_K-40_Bq/ kg_fm
- Notes field briefly explains measurement context (e.g., equilibrium relationships) or column-specific details.

## Key Variables and Measurements
- Sample identifiers and descriptors:
  - Sample_Type, Location, Sample_Description, Collection_Date, Sample_size
- Radionuclide activity concentrations (all on a fresh mass basis unless noted):
  - Ra-226_Bq/kg_fm
  - Cs-137_Bq/kg_fm
  - Ra-228_Bq/kg_fm
  - K-40_Bq/kg_fm
- Associated uncertainty fields:
  - Unc_Ra-226_Bq/kg_fm
  - Unc_Cs-137_Bq/kg_fm
  - Unc_Ra-228_Bq/kg_fm
  - Unc_K-40_Bq/kg_fm
- Detection limits:
  - Detection_Limit_Ra-226_B q/kg_fm
  - Detection_Limit_Cs-137_B q/kg_fm
  - Detection_Limit_Ra-228_B q/kg_fm
  - Detection_Limit_K-40_Bq/ kg_fm
- Equilibrium notes:
  - Ra-226 is stated to be in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is stated to be in equilibrium with Ac-228.
  - Cs-137 and K-40 entries include notes about detection limits or blanks; Cs-137 notes indicate blanks mean below detection limit.

## Detection Limits and Censoring
- Detection limits are specified per radionuclide and per sample basis (ISO 11929 method).
- If a concentration value is blank, it indicates the concentration was below the detection limit.
- Uncertainties accompany measured concentrations; for censored data (below DL), uncertainties may be absent or not meaningful.

## Equilibrium Considerations
- Ra-226 is interpreted in equilibrium with its progeny Pb-214 and Bi-214 for the dataset.
- Ra-228 is interpreted in equilibrium with Ac-228.
- These relationships can influence interpretation of Ra-226 and Ra-228 measurements and any derived activity in the decay chain.

## Data Quality, Provenance, and Usage
- Metadata supports data cleaning, transformation, and provenance tracking (e.g., units, collection dates, sample descriptions).
- Units:
  - Primary radionuclide activities: Bq/kg_fm (fresh mass basis).
  - Milk-specific measurements: Bq/L where indicated.
- Useful for analyses comparing radionuclide burdens across sample types, locations, or collection periods; also supports dose assessment and trend analysis when paired with metadata.
- Data may require handling of censored values (below DL) and careful treatment of equilibrium assumptions in modeling.

## Implications for Analysis
- Prepare to handle left-censored data due to detection limits.
- Consider modeling approaches that accommodate censored data (e.g., Tobit models) or substitution methods with DL.
- Use equilibrium notes to justify or inform interpretation of Ra-226 and Ra-228 values within decay chains.
- Ensure unit consistency across radionuclides (kg_fm vs L for milk) during aggregation or comparison.
- Validate data completeness for key fields (Sample_Code, Collection_Date, Sample_size) before analyses.

## Caveats and Data Gaps
- Some fields use non-uniform formatting or contain typographical inconsistencies (e.g., spacing in field names for detection limits).
- Blank entries denote concentrations below detection limits but may limit precise quantitative conclusions for those samples.
- Detailed context about sample types, locations, and collection methods beyond what's specified in this documentation may be necessary for deeper interpretation.