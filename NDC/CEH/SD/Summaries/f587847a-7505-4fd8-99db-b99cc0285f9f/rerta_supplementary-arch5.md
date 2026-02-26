# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Purpose and scope
- Investigates greenhouse gas (GHG) fluxes (N2O and CH4) under four riparian buffer treatments in oil palm plantations in Riau, Indonesia.
- Part of the Riparian Ecosystem Restoration in Tropical Agriculture (RERTA) project within BEFTA; aims to inform oil palm management and policy on environmental impacts of riparian management.
- Study site: Ujung Tanjung estate (one of two RERTA sites; Kandista and Ujung Tanjung), with measurements spanning 2019–2021.

## Experimental design
- Setup: Four treatment zones along a river, each 50 x 400 m, on plots slated for replanting.
- Treatments (per side of river):
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, 50 m buffer of mature oil palm
  3) Native trees – enrichment planting with forest trees in a 50 m buffer, mature palms removed
  4) Mature oil palm and native trees – enrichment planting with forest trees in a 50 m buffer, mature palms maintained
- Replication: Six replicates per treatment plus 16 samples in surrounding plantation; 40 static chambers installed overall (one per chamber ID) for GHG measurements.

## Field collection and laboratory instrumentation
- Chamber setup: 40 cm diameter collars inserted ~7 cm into soil; lids used to seal for sampling; sampling at 0, 15, 30, 45 minutes over a 45-minute incubation.
- Gas analysis: Air samples analyzed at UKCEH Edinburgh using GC with μECD for N2O and FID for CH4 and CO2; concentrations calibrated with four-point mixed gas standards.
- Ancillary measurements: Volumetric soil moisture measured concurrently around each chamber (Theta probe).
- Permits: Foreign Research Permit Division approvals (RISTEK) for 2019 and 2020 (two permit numbers provided).

## Analytical methods and quality control
- Flux calculation: Use of the RCFlux R package to fit six models and select the best-fit flux per chamber (expressed as μmol m^-2 s^-1); 95% confidence intervals reported to indicate uncertainty.
- Calibration: Four-point calibration every ~20 samples; standards provided CH4, CO2, and N2O concentrations.
- Quality control: Visual inspection of regression plots; data points flagged as invalid/valid; outliers retained if not clearly unreliable; most data analyzed with linear or HM(R) models as best-fit.

## Data outputs and structure
- rerta_ghg_rcflux.csv
  - Contains flux estimates for each chamber (1–40) across sampling occasions (monthly Jan 2019–Sep 2021).
  - Columns document: gasName, multiple flux estimates (linear, quadratic, 2nd linear, 2nd quadratic, asymptotic, HMR, best-fit), 95% CIs, model codes, year/month/day, chamber IDs, spatial metadata (position, plot, treatment_zone, treatment, date_installed, soil_moisture, chamber dimensions, area, volume, latitude, longitude, elevation), and data quality flags.
- rerta_chambers.csv
  - Metadata for the 40 chambers (RERTA_code, position, plot, treatment_zone, treatment, date_planted, date_installed, lat, lon, elev).
  - Includes chamber-specific descriptors (inside/outside circle, distance from treatment, etc.) to contextualize sampling location.

## Data provenance and governance
- Data lineage: Volumetric soil moisture and chamber-based gas concentrations collected and processed into flux estimates; regression-based flux modeling chosen by best fit.
- Data availability and structure: CSV files with clearly defined columns and units; supports traceability from raw samples to final flux estimates.
- Access and reuse: Data documented with methodological details (sampling protocol, calibration, QC, RCFlux usage) and metadata fields enabling discovery, interoperability, and re-use in related studies of riparian buffers and GHG emissions.
- Permissions: Project conducted under Indonesian research permits; dataset includes permit references for 2019 and 2020.

## Data limitations and considerations
- Temporal interruptions: Breaks in sampling due to felling/replanting (April 2019–October 2019) and COVID-19 restrictions (Jan 2021–June 2021) create gaps in time series.
- Uncertainty: Flux estimates include 95% confidence intervals; some data points may be excluded as invalid based on sampling or quality checks.
- Scope: Focused on four riparian treatments at one estate (within the Ujung Tanjung site), measures CH4, N2O, and CO2 fluxes using static chamber techniques.

## Implications for data users and governance
- Provides a benchmark dataset linking riparian restoration strategies with soil GHG fluxes in oil palm landscapes, useful for life-cycle assessments and policy deliberations on riparian buffer regulations.
- Rich metadata enables reproducibility of flux calculations, calibration, and QA/QC processes; supports data stewardship best practices for large, multi-year environmental datasets.
- Highlights the importance of documenting experimental treatments, sampling schedules, and site-specific factors (soil moisture, chamber specs) for proper data discovery and reuse. 

## References (contextual)
- Foundational methodological and contextual literature on riparian buffers, oil palm environmental impacts, and flux measurement techniques referenced in the study (e.g., works by Drewer et al., Luke et al., Sayer et al., Williamson et al., Levy et al.).