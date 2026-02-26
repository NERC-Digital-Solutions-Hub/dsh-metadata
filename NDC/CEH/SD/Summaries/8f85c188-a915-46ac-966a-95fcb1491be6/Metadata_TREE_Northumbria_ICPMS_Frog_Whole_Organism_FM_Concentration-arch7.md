# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset describing concentrations of numerous elements in frog whole-organism tissue, measured by ICP-MS.
- Columns include taxonomic identifiers, sampling metadata, and per-element concentration values.
- Concentrations are reported as milligrams per kilogram fresh mass (mg/kg FM) for most elements.
- Notes field captures tissue types or methods related to how concentrations were calculated.

## Key fields and structure
- Taxonomy and naming
  - Latin_Species_Name (explanation: Latin name of species)
  - Common_Species_Name (explanation: Common name of species)
- Sampling and site information
  - Site (explanation: Sampling site)
  - Date_Sample_Collected (explanation: Date sample collected)
  - CEH_Sample_Description (explanation: UKCEH sample description)
  - Notes (explanation: Notes relating to tissues used to calculate frog whole-organism concentrations)
- Concentration data (all in mg/kg fresh mass unless noted)
  - I_mg_kg_whole_organism_FM (Iodine)
  - Li_mg_kg_whole_organism_FM (Lithium)
  - Be_mg_kg_whole_organism_FM (Beryllium)
  - Na_mg_kg_whole_organism_FM (Sodium)
  - Mg_mg_kg_whole_organism_FM (Magnesium)
  - Al_mg_kg_whole_organism_FM (Aluminium)
  - P_mg_kg_whole_organism_FM (Phosphorus)
  - K_mg_kg_whole_organism_FM (Potassium)
  - Ca_mg_kg_whole_organism_FM (Calcium)
  - Ti_mg_kg_whole_organism_FM (Titanium)
  - V_mg_kg_whole_organism_FM (Vanadium)
  - Cr_mg_kg_whole_organism_FM (Chromium)
  - Mn_mg_kg_whole_organism_FM (Manganese)
  - Fe_mg_kg_whole_organism_FM (Iron)
  - Co_mg_kg_whole_organism_FM (Cobalt)
  - Ni_mg_kg_whole_organism_FM (Nickel) (note: <Ni indicates a "<" value marker)
  - Cu_mg_kg_whole_organism_FM (Copper)
  - Zn_mg_kg_whole_organism_FM (Zinc)
  - As_mg_kg_whole_organism_FM (Arsenic)
  - Se_mg_kg_whole_organism_FM (Selenium)
  - Rb_mg_kg_whole_organism_FM (Rubidium)
  - Sr_mg_kg_whole_organism_FM (Strontium)
  - Mo_mg_kg_whole_organism_FM (Molybdenum)
  - Ag_mg_kg_whole_organism_FM (Silver)
  - Cd_mg_kg_whole_organism_FM (Cadmium)
  - Cs_mg_kg_whole_organism_FM (Cesium)
  - Ba_mg_kg_whole_organism_FM (Barium)
  - Tl_mg_kg_whole_organism_FM (Thallium)
  - Pb_mg_kg_whole_organism_FM (Lead)
  - U_mg_kg_whole_organism_FM (Uranium) (note: <U indicates a "<" value marker)
- Value qualifiers
  - Some concentration fields may include a "<" marker indicating below-detection or below-threshold values (e.g., <Be, <Ni, <U)

## Data quality and interpretation notes
- Units: Most element concentrations are reported as mg/kg fresh mass.
- Tissue/extraction context: Notes describe tissues or calculation methods used to derive whole-organism concentrations.
- Missing or below-detection values: "<" markers indicate concentration values below a reporting threshold for the respective element.

## GIS and analysis considerations
- Spatial linkage: Data include a Site field enabling mapping of concentrations across locations.
- Temporal aspect: Date_Sample_Collected supports time-series visualization and trend analysis.
- Data integration: Many elements are included in a single dataset, allowing multi-element spatial analyses and pattern exploration.
- Data preparation needs:
  - Standardize units and handle "<" values appropriately (imputation or censoring rules may be needed).
  - Resolve any inconsistencies in site naming or sampling descriptions to enable reliable joins.
  - Verify tissue-type notes to ensure consistent whole-organism interpretation across samples.

## Challenges and considerations for use
- Data scattered across multiple datasets and locations; ensure provenance and UKCEH/CEH-supplied descriptions are preserved.
- Lack of uniform data standards across all fields; plan for harmonization when integrating with other GIS data.
- Handling large/complex multi-element tables: consider creating per-element layers or summary dashboards for effective visualization.
- Ensuring data quality through verification against metadata (sampling site, date, and description) before spatial analysis.