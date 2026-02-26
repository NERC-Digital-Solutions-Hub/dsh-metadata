# Supporting documentation for air pollution removed by vegetation in the UK 2015

- Purpose: Provides 2015 UK-specific annual averages of surface concentrations and annual total deposition for selected pollutants, as calculated by the EMEP4UK atmospheric chemistry transport model.
- Target users: Researchers and practitioners needing model-based air pollution and vegetation-related deposition assessments within the UK.

## Dataset scope and domain

- Coverage: UK domain only (EU domain at 0.5° × 0.5° with a nested UK domain at ~5 km resolution).
- Temporal extent: 01/01/2015 to 01/01/2016 (annual averages and annual deposits).
- Pollutants and outputs: Surface concentrations and deposition for multiple species (e.g., PM2.5, PM10, sulfur dioxide, nitrogen oxides, ammonia, ozone, etc.), including dry and wet deposition metrics.
- Units and definitions: 
  - Fine PM (PM2.5) and coarse PM (PMcoarse: 2.5–10 µm).
  - PM2.5 and PM10 deposition and surface concentrations expressed with specified NetCDF variable names (e.g., DDEP_NH3_m2Grid, SURF_ppb_O3, WDEP_NO2, etc.).
  - Near-surface concentrations reported in appropriate units (mgS/m2 or µg/m3 as defined per variable).
- File formats: NetCDF data files with clearly named variables and NetCDF metadata describing units and variable mappings.

## Experimental design and data sources

- Models:
  - ACTM: EMEP4UK (rv4.10 and rv4.17), derived from EMEP MSC-W.
  - Meteorology: WRF model v3.7.1 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis (1° × 1°, every 6 hours).
- Emissions:
  - UK emissions: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from NAEI (2014 for rv4.10, 2015 for rv4.17).
  - Non-UK emissions: EMEP v2016 (year 2014) and v2017 (year 2015) at 0.5° × 0.5°.
  - Shipping: FMI-derived (2011) with rescaling to NMVOC and PM to align with EMEP shipping estimates (NMVOC = 0.029 × NOx; PM2.5 = 0.95 × PM; PMcoarse = 0.05 × PM).
- Scenarios (Table 1):
  - 1) UKBASE: current vegetation; EMEP rv4.10; LCM2007; soil NO emissions per land cover.
  - 2) NoVEG: no vegetation.
  - 3) UrbanBASE: urban current vegetation; rv4.17; LCM2015; prescribed soil NO.
  - 4) NoUrbanVEG: no urban vegetation; rv4.17.
  - 5) 25OGSC: 25% open greenspace conversion; rv4.17; LCG2015; prescribed soil NO.
  - 6) 50OGSC: 50% open greenspace conversion; rv4.17; LCG2015; prescribed soil NO.
- Filenames: Six NetCDF files corresponding to the six scenarios (e.g., current_vegetation_land.nc, no_vegetation_land.nc, urban_current_vegetation_prescri.nc, etc.).

## Data processing, structure, and provenance

- Data handling:
  - Model outputs are compiled from FORTRAN-based WRF and EMEP4UK runs on the UKCEH NEMSIS cluster.
  - The time stamps in NetCDF files denote the end of the model runs.
- NetCDF data structure:
  - Variables include dry deposition, near-surface concentrations, and deposition fluxes for multiple species.
  - Examples shown: DDEP_NH3_m2Grid, DDEP_NO2_m2Grid, DDEP_O3_m2Grid, DDEP_PM10ONS_m2Grid, DDEP_PM25ONS_m2Grid, SURF_O3, SURF_NH3, SURF_NO2, SURF_PM10ONS, SURF_PM25ONS, SURF_SO2, WDEP_NH3, WDEP_NO2, WDEP_PM10ONS, WDEP_PM25ONS, WDEP_SO2, etc.
  - NetCDF metadata includes number of records and current_date_last for traceability.
- Documentation and references:
  - Publications describing model setups and applications cited (Jones et al., 2019; Nemitz et al., 2020; Simpson et al., 2012; Skamarock et al., 2019; Saha et al., 2011; Vieno et al., 2016; Jalkanen et al., 2016).

## Quality control, limitations, and use cautions

- QA approach:
  - Model outputs are validated against observational datasets:
    - AURN monitoring network for hourly EMEP4UK output.
    - UK Met Office AWS for WRF output.
  - Simple linear regression is used to compare model vs. observations for base and experimental runs.
- Limitations and risk disclosures:
  - No additional QA/QC beyond the described validation.
  - Use of content is at the user’s own risk; no warranty or guarantee of correctness or fitness for a particular purpose.
  - Some data components rely on legacy or non-interoperable data sources and bespoke processing (e.g., NMVOC/PM rescaling for FMI shipping data).
- Data availability and updates:
  - Six predefined scenario files are provided; the document does not specify an ongoing update mechanism beyond these runs.
  - Embargoes or access restrictions are not described; however, users should refer to the provided metadata and references for appropriate interpretation.

## Metadata, governance, and reuse considerations for Data Stewards

- Provenance and versioning:
  - Clear versioning via rv4.10 and rv4.17 model iterations; domain and land-cover variants noted per scenario.
  - Documentation aligns each scenario with exact WRF/EMEP4UK configurations and land-cover inputs.
- Metadata coverage:
  - Detailed description of model domains, resolutions, emissions data sources, and scenario definitions.
  - File naming conventions and NetCDF variable mappings are specified to aid discoverability and interoperability.
- Documentation on limitations:
  - Explicit QC approach and caveats included; models are validated but not guaranteed to be error-free.
  Data stewards should:
  - Ensure metadata remains synchronized with any future model updates.
  - Provide guidance on interpreting units, variable names, and scenario context for end users.
  - Highlight that usage should consider the governance statements and warranty disclaimer.
- References for reproducibility and context:
  - Core methodology and validation publications listed (e.g., Jones et al. 2019; Nemitz et al. 2020; Simpson et al. 2012; Skamarock et al. 2019; Saha et al. 2011; Vieno et al. 2016).