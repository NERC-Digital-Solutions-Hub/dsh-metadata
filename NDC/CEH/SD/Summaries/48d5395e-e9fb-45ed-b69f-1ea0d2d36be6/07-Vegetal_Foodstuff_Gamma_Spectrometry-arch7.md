# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Overview
- Metadata/documentation for a CSV of vegetal foodstuff spectrometry measurements.
- Contains sample identifiers, sample type, collection location, description of plant part analyzed, collection date, and sample size.
- Reports activity concentrations of radionuclides (Ra-226, Ra-228, Cs-137, K-40) on a dry-mass basis, with uncertainties and detection limits.
- Some values are specified for olive oil and wine (units may be Bq/L instead of Bq/kg_dm).
- Data references ISO 11929 for detection limits and notes on equilibrium among radionuclides.
- Blank values typically indicate concentrations below detection limits.

## Data fields and descriptions
- Sample_Code
  - Explanation: Unique sample identifier
  - Units: n/a
- Sample_Type
  - Explanation: General description of sample (e.g., foodstuff group)
  - Units: n/a
- Location
  - Explanation: Name of the location where the sample was collected
  - Units: n/a
- Sample_Description
  - Explanation: Part of the plant analysed (e.g., whole plant vs. specific tissue)
  - Units: n/a
- Collection_Date
  - Explanation: Date of sample collection
  - Units: dd-mm-yyyy
- Sample_size
  - Explanation: Amount of sample analyzed
  - Units: kg fresh matter or L for olive oil and wine
- Radionuclide concentrations and related fields (for each isotope)
  - Ra-226_Bq/kg_dm
    - Explanation: Activity concentration on a dry mass basis
    - Units: Bq per kg dry mass (or Bq/L for olive oil/wine)
    - Notes: In equilibrium with Pb-214 and Bi-214; blank = below detection limit
  - Unc_Ra-226_Bq/kg_dm
    - Explanation: Uncertainty of Ra-226 concentration
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: In equilibrium with Pb-214 and Bi-214
  - Detection_Limit_Ra-226_Bq/kg_dm
    - Explanation: Detection limit calculated per ISO 11929
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: In equilibrium with Pb-214 and Bi-214; blank = below detection limit
  - Cs-137_Bq/kg_dm
    - Explanation: Activity concentration of Cs-137
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank
  - Unc_Cs-137_Bq/kg_dm
    - Explanation: Uncertainty of Cs-137 concentration
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank
  - Detection_Limit_Cs-137_Bq/kg_dm
    - Explanation: Detection limit for Cs-137 calculated per ISO procedures
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank
  - Ra-228_Bq/kg_dm
    - Explanation: Activity concentration of Ra-228
    - Units: Bq per kg dry mass (or Bq/L) with ISO 11929 reference
    - Notes: Below detection limit if blank; in equilibrium with Ac-228
  - Unc_Ra-228_Bq/kg_dm
    - Explanation: Uncertainty of Ra-228 concentration
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank; in equilibrium with Ac-228
  - Detection_Limit_Ra-228_Bq/kg_dm
    - Explanation: Detection limit for Ra-228
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank; in equilibrium with Ac-228
  - K-40_Bq/kg_dm
    - Explanation: Activity concentration of K-40
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank; in equilibrium with other references
  - Unc_K-40_Bq/kg_dm
    - Explanation: Uncertainty of K-40 concentration
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank
  - Detection_Limit_K-40_Bq/kg_dm
    - Explanation: Detection limit for K-40
    - Units: Bq per kg dry mass (or Bq/L)
    - Notes: Below detection limit if blank

## Units and measurement context
- Primary unit: Bq/kg_dm (activity per kilogram of dry mass)
- For olive oil and wine: Bq/L may be used
- Collection date format: dd-mm-yyyy
- Detection limits and uncertainties follow ISO 11929 guidance
- Some fields indicate radionuclide equilibrium relationships (e.g., Ra-226 with Pb-214 and Bi-214; Ra-228 with Ac-228)

## GIS and data integration considerations
- Location field provides place names; to map spatially, coordinate data should be added or linked.
- Collection_Date enables temporal mapping or time-series analysis.
- Sample_Type and Sample_Description support filtering by plant part or product type (e.g., specific vegetables, olive oil, wine).
- Unit consistency is essential for mapping; convert to a common unit (preferably Bq/kg_dm) or annotate per-sample units (Bq/kg_dm vs Bq/L) to avoid misinterpretation.
- Handling non-detects: blanks indicate below detection limits; consider using detection limit values or a nondetect flag in GIS layers.
- Uncertainty fields enable visualization of measurement confidence (e.g., error bars, choropleth confidence shading).
- ISO 11929-aligned detection limits support standardized interpretation across samples.

## Practical guidance for map-based data products
- Visualize spatial distribution of Ra-226, Ra-228, Cs-137, and K-40 concentrations across locations.
- Use Collection_Date to display temporal trends or seasonal patterns if multiple dates exist.
- Filter by Sample_Type to compare different foodstuff groups or plant parts.
- Incorporate Unc_ fields to convey measurement precision alongside concentration values.
- Where units vary (Bq/kg_dm vs Bq/L), document unit per sample and convert when creating comparative maps.
- Flag non-detects clearly and consider representing them with capped color scales or separate nondetect layers.

## Data quality and consistency considerations
- Potential issues:
  - Missing values in concentration, uncertainty, or detection-limit fields.
  - Mixed units across samples (kg_dm vs L) requiring careful standardization for aggregation.
  - Variations in reporting of equilibrium relationships and ISO references.
- Recommendations:
  - Standardize to a single unit (preferably Bq/kg_dm) with clear per-sample unit annotation.
  - Add explicit coordinates for precise GIS mapping.
  - Implement a nondetect flag and store detection limits for all non-detect cases.
  - Include metadata on sampling protocol and data provenance to support reproducibility and cross-dataset comparisons.