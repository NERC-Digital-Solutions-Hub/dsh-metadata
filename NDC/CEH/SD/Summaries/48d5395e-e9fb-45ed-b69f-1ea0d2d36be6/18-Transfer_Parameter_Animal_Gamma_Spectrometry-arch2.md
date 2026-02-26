# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

## Overview
- Supporting documentation for a dataset of gamma spectrometry transfer parameters related to animal samples.
- Defines field names, explanations, units, and data quality notes to enable standardised data capture, QA, and subsequent analysis.
- Intended to support environmental monitoring by ensuring consistent, reusable data suitable for integration and portal uploads.

## Data fields and definitions
- Sample_Code
  - Unique sample identifier.
  - Sample_Code is not associated with a unit (n/a) and has no notes.
- Sample_Type
  - Description: Soil.
  - Units: n/a.
  - Notes: n/a.
- Location
  - Name of the sampling location.
  - Units: n/a.
  - Notes: n/a.
- Sample_Description
  - Specifies part of the organism analysed (e.g., tissue/section) or how the whole organism was divided for analysis.
  - Units: n/a.
  - Notes: n/a.
- Collection_Date
  - Date when the sample was collected.
  - Units: dd-mm-yyyy.
  - Notes: n/a.
- Radionuclide transfer ratio (CR) values
  - Ra-226_CR: CR value for Ra-226.
  - Cs-137_CR: CR value for Cs-137.
  - Ra-228_CR: CR value for Ra-228.
  - K-40_CR: CR value for K-40.
  - Units: Unitless or kg dry matter per L for milk (context-dependent per radionuclide).
  - Notes: If blank or Not Determined, the CR value is below the detection limit.
- Unc_ fields (uncertainties)
  - Unc_Ra-226_CR, Unc_Cs-137_CR, Unc_Ra-228_CR, Unc_K-40_CR: uncertainties for the corresponding CR values.
  - Units: Unitless or kg dry matter per L for milk (context-dependent).
  - Notes: If blank, the CR value was below the detection limit.
- Detection_Limit_ fields
  - Detection_Limit_Ra-226_CR, Detection_Limit_Cs-137_CR, Detection_Limit_Ra-228_CR, Detection_Limit_K-40_CR: detection limits for the respective CR values.
  - Units: Unitless or kg dry matter per L for milk (context-dependent).
  - Notes: If blank, the CR value was above the detection limit.

## Measurements and interpretation
- CR values are the quantified measurements for each radionuclide’s transfer ratio or concentration parameter.
- Detection limits indicate the threshold below which values are not determinable.
- Blank or “Not Determined” entries correspond to measurements below the detection limit.
- Uncertainty fields provide a quantitative estimate of measurement precision when available; blanks imply detection-limit–level uncertainty or non-detection.

## Data quality and workflow implications
- Emphasises standardized data definitions to support QA, cleaning, and transformation into consistent outputs (e.g., reports, maps, charts).
- Facilitates storage and provisioning of underlying data to appropriate data portals, aligning with monitoring practices that value data reuse and cross-dataset integration.
- Supports environmental health assessment by enabling comparisons over time and integration with other data sources.

## Practical guidance for analysts
- Ensure Collection_Date adheres to dd-mm-yyyy format.
- Treat CR values as unitless or expressed per kg dry matter per L for milk, depending on context; verify unit convention for each radionuclide in downstream analyses.
- Use detection-limit fields to interpret non-detects (values left blank or marked as Not Determined indicate measurements below detection capability).
- Leverage the Sample_Description and Location fields to enable spatial and contextual analyses when integrating with other environmental datasets.

## Relevance to monitoring objectives
- Provides a standardised metadata framework for environmental monitoring data, enabling consistent reporting of radionuclide transfer in animal-related samples.
- Supports clear, comparable outputs for policy evaluation and health risk assessments over time.
- Aligns with the goal of increasing data value through interoperability and accessible underlying data.