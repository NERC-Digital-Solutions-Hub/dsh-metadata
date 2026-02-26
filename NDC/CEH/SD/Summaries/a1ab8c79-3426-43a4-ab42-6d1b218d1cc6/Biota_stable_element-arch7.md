# Supporting documentation for Biota_Stable_Element.csv

## Overview
- This document describes the schema and metadata for Biota_Stable_Element.csv, a soil sample dataset containing unique sample identifiers, sample type, descriptive notes, collection date, and concentrations of numerous elements on a fresh mass basis.
- It follows ICRP RAP (Reference Animals and Plants) classifications for sample type (RAP) and includes replication notes for certain soil samples (RCN119, 120, and 121).

## Schema and key fields
- Sample_Code: unique sample identifier.
- RAP: sample type based on International Commission on Radiological Protection (ICRP) RAPs.
- Sample_Description: additional explanation of the sample; units specified as cm for length-related notes. Notes indicate some replicate soils (RCN119, 120, 121).
- Collection_Date: date of soil sample collection; format is dd-mmm-yyyy.
- Element concentration fields (mg_kg_fw): for each element, concentration on a fresh mass basis.
  - Examples include I-127_mg_kg_fw, Li_mg_kg_fw, Be_mg_kg_fw, B_mg_kg_fw, Na_mg_kg_fw, Mg_mg_kg_fw, Al_mg_kg_fw, P_mg_kg_fw, S_mg_kg_fw, K_mg_kg_fw, Ca_mg_kg_fw, Ti_mg_kg_fw, V_mg_kg_fw, Cr_mg_kg_fw, Mn_mg_kg_fw, Fe_mg_kg_fw, Co_mg_kg_fw, Ni_mg_kg_fw, Cu_mg_kg_fw, Zn_mg_kg_fw, As_mg_kg_fw, Se_mg_kg_fw, Rb_mg_kg_fw, Sr_mg_kg_fw, Mo_mg_kg_fw, Ag_mg_kg_fw, Cd_mg_kg_fw, Cs_mg_kg_fw, Ba_mg_kg_fw, Tl_mg_kg_fw, Pb_mg_kg_fw, U_mg_kg_fw.
- Detection_Limit_<element>_mg_kg_fw fields: corresponding detection limits for each element on a fresh mass basis, with the same element suffix order as the concentration fields.
- Notes (associated with samples): information on analyses or how samples were used in estimating whole-organism concentrations; value often n/a or provided where required.
- Units: all concentration fields use milligrams per kilogram (mg/kg_fw); Sample_Description uses centimetres for descriptive measurements as noted.

## Data semantics and handling of non-detects
- Non-detects are indicated by blanks in the concentration fields.
- Detection limits are provided in the corresponding Detection_Limit_<element>_mg_kg_fw fields to assist interpretation of non-detects.
- In many column descriptions, blanks in concentration fields imply the concentration was below the stated detection limit (as described in the adjacent detection-limit field). The exact wording varies slightly by element but follows this general rule.
- Replicate soil samples are explicitly noted in Sample_Description for specific samples (e.g., RCN119, 120, 121).

## Sample and RAP details
- RAP: Provides context for the sample type according to ICRP RAP classifications.
- Sample_Description: may include replication notes (e.g., replicates) and descriptive context; unit for descriptive measurements is centimetres.
- Collection_Date: standardized date format to enable temporal analyses and mapping of sampling events.

## Practical considerations for GIS use
- This dataset supports map-based visualization of soil element concentrations, with clear unit definitions and detection-limit semantics essential for accurate symbolization (e.g., handling of non-detects).
- For GIS workflows, consider:
  - Converting non-detects to a consistent proxy value or using detection limits to indicate censored data in maps.
  - Aligning replication notes to assess uncertainty or to create confidence ribbons for mapped values.
  - Linking RAP classifications to thematic layers representing sampling contexts or land-use categories.
  - Ensuring date fields are parsed correctly for time-enabled mapping or temporal analyses.
- Data quality and standardization considerations:
  - Data may originate from multiple sources with varying standards; align units and metadata consistently.
  - Large or complex datasets require cleaning and validation, particularly around detection-limit interpretation and replicates.