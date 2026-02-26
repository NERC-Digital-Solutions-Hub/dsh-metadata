# Experimental design/Sampling regime

- Overview of the modeling framework
  - EMEP4UK is an atmospheric chemistry transport model (ACTM) paired with the weather research and forecast model (WRF) to simulate hourly to annual atmospheric composition and deposition of pollutants; daily-averaged data are provided.
  - Covers anthropogenic and natural emissions; simulations include NOx, NH3, SO2, primary PM2.5, primary PM10, CO, and NMVOC, with emissions sources and resolutions described below.

- Emissions and spatial domain
  - UK emissions: from the National Atmospheric Emission Inventory (NAEI) at 1 km x 1 km, aggregated to 5 km x 5 km for the model.
  - Rest of Europe: EMEP CEIP 50 km x 50 km resolution.
  - International shipping emissions (ENTEC, 2010) aggregated to 5 km x 5 km within the British Isles domain.
  - Forest fires are included; biogenic emissions of isoprene and monoterpenes are calculated per grid cell and time-step as required.

- Model configuration and computing
  - WRF and EMEP4UK compiled with the FORTRAN Intel compiler (2013_sp1.3.174); computations run on the CEH computer cluster NEMSIS.
  - Units and species recorded in NetCDF files, representing surface concentrations such as:
    - NO, NO2, PM10, PM2.5, NH3, HNO3, SO2, NH4, TNO3, SO4, PART_OM_F, O3.
  - Temporal coverage: daily averaged outputs are documented; other timescales (hourly to annual) are described in the model setup.

- NetCDF data structure and metadata
  - Example dataset: EMEP4UK_UK_webrun_emep_4.3_2001_day.nc
    - Dimensions: time (days), i (x-grid), j (y-grid)
    - Variables include SURF_ug_SO2 and other species with units (e.g., ug/m3 for surface species; time units in days since 1900-01-01).
    - Grid: Polar Stereographic projection with associated coordinate variables i and j and transformation metadata.
    - Metadata fields include current_date_first and current_date_last to denote data coverage.
  - Data format notes: NetCDF structure is provided with explicit variable naming and coordinates to support data access and reuse.

- Quality control, verification, and caveats
  - Verification is performed by comparing model outputs with observations:
    - AURN monitoring network used to verify hourly model outputs.
    - UK Met Office AWS used to verify WRF outputs.
  - Quality assurance: simple linear regression analyses are used; no extensive QA/QC beyond this is described.
  - User caution: content is provided without warranty; data usage is at the user’s risk.

- Notable data limitations and historical notes
  - Forest fire data are only included for the years 2002–2012.
  - Emissions for 2013 and 2014 are the same as 2012.
  - WRF model versions differ by period: 2001–2012 used WRF 3.1.1; 2013–2014 used WRF 3.6.1 with changes (notably humidity nudging in the later version).
  - Documentation and metadata may contain occasional formatting inconsistencies or typos, but core structure and variables are defined.

- Practical implications for monitoring and policy evaluation
  - Provides high-resolution, model-based estimates of atmospheric composition to support monitoring and decision-making.
  - Enables comparison with observational networks and alignment with emissions inventories for policy assessment.
  - Metadata, data formats (NetCDF), and documentation support data sharing and reproducibility, though data accessibility and transformation requirements may pose challenges.
  - Transparency about limitations (e.g., years with limited data types, version changes) aids interpretation of trends and policy impact assessments.