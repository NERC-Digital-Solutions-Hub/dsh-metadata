# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- Document describes concentrations of multiple elements in wood mice tissues from Northumbria, measured by ICP-MS, to support environmental health monitoring and inform policy decisions.
- Includes sampling metadata (species names, site, collection date) and tissue-level concentration data (reported as mg/kg dry mass) with data quality indicators.

## Dataset structure and fields
- Primary identifier: TREE_Northumbria_ICPMS_Woodmice_DM_Concentration.
- Taxonomy and sampling info: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Tissue, Fresh_Mass_Dry_Mass_Ratio.
- Concentration data (mg/kg dry mass): I_mg_kg_DM, Li_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Data qualifiers and notes: some values are prefixed with “<” indicating concentrations below detection/quantification; <I, <Al, etc. appear in the table to mark such cases.
- Data gaps and tissue specificity: explicit notes indicate no data for Hind Leg Bone and woodmouse 8 liver; no data for tissue containing thyroid for several elements.

## Data quality, gaps and challenges
- Gaps: Hind Leg Bone data missing; woodmouse 8 liver data missing; tissue containing thyroid often has no data for multiple elements.
- Measurement qualifiers: presence of “<” values requires careful interpretation (below detection limits).
- Metadata clarity: field labels and explanations provided, but some tissues have restricted data (e.g., thyroid-containing tissues) for certain elements, affecting comparability across tissues.
- Data standardization needs: consistent tissue terminology and unit interpretation (mg/kg dry mass) are essential for cross-study comparability.

## Relevance for monitoring and decision making
- Enables spatial and temporal assessment of environmental metal exposure in a sentinel rodent, informing environmental health risk assessments.
- Rich metadata (site, collection date, sample codes) supports traceability, reproducibility, and policy-relevant reporting.
- The breadth of elements covered supports multi-pollutant exposure insights and prioritization of contaminants in policy evaluation.

## Practical considerations for use
- Treat < values as censored data requiring appropriate statistical handling.
- Be mindful of data gaps by tissue (e.g., thyroid-containing tissues) when designing analyses or aggregations.
- Ensure clear data governance and licensing if sharing or repurposing, acknowledging potential barriers to open data highlighted in broader monitoring challenges.