# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Built with EMEP4UK rv4.36 (an atmospheric chemistry transport model) and WRF v4.1.1 for 3D meteorology.
- Domain spans EU at 27×27 km2 with a nested UK domain at 1×1 km2; only UK results are presented.
- Meteorology data assimilated from NCEP/NCAR GFS at 1°×1° resolution every 6 hours.
- Emissions inputs: UK NOx, NH3, SO2, PM2.5, PMcoarse, CO, NMVOCs from NAEI 2019 rescaled to 2018; non-UK emissions from CEIP at 0.1°×0.1°; UK total used for 2018.

## Data Content and Structure
- Outputs are annual totals (NetCDF) of surface deposition/fluxes for oxidised and reduced nitrogen and oxidised sulphur, including area-weighted and land-use-specific deposition components.
- NetCDF variables include:
  - Area_Grid_km2 (grid area, km2)
  - DDEP_SOX_m2Grid, DDEP_SOX_m2Conif, DDEP_SOX_m2Seminat, DDEP_SOX_m2Water_D, DDEP_SOX_m2Decid, DDEP_SOX_m2Crops (dry deposition of oxidised sulphur by area-weighted and specific land uses)
  - DDEP_OXN_m2Grid, DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops (dry deposition of oxidised nitrogen)
  - DDEP_RDN_m2Grid, DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops (dry deposition of reduced nitrogen)
  - Time, i, j indices; lon/lat coordinates
- Units are specified per variable (e.g., mgS/m2 for oxidised sulphur; mgN/m2 for oxidised/reduced nitrogen).
- Output example shows a typical NetCDF structure with time (unlimited), i and j grid dimensions, and geographic coordinates.

## Data Provenance, Methods, and Computing Context
- Modelling framework: EMEP MSC-W chemistry transport model rv4.36; WRF meteorology v4.1.1 with data assimilation (Newtonian nudging) of NWP reanalysis from GFS.
- Domain and resolution: EU domain at 27×27 km2; UK nested domain at 1×1 km2; results pertain to the UK.
- Emissions data: UK 2019 NAEI emissions rescaled to 2018; CEIP 0.1°×0.1° for non-UK emissions; UK total used for 2018.
- Model compilation and computing environment: FORTRAN Intel compiler 19.1.3.304; run on the UKCEH POLAR cluster (CentOS Linux 7.9).
- Model lineage and peer-reviewed basis cited (e.g., Simpson et al., Vieno et al., Skamarock et al., etc.).

## Quality Assurance and Limitations
- QA/QC: simple qualitative and quantitative checks for 2018; emissions totals compared to official inventories; visuals and standard statistics used for evaluation.
- Reported limitations: content is provided without warranty; QA/QC reports are available on request but not included in this document.
- The dataset reflects model-based estimates and should be treated as such for scientific analyses.

## Guidance for Access, Use, and Metadata
- Projection and CRS: data projected on a polar stereographic grid; recommended to apply the provided proj4 string: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs.
- Data format: NetCDF; requires a NetCDF library compatible with R, Python, or FORTRAN.
- Metadata and variable naming: detailed variable names map to specific deposition components and land-use types; time is days since 1900-01-01, with dimensions time, i, j.
- Usage context: peer-reviewed, widely used in atmospheric deposition studies; appropriate for UK-scale deposition assessments and model intercomparison.

## References and Related Documentation
- Key methodological and data references include publications and inventories related to EMEP4UK, WRF, NAEI, and CEIP inputs (e.g., Ge et al., Vieno et al., Simpson et al., Skamarock et al., NAEI 2022).