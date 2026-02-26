# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Overview
- Provides daily averaged atmospheric composition and fluxes for the UK, focusing on nitrogen, sulphur, particulate organic matter, and ozone for 2001–2015.
- Generated with EMEP4UK model rv4.17, based on the EMEP MSC-W rv4.17 chemistry-transport model and using WRF v3.7.1 for meteorology.
- Dataset intended to support environmental monitoring, evaluation, and policy performance assessments.

## Data Coverage and Content
- Spatial domain:
  - EU-wide ACTM domain at 0.5° × 0.5° resolution with a nested UK domain at ~5 × 6 km (0.05° × 0.055°); results provided for the UK portion only.
- Temporal coverage:
  - Daily averaged outputs for 2001–2015.
- Components and outputs:
  - Atmospheric composition and fluxes for key pollutants: NOx, NH3, SO2, CO, NMVOC, PM2.5, PMcoarse, PM10 (as defined within the dataset), and ozone (O3).
  - Various deposition fluxes and near-surface concentrations, including detailed deposition terms to multiple land-use types and water, as well as mixing height and several meteorological-context variables.
- Units and definitions:
  - Includes surface concentrations, dry and wet deposition, and other flux terms with clearly defined NetCDF variable names and units (e.g., PM2.5, PMcoarse, O3 deposition, etc.).

## Experimental Design and Modelling Approach
- Modelling framework:
  - EMEP4UK rv4.17 atmospheric chemistry transport model, derived from EMEP MSC-W rv4.17.
  - Meteorology from WRF v3.7.1 with data assimilation (Newtonian nudging) of NWP meteorological reanalysis from NCEP/NCAR GFS at 1° × 1° resolution every 6 hours.
- Domain and resolution:
  - EU-wide domain at 0.5° × 0.5° with a nested UK domain at ~5 × 6 km, focusing analysis on UK results.
- Emissions inputs:
  - UK emissions: 2015 National Atmospheric Emission Inventory (NAEI) estimates rescaled to 2001–2015 yearly totals.
  - Non-UK emissions: EMEP 0.5° × 0.5° emissions (CEIP v2015 for 2001–2013, v2016 for 2014, v2017 for 2015), used to allocate non-UK contributions and UK total used for year-specific scaling.
  - Shipping emissions: FMI 2011 estimates with specific rescalings for NMVOC and PM components due to data gaps (NMVOC = 0.029 × NOx; PM2.5 = 0.95 × PM; PMcoarse = 0.05 × PM).
- Emissions handling:
  - UK emissions adjusted yearly to match the 2001–2015 period; non-UK emissions sourced from CEIP; shipping emissions adjusted as described.
- Model and compute environment:
  - Fortran-based computations compiled with Intel Fortran 2013_sp1.3.174; run on the CEH NEMSIS cluster.

## Data Structure, Content, and Access
- File format:
  - NetCDF files containing a wide range of variables (surface concentrations, deposition, mixing height, ozone metrics, near-surface chemical species, etc.).
- Example variable families:
  - Surface concentrations: PM, NOx-related species, O3, NMVOC, NH3, NO2, NO, etc.
  - Depositions: dry and wet deposition of various nitrogen, sulphur, and particulate components to different land-use types and water.
  - Physical/meteorological context: mixing height, near-surface gas and particle concentrations, and related metrics.
- Documentation:
  - Supporting QA/QC information exists (QA/QC reports available on request); dataset usage carries a risk assumption and no warranty of suitability.

## Quality Control and Documentation
- QA/QC:
  - QA/QC activities performed for 2001–2015; detailed QA/QC reports are available on request.
- Disclaimers:
  - The dataset’s content is provided “as is” with no warranty; use is at the user’s own risk.
- Bibliography and references:
  - Key technical references for the EMEP4UK model, WRF, and supporting datasets are provided (e.g., Simpson et al. 2012; Vieno et al. 2016; Skamarock et al. 2019; Jalkanen et al. 2016).

## Use, Integration, and Accessibility Considerations for Analysts
- Purpose alignment:
  - Fits standardised monitoring workflows: verified data sources, quality assurance, and clear outputs (maps, charts, and reports) suitable for tracking environmental health and policy performance over time.
- Data integration:
  - Designed to be combined with other relevant datasets to maximise value beyond single-use applications (one of the stated challenges).
- Data accessibility:
  - Underlying data are versioned by emissions sources and model configuration; users can request QA/QC details and references to accessors or portals as needed.
- Reproducibility and provenance:
  - Clear description of model versions (EMEP4UK rv4.17, WRF v3.7.1), emissions inputs (NAEI, CEIP, FMI), and processing steps to support reproducibility and traceability.