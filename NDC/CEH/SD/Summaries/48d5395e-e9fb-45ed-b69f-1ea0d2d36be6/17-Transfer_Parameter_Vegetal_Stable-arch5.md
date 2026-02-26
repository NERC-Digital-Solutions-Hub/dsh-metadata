# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

## Overview
- Provides metadata and field definitions for the dataset 17-Transfer_Parameter_Vegetal_Stable.csv.
- Documents transfer factor values (Fv) for stable elements across samples, focusing on components such as Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th.
- Includes guidance on how to interpret and record each variable (explanation, units, notes).

## Dataset structure and key fields
- Core identifiers and context
  - Sample_Code: unique sample identifier.
  - Sample_Type: general description of the sample (foodstuff group).
  - Location: collection site name.
  - Sample_Description: part of the plant analyzed (e.g., specific tissue or part).
  - Collection_Date: date of sample collection (format dd-mm-yyyy).
- Transfer factor values (Fv) and quality metrics
  - Cs_Fv, Sr_Fv, K_Fv, Na_Fv, Ca_Fv, Mg_Fv, U_Fv, Th_Fv: Fv values for each element, with unit details.
  - P_Fv, Pb_Fv: Fv values with multi-part definitions (e.g., P_Fv, 1/2/3; Pb_Fv, 1/2/3) indicating variant components or scenarios.
  - Unc_Cs_Fv, Unc_Sr_Fv, Unc_K_Fv, Unc_Na_Fv, Unc_Ca_Fv, Unc_Mg_Fv, Unc_P_Fv, Unc_Pb_Fv, Unc_U_Fv, Unc_Th_Fv: associated uncertainties (unitless or specific to units used for olive oil and wine).
  - Detection_Limit_Cs_Fv, Detection_Limit_Sr_Fv, Detection_Limit_K_Fv, Detection_Limit_Na_Fv, Detection_Limit_Ca_Fv, Detection_Limit_Mg_Fv, Detection_Limit_P_Fv, Detection_Limit_Pb_Fv, Detection_Limit_U_Fv, Detection_Limit_Th_Fv: detection limits for each Fv value.
  - Notes: indicates special cases, e.g., values below detection limit or blanks.
- Special conventions
  - Blank Fv-related fields imply values below the detection limit.
  - For some elements, units are described as “Unitless or kg dry matter per L for olive oil and wine,” signaling dual contexts or conditional unit use.
  - Collection_Date format and metadata consistency are emphasized to ensure harmonized records across datasets.

## Data quality and metadata considerations
- Clear documentation of each field’s meaning, units, and handling of non-detects or missing data.
- Emphasis on capturing uncertainty and detection limits to support traceability and reliability of Fv values.
- Consistency in sample context (Sample_Type, Location, Sample_Description) to enable comparison across datasets and studies.
- Handling of multi-part fields (e.g., P_Fv, Pb_Fv) with explicit subcomponents to avoid ambiguity.

## Data governance and stewardship implications
- Metadata completeness is essential for discoverability and reuse by data users with diverse needs.
- Standardized units and clearly defined handling of non-detects support interoperability across systems and portals.
- Documentation enables accurate data provenance, enabling update workflows and traceability when datasets are revised or extended.
- The dataset aligns with governance practices that help reveal data availability, limitations, and potential embargoes or proprietary concerns.

## Practical implications for Data Stewards
- Ensure the dataset is uploaded with complete metadata mappings (Explanation, Units, Notes) for all fields.
- Validate that non-detects are consistently represented as blank fields and interpreted as below detection limit.
- Maintain consistency of date formats and site/location descriptors to support robust data discovery.
- Preserve the multi-part Fv fields (P_Fv, Pb_Fv, etc.) with their respective subcomponents and corresponding Unc and Detection_Limit entries.
- Plan for regular reviews to accommodate updates, corrections, or expansions (e.g., adding additional elements or contexts beyond the current list).
- Ensure alignment with portal-specific metadata schemas and controlled vocabularies to facilitate cross-dataset searches and integration.