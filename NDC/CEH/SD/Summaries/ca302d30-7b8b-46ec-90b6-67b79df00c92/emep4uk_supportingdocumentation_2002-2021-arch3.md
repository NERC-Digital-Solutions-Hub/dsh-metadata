# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

- Overview of the dataset
  - Daily averaged atmospheric composition for the UK (2002–2021) focusing on main nitrogen, sulfur, particulate matter, organic matter, and ozone.
  - Generated using the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) with the WRF model (v4.2.2) for meteorology.

- Modelling framework and data sources
  - ACTM: EMEP4UK rv4.36, derived from EMEP MSC-W rv4.36; outputs include various pollutant species and fluxes.
  - Meteorology: Weather Research and Forecasting Model (WRF) v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis (1°x1° every 6 hours).
  - Emissions:
    - UK: 2019 National Atmospheric Emission Inventory (NAEI) for NOx, NH3, SO2, primary PM2.5, primary PM coarse, CO, non-methane VOC; UK totals for each year were used to rescale 2002–2019.
    - Non-UK: CEIP EMEP emission estimates (0.1° x 0.1°) used for all non-UK emissions; 2020–2021 emissions set to 2019 levels.
  - Domain and resolution: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK domain results are included here.

- Data handling and technical setup
  - Model compilation: FORTRAN with Intel compiler (19.1.3.304, 20200925).
  - Computation platform: UKCEH POLAR cluster (CentOS 7.9, 3.10.0 kernel).
  - QA/QC: Performed for 2002–2021; QA/QC reports available on request; dataset usage is at the user’s risk with no warranty.

- Recorded variables, definitions, and units
  - Fine and coarse particulate matter definitions:
    - PM2.5: aerodynamic diameter < 2.5 µm (composed of multiple components including sulfate, nitrate, ammonium, sea salt, mineral dust, secondary organics, primary PM2.5, and select coarse fractions).
    - PMcoarse: aerodynamic diameter 2.5–10 µm.
    - PM10: PM2.5 + PMcoarse.
  - Near-surface and related atmospheric constituents (examples):
    - Ozone, dust, black carbon, organic matter, ammonium, nitrate, ammonia, nitrogen oxides, sulfur compounds, and primary/secondary PM components.
  - NetCDF variable naming and units are specified in the documentation (e.g., SURF_ug_PM25_rh50 for PM2.5 near-surface concentration; mixing layer height HMIX in meters; SURF_ppb_O3 for near-surface ozone in ppbv).
  - Projection and grid: polar stereographic projection; proj4 string provided for mapping; data is presented on NetCDF files with specific variable names and units.

- Data structure, format, and usage guidance
  - NetCDF format with a detailed mapping of variables to physical quantities and units.
  - Projection: polar stereographic grid; users may need to specify the provided proj4 string in applications.
  - Data access considerations: requires a NetCDF library compatible with R, Python, or FORTRAN; example outputs and variable definitions are included.

- Guidance, caveats, and references
  - Guidance for using the data is provided in the documentation; researchers should reference the cited literature for model descriptions and evaluation.
  - Bibliography includes key model descriptions and related air quality studies (e.g., Simpson et al. 2012; Vieno et al. 2016; Skamarock et al. 2019; Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016).

- Key takeaway for monitoring and evaluation
  - Provides a comprehensive, UK-focused, daily atmospheric composition dataset (2002–2021) suitable for monitoring policy impacts and informing future decisions, with transparent modelling choices, detailed variable definitions, and clear data provenance, while noting QA/QC limitations and the importance of data governance and data sharing considerations.