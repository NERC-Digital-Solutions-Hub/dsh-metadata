# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Overview
- Dataset describing concentration ratios of vegetation (fresh mass) to adjacent dry soil mass for multiple elements, used to assess uptake from soil by vegetation.
- Included metadata for species, sampling site, collection date, and sample identifiers to support traceability and reuse.

## Data structure and key fields
- Species information: Latin_Species_Name, Common_Species_Name
- Spatial and temporal context: Site, Date_Sample_Collected
- Sample identifiers and descriptions: CEH_Sample_Identifier, CEH_Sample_Description
- Notes on preparation: Notes
- Co-located soil reference: Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio fields (fresh vegetation mass / dry soil mass):
  - I_Concentration_Ratio (with < marker usage for < values)
  - Element-specific ratios: Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - For some elements, accompanying metadata columns may indicate alternative indexing (e.g., 1/2 suffixes) describing how the ratio is stored or interpreted.
- Note on markers: "<" indicates a less-than value for the corresponding concentration ratio.

## Measurement meaning and scope
- Concentration ratios are defined as Fresh Mass Vegetation divided By Dry Mass Soil for each listed element.
- Includes a broad suite of elements (alkaline to trace metals), enabling cross-element uptake comparisons by species and site.
- Data are accompanied by descriptive notes to aid interpretation of vegetation preparation and sampling context.

## Data quality and preparation considerations
- Units: Many fields list Units = n/a; explicit units may not be provided, requiring careful handling during analysis.
- Data formats: Patchy data formats across the dataset implied by the notes on preparation and the need to co-locate soil samples for calculation.
- Less-than values: Special handling required for values marked with "<" in I_Concentration_Ratio or element-specific ratios.
- provenance and traceability: CEH_Sample_Identifier and CEH_Sample_Description support linking to original lab data and methods.
- Potential gaps: Incomplete species/site coverage or missing dates could affect cross-site comparisons.

## Use cases and data products
- Self-service data exploration: dashboards or pivot-table style views by species, site, date, and concentration ratio by element.
- Environmental monitoring: assess uptake patterns across sites and across seasons or years.
- Policy and communication: support advisory notes on vegetation-based bioindicators and data-driven decisions in land management.
- Data integration: join with soil chemistry, site metadata, or broader ecological datasets to contextualize uptake.

## Practical guidance for use
- Treat less-than values as upper bounds and choose appropriate statistical methods for censored data.
- Validate units and ensure consistent interpretation across elements and sample pairs.
- Link vegetation ratios to co-located soil samples to ensure correct matching and context.