# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- A metadata/dictionary for a dataset of wood mice concentration ratios collected in Northumbria using ICP-MS.
- Focuses on the ratio of Fresh Mass Woodmice (whole body) to Dry Mass Soil for multiple elements.
- Includes sample and site metadata to contextualise each concentration ratio measurement.

## Data fields and structure

- Taxonomic and sample identifiers
  - Latin_Species_Name: Latin name of the woodmice species
  - Common_Species_Name: Common name of the species
- Sampling metadata
  - Site: Sampling site
  - Date_Sample_Collected: Date of sample collection
  - CEH_Sample_Description: Description of the CEH (Centre for Ecology & Hydrology) sample
  - Notes: Additional notes related to the Woodmice sample
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: Description of the soil sample used to compute the concentration ratio
- Concentration ratio fields (dimensionless)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Notes: Some elements have two related fields indicated by a suffix (1 and 2) (e.g., V_Concentration_Ratio_1, V_Concentration_Ratio_2). The 1/2 variants reflect multiple related measurements or dataset versions per element.
  - Some concentration ratio fields may be prefixed with a less-than marker (e.g., <I_Concentration_Ratio) to denote an upper-bound value.
- Derived measurement
  - All concentration ratios are defined as: Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil
- Units
  - All concentration ratio values are n/a (dimensionless, as they are ratios)

## Key data characteristics

- The dataset links each woodmice sample to a co-located soil sample used for calculating the concentration ratio.
- For many elements, there are multiple concentration ratio entries (two variants) to capture different measurements or dataset versions.
- Some entries indicate upper-bound values using a less-than marker (e.g., <I_Concentration_Ratio).

## Data quality and interpretation considerations

- Ratios are dimensionless; interpret them as relative concentrations of elements in woodmice tissue versus soil mass.
- "<" markers denote upper limits rather than exact measurements; treat them according to the analytical convention used (e.g., censored data handling).
- Metadata completeness (dates, sites, and CEH sample descriptions) is essential for temporal/spatial analyses.
- Data may require integration with external datasets (e.g., site boundaries, administrative areas) for broader analyses.

## Potential uses

- Examine spatial and temporal patterns of trace element accumulation in woodmice relative to soil concentrations.
- Support ecological risk assessments and environmental monitoring in the Northumbria region.
- Inform correlations between soil metal content and bioaccumulation in small mammal populations.
- Facilitate data quality checks and provenance tracking by linking sample metadata to concentration results.

## Data provenance and access notes

- Dataset appears to be structured for reuse in environmental and ecological analyses, with emphasis on traceability (sample descriptions, site, date, and co-located soil samples).
- An emphasis on interoperability and discoverability, potentially by uploading datasets with metadata to appropriate data portals.