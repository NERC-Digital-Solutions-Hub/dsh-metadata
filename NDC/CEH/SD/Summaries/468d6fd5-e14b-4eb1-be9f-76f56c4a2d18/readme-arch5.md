# CWatM-Ebro-1km

## Overview
- Dataset containing the input data and settings needed to run a Community Water Model (CWatM) of the Ebro River basin, Spain.
- Includes elevation, flow direction, river routing, lakes/reservoirs, soils, groundwater, land cover, crop coefficients, population and GDP, and water demands for irrigation, livestock, industry, and domestic sectors.
- Developed by Dr David Haro Monteagudo (University of Aberdeen) with Dr Andrea Momblanch Benavent (Cranfield University) and IIASA technical support.

## File formats
- netCDF (.nc)
- Text (.txt)
- TIFF (.tif)
- CSV (.csv)

## Directory structure and key files
- CWatM-Ebro-1km
  - init: initialization file (reduces warm-up effects); Ebro1km_20121231.nc
  - input_netcdf: earth’s surface input maps; includes catchment mask (basin2.tif)
  - groundwater: Europe_porosity_1km_GLHYMPS.nc, Europe_porosity_1km_GLHYMPS1.tif, k_v20_1km.nc
  - landcover: forest, grassland, irrPaddy, irrNonPaddy (each contains multiple 10-day or related files for crop coefficients, interception, root depth, etc.)
  - landsurface: topo (topography files) and waterDemand (lift_areas.tif)
  - routing: ldd.nc, ups.nc
  - kinematic: chanbnkf.nc, chanbw.nc, changrad.nc, chanleng.nc, chanman.nc
  - lakesreservoirs: IrrCZone.tif, lakeresVolres.tif, lakeresDis.tif, lakeresType.tif, lakeresYear.tif, lakeresID.tif, lakeresArea.tif
  - soil: alpha1_1km.nc, alpha2_1km.nc, ..., thetas3_1km.nc (19 files)
  - settings: readme, cwat_settings_Reservoir_transfers.csv, cwat_settings_Reservoir_downstream.csv, cwat_settings_Reservoir_supply.csv, settings_CWatM-Ebro-1km.ini
  - meteo: EMO-5 meteorological inputs (daily) and alternative precipitation datasets (pr_pen_proj_near.nc, pr_chelse_ebro_near.nc, pr_eobs_ebro_near.nc, pr_mswep_proj_near.nc, etc.)
- All datasets have a 1x1 km grid setup for the Ebro basin.

## Spatial and temporal coverage
- Spatial: Ebro River basin, Spain
- Bounding box: 43°08'56.2"N 4°27'23.1"W to 40°32'22.8"N 2°27'20.9"E (WSG84)
- Resolution: 1 x 1 km
- Temporal: 1990-01-01 to 2012-12-31, daily

## Model and workflow
- Model: CWatM (Community Water Model) for high-resolution hydrological assessment; calibrated against Tortosa gauging station.
- Calibration: via evolutionary computation framework described in the CWatM user manual; EMO-5 dataset primarily used for calibration.
- Run environment: Windows 10 (64-bit) or Windows 11 on a desktop (example: i7, 128 GB RAM).
- Parameterization and inputs can be adjusted via cwatm_settings_*.ini and related CSVs; detailed instructions in the CWatM user manual.

## Data sources and provenance
- Input data originate from multiple published sources and repositories:
  - Elevation, land cover, and flow maps from Copernicus; EUDEM v1.1; EU-Hydro
  - River routing: EUDEM v1.1 and EU-Hydro-derived networks; EU-Hydro routing methods
  - Lakes and reservoirs: HydroLakes database
  - Soils: Dai et al. (soil hydraulic properties)
  - Groundwater: GLHYMPS (Global Hydrogeology MaPS)
  - Crop coefficients: MIRCA2000
  - Water demand components: literature (e.g., Klein Goldewijk et al., Wriedt et al., Pastor et al.)
  - Meteorology: EMO-5 dataset; alternative precipitation datasets (MSWEP, CHELSA, CRU TS3.10, SPREAD)
- References and data provenance are documented in the accompanying materials and reference sections.

## Data processing and quality control
- Transformation: all datasets are projected, cropped to the Ebro area, and resampled to a 1x1 km grid prior to model runs.
- Quality control: no additional QC performed beyond reliance on published sources.

## Usage, update and governance
- Model usage instructions available in the CWatM user manual; model can be modified via cwatm_settings*.csv/cwat_settings*.ini.
- The dataset includes multiple precipitation inputs for comparative analysis beyond the EMO-5 dataset.
- Miscellaneous: related articles and documents are in preparation and may be updated in this repository.

## References and metadata
- Core CWatM references (e.g., Burek et al. 2020; Guillaumot et al. 2022) and extensive input data references (MSWEP, CHELSA-W5E5, CRU TS3.10, MIRCA2000, HYDE, CORINE, GLHYMPS, etc.) are provided within the document.