# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Overview
- Dataset metadata for ICP-MS concentrations of multiple elements in deer tissue (fresh mass basis).
- Includes sampling details (site, date, tissue type), specimen identifiers, and UKCEH/CEH sample codes and descriptions.
- Records concentrations for a wide range of elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Some values are reported as less-than (<) detections or marked as "No data" for specific samples (notably Roe deer 4 thyroid for many elements).

## Key fields and what they represent
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Sample identifiers and descriptions
  - CEH_Sample_Codes
  - CEH_Sample_Description
- Data content
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM
  - Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM
  - Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM
  - Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM
  - As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM
  - Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM
  - Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data interpretation notes
  - "<" indicates concentration below the detection limit for that column
  - Some entries state "No data for Roe deer 4 thyroid" (missing data for that sample/tissue)

## Data quality and standardization
- Concentrations are provided on a mg/kg fresh mass (FM) basis.
- Uses UKCEH/CEH sample coding and descriptions to enable traceability.
- Some concentrations are reported as "<" values; others are missing entirely for particular samples (notably Roe deer 4 thyroid across multiple elements).
- Clear structure supports standardised comparison across sites and samples, with explicit metadata to support provenance and interpretation.

## Relevance for environmental monitoring
- Enables consistent reporting of elemental concentrations in deer tissue, contributing to environmental health assessments and ecological exposure monitoring.
- Facilitates cross-site and temporal comparisons when integrated with standardized formats and provenance data.
- Supports data sharing and portal deposition through standardized sample codes and descriptions.

## Key considerations and limitations
- Missing data for Roe deer 4 thyroid across many elements limits some comparative analyses for that specimen.
- The provided text includes some formatting irregularities and merged lines, indicating potential data extraction or transcription issues to be resolved before downstream analyses.
- Ensuring uniform application of “less than” values and detection limits is important for accurate interpretation of low-level exposures.