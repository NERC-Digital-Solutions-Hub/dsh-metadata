# CWatM-Ebro-1km

## Overview
- Dataset of input data and settings to run the Community Water Model (CWatM) for the Ebro River basin, Spain.
- CWatM is a distributed hydrological model used to assess water supply, demand, and environmental needs; calibrated to the Tortosa gauging station.
- Temporal and spatial scope: daily data from 1990-01-01 to 2012-12-31 at 1 km resolution.
- Model runs on Windows desktop; parameters can be adjusted via provided configuration files.

## Data contents and structure
- Initialization and inputs
  - init: contains a single initialization file to reduce warm-up effects.
  - Ebro1km_20121231.nc: main input NetCDF file.
  - input_netcdf: contains earth-surface input maps and a catchment mask (basin2.tif).
- Subsystems and inputs by theme
  - groundwater: Europe_porosity_1km_GLHYMPS.nc, Europe_porosity_1km_GLHYMPS1.tif, k_v20_1km.nc
  - landcover: forest, grassland, irrPaddy, irrNonPaddy (each with 4 files for crop coefficients, interception capacity, max root depth, root fraction1)
  - landsurface: topo (topography and related files), plus a land-cover fraction file
  - soil: 19 files for soil hydraulic properties and related parameters
  - routing: ldd.nc, ups.nc
  - kinematic: chanbnkf.nc, chanbw.nc, changrad.nc, chanleng.nc, chanman.nc
  - lakesreservoirs: multiple files (e.g., IrrCZone.tif, lakeresVolres.tif, lakeresDis.tif, lakeresType.tif, lakeresYear.tif, lakeresID.tif, lakeresArea.tif)
  - meteo: EMO-5 and other precipitation datasets (10 files total, e.g., EMO-5-pr_ebro.nc)
- settings and met data
  - settings: cwatm_settings_readme.txt, cwat_settings_Reservoir_transfers.csv, cwat_settings_Reservoir_downstream.csv, cwat_settings_Reservoir_supply.csv, settings_CWatM-Ebro-1km.ini
  - input data are projected and cropped to the study area and resampled to a 1x1 km grid

## File formats
- NetCDF (.nc)
- TIFF (.tif)
- Text (.txt)
- CSV (.csv)

## Spatial and temporal coverage
- Region: Ebro River basin, Spain
- Bounding box: 43°08'56.2"N 4°27'23.1"W to 40°32'22.8"N 2°27'20.9"E (WSG84)
- Resolution: 1 x 1 km
- Time: 1990-01-01 to 2012-12-31, daily resolution
- Coverage supports mapping of elevation, slope, river routing, lakes/reservoirs, soils, groundwater, land cover, crop coefficients, population/GDP, and sectoral water demands

## Model and inputs
- Model: CWatM (Burek et al., 2020), a high-resolution hydrological model used for regional water resources analysis
- Calibrated against streamflow at Tortosa; calibration described in CWatM user manual using evolutionary computation
- EMO-5 precipitation dataset primarily used; alternative precipitation datasets provided for sensitivity analyses
- Configuration file (cwatm_settings_Reservoir_*.csv and settings_CWatM-Ebro-1km.ini) enables parameter tweaks and input substitutions
- Documentation and manuals: CWatM user manual with running instructions

## Data sources and provenance
- Elevation and land cover: Copernicus
- Flow direction and routing: EU-Hydro and EUDEM-derived products; supported by pyflwdir-based routing
- Lakes/reservoirs: HydroLakes database
- Soils: global soil property datasets (Dai et al., Rosetta-related parameters)
- Groundwater: GLHYMPS (Global Hydrogeology MaPS)
- Crop coefficients: MIRCA2000
- Water demand components: literature sources (e.g., Klein Goldewijk et al., Wriedt et al., Steinfeld et al., Gleick et al., Pastor et al.)
- Meteorology: EMO-5 and alternative precipitation datasets (CHELSA-W5E5, CRU TS3.10, MSWEP, SPREAD)

## Processing and quality assurance
- All datasets projected and cropped to the Ebro study area and resampled to 1x1 km before model run
- No additional quality control performed beyond using published sources
- Data packaging supports straightforward GIS integration and map-based visualization

## Running the model and configuration (for GIS context)
- Core configuration and input control via:
  - cwat_settings_readme.txt
  - cwat_settings_Reservoir_transfers.csv
  - cwat_settings_Reservoir_downstream.csv
  - settings_CWatM-Ebro-1km.ini
  - cwatm_settings.csv (reference within the narrative) to modify parameters and input files
- Precipitation and meteorological inputs can be swapped or extended with alternative datasets for scenario analysis
- Instructions and workflow are documented in the CWatM user manual

## Miscellaneous and references
- CWatM references (developers and methodological papers)
- Input data references and supporting literature listed, enabling traceability of each dataset’s origin and parameters
- Web resources:
  - CWatM project: cwatm.iiasa.ac.at
  - Related papers and manuals linked in the references

## How this GIS-ready dataset supports map-based analysis
- Provides a complete geospatially organized suite of inputs at 1 km resolution suitable for map-based visualizations and spatial analyses
- Rich land-surface, soil, hydrological, and meteorological inputs enable detailed spatial exploration of water balance, routing, reservoir storage, and sectoral water demands
- Clear directory structure and standard formats (NetCDF, GeoTIFF, CSV, TXT) facilitate integration into GIS workflows and hydrological modeling tools