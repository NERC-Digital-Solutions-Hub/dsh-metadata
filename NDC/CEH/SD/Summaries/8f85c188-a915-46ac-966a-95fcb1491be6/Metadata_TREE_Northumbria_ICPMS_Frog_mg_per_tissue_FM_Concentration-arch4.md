# TREE_Northumbria_ICPMS_Frog_mg_per_tissue_FM_Concentration

## Overview
- A dataset of metal and element concentrations measured in frog tissue using ICP-MS.
- Captures contextual metadata (species, site, sampling date, UKCEH sample codes) and tissue type alongside multi-element concentration values in milligrams per total frog tissue fresh mass.
- Includes censored data (values marked with “<” indicating upper bounds) and non-applicable indicators (n/a).

## Core metadata and context
- Species identifiers:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
- Biological/tissue details:
  - Tissue (tissue type sampled)
- Measurement scope:
  - I_mg_tissue_FM, Li_mg_tissue_FM, Be_mg_tissue_FM, Na_mg_tissue_FM, Mg_mg_tissue_FM, Al_mg_tissue_FM, P_mg_tissue_FM, K_mg_tissue_FM, Ti_mg_tissue_FM, V_mg_tissue_FM, Cr_mg_tissue_FM, Mn_mg_tissue_FM, Fe_mg_tissue_FM, Co_mg_tissue_FM, Ni_mg_tissue_FM, Cu_mg_tissue_FM, Zn_mg_tissue_FM, As_mg_tissue_FM, Se_mg_tissue_FM, Rb_mg_tissue_FM, Mo_mg_tissue_FM, Ag_mg_tissue_FM, Cd_mg_tissue_FM, Cs_mg_tissue_FM, Ba_mg_tissue_FM, Tl_mg_tissue_FM, Pb_mg_tissue_FM, U_mg_tissue_FM
- Units:
  - Concentrations are in milligrams per total frog tissue fresh mass (mg per tissue_FM)

## Data structure and important notes
- Value formatting:
  - "<X" denotes a concentration less than the specified value (censored data).
  - n/a indicates not applicable for that field.
- Data quality considerations:
  - Some field descriptions show inconsistencies (e.g., a description referencing Ca when the column is Ti), indicating potential labeling errors to resolve.
  - Metadata completeness is essential for comparability across sites, species, and tissues.
- Scope of elements:
  - A broad suite of elements/metals is included (I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) typical of environmental contaminant assessments.

## Data quality and governance considerations for Data Leaders
- Discoverability and standardization:
  - Clear association with UKCEH Northumbria data and sampling context supports integration into broader data ecosystems.
  - Metadata should be harmonized (consistent naming, units, and definitions) to enable cross-site comparisons.
- Handling censored data:
  - Provisions for < signs must be consistently applied in analyses and documentation.
- Metadata integrity:
  - Resolve potential mislabeling (e.g., mismatches in descriptive text vs. column content) to avoid misinterpretation.
- Data gaps and granularity:
  - Some elements or tissues may have incomplete data, affecting granularity and powered analyses.
  - Consider coordination with wider data networks to fill gaps and reduce duplicated efforts.
- Privacy and access:
  - While not detailed in the text, prepare to align with data protection and access controls as part of broader data governance, especially when linking to partner networks.

## How this dataset supports data strategy for Data Leaders
- Provides a multi-element, tissue-level contaminant profile essential for ecosystem risk assessment and monitoring programs.
- Demonstrates the importance of robust metadata to enable data discoverability, reuse, and cross-network collaboration.
- Illustrates practical handling of imperfect data (censoring, n/a values, and labeling inconsistencies) within a governance framework.
- Highlights opportunities for standardizing data schemas and coordinating with the wider data community to minimize duplication and improve practice.