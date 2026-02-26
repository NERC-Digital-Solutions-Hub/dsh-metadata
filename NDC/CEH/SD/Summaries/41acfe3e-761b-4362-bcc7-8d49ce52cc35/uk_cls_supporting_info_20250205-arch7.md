# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

- This dataset provides long-term, half-hourly measurements of greenhouse gas exchange (CO2 and CH4) and related meteorological and pedological observations from an unmodified blanket bog in the Flow Country, Caithness and Sutherland (Forsinard Flows). It supports assessment of other observations and comparisons with nearby restored or managed sites.

## Spatial and Temporal Coverage

- Spatial
  - Location: 58.371598, -3.965194 (OS grid NC 85220 44146)
  - Spatial type: point data from a single bog site in the Flow Country
- Temporal
  - Coverage: 2016-10-19 to 2022-12-31 (dataset overview); includes updates through 2023-01-01 in the table, with primary emphasis 2016–2022
  - Temporal resolution: 30-minute (half-hourly) observations

## Data Content Overview

- Core measurements
  - Land–atmosphere exchange: net ecosystem exchange (NEE) of CO2, methane (FCH4), and related atmospheric turbulence, heat fluxes (G, H, LE), net radiation
  - Gases and fluxes: CH4 mole fraction (CH4), CO2 concentration/fluxes, FCH4, FCH4_QC
  - Derived/diagnostic variables: GPP (gross primary production) at day and night partitions, RECO (ecosystem respiration), various NEE variants (including VUT methods), and H/LE gap-filled estimates
  - Footprint and footprint-related metrics: FETCH_10/30/50/70/90, FETCH_MAX
  - Environmental context: air temperature, relative humidity, pressure, solar radiation, precipitation, soil moisture, soil temperature
  - Soil/energy terms: soil heat flux (G), PAR (PPFD_IN), net radiation, VPD, wind-related variables (USTAR, etc.)
- File contents structure
  - Column headers include TIMESTAMP, descriptions, units, and notes for each variable (e.g., CH4, CO2, ET, NEE, GPP variants, RECO variants, QC flags)
  - Values missing encoded as -9999
  - Multiple quality flags per variable (Biomet Flag, EddyPro Flag, REddyProc Flag) and gap-filling indicators

## File Format, Naming, and Contents

- File format: CSV
- File naming convention: UK_$$$_DataProduct.csv
  - $$$ is a site reference code based on Fluxnet conventions (site reference: UK_CLS)
- File contents key examples
  - TIMESTAMP (YYYY-MM-DD HH:mm)
  - CH4 (nmol CH4 mol-1)
  - CO2 (µmol CO2 m-2 s-1)
  - ET (mm)
  - FCH4 and associated QC, G, GPP_DT_VUT_REF/_USTAR variants, NEE and NEE_VUT variants, RECO variants
  - Flux gaps filled and quality flags (H, LE, NEE, etc.)
  - Footprint metrics (FETCH_10, FETCH_30, etc.)
  - Biomet, EddyPro, and REddyProc QC flags with defined meanings

## Measurements and Methods

- Instrumentation (mounted ~3 m above surface)
  - Eddy-covariance gas/eddy measurements: IRGASON (CO2/H2O) and LI-7700 (CH4)
  - Sonic anemometer (IRGASON)
  - Net radiometer (Kipp & Zonen NRLite2), global solar (CMP11), PAR (SKP215)
  - Soil moisture (CS616), soil temp (105T), soil heat flux (HFP01)
  - Other environmental sensors: air temperature, RH, pressure, rainfall (RM Young), etc.
- Data acquisition and processing
  - Data acquisition: 10 Hz for gas/flux measurements; met sensors at 5 s; half-hourly values stored
  - Data transmission: remote via 4G; local site visits for retrieval
  - Processing: EddyPro for flux calculations and QC; REddyProc for gap-filling and partitioning; MDS for gap-filling of H/LE/NEE
  - Footprint analysis: 2D footprint model (Kljun et al., 2015)
- Experimental design context
  - Site represents near-ecohydrologically pristine blanket bog, with minimal direct management
  - Continuous operation supported by off-grid power (batteries, solar, methanol fuel cell, wind)

## Calibration, Quality Control, and Flags

- Calibration
  - IRGASON calibrated in 2019; other sensors regularly checked for drift against co-located instruments or nearby sites
  - Soil heat flux sensors updated in 2019 (range/variability changes)
- Quality control (QC) workflow
  - Fluxes processed with EddyPro; screening for outliers and physically implausible values
  - Corrections for instrument behavior (e.g., cospectral attenuation, time lags)
  - Stationarity tests, friction velocity (u*) thresholding, and full footprint checks
  - Gap-filling and partitioning performed with REddyProc; gap-filling of H/LE/NEE via Marginal Distribution Sampling (MDS)
- QC flags defined
  - Biomet Flag: codes indicating raw, reviewed, calibrated, interpolated gap, alternative site/instrument data, modelled data, etc.
  - EddyPro Flag: 0 (best), 1 (suitable for general analysis), 2 (discard)
  - REddyProc Flag: 0 (original), 1–3 (reliability levels)
  - Flags use -9999 for missing values where applicable

## Spatial and Data Provisions for GIS Use

- Geospatial suitability
  - Precise point location enables mapping of fluxes and footprints
  - Footprint metrics (FETCH_x) aid in understanding spatial representativeness and uncertainty
- Temporal depth
  - Long-term, semi-continuous half-hour data enable time-series mapping, trend analyses, and integration with other spatial datasets
- Data integration notes
  - Data come with extensive metadata on sensors, calibration, and processing steps
  - Data are designed for integration with other Fluxnet-style or peatland datasets, with consistent units and QC conventions

## Limitations and Considerations

- Calibration and maintenance gaps due to Covid impacts and sensor changes; some sensors not recalibrated within the dataset period
- Soil moisture dynamics are noted as undergoing review; a finalised soil moisture dataset will be published separately
- Data gaps exist and are gap-filled using established methods; users should consider uncertainties from gap-filling when mapping long-term trends

## References and provenance

- Data processing references and methodological standards for eddy covariance, QC, and gap-filling are included (EddyPro, REddyProc, MDS, and associated literature)
- Acknowledges contributing institutions and funding bodies (UKCEH, NERC, RESAS, JHI, UHI, RSPB)