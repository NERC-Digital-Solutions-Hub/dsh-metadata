# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Overview
- Dataset of trace element concentrations in Northumbria wood mice tissues analyzed by ICPMS.
- Includes sampling metadata (Latin/Common species, site, date, CEH sample codes/descriptions, tissue) and tissue-specific fresh mass to dry mass ratio.
- Concentrations reported as mg/kg fresh mass (FM) with qualifiers for non-detects.

## Data structure and key fields
- Taxonomy and identification:
  - Latin_Species_Name, Common_Species_Name
- Sampling metadata:
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
- Biological/physical data:
  - Tissue, Fresh_Mass_Dry_Mass_Ratio
  - Indicators (<I, <Al, <V, etc.) mark concentration values reported as below a threshold
- Element concentrations (mg/kg FM):
  - I_mg_kg_FM, Li_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM
  - P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM
  - Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM
  - Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM
  - Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM
  - Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Notes on data structure:
  - Some columns include two-part entries (e.g., 1 = mg/kg, 2 = fresh mass) for certain measurements
  - Some elements have data only in specific tissues; others note “No data” for certain tissues

## Data coverage, gaps, and qualifiers
- Data gaps:
  - No data for Hind Leg Bone and woodmouse 8 liver
  - No data for tissue containing thyroid for several elements
- Non-detects and qualifiers:
  - "<I", "<Al", "<V", and similar markers indicate concentrations below detection or reporting thresholds
- Metadata quality considerations:
  - Some tissue categories described as “tissue containing thyroid” with restricted data
  - Metadata completeness varies, affecting ease of cross-study comparability

## Data quality, transformation, and governance
- Quality considerations:
  - Concentrations are raw MG/kg FM with potential non-detect qualifiers; careful interpretation required
  - Some fields require transformation or alignment (e.g., subfield interpretation, mass basis)
- Governance and sharing:
  - Emphasizes the need for quality assurance, data cleaning/transformation, and clear presentation of findings
  - Supports sharing underlying data to enable stakeholder scrutiny and policy use
  - Highlights data management needs, including clear descriptions, provenance, and standardized metadata

## Relevance to monitoring framework aims
- Provides environmental health indicators through a sentinel species (wood mice) to assess exposure to trace elements across sites and dates.
- Supports decision-making, policy scrutiny, and future actions by enabling spatial and temporal trend analyses of metal accumulation.
- Illustrates common monitoring challenges:
  - Data gaps and access barriers
  - Silos or fragmentation of metadata
  - Need for robust metadata, data transformation, and governance to ensure data usability and openness