# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

## Overview
- Long-term environmental dataset measuring greenhouse gas exchange (CO2 and CH4) and associated meteorological/pedological observations from a near-natural blanket bog in the Flow Country, Scotland.
- Time period: approximately 2016-10-19 to 2023-01-01 (half-hourly intervals); installation and ongoing operation supported by multiple projects and organisations.
- Purpose: provide a vital reference state and target measurements to evaluate other observations at nearby sites undergoing restoration from plantation forestry back to blanket bog; used within the SCO2FLUX network and linked institutions.
- Governance and support: coordinated by the James Hutton Institute with funding from NERC and RESAS; local operations by UHI; land access via RSPB; data processing and archiving through UKCEH workflows.

## What is measured (parameters)
- Land-atmosphere exchange: net ecosystem exchange (NEE) of CO2; methane (CH4) flux.
- Turbulence and energy fluxes: atmospheric turbulence, latent heat (LE) and sensible heat (H) fluxes; net radiation; eddy-covariance metrics.
- Meteorology and pedology: air temperature, relative humidity, barometric pressure, solar radiation, precipitation; soil moisture content and soil temperature; soil heat flux; water table depth.
- Derived indicators: footprint metrics (FETCH_10/30/50/70/90, FETCH_MAX); gross primary production (GPP) estimates via daytime and nighttime partitioning methods; ecosystem respiration (RECO) estimates; various VUT (variable Ustar threshold) variants; gap-filled fluxes and quality flags.

## Data structure and file information
- File format: CSV.
- File naming: UK_$$$_DataProduct.csv, site reference code based on Fluxnet conventions (UK_CLS).
- Key variables include: TIMESTAMP; CH4 and CO2 concentrations/fluxes; ET; G, GPP variants (GPP_DT_VUT_REF, GPP_DT_VUT_USTAR_05/50/95, GPP_NT_VUT_REF, etc.); NEE and NEE_VUT variants; H, LE and associated QC; NEE-related uncertainties; PPFD_IN; PA_F_NS; P_F_NS; RECO variants; flux QC flags (Biomet, EddyPro, REddyProc); and missing value indicator (-9999).

## Spatial and temporal coverage
- Spatial: exact coordinates 58.371598, -3.965194 (OS grid: NC 85220 44146); point data resolution.
- Temporal: 2016-10-19 00:30:00 to 2023-01-01 00:00 (dataset description notes 2016–2022 for the study period, with metadata extending into 2023).

## Experimental design and data collection
- Setup: sensors mounted on ~3 m tripod masts on a flat expanse of intact blanket bog; minimal management influence (low-level grazing, no burning/drainage).
- Instrumentation: weather, gas exchange, and soil sensors using off-grid power (solar, methanol fuel cell, wind turbine); data logger (Campbell Scientific CR3000); remote retrieval via 4G; half-hour aggregations stored on-site.
- Gas exchange methods: eddy-covariance for CO2/H2O (IRGASON) and CH4 (LI-7700); 10 Hz sampling; processing with EddyPro; gap-filling with REddyProc.
- Additional data: soil moisture dynamics noted but pending final publication; other environmental sensors as listed.

## Data processing and quality control
- Processing workflow: raw data processed with EddyPro (v7.0.6) with standard corrections; REddyProc used for gap-filling and partitioning NEE into GEP and RECO; MDS (marginal distribution sampling) for gap-filling of fluxes.
- Footprint and data quality: 2D footprint model used; QC includes outlier screening, stationarity checks, physically plausible value ranges, u* threshold filtering, and detailed QC flags.
- Gap-filling and partitioning: short gaps filled by interpolation of biomet observations; longer gaps filled using co-located or nearby station data; NEE partitioned into GEP and RECO using daytime/nighttime methods; annual sums enabled by short-gap interpolation.
- Data flagging:
  - Biomet Flag: indicates raw to model-filled status with codes (e.g., 00 raw, 01 primary, 02 calibrated, 13/14 gaps/interpolations, 32 modelled data, 23 interpolated from another site, 03/04 data removed).
  - EddyPro Flag: 0 = best quality, 1 = suitable for general analysis, 2 = discardable; -9999 = missing.
  - REddyProc Flag: 0 original, 1 most reliable, 2 medium, 3 least reliable, -9999 missing.
- Additional notes: soil moisture data flagged as pending a separate publication; biomet and flux data are gap-filled with associated QC metadata.

## Calibration and data integrity considerations
- 2016 refurbishment included IRGASON replacement; 2019 calibration showed no significant deviations, but recalibration was not performed due to COVID-19 within the period.
- Soil heat flux sensors changed in 2019 (five sensors installed around the flux tower); current time series reflects averaging across all five post-installation sensors.
- Calibration and sensor changes may affect continuity across the full time series and should be considered in trend analyses.

## Data governance and accessibility
- Data are produced and archived within UKCEH networks, with robust metadata, QC flags, and standard processing pipelines ( EddyPro, REddyProc ).
- Data are accompanied by extensive methodological documentation and references; soil moisture data are to be published separately, indicating ongoing data integration efforts.
- The documentation emphasizes data quality, reproducibility, and transparent data provenance to support monitoring framework use.

## Key uses for monitoring frameworks
- Evaluate long-term carbon balance and greenhouse gas flux dynamics of an intact peat bog as a reference state for restoration sites.
- Assess policy-relevant indicators (NEE, CH4 flux, GPP, RECO) and their sensitivity to environmental conditions and management actions.
- Provide high-resolution, standardized data for validation of remote sensing products, climate/land-use models, and restoration impact assessments.
- Support data governance and quality standards for environmental monitoring programs through explicit QC flags, metadata schemas, and gap-filling methodologies.

## Notes and references
- Substantial references underpinning methods and quality control (EddyPro, REddyProc, footprint modelling, etc.), alongside site-specific methodological papers and project reports.
- Collaborating organisations include NERC, RESAS, JHI, UHI, and RSPB, with UKCEH coordinating data processing and archiving.