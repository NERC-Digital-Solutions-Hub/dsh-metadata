# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Purpose and scope
- A dataset of ICP-MS measured elemental concentrations in vegetation from Northumbria.
- Includes species identification (Latin and common names), sampling site, and sampling date.
- Provides traceable sample metadata via UKCEH identifiers and descriptions.
- Concentrations are reported as mg/kg fresh mass (FM); a Fresh Mass to Dry Mass ratio is included to aid interpretation.
- Contains a broad suite of elements from Li to U, with both major and trace elements measured.
- Some values include less-than qualifiers indicating concentrations below a detection/ reporting threshold.

## Data structure and key variables
- Species and site metadata
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: common name of species
  - Site: sampling site
  - Date_Sample_Collected: date of sampling
  - CEH_Sample_Identifier: UKCEH sample identifier
  - CEH_Sample_Description: UKCEH sample description
- Mass metadata
  - Fresh_Mass_Dry_Mass_Ratio: ratio of fresh mass to dry mass of the sample
- Concentration data (elements measured in mg/kg FM)
  - I_mg_kg_FM (Iodine), Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Some entries use a "<" marker (e.g., <I, <Li) indicating concentrations reported as “less than” a threshold.
- Data quality and notes
  - Units for most concentrations: mg/kg FM
  - Some fields are marked as n/a or have explanatory notes (e.g., “< marker is used to identify concentration given in column …”)
  - Several fields provide explanations rather than numeric data (e.g., “Explanation = …”)

## Data quality, limitations, and challenges
- Presence of many n/a and explanatory fields; some columns may lack information or be metadata rather than numeric values.
- Less-than qualifiers require special handling in analyses (imputation or censoring considerations).
- Data may be localized to specific sites and times, posing challenges for broad generalization without harmonization.
- Potential needs for data standardization across datasets or sources (unit consistency, boundary definitions).

## Practical uses and analytical opportunities
- Compare element concentrations across species and sites to identify uptake patterns.
- Explore correlations between elemental profiles (e.g., major vs. trace elements) within species or at sites.
- Develop predictive models of element accumulation in vegetation based on species identity, site, and sampling date.
- Support environmental monitoring and impact assessments by linking concentrations to ecological or pollution indicators.
- Use metadata (CEH_Sample_Identifier, CEH_Sample_Description) for traceability and reproducibility in analyses.

## Reproducibility and data accessibility considerations
- Sample traceability is supported via UKCEH identifiers and descriptions.
- Fresh mass vs. dry mass information aids in normalizing or converting concentrations for comparisons.
- Clear documentation of units and the presence of less-than values facilitates transparent analysis, provided appropriate handling of censored data.