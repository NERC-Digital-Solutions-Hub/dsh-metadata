# Supporting documentation for air pollution removed by vegetation in the UK 2015

- Purpose and scope
  - Provides 2015 UK annual average surface concentrations and annual total deposition for a selection of pollutants, as calculated by the EMEP4UK atmospheric chemistry transport model (ACTM).
  - Designed to support assessment of air pollution and the influence of vegetation on pollutant removal.

- Model and data generation
  - Model: EMEP4UK (rv4.10 and rv4.17), derived from EMEP MSC-W; uses hourly to annual averages.
  - Meteorology: 3D WRF with data assimilation (NCEP/NCAR GFS reanalysis) at 1° resolution, with a UK nested domain at ~5 km (0.055°) resolution.
  - Emissions: UK domain from NAEI (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC); non-UK EMEP emissions (v2016 for 2014, v2017 for 2015); shipping emissions from FMI (2011) with NMVOC and PM rescaling.
  - Time frame: Annual data for 2015 (calendar year 01/01/2015 to 01/01/2016 end times).
  - Output products: NetCDF files detailing surface concentrations and deposition fluxes; units defined per variable (e.g., DDEP_NH3_m2Grid for dry deposition of NH3, SURF_ppb_O3 for near-surface ozone, etc.).

- Experiments / scenarios
  - 6 land-cover and vegetation scenarios to test impacts on pollution:
    - 1 UKBASE: current vegetation
    - 2 NoVEG: no vegetation
    - 3 UrbanBASE: urban current vegetation
    - 4 NoUrbanVEG: no urban vegetation
    - 5 25OGSC: urban with 25% open greenspace conversion
    - 6 50OGSC: urban with 50% open greenspace conversion
  - Each scenario uses corresponding WRF/EMEP versions and land-cover assumptions; soil NO emissions are either land-cover dependent or prescribed.

- Output data and structure
  - Filenames (six NetCDF files) corresponding to each scenario:
    - current_vegetation_land.nc
    - no_vegetation_land.nc
    - urban_current_vegetation_prescri.nc
    - no_urban_vegetation_prescr.nc
    - 25OGSC_open_greenspace_prescri.nc
    - 50OGSC_open_greenspace_prescri.nc
  - Variables include dry deposition (NH3, NO2, O3, PM10, PM2.5), near-surface concentrations (O3, NO2, NH3, PM indicators, dust), and wet deposition terms (NO2, NH3, PM, SO2, etc.).
  - NetCDF time stamps mark the end of model runs: 01/01/2015 to 01/01/2016.
  - Example variable: DDEP_NH3_m2Grid (dry deposition of ammonia); dataset documents units and NetCDF naming conventions.

- Quality control and validation
  - Validation against observations:
    - AURN monitoring network used to verify hourly EMEP4UK outputs.
    - UK Met Office AWS used to verify WRF outputs.
  - Evaluation method: simple linear regression comparing model results to observations for base runs and experiments.
  - Limitations: no additional QA/QC beyond the described validation; content is used at user’s own risk with no warranty of fitness for purpose.

- Data provenance and referencing
  - Experimental and methodological details described in related publications:
    - Jones et al. 2019 and Nemitz et al. 2020 for vegetation/urban scenarios.
    - Simpson et al. 2012; Saha et al. 2011; Skamarock et al. 2019; Vieno et al. 2016 for model and data framework.
  - Supporting references include Jalkanen et al. 2016 (shipping emissions), among others.

- Practical use for Analysts Monitoring the Environment
  - Delivers standardized, model-derived indicators of UK air pollution concentrations and deposition across multiple vegetation/land-cover scenarios.
  - Facilitates monitoring of environmental health indicators and policy performance related to urban greenspace and vegetation in pollution mitigation.
  - Enables integration with other datasets to enhance value (e.g., combining with vegetation removal/remediation data or health outcomes); underlying emission inputs are catalogued for traceability.
  - Outputs are stored as NetCDF files suitable for mapping, time-series analysis, and cross-scenario comparisons, with clear variable definitions and unit conventions.

- Access and usage considerations
  - Outputs are designed for use within standard environmental monitoring workflows, with explicit data provenance and scenario documentation.
  - Users should consider the stated QA limitations and rely on the embedded validation when interpreting results.
  - The dataset emphasizes transparency of data sources, modelling framework, and scenario design to support scrutiny of environmental health assessments over time.

- References
  - Jalkanen, Johansson, and Kukkonen (2016)
  - Jones et al. (2019)
  - Nemitz et al. (2020)
  - Saha et al. (2011)
  - Simpson et al. (2012)
  - Skamarock et al. (2019)
  - Vieno et al. (2016)