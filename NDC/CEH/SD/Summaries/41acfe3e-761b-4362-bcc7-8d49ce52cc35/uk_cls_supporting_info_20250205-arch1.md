# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

## Overview
- Long-term dataset of greenhouse gas exchange (CO2 and CH4) and associated meteorological and pedological observations.
- Half-hourly measurements from 2016-10-19 to 2022-12-31 at a near-natural blanket bog in the Flow Country, Caithness and Sutherland, Scotland.
- Site established in 2008; currently managed by the James Hutton Institute as part of the SCO2FLUX network; funded by NERC and RESAS; operational support from UHI and RSPB.
- Purpose: support assessment of observations at nearby sites and provide a reference state for restoration context.

## Parameters
- Gas fluxes and related variables: net ecosystem exchange (NEE) of CO2, CH4 fluxes, CO2 and CH4 mole fractions, turbulent fluxes (H, LE), groundwater/soil measurements, and meteorology (air temperature, humidity, pressure, solar radiation, precipitation, net radiation).
- Pedology and soil conditions: soil moisture content and soil temperature; soil heat flux.
- Derived/related metrics: evapotranspiration (ET), various gross photosynthesis/respiration estimates, footprint metrics (FETCH_10/30/50/70/90/MAX).

## File format
- CSV files.
- File naming: UK_$$$_DataProduct.csv, with site code UK_CLS according to Fluxnet conventions.

## File contents
- Columns include: TIMESTAMP (YYYY-MM-DD HH:mm), CH4 (methane concentration and flux terms), CO2 (mole fraction metrics), FCH4 (CH4 flux) and QC flags, ET, fluxes and quality flags for H, LE, NEE, NEE_VUT, RECO, GPP, PPFD, P_F_NS, RH, TA, VPD, PAR-related fields, radiative and atmospheric variables, footprint metrics, and multiple QC and gap-filling indicators (e.g., H_F_MDS, LE_F_MDS, REddyProc flags).
- Extensive metadata for each variable, including units and quality-control context.
- Missing values indicated by -9999.

## Missing values
- Missing data are marked as -9999.

## Spatial coverage
- Location: 58.371598, -3.965194 (OS grid NC 85220 44146).
- Spatial resolution: point measurements at a fixed bog site.

## Temporal coverage
- 2016-10-19 00:30:00 to 2023-01-01 00:00.

## Experimental design / sampling regime
- Instruments mounted on ~3 m tripods on a flat blanket bog with natural hydrology and limited deer grazing.
- Continuous measurements powered off-grid (12 V batteries, solar, methanol fuel cell, wind turbine).
- Gas exchange measured with eddy-covariance: IRGASON for CO2/H2O and Li-Cor LI-7700 for CH4; data logged at 10 Hz; meteorology and soil sensors sampled every 5 s; half-hourly aggregates stored for retrieval.
- Site operated with Land access by RSPB; data retrieval via 4G or monthly site visits.

## Data acquisition and processing
- Processing: EddyPro for flux calculations (30-min intervals) with standard corrections (cosine correction, time-lag removal, footprint, etc.); gaps filled with REddyProc.
- Gap-filling: marginal distribution sampling (MDS) for H, LE, and NEE; short gaps interpolated; longer gaps filled with co-located or nearby site data, Kinbrace Met Office data, etc.
- Footprints: 2D footprint model applied (Kljun et al., 2015).
- Primary software: EddyPro, REddyProc; R-based processing pipeline.

## Calibration steps and values
- IRGASON recalibrated in 2019; other sensors regularly checked for drift; some calibration gaps due to Covid-19 timeframe.
- Soil heat flux sensor changes in 2019 (increased number of plates; average time series across five sensors from 26/08/2019).

## Quality control
- Flux processing standards: Mauder et al. (2013) guidelines; rotation and cospectral corrections; lag removal; high/low frequency attenuation corrections; density corrections for H/LE/NEE.
- QC flags:
  - Biomet Flag: codes for raw, reviewed, calibrated, interpolated gaps, replaced by alternatives, modelled data, etc.
  - EddyPro Flag: 0 (best quality) to 2 (discard), with -9999 for missing.
  - REddyProc Flag: 0 original, 1 most reliable, 2 medium, 3 least reliable, -9999 missing.
- Quality screening: outlier removal (MAD), stationarity test, sensible flux ranges, u* threshold; 2D footprint filtering.
- Gap-filling and partitioning: NEE split into GEP and respiration using REddyProc; NEE gap-filled with MDS; short gaps interpolated for annual sums.

## Miscellaneous
- Biomet and flux QC flags are used to flag data quality and applicability for analysis.
- Documentation and methodology align with established field and data processing standards in eddy covariance research.
- Data provenance and processing chain are documented, with references to the underpinning literature.

## References (selected)
- Foundational methods and standards for eddy covariance processing and quality control (e.g., Mauder et al., Reichstein et al., Foken et al., Moncrieff et al., Papale et al.).
- Related studies and datasets in peatlands and Flow Country contexts (e.g., Levy & Gray; Hambley et al.; Reichstein et al.; Kljun et al.).
- Data processing and gap-filling tools: EddyPro, REddyProc, MDS methods.