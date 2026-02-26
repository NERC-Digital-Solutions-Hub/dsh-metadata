# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- A dataset of elemental concentrations in bee samples, measured as mg/kg fresh mass (FM).
- Includes taxonomic identifiers (Latin and Common species names), sampling site, and sampling metadata.
- Contains UKCEH sample codes and descriptions, sample details, and notes.
- Key matrix: multiple elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with corresponding concentrations.
- Some concentration fields use “<” notation to indicate detection limits (e.g., <Be, <Se, <U).

## Data Structure / Fields
- Taxonomy and identifications
  - Latin_Species_Name
  - Common_Species_Name
- Sampling information
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
  - Notes
- Elemental concentrations (mg/kg FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM (and <Be), Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM (and <Se), Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM (and <U)
- Data notes on formatting
  - “<” markers denote reported lower-than values (detection limits)
  - Some field descriptions contain typographical errors (e.g., Al_mg_kg_FM description mentions “A Concentration of l”)

## Key Considerations for Data Support
- Data completeness and consistency
  - Check for missing values across sites, dates, species, and concentration fields.
  - Validate and standardize site naming and date formats for cross-dataset joins.
- Detection limits handling
  - Properly interpret and visualize <Be, <Se, <U values (distinguish between actual zero, below detection, and reported value).
- Data quality and documentation
  - Address typographical inconsistencies in field descriptions (e.g., Al_mg_kg_FM note) to ensure clear understanding.
  - Verify crosswalks for CEH_Sample_Codes and CEH_Sample_Description for traceability.
- Data interrelationships
  - Potential to link species-level data with site-level metadata (location, environmental context).
  - Temporal analysis possible if multiple Date_Sample_Collected entries exist across sites/species.
  
## Suggested Analyses and Outputs (Data Support Perspective)
- Exploratory dashboards
  - Filter by species, site, date, and sample codes to compare elemental profiles.
  - Visualize concentration distributions by element across sites or species.
- Self-serve data products
  - Pivot tables summarizing median and range of each element by species or site.
  - Tables showing samples with elevated concentrations for environmental monitoring.
- Data prep steps for end users
  - Normalize or flag detection-limit values (e.g., treat <X as censored values).
  - Ensure numeric parsing of all mg/kg_FM fields; maintain a clear data dictionary for units and handling of “n/a” fields.
- Potential reporting and communication
  - Generate concise reports highlighting notable elemental patterns by species or sampling site, with notes on data quality and limits.

## Practical Usage Notes
- Units: All concentration fields are mg/kg fresh mass (FM) unless noted otherwise.
- Metadata rich: Includes taxonomic names, sampling site, collection date, and UKCEH coding for traceability.
- Cautions: Watch for data quality issues indicated by metadata typos and mixed field descriptions; confirm interpretation of detection-limit markers before analysis or public dissemination.