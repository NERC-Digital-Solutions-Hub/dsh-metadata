# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

- Purpose and scope
  - Provides daily averaged atmospheric composition for the UK (2002–2021) for main nitrogen, sulphur, particulate organic matter, and ozone.
  - Data produced with EMEP4UK model rv4.36 and WRF model v4.2.2; daily averaged outputs included.

- Experimental design and data sources
  - EMEP4UK rv4.36: atmospheric chemistry transport model derived from EMEP MSC-W rv4.36.
  - Meteorology: 3D fields from WRF v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°×1° every 6 hours.
  - Domains: EU domain at 27×27 km2 with nested UK domain at 3×3 km2; only UK domain results are included.
  - Emissions inputs: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from 2019 NAEI; non-UK emissions from CEIP (0.1° × 0.1°). 2020–2021 emissions use 2019 values.

- Data products and content
  - Daily averaged surface concentrations and fluxes for pollutants (e.g., NOx, NH3, SO2, PM2.5, PMcoarse, PM10, O3, VOCs, etc.).
  - Surface concentration variables defined for multiple species (e.g., SURF_ug_PM25_rh50, SURF_ppb_O3, SURF_ug_NO2, SURF_ug_SO4, SURF_ug_NH3, SURF_ug_NH4_F, etc.).
  - PM definitions: PM2.5 (aerodynamic diameter < 2.5 µm), PMcoarse (2.5–10 µm), PM10 = PM2.5 + PMcoarse.
  - Other surface variables include mixing layer height (HMIX, m), near-surface dust (SURF_ug_DUST, µg m-3), black carbon, organic matter from biomass burning, secondary organic aerosols, ammonium, nitrate species, sea salt, and related components.
  - Units and NetCDF naming are detailed in the documentation; data described as surface concentrations in µg m-3, ppbv for O3, etc.

- Grid, projection, and data format
  - Data projected on a polar stereographic grid; proj4 description provided (stereographic projection with specific parameters).
  - NetCDF format; requires NetCDF library compatible with R, Python, FORTRAN, etc.
  - UK domain resolution: 3×3 km; EU domain resolution: 27×27 km.

- Data structure and example
  - Example given for SURF_ug_PM25_rh50 (structure shown as NetCDF variables per field); outputs are daily averages for the UK domain.

- Quality control and usage notes
  - QA/QC performed for 2002–2021; QA/QC reports available on request (not included in this document).
  - Use of dataset is at your own risk; no warranty or guarantee of error-free content or fitness for purpose.

- Guidance for use
  - Guidance provided to help users integrate the data into applications; the dataset is suitable for analyses of daily atmospheric composition over the UK, trends, and model-observation comparisons.

- Access, citation, and references
  - Bibliography includes key technical descriptions, evaluations, and related methodological studies (e.g., Simpson et al., Vieno et al., Skamarock et al., Ge et al., Gu et al., Jalkanen et al.).
  - Emphasizes proper citation of the EMEP4UK/UK-SCAPE model outputs when used in research or policy contexts.