# TREE_Northumbria_ICPMS_Bee_DM_Concentration

- A dataset describing concentrations of multiple elements in bee samples (dry mass) from Northumbria, measured by ICP-MS. Includes biological, sampling, and analytical metadata to support environmental monitoring and policy evaluation.

## Aim and scope

- Provide standardized, comparable measurements of elemental concentrations in bees to assess environmental health over time.
- Data intended for quality-assured verification, transformation, and analysis to support standardised outputs (e.g., reports, maps, charts) and policy performance assessment.
- Concentrations are reported as mg/kg dry mass for a wide suite of elements; some values are flagged as "<" indicating below-detection values.

## Data structure and fields

- Biological information
  - Latin_Species_Name: Latin name of the bee species.
  - Common_Species_Name: Common name of the species.
- Sampling information
  - Site: Sampling site identifier.
  - Date_Samples_Collected: Date when samples were collected.
  - CEH_Sample_Codes: UKCEH sample codes.
  - CEH_Sample_Description: UKCEH sample description.
  - Sample_Details: Sample preparation and related details.
- Analytical data (element concentrations in mg/kg dry mass)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
  - Notes: Each concentration is reported as mg/kg dry mass; a "<" marker indicates a concentration reported as a value below the threshold of detection for that analyte (e.g., <Be, <Se, <U). Some column descriptions include minor typographical inconsistencies (e.g., “A Concentration of l” for Al).
- Data quality flags
  - Many fields contain n/a where not applicable or not provided in the excerpt.

## Data quality, standardisation, and processing

- Data are derived from established sources and intended to be verified, quality assured, cleaned, and transformed before analysis.
- Standardised methods are used to generate outputs such as categorising environmental health against standards.
- Outputs are intended to be presented in clear formats (reports, maps, charts) and the resulting datasets stored and uploaded to appropriate data portals.

## Outputs, interpretation, and use

- Enables monitoring of environmental health by comparing bee tissue concentrations against standards or benchmarks.
- Supports time-series analyses and spatial comparisons across sites.
- Facilitates assessment of policy performance and environmental exposure assessments through standardized metrics.

## Data management and access

- Datasets are designed to be stored in appropriate data portals and linked to UKCEH sampling codes and descriptions.
- Emphasis on ensuring underlying data are accessible to other analysts and stakeholders to promote transparency and reuse.

## Challenges and opportunities

- Increasing the value of the datasets by integrating these bee concentration data with additional environmental datasets (e.g., habitat, climate, pollutant sources) for broader analyses.
- Enhancing access to underlying data to support broader use, replication, and secondary analyses by other researchers and decision-makers.

## Notes and caveats

- Presence of "<" markers denotes concentrations below detection limits for the respective analytes.
- Some column descriptions contain minor typographical errors in the provided data (e.g., “A Concentration of l” for Al), which should be cleaned during data curation.
- Overall emphasis on standardized naming, units (mg/kg dry mass), and metadata to support consistent interpretation across analyses.