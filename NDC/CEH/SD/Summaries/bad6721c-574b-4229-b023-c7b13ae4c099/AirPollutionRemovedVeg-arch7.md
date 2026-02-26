# Supporting documentation for air pollution removed by vegetation in the UK 2015

## Overview
- Dataset provides 2015 UK annual average surface concentration and annual total deposition for selected pollutants, computed by the EMEP4UK atmospheric chemistry transport model (ACTM).
- Covers EU domain at 0.5° × 0.5° with a nested UK domain at ~0.055° (about 5 × 6 km); only UK model results are included.
- Recorded outputs include surface concentrations and deposition terms (dry and wet) for multiple species; time span from 2015-01-01 to 2016-01-01.

## Experimental design and domain
- Model framework: EMEP4UK rv4.10 and rv4.17, derived from the EMEP MSC-W model; meteorology from WRF v3.7.1 with 1° × 1° NWP reanalysis nudging from NCEP/NCAR GFS (every 6 hours).
- UK-specific domain: nested within EU domain, at high resolution for UK results.
- Emissions: UK emissions from NA EI (2014 for rv4.10, 2015 for rv4.17); non-UK emissions from CEIP (0.5° × 0.5°; 2014/2015 data); shipping emissions adjusted post hoc due to NMVOC/PM data gaps.
- WRF/EMEP4UK setups span six experiments (scenarios) described in related publications.

## Experiments and scenarios
- Table of six experiments with corresponding configurations:
  1) UKBASE: current vegetation, LCM2007, Soil NO as per land cover.
  2) NoVEG: no vegetation, LCM2007, Soil NO as per land cover.
  3) UrbanBASE: urban current vegetation, LCM2015, prescribed soil NO.
  4) NoUrbanVEG: no urban vegetation, NoUrbanVEG, prescribed soil NO.
  5) 25OGSC: urban 25% open greenspace conversion, 25GLC, prescribed soil NO.
  6) 50OGSC: urban 50% open greenspace conversion, 50GLC, prescribed soil NO.
- Filenames correspond to each scenario (six NetCDF files listed).

## Data files (NetCDF)
- 1. current_vegetation_land.nc
- 2. no_vegetation_land.nc
- 3. urban_current_vegetation_prescri.nc
- 4. no_urban_vegetation_prescr.nc
- 5. 25OGSC_open_greenspace_prescri.nc
- 6. 50OGSC_open_greenspace_prescri.nc

## Model and computing environment
- Model compiler: FORTRAN Intel compiler 2013_sp1.3.174.
- Computation: UKCEH computer cluster NEMSIS.
- Time stamp: NetCDF files record the end-of-run time (2015-01-01 to 2016-01-01).

## Variables, units, and data structure
- Pollutants and deposition/degradation terms include:
  - PM2.5 and PM10 (aerodynamic diameters <2.5 µm and <10 µm; separated into fine and coarse where applicable).
  - Dry deposition fields for NH3, NO2, O3, PM10, PM2.5 with representative units.
  - Wet deposition fields for NH3, NO2, PM10, PM2.5, and SO2.
  - Near-surface concentrations for O3 and various dust and ammonia species.
- NetCDF variable naming conventions (examples):
  - DDEP_NH3_m2Grid (dry deposition NH3, area-weighted)
  - SURF_ppb_O3 (near-surface ozone concentration)
  - DDEP_PM25ONS_m2Grid, DDEP_PM10ONS_m2Grid (deposition of PM2.5/PM10 without wind-blown dust)
- Time reference: end of model runs; includes data for 01/01/2015 to 01/01/2016.
- Units and variable definitions are specified within the NetCDF files (e.g., mgN/m2 for ammonia deposition; mg/m2 for O3 deposition depending on variable).

## Quality control and validation
- Validation against observed data:
  - AURN network used to verify hourly EMEP4UK output.
  - UK Met Office AWS used to verify WRF output.
  - Simple linear regression used to compare observations with base runs and experimental outputs.
- No additional QA/QC beyond the described validation; usage is at user risk with no warranty of fitness for purpose.

## GIS-ready considerations
- Spatial resolution (UK domain ~5 × 6 km) is suitable for regional mapping and assessment of vegetation-related changes in air pollution.
- NetCDF format with clearly named deposition and concentration variables enables map-based visualizations and spatial analyses in GIS.
- Six scenario files allow comparative analyses of vegetation cover and urban greenspace effects on pollutants and deposition.

## Reference context
- Model and data sources are linked to published works detailing EMEP4UK methodology, vegetation-related air quality accounting, and urban vegetation studies.
- References include Jalkanen et al. (ship emissions), Jones et al. (urban vegetation accounts), Nemitz et al. (vegetation-mediated mitigation), Saha et al. (CFSv2 data), and Simpson et al. (EMEP MSC-W model), among others.