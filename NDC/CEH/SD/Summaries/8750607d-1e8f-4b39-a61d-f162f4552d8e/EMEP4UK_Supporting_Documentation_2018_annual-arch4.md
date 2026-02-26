# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Purpose and scope
- Provides the annual total surface resistance-based atmospheric deposition for the UK for 2018.
- Produced with EMEP4UK model rv4.36 and WRF model v4.2.2; domain covers the EU at 27×27 km2 with a nested UK domain at 3×3 km2 (results shown for the UK domain only).

## Experimental design and data sources
- ACTM-based modeling derived from EMEP MSC-W rv4.36; simulates hourly to annual deposition and atmospheric concentrations of pollutants.
- Meteorology from WRF with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1° every 6 hours.
- UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOCs) from 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP (0.1° resolution) using UK total for 2018.

## Model, implementation, and environment
- Models compiled with Intel FORTRAN compiler; calculations run on the UKCEH POLAR compute cluster (CentOS 7).

## Data products and content
- NetCDF outputs with grid-area and deposition variables for oxidised/reduced nitrogen and oxidised sulfur, at area-weighted and land-use-specific (coniferous forest, semi-natural, water, deciduous forest, coniferous crops) categories.
- Variables include:
  - Area_Grid_km2 (grid area)
  - DDEP_SOX_m2Grid, DDEP_SOX_m2Conif, DDEP_SOX_m2Seminat, DDEP_SOX_m2Water_D, DDEP_SOX_m2Decid, DDEP_SOX_m2Crops
  - DDEP_OXN_m2Grid, DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops
  - DDEP_RDN_m2Grid, DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops
- Data are provided on a polar stereographic grid; specific projection details are described by the included proj4 string.

## Data quality, governance, and notes
- QA/QC performed for 2018; QA/QC reports available on request (not included in this document).
- Content is provided without warranty; use is at the user’s own risk.
- Data accessibility requires a NetCDF library compatible with R, Python, or FORTRAN.

## Guidance for use and accessibility
- Projection: polar stereographic; proj4 string provided for integration into applications.
- NetCDF-based data; compatible tooling needed (R, Python, FORTRAN).
- Bibliography and methodological references are provided to support validation and comparison (e.g., model descriptions and related emissions studies).