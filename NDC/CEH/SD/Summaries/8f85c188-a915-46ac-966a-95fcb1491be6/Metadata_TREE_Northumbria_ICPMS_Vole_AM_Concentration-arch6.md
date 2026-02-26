# TREE_Northumbria_ICPMS_Vole_AM_Concentration

- Overview
  - Dataset containing ICP-MS measured concentrations of multiple elements in vole ash mass (AM) from Northumbria, UK, prepared for UKCEH contexts.
  - Includes taxonomic names (Latin and Common), sampling site, date collected, UKCEH sample codes, and detailed sample preparation notes.
  - Concentrations are reported as mg/kg of ash mass for a wide panel of elements; some values are reported as "<" (below detection) values.
  - Contains a mass-related field (Fresh_Mass_Ash_Mass_Ratio) and a notes field describing vole preparation (e.g., “separate tissues were not prepared”).

- Key fields and structure
  - Taxonomy and identity
    - Latin_Species_Name
    - Common_Species_Name
  - Sampling and metadata
    - Site
    - Date_Sample_Collected
    - CEH_Sample_Codes
    - Sample_Details
    - CEH_Sample_Description
    - Notes
  - Sample mass relationship
    - Fresh_Mass_Ash_Mass_Ratio
  - Element concentrations (mg/kg_AM)
    - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM, P_mg_kg_AM, K_mg_kg_AM
    - Ti_mg_kg_AM, V_mg_kg_AM, Cr_mg_kg_AM, Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM, Cu_mg_kg_AM, Zn_mg_kg_AM
    - As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM, Sr_mg_kg_AM, Mo_mg_kg_AM
    - Ag_mg_kg_AM (paired columns: Ag_mg_kg_AM, 1 and Ag_mg_kg_AM, 2)
    - Cd_mg_kg_AM (paired: 1 and 2)
    - Cs_mg_kg_AM (paired: 1 and 2)
    - Ba_mg_kg_AM (paired: 1 and 2)
    - Tl_mg_kg_AM (paired: 1 and 2)
    - Pb_mg_kg_AM (paired: 1 and 2)
    - U_mg_kg_AM (paired: 1 and 2)
  - Notation and data issues
    - Some column descriptions appear mislabelled (e.g., “Ti_mg_kg_AM” description vs. element naming, and repeated “Concentration of Ca” text in several lines).
    - Some columns indicate laterality or dual-field structures (e.g., “1” and “2” suffixes for values per element).

- Measurements and units
  - All primary concentrations are in mg/kg of ash mass (AM), except where values are explicitly marked as less-than signs.
  - Some fields denote values as “<” to indicate below-detection concentrations.
  - Date and site are descriptive fields; date units are not specified in the header (n/a for date units).

- Data quality and caveats
  - Patchy and heterogeneous data formats across the wide range of elements.
  - Inconsistent or erroneous metadata descriptions require validation (e.g., some element descriptions repeated or mislabeled).
  - Handling of censoring (<) values will be needed during analysis (e.g., substitution or imputation strategies).
  - Some fields imply two-part value storage (indices 1 and 2) which should be harmonized before analysis.

- Potential data preparation steps
  - Validate and harmonize column descriptions, especially mislabelled ones.
  - Normalize element concentration columns, consolidating paired fields (1/2) into single numeric representations as appropriate.
  - Implement handling rules for "<" values, documenting detection limits and substitution strategy.
  - Standardize date formats and ensure site metadata aligns with sampling metadata.
  - Create a data dictionary documenting each column, its unit (mg/kg_AM), and any caveats.

- Suggested data products and analyses for end users
  - Dashboards or pivot tables to compare concentrations by species, site, and collection date.
  - Summary statistics by element across all samples or by site/species.
  - Self-serve capability to filter by detection status (above/below detection) and by mass-related ratio.
  - Visualizations of temporal or spatial trends in key elements (e.g., essential vs. trace metals).
  - Exportable tables for downstream ecological or toxicological analyses.

- Relevance to data support aims
  - Demonstrates end-to-end data support: understanding the ask (multielement concentration dataset linked to vole samples), data discovery (taxonomy, site, date, codes), data cleaning needs (inconsistent metadata and censored values), and data product creation (element concentration tables and dashboards).
  - Highlights practical challenges in multi-source, multi-element, patchy datasets common in environmental ecology.