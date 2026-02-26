# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Purpose and scope
- Provides concentrations of multiple elements in bee samples (fresh mass, mg/kg) from sampling sites.
- Supports environmental monitoring by standardising data for assessing environmental health and policy performance over time.
- Includes taxonomic and sample metadata to enable traceability and context.

## Data structure and key fields
- Species and site information:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sample identification and description:
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description
  - Sample_Details
  - Notes (bees-related notes)
- Concentration data (all in mg/kg fresh mass):
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM (with a <Be flag for less-than values), Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM (with a <Se flag for less-than values), Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM (with a <U flag for less-than values).
- Flags for less-than values:
  - <Be, <Se, <U indicating concentrations reported as below detection/threshold for the corresponding element.

## Data quality, standardisation and access
- Data are tied to established sampling and coding conventions (UKCEH sample codes; standardized descriptions).
- Data undergo verification, quality assurance, cleaning, and transformation to enable consistent outputs.
- Outputs are designed as clear formats (reports, maps, charts) and datasets are stored/uploaded to appropriate portals for access.

## Practical uses and implications
- Enables comparison of environmental metal exposure across sites and times using bee tissue as a bioindicator.
- Supports readiness to assess compliance with environmental standards and policy performance over time.
- Facilitates integration with other environmental datasets to enrich monitoring and analysis.

## Challenges and opportunities
- Increasing the value of datasets by pairing these concentrations with other relevant environmental data (e.g., soil, water, atmospheric deposition) to avoid single-use data.
- Ensuring easy access to underlying data used to generate final outputs for transparency and re-use.