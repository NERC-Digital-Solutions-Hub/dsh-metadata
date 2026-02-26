# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

- Scope and purpose
  - Provides daily averaged atmospheric composition for the UK for main nitrogen, sulphur, particulate organic matter, and ozone from 2002 to 2021.
  - Based on EMEP4UK model rv4.36 and WRF model v4.2.2; results pertain to the UK domain.

- Spatial and temporal coverage
  - Spatial: UK domain at 3 x 3 km2 resolution nested within a 27 x 27 km2 European domain.
  - Temporal: daily averages from 2002 to 2021 (emissions and inputs cover 2002-2021 with 2020-2021 using 2019 emissions).

- Model and data model
  - Atmospheric chemistry transport model (ACTM) derived from EMEP MSC-W rv4.36; 3D meteorology from WRF v4.2.2.
  - NWP meteorology assimilated from NCEP/NCAR GFS reanalysis at 1° x 1° every 6 hours (Newtonian nudging).

- Emissions and inputs
  - UK anthropogenic emissions: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs from 2019 NAEI; rescaled to 2002-2019 UK totals.
  - Non-UK emissions: 0.1° x 0.1° CEIP data used for all non-UK emissions; UK total used for 2002-2019.
  - For 2020-2021, 2019 emissions were used.
  - Daily EMEP emissions data integrated into the model outputs.

- Variables and units
  - Surface concentrations for a wide set of species, including:
    - Ozone (SURF_ppb_O3)
    - PM components (PM2.5_rh50, PMcoarse, PM_ASOA, PM_BSOA, PM_OM25, PM_OMCOARSE, PM_PMFINE, PM_SEASALT_F/C, PM_SEASALT_C, PM_DUST, etc.)
    - Nitrogen and sulfur species (NO, NO2, NO3_C, NO3_F, HONO, HNO3, NH3, NH4_F, ECCOARSE, ECFINE, SO2, SO4)
    - Organic matter and elemental carbon (OM, EC; EC_FINE, EC_COARSE)
    - Black carbon components (BC from biomass burning)
    - Sea salt, mineral dust, and other tracers
  - Mixing layer height (HMIX; units: m)
  - All specified in NetCDF with appropriate NetCDF variable names (e.g., SURF_ug_PM25_rh50, SURF_ug_NO2, SURF_ug_SO2, SURF_ug_NH3, SURF_ug_NH4_F, etc.).

- Projections and data access
  - Data is projected on a polar stereographic grid.
  - Proj4 string provided for GIS usage: '+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs'.
  - Data requires a NetCDF library compatible with R, Python, and FORTRAN.

- Data quality and notes
  - QA/QC performed for 2002-2021; QA/QC reports available on request (not included in the document).
  - Use of content is at user’s risk; no warranty of fitness or error-free content.

- Structure and example data
  - NetCDF data structure described; an example is provided for SURF_ug_PM25_rh50 (though the example appears truncated in the text).

- Computational and access details
  - Models compiled with the Intel FORTRAN compiler; computations run on the UKCEH POLAR cluster (CentOS 7.9).
  - Cross-domain emissions and model inputs summarized above; UK-specific results are included.

- References and bibliography
  - Key literature detailing the EMEP4UK model, WRF, emissions inventories (NAEI, CEIP), and related methodologies are cited for further context and validation.