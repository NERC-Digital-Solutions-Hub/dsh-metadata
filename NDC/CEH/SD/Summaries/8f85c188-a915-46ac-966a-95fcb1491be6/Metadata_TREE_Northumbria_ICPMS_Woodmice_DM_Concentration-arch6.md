# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- Dataset describing concentrations of multiple elements in wood mice tissues, measured by ICP-MS on a dry-mass (DM) basis.
- Includes metadata fields for species, sampling site, collection date, UKCEH sample codes/descriptions, and tissue sampled.
- Concentrations are reported in mg/kg DM, with handling guidance for values reported as “less than” and for samples with missing data in certain tissues.

## Data structure and key fields
- Core metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration columns (units: mg/kg DM)
  - I_mg_kg_DM
  - Li_mg_kg_DM
  - Na_mg_kg_DM
  - Mg_mg_kg_DM
  - Al_mg_kg_DM
  - P_mg_kg_DM
  - K_mg_kg_DM
  - Ca_mg_kg_DM
  - Ti_mg_kg_DM
  - V_mg_kg_DM
  - Cr_mg_kg_DM
  - Mn_mg_kg_DM
  - Fe_mg_kg_DM
  - Co_mg_kg_DM
  - Ni_mg_kg_DM
  - Cu_mg_kg_DM
  - Zn_mg_kg_DM
  - As_mg_kg_DM
  - Se_mg_kg_DM
  - Rb_mg_kg_DM
  - Sr_mg_kg_DM (with subcomponents 1 and 2 for less-than and actual value)
  - Mo_mg_kg_DM (with subcomponents 1 and 2)
  - Ag_mg_kg_DM (with subcomponents 1 and 2)
  - Cd_mg_kg_DM (with subcomponents 1 and 2)
  - Cs_mg_kg_DM
  - Ba_mg_kg_DM (with subcomponents 1 and 2)
  - Tl_mg_kg_DM
  - Pb_mg_kg_DM
  - U_mg_kg_DM
- Special notations and data handling
  - "<" markers indicate values below the detection/quantification limit.
  - Some columns note tissue-specific applicability (e.g., “Tissue containing thyroid”) and indicate absence of data for that tissue.
  - Explicit notations such as “No data for Hind Leg Bone and woodmouse 8 liver” and “No data for Tissue containing thyroid” for several elements.

## Data quality, limitations, and gaps
- Patchy data across tissues and elements; many entries marked as missing for certain tissues (notably thyroid-containing tissues) and for Hind Leg Bone or woodmouse 8 liver.
- Presence of censoring indicators (<) requiring careful handling in analyses (e.g., survival analysis, censored data techniques).
- Several typographical inconsistencies in column descriptions (e.g., spacing or labeling), which may require cleaning before integration.
- Overall emphasis on dry-mass-based concentrations with metadata to support conversion or interpretation.

## Practical uses and data products
- Enable self-serve exploration of element concentrations by site, date, and tissue (e.g., dashboards, pivot tables).
- Cross-tac data products to compare metal burdens across tissues and individuals, accounting for dry-mass normalization.
- Documentation aids in communicating limitations due to missing data and detection limits when presenting results.

## Data preparation and cleaning recommendations
- Standardize column names and fix typographical issues (e.g., “Fresh_Mass_Dry_Mass_Ratio”).
- Harmonize handling of < values (impute, censor, or flag for analysts).
- Explicitly document tissues with missing data (especially thyroid-containing tissues) and any sample-specific exclusions (e.g., Hind Leg Bone, woodmouse 8 liver).
- Preserve metadata (CEH sample codes/descriptions, site, date) to support traceability and reproducibility.
- Consider separate handling for Sr, Mo, and Ag (and other multi-part columns) where 1 and 2 subfields denote distinct interpretations (e.g., actual value vs. lower bound).

## Notable caveats
- Data are reported on a mg/kg DM basis; ensure alignment of tissue mass normalization in analyses.
- Some elements or tissues lack data entirely; analyses should account for these gaps to avoid bias.
- Detection-limit indicators (<) must be treated appropriately to avoid over-interpretation of non-detects.