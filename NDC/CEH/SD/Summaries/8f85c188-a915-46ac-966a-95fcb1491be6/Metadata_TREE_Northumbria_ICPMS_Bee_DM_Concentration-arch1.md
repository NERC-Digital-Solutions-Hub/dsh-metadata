# TREE_Northumbria_ICPMS_Bee_DM_Concentration

## Overview
- Dataset of ICP-MS measured concentrations of multiple elements in bee samples from Northumbria.
- Concentrations reported as milligrams per kilogram dry mass (mg/kg DM).
- Includes both the elemental measurements and rich sample metadata (species names, site, date, sample codes, and preparation details).

## Data schema and key fields
- Species identifiers:
  - Latin_Species_Name, Common_Species_Name
- Sampling and site information:
  - Site
  - Date_Samples_Collected
- Sample references and descriptions:
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
- Concentration variables (elements): I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Each element has a corresponding _mg_kg_DM value and explanation
  - Units for all listed elements: mg/kg DM
  - Some columns include less-than indicators (e.g., <Be, <Se, <U) to denote censored concentration values
- Data semantics:
  - Latin_Species_Name and Common_Species_Name provide species context
  - < marker values are used to identify concentration given in the corresponding column (e.g., Be_mg_kg_DM)

## Concentration measurements
- I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Some elements have designated censoring (<) values (e.g., <Be, <Se, <U) indicating concentrations below a reporting threshold

## Metadata and sample information
- CEH_Sample_Codes and CEH_Sample_Description provide UKCEH-specific identifiers and context
- Sample_Details include preparation and processing information

## Data quality and handling notes
- All concentration values are in mg/kg dry mass; some fields show n/a for certain metadata units
- Occurrence of typographical inconsistencies in the header (e.g., "A Concentration of l") suggests careful data cleaning may be needed
- Presence of "<" indicators requires appropriate handling (censoring) in analyses
- Data may rely on UKCEH sources and associated sample coding for traceability

## Potential analyses and questions
- Compare metal/element profiles across sites and sampling dates
- Examine correlations between elements (e.g., heavy metals) and site characteristics or bee species
- Develop predictive models of environmental exposure using multi-element fingerprints
- Assess temporal trends in key contaminants and their potential ecological implications

## Provenance and access
- Data references include UKCEH sample codes and descriptions, enabling traceability to the original sampling and analysis workflow
- Dataset structured for integration into data portals with metadata for discovery and reuse