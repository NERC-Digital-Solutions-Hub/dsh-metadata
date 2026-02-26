# CWatM-Ebro-1km

## Overview
- This dataset provides input data and settings to run a Community Water Model (CWatM) of the Ebro River basin in Spain.
- The model was developed by Dr. David Haro Monteagudo (University of Aberdeen) with Dr. Andrea Momblanch Benavent (Cranfield University) and IIASA collaborators.
- CWatM is a distributed hydrological model used to assess water supply and demand, environmental needs, and water management implications.
- The dataset includes guidance (manuals) and a configuration file to modify parameters and input files for analysis.

## What is included
- Input data for surface processes, soils, groundwater, land cover, crop coefficients, population and GDP, and water demands for irrigation, livestock, industry, and domestic sectors.
- Data and settings to run the Ebro basin 1 km^2 setup of CWatM, including an initialization file to reduce warm-up effects.
- Files cover: elevation, flow direction, river routing, lakes/reservoirs, soils, groundwater, land cover (forest, grassland, irrPaddy, irrNonPaddy), land surface/topography, water demand fractions, routing, kinematic properties, soils, meteorology, and model settings.

## File formats
- netCDF (.nc)
- Text (.txt)
- TIFF (.tif)
- CSV (.csv)

## Directory structure (highlights)
- init: warm-up initialization file
- input_netcdf: earth surface input maps (including catchment mask)
- groundwater: GLHYMPS porosity, groundwater data
- landcover: forest, grassland, irrPaddy, irrNonPaddy data (crop coefficients, interception, root depth)
- landsurface: topo data and demand fraction data
- topo: cellarea, elevation and slope-related files
- waterDemand: lift_areas.tif
- routing: ldd.nc, ups.nc
- kinematic: chanbnkf.nc, chanbw.nc, changrad.nc, chanleng.nc, chanman.nc
- lakesreservoirs: multiple lake/reservoir attributes (type, area, year, id, etc.)
- soil: 19 soil data files for hydrological properties
- settings: cwatm_settings_readme.txt and ini/csv files for initialization and reservoir settings
- meteo: EMO-5 meteorological inputs (plus alternatives like pr_pen_proj_near.nc, CHELSA, CRU, MSWEP)

## Spatial and temporal scope
- Region: Ebro River basin, Spain
- Spatial resolution: 1 x 1 km
- Bounding box: 43°08'56.2"N to 40°32'22.8"N; 4°27'23.1"W to 2°27'20.9"E (WSG84)
- Temporal coverage: Daily data from 1990-01-01 to 2012-12-31
- Model: CWatM (distributed hydrological model)

## Model details and calibration
- Model version: CWatM (Burek et al., 2020) with calibration against Tortosa gauging station; uses an evolutionary computation framework per CWatM user manual.
- Running environment: Windows 10/11 desktop (e.g., 11th Gen i7, 128 GB RAM)
- Run control: cwatm_setting.csv allows parameter and input file modifications; EMO-5 is used for calibration but other precipitation datasets can be substituted.
- Warm-up handling: initialization file reduces warm-up impact; recommended to initialize storages with stable values or discard warm-up years.

## Input data sources and methods
- Elevation and land cover from Copernicus; flow direction from EU-Hydro; river routing with EUDEM-based methods; lakes/reservoirs from HydroLakes.
- Soil hydraulic properties from Dai et al. (2019); groundwater from GLHYMPS; crop coefficients from MIRCA2000.
- Water demand and usage data drawn from literature (e.g., Klein Goldewijk et al., Wriedt et al., Steinfeld et al., Gleick et al., Pastor et al.).
- Representative environmental flows and other inputs described in Table 1 (spatial datasets for 1x1 km2 setup).
- Meteorology datasets: EMO-5 daily data (precipitation, vapour pressure, radiation, temperature, wind), with alternatives such as SPREAD, CHELSA-W5E5, CRU TS3.10, and MSWEP available for analysis.

## Data processing and quality control
- All input datasets are projected, cropped to the study area, and resampled to 1 km2 before model execution.
- Data are sourced from published datasets; no additional quality control was performed by the authors.

## How to run and modify
- Run instructions and detailed parameter adjustments are provided in the CWatM user manual.
- The cwatm_settings_readme.txt and cwat_settings_Reservoir_*.csv plus settingsini guide usage and initialization.
- The EMO-5 precipitation dataset can be replaced with alternative precipitation inputs for scenario analysis.

## Additional notes
- Several articles are in preparation and will be updated when published.
- Input references span meteorological, hydrological, soil, land use, and socio-economic datasets underpinning the model inputs.

## References and sources
- CWatM model development and coupling papers
- Input data sources including EUDEM, EU-Hydro, HydroLakes, MIRCA2000, GLHYMPS, CORINE, HYDE, MIRCA, and ISIMIP-related datasets
- Meteorological datasets (EMO-5, MSWEP, CHELSA, CRU TS3.10, SPREAD)
- Soil and hydrological parameter datasets (SoilGrids, Dai et al., Yamazaki et al., etc.)