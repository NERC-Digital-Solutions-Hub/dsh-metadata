# Supporting documentation for Biota_Stable_Element.csv

## Purpose and scope
- Defines the data dictionary for Biota_Stable_Element.csv, detailing every field, its meaning, units, and notes.
- Covers sample identification, sample context (RAP/type), descriptive sample information, collection date, and a comprehensive set of element concentration measurements.
- Includes replicate soil samples and notes on analyses used to estimate whole-organism concentrations.

## Data fields overview
- Identifiers and context
  - Sample_Code: unique sample identifier (no units).
  - RAP: sample type based on ICRP Reference Animals and Plants (RAPs).
  - Sample_Description: further explanation of the sample (units: cm).
  - Collection_Date: date of soil sample collection (format: dd-mmm-yyyy).
  - Notes: note on analyses or how samples were used; provided where required.
- Concentration measurements (fresh mass basis; units: mg/kg_fw)
  - I-127_mg_kg_fw, Li_mg_kg_fw, Be_mg_kg_fw, B_mg_kg_fw, Na_mg_kg_fw, Mg_mg_kg_fw, Al_mg_kg_fw, P_mg_kg_fw, S_mg_kg_fw, K_mg_kg_fw, Ca_mg_kg_fw, Ti_mg_kg_fw, V_mg_kg_fw, Cr_mg_kg_fw, Mn_mg_kg_fw, Fe_mg_kg_fw, Co_mg_kg_fw, Ni_mg_kg_fw, Cu_mg_kg_fw, Zn_mg_kg_fw, As_mg_kg_fw, Se_mg_kg_fw, Rb_mg_kg_fw, Sr_mg_kg_fw, Mo_mg_kg_fw, Ag_mg_kg_fw, Cd_mg_kg_fw, Cs_mg_kg_fw, Ba_mg_kg_fw, Tl_mg_kg_fw, Pb_mg_kg_fw, U_mg_kg_fw
- Detection limits
  - Each element has a corresponding Detection_Limit_<element>_mg_kg_fw field (and related Notes when applicable) to indicate the detection threshold for that sample.
- Data interpretation notes
  - Many fields include guidance such as: if a concentration is below detection limit, the corresponding Detection_Limit field is used and the primary concentration field may be blank.
  - Notes fields accompany analyses, including how samples were used in estimating whole-organism concentration.

## Units, formats, and conventions
- Concentrations: milligrams per kilogram of fresh mass (mg/kg_fw).
- Sample_Description: centimetres (cm).
- Collection_Date: format is day-month-year with three-letter month (dd-mmm-yyyy).
- Replicate samples: some samples (e.g., RCN119, RCN120, RCN121) are flagged as replicates in Sample_Description.

## Metadata, data quality, and governance aspects
- Emphasizes the use of metadata to verify data suitability and provenance.
- Provides explicit fields for detection limits to enable proper handling of non-detects.
- Includes a dedicated Notes field for contextual information about analyses and data usage.
- Supports data sharing and transparency by documenting how analyses contribute to estimating concentrations in whole organisms.

## Relevance to monitoring frameworks
- Delineates a structured, standards-based data dictionary that supports:
  - Identification of environmental health measures through detailed biota element concentrations.
  - Clear data provenance and quality control through explicit metadata and detection-limit information.
  - Public dissemination and governance through clearly defined fields, units, and notes.
- Facilitates comparability across datasets by standardizing measurement units, formats, and interpretation of non-detects.

## Practical implications and considerations
- Users must interpret non-detects via the corresponding Detection_Limit fields and notes.
- Replicate samples are identified and distinguished within the metadata.
- The dataset requires careful metadata management to ensure all analyses and samplings are properly documented for policy evaluation and future decision-making.