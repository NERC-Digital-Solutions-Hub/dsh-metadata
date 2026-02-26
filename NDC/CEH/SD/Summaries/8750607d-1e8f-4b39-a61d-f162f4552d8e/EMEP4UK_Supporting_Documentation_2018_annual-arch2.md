# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

- Dataset provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model version rv4.36 and WRF model version 4.2.2.

## Purpose and scope
- Supports assessment of atmospheric deposition of pollutants by providing area-weighted deposition components and surface concentrations needed for environmental health monitoring and policy evaluation.
- Outputs are designed for consistent comparison over time and across UK regions.

## Model description and data sources
- Atmospheric chemistry transport model: EMEP4UK rv4.36 (based on EMEP MSC-W rv4.36).
- Meteorology: 3D meteorology from WRF Version 4.2.2, with data assimilation (Newtonian nudging) of NWP reanalysis from NCEP/NCAR GFS at 1°×1° every 6 hours.
- Emissions: UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) from 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP 0.1°×0.1° data.
- Domain: EU domain at 27×27 km2 with a nested UK domain at 3×3 km2; results reported for the UK domain only.
- Model compiler: FORTRAN Intel compiler 19.1.3.304 (2020-09-25); run on UKCEH POLAR cluster.

## Temporal and spatial coverage
- Temporal: Year 2018 (annual total).
- Spatial: UK within a European modelling domain; results provided as area-weighted grid deposition.

## Data content and variables (NetCDF)
- Grid area: Area_Grid_km2 (km2).
- Dry deposition components (oxidised and reduced nitrogen; oxidised sulphur) by area-weighted and by land-cover types:
  - Oxidised sulphur: DDEP_SOX_m2Grid (area-weighted), DDEP_SOX_m2Conif (coniferous forest), DDEP_SOX_m2Seminat (semi-natural), DDEP_SOX_m2Water_D (water), DDEP_SOX_m2Decid (deciduous forest), DDEP_SOX_m2Crops (crops).
  - Oxidised nitrogen: DDEP_OXN_m2Grid (area-weighted), DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops.
  - Reduced nitrogen: DDEP_RDN_m2Grid (area-weighted), DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops.
- NetCDF files contain the above variables in the specified units.

## Quality assurance and caveats
- QA/QC conducted for 2018; QA/QC reports available on request.
- Dataset use is at the user’s risk; no warranty that content is error-free or fit for a particular purpose.

## Data structure and access guidance
- Data projected on a polar stereographic grid.
- Proj4 string for the coordinate reference system: '+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs'.
- NetCDF compatibility required with common data analysis tools (R, Python, FORTRAN).

## Use for monitoring and policy performance
- Provides standardized annual deposition estimates to evaluate environmental health, track policy impacts, and compare across years.
- Fits the Analyst Monitoring the Environment archetype by enabling verification, quality assurance, and clear presentation in reports and visual formats.

## References and sources
- Core model and methodological references include Simpson et al. (2012), Vieno et al. (2016a, 2016b), Skamarock et al. (2019), Ge et al. (2021), Gu et al. (2021), Jalkanen et al. (2016), and related NCEP/NCAR and CEIP/NAEI documentation.