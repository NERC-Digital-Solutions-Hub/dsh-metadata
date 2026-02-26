# CWatM-Ebro-1km

## Overview
- Dataset containing input data and settings to run a Community Water Model (CWatM) simulation for the Ebro River basin in Spain.
- Developed by Dr David Haro Monteagudo (University of Aberdeen) with Dr Andrea Momblanch Benavent (Cranfield University) and IIASA technical assistance.
- Used to assess water supply, demand, environmental needs, and human influence within the basin.

## Data inputs and contents
- Elevation model, flow direction, river routing, lakes/reservoirs, soils, groundwater, land cover, crop coefficients, population and GDP, and water demands for irrigation, livestock, industry, and domestic sectors.
- Input formats: netCDF (.nc), text (.txt), TIFF (.tif), and CSV (.csv).
- Land cover classes and related parameters (forest, grassland, irrPaddy, irrNonPaddy) with corresponding crop coefficients, interception, root depth, etc.
- Met data options include EMO-5 and several alternatives (SPREAD, CHELSA-W5E5, CRU TS3.10, MSWEP).

## Directory structure (highlights)
- CWatM-Ebro-1km
  - init: warm-up initialization file (optional but recommended for stability)
  - input_netcdf: earth-surface input maps; includes a catchment mask
  - groundwater: GLHYMPS porosity, groundwater-related files
  - landsurface: topo and related land-surface inputs
  - landsurface/topo: elevation, slope, cell area, etc.
  - waterDemand: demand-related inputs (lift areas)
  - routing/kinematic: river network routing parameters
  - lakesreservoirs: lake/reservoir properties and identifiers
  - soil: soil hydraulic properties and related parameters
  - meteo: meteorological inputs (EMO-5 and alternatives)
  - settings: model settings, initialization, and reservoir transfer/downstream/supply files
  - input_netcdf and meteo folders include subfiles and additional data as needed

## Spatial and temporal coverage
- Spatial: Ebro River basin, Spain; bounding box roughly from 43°08'56.2"N, 4°27'23.1"W to 40°32'22.8"N, 2°27'20.9"E (WSG84); resolution 1 x 1 km.
- Temporal: 1990-01-01 to 2012-12-31; daily data resolution.

## Model and calibration
- Model: CWatM (Community Water Model), distributed hydrological model for global/regional water resource assessment.
- Calibration: against observed streamflow at Tortosa, using an evolutionary computation framework described in CWatM documentation.
- Platform: designed for desktop Windows 10/11 with substantial RAM (example setup: 11th Gen i7, 128 GB RAM).
- Reproducibility: parameter adjustments via cwatm_settings_readme.txt and cwat_settings_Reservoir_*.csv / .ini files; EMO-5 used for calibration with additional precipitation datasets available.
- Operational guidance: run instructions available in the CWatM user manual.

## Data sources and processing
- Data sources: Elevation/land cover from Copernicus; river routing from EU-DEM and EU-Hydro; HydroLakes for lakes/reservoirs; soils from Dai et al.; GLHYMPS for groundwater; MIRCA2000 for crop coefficients; various literature for water demand components.
- Data processing: all datasets projected, cropped to the study area, and resampled to a 1x1 km grid prior to modeling.
- References and provenance: detailed in the accompanying table of spatial datasets; extensive citation list for input data origins and supporting literature.

## Quality control and governance
- Quality control: no additional QC performed beyond relying on published sources; data provenance and documentation are provided for transparency.
- Data governance: emphasis on openness and reproducibility through explicit metadata, data sources, and model settings; instructions to share underlying data and use standardized data management practices.

## Usage notes and miscellaneous
- Model outputs and further analyses are referenced in articles in preparation; updates anticipated as publications finalize.
- Input data and model parameters can be modified to explore alternative scenarios or updated datasets; instructions and manuals referenced for detailed guidance.