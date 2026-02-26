# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

## Overview
- This document provides field-by-field explanations for a dataset of vegetal transfer parameters (Fv) for stable elements in olive oil and wine.
- It defines sample-level metadata and per-element transfer factors, including associated uncertainty and detection-limit fields.
- Elements covered include Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th, with multiple sub-fields for some (e.g., P_Fv, Pb_Fv, U_Fv, Th_Fv).

## Key Data Elements
- Sample-level metadata
  - Sample_Code: unique identifier
  - Sample_Type: general description of the sample (foodstuff group)
  - Location: collection site name
  - Sample_Description: part of the plant analyzed (e.g., whole plant vs. specific tissue)
  - Collection_Date: date of sampling (dd-mm-yyyy)
- Per-element transfer factors (Fv) and quality indicators
  - Cs_Fv, Sr_Fv, K_Fv, Na_Fv, Ca_Fv, Mg_Fv, U_Fv, Th_Fv: transfer value for each element
  - Unc_<Element>_Fv: uncertainty of the corresponding Fv
  - Detection_Limit_<Element>_Fv: detection limit for the corresponding Fv
  - For P, Pb, U, Th, multiple sub-fields (1, 2, 3) indicate different measurements or contexts; each has its own Fv, Unc_Fv, and Detection_Limit_Fv
- Matrix context and units
  - Notes indicate matrices as olive oil and wine
  - Fv units described as unitless or kg dry matter per L, depending on element and context
  - Some fields specify “Where blank, then below detection limit,” indicating non-detects are represented visually in blanks

## Data Quality and Metadata Considerations
- Metadata completeness is variable; missing values (blanks) may denote non-detects or unknowns
- Some fields require confirmation from originators to verify data and fill gaps
- Transformation of data formats and standardization of units may be needed for cross-dataset comparability
- Uncertainty columns support assessment of reliability and comparability of transfer factors
- Public sharing of underlying data is required but can be a barrier in practice

## Governance and Monitoring Framework Implications
- Illustrates the importance of robust data governance: standardized metadata, clear measurement methods, and up-to-date datasets
- Highlights trade-offs between data openness and practical data-sharing barriers
- Demonstrates how detailed transfer factors with uncertainties and detection limits can inform environmental health monitoring and policy evaluation across food matrices

## Practical Guidance for Authors of Monitoring Frameworks
- Provide comprehensive metadata templates covering sample context, collection date, and matrix
- Include for each relevant element: Fv, Unc_Fv, and Detection_Limit_Fv, with clear handling of non-detects
- Accommodate multiple sub-entries per element (e.g., P_Fv_1, P_Fv_2, P_Fv_3) in data models
- Ensure governance practices for data storage, sharing, and ongoing quality assurance to support transparent decision-making