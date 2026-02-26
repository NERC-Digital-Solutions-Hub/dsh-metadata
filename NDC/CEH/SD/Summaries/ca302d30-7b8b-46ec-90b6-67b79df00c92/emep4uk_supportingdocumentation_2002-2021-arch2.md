# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

## Overview
- Provides daily averaged atmospheric composition for the UK (2002–2021) focusing on main nitrogen and sulfur species, particulate matter, organic matter, and ozone.
- Generated with EMEP4UK model rv4.36 and WRF model v4.2.2.
- UK-domain results are presented on top of a larger EU domain; UK resolution is 3 x 3 km, nested within a 27 x 27 km EU domain.

## Experimental design and data sources
- Model framework: atmospheric chemistry transport model (ACTM) derived from EMEP MSC-W rv4.36; simulates hourly to annual averages of atmospheric composition and deposition.
- Meteorology: 3D fields from WRF v4.2.2 with data assimilation (Newtonian nudging) using NCEP/NCAR GFS reanalysis at 1° x 1° every 6 hours.
- Domain and resolution: EU domain 27 x 27 km with a nested UK domain at 3 x 3 km; results shown for the UK domain only.
- Emissions driving the model: anthropogenic NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and NMVOCs derived from 2019 NAEI; UK totals for 2002–2019 rescaled accordingly; non-UK emissions from CEIP 0.1° data; 2020–2021 emissions use 2019 values.

## Data products and recorded variables
- Daily averaged fields include near-surface concentrations of ozone (ppbv), various PM components (PM2.5, PMcoarse; detailed SURF_ variables), and other trace species.
- PM definitions:
  - PM2.5: fine particulate matter with aerodynamic diameter ≤ 2.5 µm.
  - PMcoarse: 2.5–10 µm fraction.
  - PM10: PM2.5 plus PMcoarse.
- NetCDF-described surface variables include mixing layer height (HMIX, m) and a wide range of surface concentrations (e.g., SURF_ppb_O3 for ozone, SURF_ug_PM25_rh50 for fine PM2.5, SURF_ug_NO2 for nitrogen dioxide, SURF_ug_SO2, SURF_ug_NH3, SURF_ug_SEASALT_F, SURF_ug_ECCOARSE for coarse elemental carbon, SURF_ug_ECFINE for fine elemental carbon, SURF_ug_PM_ASOA for anthropogenic secondary organic aerosols, SURF_ug_PM_BSOA for biogenic SOA, SURF_ug_DUST for dust, and various nitrate, ammonium, and organic/inorganic species).
- Example naming: SURF_ug_PM25_rh50 (PM2.5 with RH correction to 50%), and related SURF_ variable names listed in the dataset documentation.

## Data structure and access
- Data format: NetCDF files; data projected on a polar stereographic grid.
- Proj4 description: '+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs'.
- Compatibility: Requires a NetCDF library compatible with R, Python, and FORTRAN.
- Model and compiler: Calculations performed with FORTRAN Intel compiler 19.1.3.304 (2020); run on UKCEH POLAR cluster.

## Quality control and limitations
- QA/QC performed for 2002–2021; QA/QC reports available on request (not included in this document).
- The dataset use is at the user’s risk; no warranty is provided regarding error-freedom or fitness for specific purposes.

## Guidance for using the data
- The dataset is designed for consistent monitoring of atmospheric composition over the UK, enabling assessments of environmental health and policy performance over time.
- Users may need to configure their applications to the polar stereographic projection and NetCDF data structures described above.

## Bibliography and context
- Key references detailing model components, emissions, and validation include works by Simpson et al., Vieno et al., Skamarock et al., Ge et al., Gu et al., Jalkanen et al., and others (listed in the document).