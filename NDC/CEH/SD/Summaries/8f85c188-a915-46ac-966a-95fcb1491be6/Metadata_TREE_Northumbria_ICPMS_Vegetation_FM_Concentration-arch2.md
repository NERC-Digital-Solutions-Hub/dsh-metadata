# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Aim and context
- Dataset for environmental monitoring of vegetation, capturing concentrations of multiple elements in fresh-mass samples collected at various sites for Northumbria, with UKCEH sampling identifiers and descriptive metadata.
- Supports consistent presentation of environmental health indicators and policy-relevant outputs over time.

## Data content and structure
- Taxonomy and site information
  - Latin_Species_Name (Latin name)
  - Common_Species_Name (common name)
  - Site (sampling location)
  - Date_Sample_Collected (sample date)
  - CEH_Sample_Identifier (UKCEH sample ID)
  - CEH_Sample_Description (sample description)
- Sample characteristics
  - Fresh_Mass_Dry_Mass_Ratio (ratio of fresh to dry mass)
  - <I, <Li, <Be, etc. indicators denote concentrations reported as “less than” a threshold
- Analyte concentrations (mg/kg_fresh_mass)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Notable data conventions
  - < markers indicate concentrations below a detection/quantification limit
  - n/a indicates no information available for a field

## How the data supports monitoring and analysis
- Structured, standardized format enabling trend analysis, cross-site comparisons, and assessment against environmental health standards.
- Outputs are suitable for inclusion in reports, maps, and charts to communicate environmental health and policy performance over time.
- Datasets are prepared for storage and upload to appropriate data portals, aiding transparency and reusability.

## Data management and quality
- Data undergoes verification, quality assurance, cleaning, and transformation to ensure consistency with established sources and monitoring routines.
- Metadata includes sampling date, site, species identifiers, and sample descriptions to support reproducibility and re-use.

## Particular Challenges
- Increasing the value of datasets by integrating them with other relevant data sources (to avoid single-use insights).
- Enabling broad access to the underlying data used to produce final monitoring outputs.