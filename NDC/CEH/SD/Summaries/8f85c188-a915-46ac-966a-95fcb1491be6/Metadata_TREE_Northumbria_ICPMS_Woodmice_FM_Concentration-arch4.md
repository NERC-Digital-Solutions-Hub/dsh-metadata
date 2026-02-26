# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Overview
- A dataset combining metadata and ICP-MS concentration measurements of multiple elements in wood mice (woodmice) tissue, with concentrations reported as mg/kg fresh mass (FM).
- Includes: species identifiers, sampling site, date collected, UK Centre for Environment and Human Health (CEH) sample codes/descriptions, tissue type, and fresh-to-dry mass ratio.
- Some data gaps noted (e.g., no data for Hind Leg Bone and woodmouse 8 liver; missing data for tissue containing thyroid for several elements).

## Data structure and fields
- Core identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration fields (all in mg/kg FM):
  - I_mg_kg_FM, Li_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Notes and qualifiers:
  - Some entries use “<” indicators to denote concentrations below a threshold (e.g., <I, <Al, <V, etc.), signaling censored data.
  - Several references to tissue-specific availability (e.g., “Tissue containing thyroid” vs other tissues) and data absence in certain tissues.
  - Metadata includes distinctions such as “1 = …, 2 = fresh mass” for certain paired fields (indicating multiple related measurements or data anchors).

## Measurement specifics
- Concentrations cover a wide suite of elements (trace to major) measured in woodmouse tissue.
- Data is organized to relate element concentrations to specific tissues and sampling context (site, date, sample codes).
- Some elements share tissue-specific data availability notes (e.g., thyroid-related data gaps).

## Data quality, gaps and limitations
- Data gaps:
  - No data for Hind Leg Bone and woodmouse 8 liver.
  - No data for tissue containing thyroid for several elements (specifics vary by element).
- Data qualifiers:
  - Presence of less-than indicators requires special handling in analysis (censored data).
  - Inconsistencies/garbling in some metadata notes (e.g., mixed formatting for certain fields indicating mass vs concentration), which may require data cleaning before ingestion.
- Metadata richness supports data discoverability (site, date, sample codes, tissue, mass ratio) but some fields have incomplete or missing values in places.

## Data governance, accessibility and stewardship
- Clear linkage between field data and UK CEH sample coding enables traceability and reproducibility.
- Unit consistency: concentrations reported as mg/kg FM; ensure downstream analyses consistently apply fresh mass basis.
- Metadata supports co-ownership and cross-network use (site, date, tissue, sample codes) but requires careful handling of missing tissue-specific data and censored values.
- Encourages verification and standardization across related datasets (e.g., harmonizing tissue definitions and data standards for contaminant measurements).

## Practical implications for data leaders
- Data strategy considerations:
  - Maintain detailed metadata to support discoverability and re-use across partner networks.
  - Implement clear handling procedures for censored (<) values and tissue-specific data gaps.
  - Establish data quality checks to flag missing tissues (e.g., thyroid-associated data) and missing sample components (e.g., Hind Leg Bone, liver for certain entries).
- Data integration opportunities:
  - Combine with site/date context to enable spatial-temporal analyses of element exposure in wood mice.
  - Use CEH_Sample_Codes and descriptions to align with other UK data assets and ensure consistent provenance.
- Operational actions:
  - Document data cleaning rules for interpreting less-than values and tissue-specific qualifiers.
  - Track data gaps and coordinate with data producers to prioritize filling high-impact gaps (granularity, tissue coverage).
- Analytical considerations:
  - Prepare for heterogeneous data across elements with varying detectability; apply appropriate censoring methods.
  - Align data with data governance standards to support dissemination, reproducibility, and cross-institution collaboration.