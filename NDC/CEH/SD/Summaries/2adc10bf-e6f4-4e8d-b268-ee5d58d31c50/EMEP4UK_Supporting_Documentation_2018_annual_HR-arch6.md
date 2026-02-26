# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance-based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model rv4.36 and WRF model v4.1.1.

## Experimental design and domain
- EMEP4UK rv4.36 is an atmospheric chemistry transport model (ACTM) derived from EMEP MSC-W rv4.36; simulates hourly to annual atmospheric composition and deposition.
- 3D meteorology from Weather Research and Forecasting (WRF) v4.1.1 with data assimilation of NCEP/NCAR GFS reanalysis every 6 hours.
- Domain: EU at 27×27 km2 resolution with a nested UK domain at 1×1 km2; results reported for the UK domain only.
- UK anthropogenic emissions for NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, and non-methane VOC from 2019 NAEI; rescaled to 2018. Non-UK emissions from CEIP (0.1° × 0.1°) used for all non-UK emissions; UK total used for 2018.

## Data production and computing
- Model code compiled with Fortran Intel compiler (19.1.3.304, 20200925).
- Calculations run on the UKCEH POLAR computing cluster (CentOS 7.9).

## Nature and units of recorded values
- NetCDF files containing surface concentrations and dry deposition fluxes for various species.
- Grid area: variable Area_Grid_km2 (km2).
- Dry deposition variables include:
  - Oxidised sulfur (SOx) across several land-use targets (Grid, Conifer, Seminat, Water, Decid, Crops) with units mgS/m2.
  - Oxidised nitrogen (OXN) across similar targets with units mgN/m2.
  - Reduced nitrogen (RDN) across targets with units mgN/m2.
- Time dimension: time with units days since 1900-01-01; spatial dimensions i, j; additional coordinates lon/lat.

## Quality control and reliability
- Simple QA/QC performed for 2018; reports available on request.
- Both WRF and EMEP4UK are peer-reviewed and widely used; QA includes input emission checks against official inventories and model evaluation against observations (time-series and statistics).
- Users deploy at their own risk; no warranty of correctness or fitness for purpose.

## NetCDF data structure (example)
- Output organized in netCDF with dimensions: time, i, j, plus coordinate variables (lon, i, j) and time.
- Example variables include time, i (EMEP grid x coordinate), j (EMEP grid y coordinate), lon, etc., accompanying the deposition data fields.

## Guidance for using the data
- Data are projected on a polar stereographic grid; use the provided proj4 string: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs.
- NetCDF libraries required; compatible with R, Python, and FORTRAN environments.

## Bibliography and related references
- Evaluation and methodology references for the underlying models and emissions inventories (e.g., Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016; NAEI 2022; Simpson et al. 2012; Skamarock et al. 2019; Vieno et al. 2016a,b) detailing model performance, emissions data, and related atmospheric chemistry transport modeling context.