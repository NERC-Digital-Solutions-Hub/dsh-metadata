# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

## Overview
- Dataset documenting concentrations of various elements in vegetation samples collected for environmental monitoring.
- Uses a standardized dry-mass basis (mg/kg dry mass) to enable cross-site and temporal comparisons.
- Includes both taxonomic and sampling metadata, along with a comprehensive set of elemental concentration measurements.
- Prepared for QA, standardised analysis, and dissemination through appropriate data portals.

## Data structure and key fields
- Taxonomy
  - Latin_Species_Name (Latin name)
  - Common_Species_Name (common name)
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Identifier (UKCEH sample identifier)
  - CEH_Sample_Description (UKCEH sample description)
- Concentration measurements (all in mg/kg dry mass)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM
  - Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM
  - Se_mg_kg_DM (with special handling for two subfields Se_mg_kg_DM, 1 and Se_mg_kg_DM, 2)
  - Rb_mg_kg_DM, Sr_mg_kg_DM
  - Mo_mg_kg_DM (with Mo_mg_kg_DM, 1 and Mo_mg_kg_DM, 2 handling)
  - Ag_mg_kg_DM (with Ag_mg_kg_DM, 1 and 2 handling)
  - Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM
  - Tl_mg_kg_DM (with Tl_mg_kg_DM, 1 and 2 handling)
  - Pb_mg_kg_DM (with Pb_mg_kg_DM, 1 and 2 handling)
  - U_mg_kg_DM (with U_mg_kg_DM, 1 and 2 handling)
- Data markers and special notations
  - less-than values indicated by “<” prefixes (e.g., <I, <Li, etc.) to denote concentrations below detection limits
  - Some elements have dual columns or subfields (e.g., Se, Mo, Tl, Pb) to separately record detected value and a secondary value (often related to detection limits or qualifiers)

## Purpose and use
- Enables assessment of environmental health by comparing vegetation metal concentrations over time and across sites.
- Supports standardised data processing: verification, quality assurance, cleaning, and transformation.
- Facilitates outputs such as reports, maps, and charts to communicate findings.
- Datasets are stored and uploaded to appropriate data portals for access and reuse.

## Data quality and management
- Data originate from established sources (e.g., UKCEH) with clear identifiers and descriptions to support traceability.
- Concentrations are provided on a dry-mass basis to ensure comparability.
- Detection-limit indicators (< markers and dual subfields) are used where appropriate to reflect analytical constraints.

## Accessibility and challenges
- Emphasises enabling access to underlying data used to generate outputs.
- Aligns with the aim of increasing dataset value by integrating with related environmental data and ensuring standardized, reusable formats for policy assessment and monitoring.