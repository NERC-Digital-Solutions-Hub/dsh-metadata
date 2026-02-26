# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- Eddy covariance flux data collected at Abbotts Hall salt marsh, Essex, within Salcott channel, near the Blackwater Estuary.
- Purpose: long-term monitoring of environmental conditions and carbon fluxes to support assessment of ecosystem sustainability and policy-relevant environmental health.
- Observation period: half-hourly means from 15 December 2012 to 27 January 2015.
- Location context: Sheltered, dendritic saltmarsh with clay/organic sediments; part of a network of connected marshes.

## Monitoring details
- Site: Abbotts Hall (AH), Essex.
- Instrumentation: Campbell Scientific data loggers; Closed Path Eddy Covariance (CPEC200) system with CSAT3A anemometer on a 4.3 m tower; data processed with EdiRe and Matlab; additional variables recorded at 1/60 Hz by a CR1000 with multiplexer.
- Measurements and resolution:
  - Fluxes and wind velocity at 10 Hz; most other variables at 1/60 Hz (every minute).
  - Half-hourly mean values computed in Matlab; times refer to the middle of the half-hour period.

## Variables observed
- Meteorological and micrometeorological: air temperature (T_air), relative humidity (RH), vapour pressure deficit (VPD), wind speed (Wind_Spd), wind direction (Wind_Dir), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip).
- Soil: soil temperature at 10 cm, 20 cm, 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm).
- Fluxes and energy: CO2 flux (Fc) and gap-filled Fc (Fc_Filled), latent energy (LE) and filled LE (LE_Filled) with QC flags (LE_QC), sensible heat (H) and filled H (H_Filled) with QC flags (H_QC), stored CO2 flux corrections, modelled respiration (Resp), u* friction velocity (ustar), Monin-Obukhov stability (MO).
- Quality control: QC flags accompany flux variables (0 = best, 1 = marginal, 2 = poor, 3 = very poor for some; 0-3 scheme also applied to others).
- Processing details: Fluxes corrected for frequency losses and WPL (wavelength/phase) corrections; CO2 fluxes corrected for storage terms.

## Data processing and QC
- Gap filling: conducted using the REddyProc R package, applied to data with QC = 0.
- Outlier handling: within radiation-based bins (target ~15 populated bins); data beyond 3.5 SD within a bin flagged as QC = 1, beyond 5 SD flagged as QC = 2; data affected by tower wind shadow flagged as QC = 3.
- Respiration modelling: Lloyd & Taylor 1994 respiration model fitted to nocturnal QC = 0 CO2 flux data on a monthly basis.
- Data quality and lineage: QC flags derived from gas analyser and anemometer diagnostics; basic reality checks via binning and standard deviation criteria; data ensured to be representative of valid measurements.

## File formats and metadata
- File format: CSV.
- Metadata and field descriptions: extensive, including detailed column definitions (e.g., T_air, RH, Net_rad, PAR, Precip, LE, Fc, H, QC codes, etc.).
- Data gaps: caused by sensor malfunction or power loss; NA cells indicate no data.
- Data description structure: header and row formats include field descriptions, units, scales, and nominal ordering for sorting.

## Calibration, data checks, and availability
- Calibration procedures and quality control procedures are described within the QC framework (see details under data checking/quality control).
- Data are stored and prepared for upload to appropriate data portals as part of standard monitoring activities.

## Habitat and site context
- Habitat: Saltmarsh (SM) within an embayment; small restricted area with dendritic drainage features.
- Site description: Described sediment types (clay/organic matter) and marsh fragmentation; sheltered by SW and NE wind directions.