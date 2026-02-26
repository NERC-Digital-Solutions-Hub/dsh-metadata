# TREE_Northumbria_ICPMS_Vole_AM_Concentration

## Overview
- A dataset of ICP-MS concentration measurements (mg/kg) in ash mass from vole samples collected at Northumbria (UK Centre for Ecology and Hydrology context).
- Captures species information, sampling location, collection date, sample codes, preparation details, and concentration results for a wide suite of elements.
- Includes notes on sample preparation (e.g., separation of tissues) and a mass ratio metric (Fresh_Mass_Ash_Mass_Ratio).

## Key fields (content categories)
- Biological identifiers
  - Latin_Species_Name
  - Common_Species_Name
- Sampling information
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
  - Notes
- Mass and preparation
  - Fresh_Mass_Ash_Mass_Ratio
- Element concentrations (mg/kg, ash mass)
  - I_mg_kg_AM
  - Li_mg_kg_AM
  - Be_mg_kg_AM
  - Na_mg_kg_AM
  - Mg_mg_kg_AM
  - Al_mg_kg_AM
  - P_mg_kg_AM
  - K_mg_kg_AM
  - Ti_mg_kg_AM
  - V_mg_kg_AM
  - Cr_mg_kg_AM
  - Mn_mg_kg_AM
  - Fe_mg_kg_AM
  - Co_mg_kg_AM
  - Ni_mg_kg_AM
  - Cu_mg_kg_AM
  - Zn_mg_kg_AM
  - As_mg_kg_AM
  - Se_mg_kg_AM
  - Rb_mg_kg_AM
  - Sr_mg_kg_AM
  - Mo_mg_kg_AM
  - Ag_mg_kg_AM
  - Cd_mg_kg_AM
  - Cs_mg_kg_AM
  - Ba_mg_kg_AM
  - Tl_mg_kg_AM
  - Pb_mg_kg_AM
  - U_mg_kg_AM
- Data formatting notes
  - Some elements appear with dual fields (e.g., 1 and 2 suffix variants) and some “less than” (<) markers indicating upper-bound values.

## Spatial and temporal context
- Site identifies sampling locations; dates provide temporal context for trend analyses.
- The data is suitable for GIS mapping of concentrations by site, species, and sampling event.
- CEH_Sample_Codes and CEH_Sample_Description offer source-traceability for integration with other UKCEH datasets.

## Data quality and preparation challenges
- Data originate from multiple sources and may lack consistent standards or resolutions.
- Potential inconsistencies or typographical errors in some field descriptions (e.g., Ti_mg_kg_AM description vs. actual content).
- Several concentration fields include less-than markers, requiring handling as censored or upper-bound values.
- Large or complex datasets require cleaning, standardization, and careful joining of fields (e.g., replicates or dual-field formats like Ag_mg_kg_AM_1/2).
- Species and site data need alignment with GIS layers (geographic coordinates or shapefiles) for accurate mapping.

## Using the data in GIS
- Map by Site to visualize spatial distribution of element concentrations.
- Join to site polygons or point data using the Site field; incorporate Date_Sample_Collected for temporal mapping.
- Create layer visualizations (e.g., choropleth or graduated-symbol maps) by species, site, or sampling period.
- Use Latin_Species_Name and Common_Species_Name to filter by target vole species.
- Integrate with sample metadata (Notes, Sample_Details, CEH codes) for contextual mapping (e.g., sampling methods, preparation differences).

## Data preparation and processing steps (recommended)
- Validate and standardize units across all concentration fields to ensure mg/kg consistency.
- Resolve and document any inconsistencies in element naming and field descriptions.
- Handle less-than values appropriately (e.g., treat as upper bounds or apply censoring in analyses).
- Separate or consolidate fields with dual 1/2 suffixes as appropriate for the analysis; verify intended meaning with data provider.
- Geocode Site or link to an existing GIS layer to obtain coordinates; create a spatial feature class (Shapefile/GeoJSON/Geopackage).
- Create derived fields as needed (e.g., total metal load by site, per-species aggregates, or per-sample mass-normalized metrics).
- Document data provenance, sample preparation notes, and any non-detections or exclusions.

## Notes and caveats
- The dataset appears to focus on vole ash mass concentrations following UKCEH-related sampling.
- Some column descriptions contain mismatches (e.g., Ti_mg_kg_AM description referencing calcium), indicating a need for data validation against a formal data dictionary.
- The presence of “<” markers and dual-field formats necessitates explicit handling in analysis and visualization workflows.
- Ensure alignment with project-specific data standards and any required quality assurance steps before GIS publication.