# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

- Overview
  - A dataset of multi-element concentrations measured in deer whole-organism tissue using ICP-MS, with concentrations expressed as mg/kg fresh mass.
  - Purpose aligned with environmental health monitoring: enables consistent, time-series assessment of environmental health and policy performance.

- Data content and structure
  - Taxonomy and sampling metadata
    - Latin_Species_Name and Common_Species_Name: scientific and common names of the deer sampled.
    - Site: sampling location.
    - Date_Sample_Collected: date the sample was collected.
    - CEH_Sample_Codes and CEH_Sample_Description: UKCEH sample identifiers and description.
    - Notes: notes about tissues used to calculate deer whole-organism concentrations.
  - Concentration data (elements measured in mg/kg fw)
    - I_mg_kg_whole-organism_FM, Li_mg_kg_whole-organism_FM, Be_mg_kg_whole-organism_FM, Na_mg_kg_whole-organism_FM, Mg_mg_kg_whole-organism_FM, K_mg_kg_whole-organism_FM, Ca_mg_kg_whole-organism_FM, Ti_mg_kg_whole-organism_FM, V_mg_kg_whole-organism_FM, Cr_mg_kg_whole-organism_FM, Fe_mg_kg_whole-organism_FM, Co_mg_kg_whole-organism_FM, Cu_mg_kg_whole-organism_FM, Zn_mg_kg_whole-organism_FM, As_mg_kg_whole-organism_FM, Se_mg_kg_whole-organism_FM, Rb_mg_kg_whole-organism_FM, Sr_mg_kg_whole-organism_FM, Mo_mg_kg_whole-organism_FM, Ag_mg_kg_whole-organism_FM, Cd_mg_kg_whole-organism_FM, Cs_mg_kg_whole-organism_FM, Ba_mg_kg_whole-organism_FM, Tl_mg_kg_whole-organism_FM, Pb_mg_kg_whole-organism_FM, U_mg_kg_whole-organism_FM.
    - Some columns indicate less-than values, marked with a preceding "<" (e.g., <Be, <Al, <Ni, <Mo, <Ag, <U). These denote concentrations reported as below detection or below a specified threshold.
    - Some elements have paired columns (e.g., Ba_mg_kg_whole-organism_FM, 1 and …_FM, 2) suggesting multiple related measurements or components; interpretational notes indicate 1 = mg/kg and 2 = concentration description for Ba, Tl, Pb in deer whole-organism.
    - Fresh mass (FM) designation: concentrations are given relative to fresh mass.
    - Specifics on units and column semantics are described in the header notes (e.g., Be and Ni < markers, 1 and 2 column pairs).

- Data quality, standards and handling
  - Data are sourced from established monitoring efforts and are intended to be verified, quality assured, cleaned, and transformed into standard formats prior to dissemination.
  - Outputs are designed for clear presentation (reports, maps, charts) to support environmental health assessments.
  - Datasets are stored and uploaded to appropriate portals, facilitating accessibility and reuse.

- Practical use for analysts monitoring the environment
  - Enables cross-site and temporal comparisons of deer tissue metal concentrations as indicators of environmental exposure.
  - Supports assessment against standards and trend analysis to evaluate policy performance over time.
  - Provides structured metadata to ensure traceability and reproducibility of analyses.

- Challenges and opportunities
  - Increasing the value of the dataset by integrating with additional relevant data sources beyond deer tissue measurements.
  - Improving accessibility of underlying data to support broader analysis and reuse by stakeholders.