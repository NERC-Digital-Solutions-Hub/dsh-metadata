# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- Dataset of ICP-MS-derived element concentrations in frog tissue or frogspawn from Northumbria (dry mass basis).
- Includes species identifiers, sampling metadata, and a broad suite of element concentrations measured in mg/kg dry mass.
- Captures both descriptive metadata (species names, site, collection date, sample codes/descriptions) and quantitative results for numerous elements.

## Dataset structure and key fields
- Taxonomy and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue (frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration measurements (mg/kg DM)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, B_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM
  - Al_mg_kg_DM, P_mg_kg_DM, S_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM
  - Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM
  - Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM
  - Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM
  - Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Notation and data types
  - Some columns include “<” prefixed values indicating less-than concentration values (e.g., <Be, <Al, <Ni, <Ag, <Se, <U).
  - Units are mg/kg for most elements; some fields use n/a for unit explanations.
  - DM denotes dry mass basis.

## Data quality and notation considerations
- Presence of less-than values requires special handling in analyses (censoring or substitution strategies).
- Data may include missing or irregular entries due to patchy data collection or varying data formats across sources.
- Descriptive fields (CEH_Sample_Codes/Description) facilitate linking to UKCEH records for provenance and quality checks.
- Clear distinction between fresh-to-dry mass ratios and dry-mass concentrations is essential to ensure comparability.

## Processing, transformation, and outputs
- Data Support activities recommended:
  - Validate and harmonize taxonomic names and site identifiers.
  - Clean and standardize units and handle < value entries appropriately.
  - Integrate sampling metadata with concentration data to enable multi-factor analyses (species x site x tissue x date).
  - Produce a clean, self-serve dataset (e.g., a pivot-ready table or dashboard-ready data model).
  - Generate a data dictionary and provenance notes, including how less-than values were treated.
- Potential outputs for end users
  - Dashboards comparing elemental profiles across species, sites, and tissues.
  - Summary statistics (means, medians, ranges) by site and species.
  - Visualizations of detected contaminants and potential environmental risk indicators.
  - Documentation describing data collection methods, QA steps, and any data transformations.

## Use cases and accessibility
- Environmental monitoring and contamination assessment in amphibian populations.
- Policy support for local councils or organisations monitoring ecological health.
- Public communication of contaminant levels in wildlife, with clear caveats on detection limits (less-than values).

## Challenges and recommendations for Data Support
- Time spent understanding the ask and mapping to the available fields (taxonomy, sampling metadata, and concentrations).
- Handling patchy data and multiple formats; plan data integration with cross-system access in mind.
- Communicating complex analytical implications (e.g., interpretation of < values) clearly to non-technical stakeholders.
- Promoting outputs for reuse; consider publishing early prototypes and seeking feedback to improve data products.
- Recommendations
  - Establish a standard workflow for integrating metadata with concentrations.
  - Create a consistent policy for reporting and visualizing censored (<) values.
  - Document data provenance and lineage to support traceability and reproducibility.