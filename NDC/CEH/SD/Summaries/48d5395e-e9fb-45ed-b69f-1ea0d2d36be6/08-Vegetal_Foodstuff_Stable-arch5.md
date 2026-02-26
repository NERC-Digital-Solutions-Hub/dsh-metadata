# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

## Overview
- This document serves as a data dictionary for the dataset 08-Vegetal_Foodstuff_Stable.csv.
- It defines field names, explanations, units, and notes for sample metadata and concentrations of various elements in vegetal foodstuffs.
- Fields cover both sample-level information and quantitative measurements (with detection limits and uncertainties).

## Data Model / Key Fields
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of sample (foodstuff group).
- Location: Name of the location where the sample was collected.
- Sample_Description: Part of the organism analyzed (e.g., sub-sample within a whole organism).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Sample_size: Amount of sample analyzed (units: g fresh matter or mL for olive oil and wine).
- Cs_mg/kg_dm: Concentration of stable Cesium on a dry mass basis.
- Unc_Cs_mg/kg_dm: Combined uncertainty of Cs concentration on a dry mass basis.
- Detection_Limit_Cs_mg/kg_dm: Detection limit for Cs on a dry mass basis.
- Sr_mg/kg_dm: Concentration of stable Strontium on a dry mass basis.
- Unc_Sr_mg/kg_dm: Combined uncertainty for Sr concentration.
- Detection_Limit_Sr_mg/kg_dm: Detection limit for Sr.
- K_mg/kg_dm: Concentration of stable Potassium on a dry mass basis.
- Unc_K_Mg/kg_dm: Combined uncertainty for K concentration.
- Detection_Limit_K_mg/kg_dm: Detection limit for K.
- Na_mg/kg_dm: Concentration of stable Sodium on a dry mass basis.
- Unc_Na_mg/kg_dm: Combined uncertainty for Na concentration.
- Detection_Limit_Na_mg/kg_dm: Detection limit for Na.
- Ca_mg/kg_dm: Concentration of stable Calcium on a dry mass basis.
- Unc_Ca_Mg/kg_dm: Combined uncertainty for Ca concentration.
- Detection_Limit_Ca_mg/kg_dm: Detection limit for Ca.
- Mg_mg/kg_dm: Concentration of stable Magnesium on a dry mass basis.
- Unc_Mg_mg/kg_dm: Combined uncertainty for Mg concentration.
- Detection_Limit_Mg_mg/kg_dm: Detection limit for Mg.
- P_mg/kg_dm: Concentration of stable Phosphorus on a dry mass basis.
- Unc_P_mg/kg_dm: Combined uncertainty for P concentration.
- Detection_Limit_P_mg/kg_dm: Detection limit for P.
- Pb_mg/kg_dm: Concentration of stable Lead on a dry mass basis.
- Unc_Pb_mg/kg_dm: Combined uncertainty for Pb concentration.
- Detection_Limit_Pb_mg/kg_dm: Detection limit for Pb.
- U_mg/kg_dm: Concentration of stable Uranium on a dry mass basis.
- Unc_U_mg/kg_dm: Combined uncertainty for U concentration.
- Detection_Limit_U_mg/kg_dm: Detection limit for U.
- Th_mg/kg_dm: Concentration of stable Thorium on a dry mass basis.
- Unc_Th_mg/kg_dm: Combined uncertainty for Th concentration.
- Detection_Limit_Th_mg/kg_dm: Detection limit for Th.

Notes:
- Units are described as mg per kg dry mass (dm) or mg per litre for olive oil and wine, with some fields indicating dry mass basis vs. liquid basis.
- Where a field is blank, the corresponding concentration is below the detection limit.
- Some field name entries include formatting anomalies (e.g., alternate numbering in Detection_Limit_K_mg/kg_dm), indicating potential editorial inconsistencies in the document.

## Data Quality and Metadata Details
- The document provides explicit explanations for each field, including the meaning of units and when non-detects are indicated.
- It uses standardized date formatting (dd-mm-yyyy) and specifies sample size conventions for different sample types (e.g., olive oil and wine).
- There are explicit instructions that blanks imply measurements below the detection limit across several concentration and uncertainty fields.
- There are formatting/consistency irregularities in a few field entries, which could affect automated parsing or interpretation.

## Governance and Sharing Considerations
- The dictionary supports data governance by standardizing field names, definitions, units, and signifiers for non-detects, aiding data discovery and reuse.
- Encourages consistent metadata capture to enable interoperability across datasets and portals.
- Highlights the need to document data provenance, updates, and any sharing limitations (e.g., embargoes or proprietary constraints) when publishing datasets.

## Challenges for Data Stewards
- Incomplete picture of user needs and priorities.
- Difficulty obtaining data from creators in a timely manner.
- Ensuring data creators meet standards, including metadata completeness.
- Managing data across many systems and formats, including non-interoperable ones.
- Handling large datasets and transfer challenges.
- Working with outdated databases that require bespoke solutions.

## Notes for Practitioners
- Use this metadata schema to ensure consistent data entry for both sample metadata and concentration measurements.
- Maintain clear documentation of detection limits and non-detect conventions to avoid misinterpretation.
- Consider addressing the anomalies in field naming to improve machine readability and interoperability.