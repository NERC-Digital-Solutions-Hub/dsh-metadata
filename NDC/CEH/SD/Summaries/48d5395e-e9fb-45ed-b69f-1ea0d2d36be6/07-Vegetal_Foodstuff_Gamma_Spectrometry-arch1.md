# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Overview
- Provides definitions and context for the dataset tracked in 07-Vegetal_Foodstuff_Spectrometry.csv.
- Focuses on radioactivity measurements (Bq units) of specific radionuclides in vegetal foodstuffs, reported on a dry mass basis or per liter for olive oil and wine.
- Describes sample metadata, collection details, sample sizes, and measurement-specific uncertainties and detection limits.
- Indicates equilibrium relationships with decay products where relevant (Pb-214/Bi-214 for Ra-226; Ac-228 for Ra-228).

## Data fields and conventions
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the plant analysed (e.g., specific tissue or whether the whole plant was analysed separately).
- Collection_Date: Date of sample collection (dd-mm-yyyy).
- Sample_size: Amount analyzed (kg fresh matter or L for olive oil and wine).
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 on a dry mass basis.
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 concentration (dry mass basis).
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929 method; dry mass basis; or per L for olive oil/wine).
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137 on a dry mass basis.
- Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration (dry mass basis).
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929; dry mass basis; or per L for olive oil/wine).
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228 on a dry mass basis.
- Unc_Ra-228_Bq/kg_dm: Uncertainty of Ra-228 concentration (dry mass basis).
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929; dry mass basis; or per L for olive oil/wine).
- K-40_Bq/kg_dm: Activity concentration of K-40 on a dry mass basis.
- Unc_K-40_Bq/kg_dm: Uncertainty of K-40 concentration (dry mass basis).
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929; dry mass basis; or per L for olive oil/wine).

## Units and interpretation
- Primary unit: Bq per kg dry mass (Bq/kg_dm) for Ra-226, Cs-137, Ra-228, and K-40.
- For olive oil and wine: Bq per liter (Bq/L) where noted.
- Sample_size uses kilograms (fresh matter) or liters (for olive oil and wine).
- Blank values indicate concentrations below the detection limit.

## Measurement context and assumptions
- Ra-226 and Ra-228 measurements are reported with their uncertainties and ISO 11929–based detection limits.
- Cs-137 measurements include corresponding uncertainties and detection limits.
- K-40 measurements include uncertainties and detection limits.
- Some isotopes are specified as being in equilibrium with their decay products (Ra-226 with Pb-214 and Bi-214; Ra-228 with Ac-228).

## Data quality and usage notes
- Detection limit fields help distinguish detected signals from non-detects (blank equals below detection limit).
- Metadata (Sample_Code, Sample_Type, Location, Collection_Date) supports traceability and reproducibility.
- ISO 11929 is the standard used for calculating detection limits.

## Practical applications
- Enables analysis of radionuclide activity concentrations in vegetal foodstuffs across samples.
- Supports comparisons by sample type, location, and collection date.
- Facilitates assessment of intake risks and regulatory compliance through reported activity concentrations and detection limits.
- Useful for data quality checks, including handling non-detects and ensuring consistency across isotopes and sample types.