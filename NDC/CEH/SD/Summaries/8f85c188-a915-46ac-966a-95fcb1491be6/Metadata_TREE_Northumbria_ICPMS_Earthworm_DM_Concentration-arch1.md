# TREE_Northumbria_ICPMS_Earthworm_DM_Concentration

## Overview
- A dataset of ICP-MS measured element concentrations in earthworm tissue from Northumbria (TREE_Northumbria_ICPMS_Earthworm_DM_Concentration).
- Includes sample metadata: Latin and common species names, sampling site, date collected, UKCEH sample codes and descriptions, and notes.
- Element concentration data are in mg/kg dry mass (DM) for a wide panel of elements.

## Data columns and meanings
- Taxonomy and sample metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Notes
- Element concentrations (examples; all in mg/kg DM):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM
  - P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM
  - Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM
  - Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM
  - Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM
  - Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Each column includes units and explanation notes describing the measured element concentration in dry mass.

## Data structure and scope
- Structured table format with both biological (species, site, date) and chemical (multiple elements) data.
- UKCEH-linked metadata (CEH_Sample_Codes and CEH_Sample_Description) enabling traceability to UK environmental lab records.

## Potential analyses and uses
- Explore correlations between element concentrations across species and sites.
- Compare elemental loadings by sampling location or date (temporal trends).
- Identify species- or site-specific patterns in bioaccumulation.
- Integrate with environmental variables to model drivers of earthworm tissue metal concentrations.

## Data quality and considerations for analysts
- Right-scale and local-level interpretation may be needed; dataset appears focused on specific sites within Northumbria.
- Concentrations are in mg/kg DM; ensure consistent dry mass tissue processing when combining with other datasets.
- Metadata completeness (species, site, date, CEH codes) is essential for robust analyses.
- Data provenance is anchored to CEH/UKCEH records; maintain linkage to sample codes for reproducibility.

## How to use and interpret
- Suitable for descriptive statistics, multivariate analyses (e.g., PCA, cluster analyses), and regression modeling to assess predictors of metal concentrations.
- Prior to analysis: standardize units, handle missing values, and consider species- and site-level random effects.
- Document data provenance and any transformations to maintain traceability with CEH UKCEH records.