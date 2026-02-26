# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

- Overview
  - Metadata for an ICP-MS dataset of element concentrations in Northumbria wood mice.
  - Captures species, sampling site, dates, UKCEH sample codes, and tissue sampled.
  - Concentrations are reported on a fresh mass (FM) basis; includes a Fresh_Mass_Dry_Mass_Ratio field.

- Key variables and structure
  - Identification and context
    - Latin_Species_Name; Common_Species_Name
    - Site; Date_Sample_Collected
    - CEH_Sample_Codes; CEH_Sample_Description
  - Biological and sampling details
    - Tissue (which wood mouse tissue was analyzed)
    - Fresh_Mass_Dry_Mass_Ratio (ratio used to relate fresh and dry mass)
  - Element concentrations (all in mg/kg)
    - I_mg_kg_FM; Li_mg_kg_FM; Na_mg_kg_FM; Mg_mg_kg_FM; Al_mg_kg_FM; P_mg_kg_FM
    - K_mg_kg_FM; Ca_mg_kg_FM; Ti_mg_kg_FM; V_mg_kg_FM; Cr_mg_kg_FM
    - Mn_mg_kg_FM; Fe_mg_kg_FM; Co_mg_kg_FM; Ni_mg_kg_FM; Cu_mg_kg_FM
    - Zn_mg_kg_FM; As_mg_kg_FM; Se_mg_kg_FM; Rb_mg_kg_FM; Sr_mg_kg_FM
    - Mo_mg_kg_FM; Ag_mg_kg_FM; Cd_mg_kg_FM; Cs_mg_kg_FM; Ba_mg_kg_FM
    - Tl_mg_kg_FM; Pb_mg_kg_FM; U_mg_kg_FM
  - Data nuances
    - "<" markers (e.g., <I, <Al, <V) indicate concentrations below detection/limit
    - Some columns have paired indicators (e.g., 1 = mg/kg, 2 = concentration of element in mg/kg fresh mass)
    - Several tissues labeled as “Tissue containing thyroid” have no data for certain elements
    - Specific missing data noted: Hind Leg Bone and woodmouse 8 liver

- Data quality, gaps, and accessibility
  - Local-scale data gaps: no data for some tissues or individuals
  - Data may be spread across journals/reports; this header provides the structured field definitions
  - UKCEH identifiers present to aid data traceability and reuse

- Analytical opportunities and considerations
  - Correlate element concentrations with species, site, date, and tissue to identify accumulation patterns
  - Compare across tissues to assess tissue-specific uptake (noting thyroid-related data gaps)
  - Incorporate Fresh_Mass_Dry_Mass_Ratio to adjust for mass basis or convert between fresh and dry mass
  - Properly handle censored data (values marked as < detection limit) in analyses
  - Ensure consistent data provenance and enable reproducible analyses by leveraging CEH_Sample_Codes and CEH_Sample_Description

- Practical notes for analysts
  - Plan for data cleaning to harmonize tissue definitions and units
  - Be mindful of missing data in Hind Leg Bone, liver of woodmouse 8, and thyroid-containing tissue for many elements
  - Use metadata to link to original UKCEH samples and maintain traceability through CEH_Sample_Codes
  - Document any transformations between FM and dry-mass bases if combining with other datasets