# Frame Modelling

## Overview
- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate annual mean deposition of reduced and oxidised nitrogen over the UK.
- Domain: United Kingdom and Ireland with 1 km x 1 km grid; 33 vertical layers from ground to 2500 m.
- Outputs: wet and dry deposition of NHx (reduced N) and NOy (oxidised N) at 1 km x 1 km resolution, averaged over each grid cell.

## Model Domain, Structure, and Processes
- Vertical diffusion described explicitly via a multi-layer scheme; key processes in a vertical column.
- Emissions input from UK National Atmospheric Emissions Inventory (NAEI), split into 160 subsectors and aggregated to 11 SNAP sectors; includes diffuse and point sources for NH3, NOx, and SO2.
- UK agricultural NH3 emissions derived from census data, farming practices, and emission source strength data; spatial distribution uses land-cover data at 1 x 1 km resolution.
- Ireland emissions sourced from CLRTAP/EMEP data; spatial distribution using MapEire (1 km) scaled to yearly totals.
- Wider European boundary conditions provided at 50 km x 50 km resolution from CLRTAP; boundary concentrations initialized by eight 45-degree directional simulations per year.
- Meteorology: wind from radiosondes or WRF; rain data; land-cover data from Land Cover Map 2015; deposition velocity dependent on land-cover type.

## Emissions and Input Data
- Emissions for UK domain come from NAEI (split into sectors) and agricultural emission inventories.
- Ireland inputs follow CLRTAP/EMEP and MapEire data.
- Boundary conditions rely on European domain data to initialize UK simulations.

## Simulation Setup
- For each year, eight simulations with 45-degree directional resolution are run to generate domain boundary air concentrations for initialization of the 1 km x 1 km UK simulation.
- Outputs include deposition fields for each year and land-cover type.

## Outputs and Data Structure
- Depositions provided as wet and dry, for both NHx and NOy.
- Land-cover categories: forest and moorland; grid-average deposition is a weighted mean across all five land-cover types (forest, moorland, grassland, arable, urban) based on local composition.
- Data are masked to terrestrial UK 1 km x 1 km cells and presented as average deposition per cell.
- Data are organized into 28 files named ASSIST_N_dep_kgha_xxxx.csv, where xxxx is the year (1990–2017).
- File structure (common across files):
  - x: Easting for the center of the 1 km x 1 km grid cell (OS British National Grid)
  - y: Northing for the center of the 1 km x 1 km grid cell
  - grd_NHx_dry: grid total dry deposition of reduced N (NH3 + NH4)
  - grd_NOy_dry: grid total dry deposition of oxidised N (NO2 + NO3 + HNO3 + PAN)
  - grd_NHx_wet: grid total wet deposition of reduced N
  - grd_NOy_wet: grid total wet deposition of oxidised N
  - for_NHx_dry / for_NOy_dry / for_NHx_wet / for_NOy_wet: forest-only land-cover values
  - mor_NHx_dry / mor_NOy_dry / mor_NHx_wet / mor_NOy_wet: moorland-only land-cover values
- Units: kilograms of nitrogen per hectare per year (kg N ha-1 year-1). No-data values marked NA.

## Data Quality Control and Validation
- FRAME undergoes extensive peer review; included in Defra model inter-comparison exercises.
- Model outputs validated against UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) network measurements.
- FRAME and its outputs widely published in peer-reviewed literature.

## Data Access and Documentation
- Resource: UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) information page and supporting documentation.
- Data structure and deposition outputs are documented within the data description and accompanying references.
- Key references include updates on emissions inventories, model performance evaluations, and methodological papers for FRAME and related datasets.