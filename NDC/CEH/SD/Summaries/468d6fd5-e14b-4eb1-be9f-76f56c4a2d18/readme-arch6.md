# CWatM-Ebro-1km

- Overview
  - A dataset containing input data and settings to run the Community Water Model (CWatM) for the Ebro River basin in Spain.
  - Supports evaluation of water supply, demand, and environmental needs within the Ebro basin at 1 km resolution (daily from 1990 to 2012).
  - Developed by Dr David Haro Monteagudo (University of Aberdeen) with collaborators from Cranfield University and IIASA.

- Contents and file formats
  - Input data types included: elevation, flow direction, river routing, lakes/reservoirs, soils, groundwater, land cover, crop coefficients, population and GDP, and water demands (irrigation, livestock, industry, domestic).
  - Primary file formats: netCDF (.nc), text (.txt), TIFF (.tif), and CSV (.csv).
  - Key files and folders (illustrative):
    - init: initialization file to reduce model warm-up effects.
    - Ebro1km_20121231.nc: primary input or initialization data.
    - input_netcdf: earth-surface input maps; includes catchment mask.
    - groundwater, landcover (forest, grassland, irrPaddy, irrNonPaddy), landsurface (topography and water demand), topo, waterDemand, routing, kinematic, lakesreservoirs, soil, meteo, settings.
  - Meteo inputs: EMO-5 daily meteorological dataset and alternative precipitation datasets (pr_pen_proj_near.nc, pr_chelse_ebro_near.nc, pr_mswep_proj_near.nc).

- Spatial and temporal coverage
  - Region: Ebro River basin, Spain.
  - Spatial resolution: 1 x 1 km.
  - Bounding box: 43°08'56.2"N to 40°32'22.8"N, 4°27'23.1"W to 2°27'20.9"E.
  - Temporal coverage: 1990-01-01 to 2012-12-31, daily timing.
  - Model: CWatM (distributed hydrological model) calibrated against Tortosa gauging station.

- Model and usage notes
  - CWatM version: v1.04; designed for global/regional water resources assessment.
  - Calibration: evolutionary computation approach; designed to run on standard desktop hardware.
  - Run configuration: cwatm_settings_readme.txt and cwat_settings_Reservoir_*.csv files; settings ini file available to modify parameters and input selections.
  - Output guidance: outputs can be self-serve via dashboards/pivot-like reports or used to create custom analyses; initialisation file helps stabilize storages before analysis.

- Data provenance and sources
  - Elevation and surface data: Copernicus; EUDEM v1.1; flow direction from EU-Hydro; river routing derived from EUDEM and EU-Hydro with pyflwdir.
  - Lakes/reservoirs: HydroLakes database.
  - Soil properties: Dai et al. 2019.
  - Groundwater: GLHYMPS.
  - Land cover: CORINE Land Cover (EEA) with class-specific data for forest, grassland, paddy irrigation, and other irrigated/non-irrigated crops.
  - Crop coefficients: MIRCA2000.
  - Population/GDP: HYDE 3.2; SSP grid projections (Jones & O’Neill; IIASA data).
  - Water demand data: literature-based sources (including agricultural, livestock, industry, domestic, and environmental flow considerations).
  - Meteorology and precipitation: EMO-5 and alternative precipitation datasets (MSWEP, CHELSA, CRU TS3.10, SPREAD).

- Data preparation and quality
  - All datasets are projected and cropped to the Ebro area and resampled to 1x1 km2 before model run.
  - Quality control: no additional quality checks performed beyond reliance on published sources.

- Usage considerations and caveats
  - Patchy data, multiple input formats, and diverse data sources are consolidated into a single 1 km dataset to support end-user exploration and modeling.
  - The provided initialization file helps mitigate warm-up effects; consider excluding early warm-up years if stable storages are already achieved.
  - While calibrated for EMO-5, additional precipitation datasets are provided for expanded analyses.

- Access and references
  - Model and dataset documentation available via the CWatM project (IIASA) and related publications.
  - References span foundational CWatM papers, soil and hydrological data sources, and meteorological forcing datasets (detailed in the document).

- Notes for data support and reuse
  - The dataset is designed to enable others to explore water balance, groundwater interactions, and reservoir routing at high spatial resolution within the Ebro basin.
  - Users can modify parameters and inputs via the included settings files and the CWatM user manual to suit new scenarios or regions.