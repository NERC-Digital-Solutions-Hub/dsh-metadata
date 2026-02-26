# Introduction This dataset provide a 2015 UK annual average surface concentration, and annual total deposition; for a selection of pollutants as calculated by an atmospheric chemistry transport model.

## What is included
- Model-generated UK-specific 2015 annual averages for surface concentrations and total deposition of multiple pollutants.
- Outputs produced by the EMEP4UK atmospheric chemistry transport model (ACTM), using WRF meteorology.
- Includes six scenario-based experiments with different vegetation/land-cover setups and emissions prescriptions.
- NetCDF data files containing a variety of deposition and concentration variables, with clear naming per scenario.

## Modelling framework and domain
- Model chain: EMEP4UK (rv4.10 and rv4.17) derived from EMEP MSC-W; hourly to annual outputs.
- Meteorology: WRF (v3.7.1) with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°x1° every 6 hours.
- Domain: EU-wide 0.5°×0.5° with a nested UK domain at ~0.055°×0.055° (about 5×6 km grid); UK results are included.
- Emissions:
  - UK: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from NAEI (2014 for rv4.10, 2015 for rv4.17).
  - Non-UK: CEIP emissions (0.5° resolution; v2016 for 2014, v2017 for 2015).
  - Shipping: FMI 2011 emissions with rescaling for NMVOC and PM (NMVOC=0.029×NOx; PM2.5=0.95×PM; PMcoarse=0.05×PM).

## Experiments and setup
- Six experiments:
  1) UKBASE: current vegetation.
  2) NoVEG: no vegetation.
  3) UrbanBASE: urban current vegetation.
  4) NoUrbanVEG: no urban vegetation.
  5) 25OGSC: urban with 25% open greenspace conversion.
  6) 50OGSC: urban with 50% open greenspace conversion.
- Model and land-cover configurations:
  - WRF: v3.7.1 for all experiments.
  - EMEP: rv4.10 (experiments 1–2) and rv4.17 (experiments 3–6).
  - Land-cover scenarios: LCM2007 (experiments 1–2) and LCM2015/25GLC/50GLC variants (experiments 3–6).
  - Soil NOx emissions: dependent on land cover (experiments 1–2) or prescribed (experiments 3–6).
- Filenames corresponding to each scenario:
  - current_vegetation_land.nc
  - no_vegetation_land.nc
  - urban_current_vegetation_prescri.nc
  - no_urban_vegetation_prescr.nc
  - 25OGSC_open_greenspace_prescri.nc
  - 50OGSC_open_greenspace_prescri.nc

## Output variables and units
- Deposition and concentration topics:
  - Dry deposition: NH3, NO2, O3, PM10 (without wind-blown dust), PM2.5 (without wind-blown dust).
  - Near-surface concentrations: O3 (surrogate SURF_ppb_O3 and related SURF_ fields), wind-blown dust, ammonia gas, NO2, biogenic SOA, PM10/PM2.5 (ONS), SO2.
- NetCDF variable naming (examples):
  - DDEP_NH3_m2Grid (dry deposition of NH3, area-weighted)
  - DDEP_NO2_m2Grid (dry deposition of NO2, area-weighted)
  - DDEP_O3_m2Grid (dry deposition of O3, area-weighted)
  - DDEP_PM10ONS_m2Grid, DDEP_PM25ONS_m2Grid (PM deposition)
  - SURF_ppb_O3 (near-surface ozone concentration)
  - SURF_ug_NH3, SURF_ug_NO2, SURF_ug_PM10ONS, etc.
- Time reference: outputs cover 01/01/2015 to 01/01/2016; NetCDF timestamps indicate end-of-model-run.
- The datasets provide comprehensive coverage of surface concentrations and various deposition pathways for listed pollutants.

## Data quality and validation
- Observational benchmarks used for QA:
  - AURN monitoring network to validate hourly EMEP4UK outputs.
  - UK Met Office AWS to validate WRF outputs.
- Validation method: simple linear regression comparing model outputs to observations for base and experimental runs.
- QA scope: limited to regression comparisons; no further QA/QC performed.
- Caution: use is at your own risk; no warranty of domain suitability or data accuracy beyond documented validation.

## Data structure and metadata
- NetCDF structure includes:
  - Example variable DDEP_NH3_m2Grid with metadata such as numberofrecords and current_date_last.
- Supporting documentation and metadata accompany the dataset to aid interpretation and usage.

## Access, usage, and provenance notes
- Data are produced with Fortran Intel compiler (2013_sp1.3.174) and run on the UKCEH NEMSIS cluster.
- Data provenance: derived from UK emissions inventories (NAEI), CEIP non-UK emissions, and FMI ship emissions; model configurations, scenarios, and filenames are clearly documented for reproducibility.
- Usage focus: enables re-use for impact assessments, policy analysis, or visualization of how vegetation, land-cover, and urban greenspace influence UK air pollution across a full year.

## References
- Jalkanen et al. (2016); Jones et al. (2019); Nemitz et al. (2020); Saha et al. (2011); Simpson et al. (2012); Skamarock et al. (2019); Vieno et al. (2016).