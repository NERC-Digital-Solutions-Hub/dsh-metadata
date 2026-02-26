# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Overview
- Dataset presenting concentrations of numerous elements in total deer tissue (milligrams per fresh mass) from Northumbria ICPMS analyses.
- Includes taxonomic and sampling metadata: Latin and common species names, sampling site, date collected, UKCEH sample codes and descriptions, and tissue sampled.
- Contains both general tissue concentrations and, for some elements, thyroid-specific concentrations. Some samples have missing data, notably Roe deer thyroid data.

## Key Fields and Definitions
- Identifiers and context
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
  - Site: Sampling site
  - Date_Sample_Collected: Collection date
  - CEH_Sample_Codes: UKCEH sample codes
  - CEH_Sample_Description: UKCEH sample description
  - Tissue: Deer tissue sampled
- Concentration measurements (per element)
  - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Be_mg_per_tissue_FM, Na_mg_per_tissue_FM, Mg_mg_per_tissue_FM, Al_mg_per_tissue_FM, P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM, Ti_mg_per_tissue_FM, V_mg_per_tissue_FM, Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM, Ni_mg_per_tissue_FM, Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM, Rb_mg_per_tissue_FM, Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM, Cs_mg_per_tissue_FM, Ba_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM
  - For several elements, there is also a “thyroid” concentration column variant (e.g., P_mg_per_tissue_FM, thyroid)
- Data quality and formatting notes
  - Some columns use a less-than marker (e.g., <Be, <V) to indicate censored values
  - Specific note: No data for Roe deer 4 thyroid across many elements
  - Some formatting inconsistencies and typos present in the source (affecting readability but not core content)

## Data Quality and Governance Considerations
- Data provenance and discovery
  - CEH_Sample_Codes and CEH_Sample_Description support traceability to UKCEH sampling events and contexts.
- Units and normalization
  - All concentration values are mg per tissue in fresh mass (FM); ensure unit consistency across analyses and downstream integrations.
- Handling of censored data
  - "<" markers indicate concentrations below reporting threshold; establish a consistent approach for analysis (substitution vs. censoring) and document this in metadata.
- Gaps and anomalies
  - Notable absence of data for Roe deer 4 thyroid for many elements; treat as explicit missing data in analyses.
  - Some entries show formatting irregularities (e.g., stray symbols) that should be corrected during data curation for machine readability.
- Metadata completeness
  - Ensure complete metadata for all fields (definitions, units, data provenance, measurement methods) to support discoverability and reuse.
- Data sharing and updates
  - Align with governance: confirm sharing permissions, versioning, and update mechanisms for longitudinal datasets; ensure updated records are linked to existing CEH sample codes.

## Practical Action for Data Stewards
- Validate and clean field names and values to enforce consistent nomenclature (e.g., uniform element naming and consistent thyroid vs. tissue-specific columns).
- Explicitly document treatment of censored (<) values in the data dictionary and any chosen imputation or analysis approach.
- Address Roe deer 4 thyroid data gaps by labeling as missing and, if possible, flag for potential follow-up.
- Preserve and link to CEH sample codes and descriptions to maintain provenance; ensure data is uploaded to appropriate portals with rich metadata.
- Provide clear usage guidance for researchers, including unit specifications, tissue type context, and any caveats due to data gaps or formatting issues.