# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

## Overview
- Dataset of greenhouse gas exchange measurements (CO2 and CH4) over a plantation forest on peatland (Forsinard Flow Country, Scotland), focusing on the afforestation period.
- Site: near Forsinard Reserve, Dynk (Dyke) on peat bog; coordinates provided.
- Date range: 2016-01-01 to 2017-12-31 for meteorological and pedological data; dataset submission extends to 2018-01-01 for certain records.
- Managed by the James Hutton Institute as part of the SCO2FLUX network; funding from NERC and RESAS; originally set up by UHI with JHI and RSPB; UHI owns infrastructure; RSPB provides land access.
- Purpose aligned with data stewardship aims: enable discovery and reuse by ensuring governance, standards, and usable data products.

## Purpose and scope
- Measures land-atmosphere exchange of CO2 (net ecosystem exchange) and CH4, plus turbulence, heat fluxes, radiation, and basic meteorology/pedology.
- Includes accompanying meteorological and pedological observations.
- Data processed to produce high-quality flux estimates and gap-filled time series suitable for scientific use.

## Data products and parameters
- Key variables: NEE (CO2 exchange), CH4 concentrations, sensible heat (H), latent heat (LE), net radiation, and standard meteorological pedals (air temperature, humidity, pressure, solar radiation, precipitation, soil moisture/temperature).
- Derived metrics and processing outputs include GEP, ecosystem respiration components, and various NEE representations (e.g., VUT/Ustar-based estimates) with associated uncertainty estimates.

## File format and naming
- Format: CSV files.
- Naming convention: UK_$$$_DataProduct_%d_%m_%z.csv
  - $$$ site reference code based on Fluxnet conventions (UK_DKE for the site).
  - %d_%m_%z date of data product preparation (day, month, year in R format).
- File contents include timestamped meteorological, soil, and gas-exchange measurements with descriptive labels, units, and notes.

## Data column structure and contents
- Columns cover: TIMESTAMP (YYYY-MM-DD HH:mm), CH4, CO2, various soil heat flux channels, GPP estimates, NEE variants (including NEE_VUT_REF and NEE_VUT_USTAR with different aggregations), H and LE (gap-filled), QC flags (H_F_MDS_QC, LE_F_MDS_QC, NEE_VUT_REF_QC, etc.), NETRAD, precipitation, air pressure, PAR, solar radiation components, soil temperature and moisture, VPD, wind metrics, and associated metadata.
- Multiple representations and partitioning outputs for GPP/NEE, including daytime and nighttime methods, MEF-based estimates, and various time aggregations (05, 50, 95 percentiles where applicable).
- Data entries include descriptive metadata for each parameter (units and notes) and column labels.

## Missing values
- Missing data indicated by -9999 entries.

## Spatial coverage
- Latitude/Longitude: 58.427254, -3.96934
- OS grid reference: NC85090 50453

## Temporal coverage
- 2016-01-01 00:30 to 2018-01-01 00:00 (primary dataset window; metadata includes the 2016–2017 afforestation period)

## Data acquisition, processing, and quality control
- Experimental setup:
  - Eddy-covariance system atop a ~20 m mast, sensors at ~18 m above canopy.
  - Instruments: LI-7200 enclosed-path CO2/H2O, LI-7700 CH4, sonic anemometer, HFPs, net radiometer, soil sensors, PAR sensors, etc.
  - Power: off-grid (solar, methanol fuel cell, wind turbine).
  - Data logger: Sutron; telemetry via 4G with remote retrieval; field maintenance visits.
  - Processing: RAW data processed with EddyPRO for flux calculations; gap-filling and partitioning using REddyProc (R).
- Data collection:
  - EC data at 10 Hz; met/ped data at 10 s; half-hour aggregates stored for retrieval.
  - Pre-submission calibration: LI-7200 calibrated on 18/05/2017; other sensors not recalibrated during monitoring period.
- Quality control and data processing:
  - Flux calculations: EddyPRO with standard corrections (cosine correction, time lag removal, spectral corrections, etc.).
  - QC criteria include stationarity checks, plausible flux ranges, u* filtering, and 2D footprint analyses.
  - Gaps filled using marginal distribution sampling (MDS) and REddyProc; short gaps interpolated from biomet data; longer gaps filled via nearby sites or Kinbrace Met Office data when available.
  - Biomet, EddyPro, and REddyProc flags provided to indicate data quality and processing status:
    - Biomet Flag: codes for raw, reviewed, calibrated, interpolated gaps, modelled values, etc.
    - EddyPro Flag: 0 (best quality) to -9999 (missing period); used for general analysis versus annual budgets or discarding data.
    - REddyProc Flag: 00 (original), 01 (most reliable), 02 (medium), 03 (least reliable), -9999 (missing).
- Footprint and data reliability:
  - 2D footprint model applied; u* thresholds used to screen data.
  - Random uncertainties estimated for NEE and flux components; uncertainties explicitly reported for several NEE representations.

## Calibration and maintenance
- Calibration details:
  - LI-7200 CO2/H2O analyzer calibrated on 18/05/2017.
  - Other sensors not recalibrated during the monitoring period but reviewed across Forsinard sites for drift and fault detection.
- Ongoing quality controls align with UKCEH network standards and external methodological references.

## Governance, provenance, and accessibility
- Provenance:
  - Initiated by University of Highlands and Islands (UHI) with James Hutton Institute and RSPB; managed by JHI under SCO2FLUX; infrastructure ownership and land access arrangements clarified.
  - Data processing and archiving performed with UKCEH and established software packages (EddyPRO, REddyProc) with documented QC steps.
- Access and updates:
  - Dataset designed for discovery and reuse with documented data products and QC flags; intended for updates as part of ongoing SCO2FLUX/CentrePeat efforts.
  - Metadata includes detailed file structure, parameter definitions, units, and QC practices to support interoperability.
- Reference framework:
  - Aligns with standard micrometeorological/Data Quality control practices; references include Mauder et al., Reichstein et al., Fratini & Mauder, and related EC processing literature.

## Challenges and considerations for data stewards
- Potential gap between user needs and data products; multiple NEE representations require clear documentation for end users.
- Timeliness of data submission and standardization across diverse data streams and formats.
- Ensuring metadata completeness (units, descriptions, and QC flags) to support interoperability.
- Handling large, high-frequency datasets (eddy-covariance data) and coordinating gap-filling outputs with provenance.
- Managing reporting of uncertainty alongside flux estimates; clear guidance on flag meanings for data users.

## References
- Key methodological and quality-control references used for processing and QC, including:
  - Baldocchi (eddy covariance fundamentals)
  - Foken et al. (post-field QC, data processing)
  - Reichstein et al. REddyProc and MDS gap-filling
  - Mauder et al. (flux processing strategies)
  - Moncrieff et al. (eddy covariance measurement systems)
  - Web-based and instrument-specific calibration and standard references
- Related project and institutional references:
  - UKCEH network standards
  - JHI, UHI, RSPB, NERC, RESAS funding and governance sources