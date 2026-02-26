# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts to carbon exchange, water quality, and biodiversity. WP2 focuses on plant–soil nutrient interactions and their incorporation into the JULES model.

## Geographic scope and sampling design

- Study area: Conwy catchment, North Wales (~500 km2). Features a climatic gradient and diverse habitats (blanket bog, moorland, woodlands, grasslands, lakes, floodplains, salt marshes).
- Sampling framework:
  - 23 habitats/sites with unique site numbers and mapped sampling locations.
  - Figure 1 depicts sampling across the catchment; includes locations for aboveground biomass and soil cores.
  - NPP measurements (2013–2015) on dominant species; 4 plots per site to represent main flora.
  - Aboveground biomass measured at 10 of 17 sites; soil cores collected across habitats (spring 2014) to 1 m depth (n=3 per habitat).

## Datasets and structure

- The data are organized into five CSV files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw_data.csv
- Common fields (columns):
  - Column A: Site number (aligns with Table 1)
  - Column B: Habitat
  - Column C: Habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: Plant species (for plant components; NA for soil/roots)
  - Column G: Plot number (1–4)
  - Column H: Replicate number
  - Column I: Soil depth interval (for soil and roots; NA otherwise)
- Missing data are indicated as NA.
- Data responsible and version history:
  - Data responsible: Simon Smart (ssma@ceh.ac.uk)
  - Version dates: 01/06/2016; 25/08/2016; 04/11/2016

## Key measurements and data processing (GIS-relevant highlights)

- Aboveground net primary productivity (NPP) and standing biomass:
  - Measured annually (2013–2015) for dominant species; plots protected from grazing in winter.
  - Biomass estimates include herbaceous biomass (grassy/bog habitats) and tree/shrub biomass (woodland), scaled to per m2.
- Plant photosynthesis measures:
  - Vcmax, Jmax, and Asat (field and laboratory measurements using CIRAS-I, LICOR equipment; 20–25 °C temperature corrections).
  - Data processed to fit biochemical models and linked to JULES parameters.
- Leaf traits and plant community traits:
  - Leaf N, leaf P, LDMC, SLA, LMA; canopy height; bryophyte cover.
  - Leaf traits linked to ecosystem processes and JULES inputs.
- Soil measurements (general, P fractions, available C/N, cations):
  - General soil measures: intact cores to 1 m, depth-stratified sampling, bulk density, LOI, LOI-C, pH, EC, total C and N.
  - Phosphorus fractions: Olsen-P, Root-P, Complex-P, Enzyme-P, each via colorimetric methods; multiple extraction schemes to simulate plant/microbial P access.
  - Available carbon and nitrogen: DOC and TDN via 0.5 M K2SO4 extraction; nitrate (NO3) via vanadate method; ammonium (NH4) via salicylate-nitroprusside method.
  - Soil available cations: Ca, Na, K via 0.5 M acetic acid extract; analysis by flame photometry.
  - Root biomass: 0–15 cm cores; root sorting (large vs. fine), WinRhizo analysis, and dry-weight biomass; in-growth root cores to assess root growth.
  - TXRF elemental analysis: comprehensive multi-element soil chemistry (Al, Fe, Ca, K, etc.) with sample preparation and internal standardization; limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.
- Data integration:
  - WP2 aims to couple plant and soil nutrient data for inclusion in the JULES model; data processing and scripts are documented for reproducibility.

## Data usage and GIS considerations

- GIS-ready attributes:
  - Site-level habitat type and description; spatially explicit sampling locations (map-ready via Figure 1 reference and site tables).
  - Plot and replicate metadata enabling spatial aggregation (per habitat, per site).
  - Depth-specific soil data (where applicable) for thematic mapping by soil layer.
- Potential applications:
  - Visualize spatial distribution of NPP, biomass, leaf traits, and soil nutrient pools.
  - Overlay with land-use data to assess anthropogenic pressures and nutrient inputs.
  - Support spatially explicit parameterization of JULES for catchment-scale carbon and nutrient cycling analyses.

## Limitations and notes

- Data gaps: Not all sites have every measurement type or depth interval; some measurements restricted by depth or replicate availability.
- TXRF limitations: Method-specific limitations documented in a separate file (Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).
- Dataset scope reflects 2013–2016 activities; users should align with version dates when integrating with other data sources.

## Access and contacts

- Data custodians:
  - Simon Smart (ssma@ceh.ac.uk)
  - Authors: Sabine Reinsch, Helen Glanville, Simon Smart
- Versioned documentation dates: 01/06/2016; 25/08/2016; 04/11/2016