# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- This document describes the metadata/schema for a dataset of concentration ratios of multiple elements in Woodmice (whole body) relative to the dry mass of soil, collected in Northumbria under an ICPMS framework.
- Key purpose: enable traceable, reusable data about elemental accumulation in woodmice and its relationship to surrounding soil, with accompanying sampling context.

## Data Structure and Fields
- Sample identifiers and context
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
- Co-located soil context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description linking the soil sample used for ratio calculation
- Concentration ratio fields (elemental)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio
  - V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio
  - Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Ratio definition and special notations
  - All listed ratios are defined as Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil
  - Some entries include “<” markers (e.g., <I, <Be) indicating censored or upper-limit values
  - Certain elements have paired fields with indicators like “1” and “2” (e.g., V_Concentration_Ratio, 1 = n/a; V_Concentration_Ratio, 2 = V Concentration Ratio …), suggesting alternative measurements or data layers
- Data quality cues
  - Units are frequently listed as n/a
  - Explanations provide the calculation basis and any special markers

## Data Quality and Metadata
- Rich in contextual metadata (species, site, collection date, soil co-sample linkage, sample notes)
- Concentration ratios rely on precise pairing between woodmice tissue mass and soil mass; requires clear data lineage to soil samples
- Presence of censoring markers (<) and inconsistent unit reporting indicates the need for:
  - Standardized units and naming across all concentration ratio fields
  - Consistent handling of censored data
  - A complete data dictionary and lineage tracking to ensure reproducibility

## Governance, Architecture, and Use for Data Leaders
- Supports a holistic data system approach by tying biological samples to environmental context (soil) for each sampling event
- Enables data discovery and reuse through explicit field explanations and linkage between woodmice and soil data
- Highlights the importance of metadata quality, standardization, and discoverability to overcome fragmentation and variability across datasets
- Suggests governance actions:
  - Develop a standardized data dictionary for all concentration ratio fields
  - Implement consistent units, naming conventions, and handling of censored values
  - Ensure data lineage and versioning, especially linking woodmice data to the corresponding soil samples

## Key Challenges and Mitigations
- Fragmented data landscape and inconsistent field definitions
  - Mitigation: adopt uniform naming, units, and metadata standards; centralize a data dictionary
- Lack of clear units for many concentration ratio fields
  - Mitigation: define and enforce standard units or clearly document unit conventions
- Handling of censored (<) values
  - Mitigation: establish clear rules for reporting and analysis of censored data (e.g., upper bounds)
- Complex data lineage between woodmice samples and co-located soil samples
  - Mitigation: implement robust lineage metadata and referential integrity between woodmice records and soil context

## Practical Takeaways for Data Strategy
- This dataset exemplifies the need for end-to-end data governance around ecological concentration metrics, from specimen collection to environmental context
- To maximize value, pair this schema with:
  - A comprehensive data dictionary and data quality checks
  - Standardized units and handling of censored data
  - Clear data lineage connecting each woodmice record to its soil sample and collection event
- By addressing metadata quality and standardization, Data Leaders can improve data discoverability, interoperability, and actionable analytics across networks and partners.