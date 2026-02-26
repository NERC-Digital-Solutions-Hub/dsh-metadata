# TREE_Northumbria_ICPMS_Soil_DM

## Overview
- A soil ICP-MS dataset from Northumbria, with concentrations of multiple elements measured on a dry mass basis (mg/kg DM).
- Key identifiers include UKCEH sample identifiers and sampling metadata (site and sampling date).
- Contains 29 elements measured across samples.

## Data fields and schema
- CEH_Sample_Identifier: UKCEH sample identifier
- CEH_Sample_Description: UKCEH sample description
- Site: Sampling site
- Sampling_Date: Date sample collected
- I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM: Concentrations of each element in milligrams per kilogram dry mass (mg/kg DM)

- Note: The dataset lists 29 elements, with each concentration field accompanied by the unit mg/kg_DM and an explanation of the element being measured.

## Measurements and units
- All element concentrations are reported on a dry mass basis (mg/kg DM).
- Sample and site identifiers provide traceability to the UKCEH dataset.

## Data quality and metadata considerations
- Explanations accompany each field to aid interpretation.
- Some lines in the source text show inconsistencies or mislabeling (e.g., incorrect explanations for certain elements). Validation may be needed to ensure accurate field descriptions.
- Proper data provenance is supported by UKCEH sample identifiers and clear sampling metadata.

## Potential uses for analysts
- Explore correlations between elemental concentrations and sampling sites or dates.
- Develop predictive or explanatory models of soil composition across sites in Northumbria.
- Compare observed concentrations with environmental baselines or regulatory thresholds.
- Integrate with additional site metadata (boundaries, land use, soil type) for richer analyses.

## Data management and access considerations
- Maintain metadata alongside data to ensure discoverability and reuse (e.g., through portals with descriptive metadata).
- Ensure standardization across datasets to facilitate cross-study comparisons.
- Be mindful of data quality checks to address any mislabeling or inconsistent explanations identified in the source.