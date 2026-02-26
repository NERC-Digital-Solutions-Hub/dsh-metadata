# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

- The dataset provides eddy covariance flux measurements from the Abbotts Hall site in Essex as part of the CBESS program.
- Staff responsible: Timothy Hill.

## Overview
- Half-hourly mean values collected during 15/12/2012 to 27/01/2015.
- Aimed at capturing fluxes and environmental conditions in a saltmarsh ecosystem to support biodiversity and ecosystem service assessments.

## Location and Site Description
- Location: Abbotts Hall, Essex (AH) – 51°47'9"N, 0°52'1"E.
- Site context: Abbotts Hall salt marsh in Salcott Channel, ~3 km from the Blackwater Estuary; sheltered from SW and NE winds.
- Habitat characteristics: Part of a network of connected salt marshes; highly dissected with dendritic drainage channels, clay and organic sediments, and evidence of internal fragmentation.

## Data Collection Details
- Monitoring cadence:
  - Fluxes: 10 Hz (CPEC200 system with CSAT3A anemometer on a 4.3 m tower).
  - Other variables: 1/60 Hz (every minute).
  - Flux data processing: Corrected for frequency losses (WPL corrections) and CO2 fluxes corrected for storage terms; mean half-hour values calculated in Matlab.
- Instrumentation:
  - Dataloggers: Campbell Scientific (CS).
  - Flux measurement: CS CPEC200 system; CSAT3A anemometer.
  - Data loggers for other variables: CS CR3000 and CS CR1000 with multiplexer.
  - Air temperature/humidity: Vaisala HMP155A.
  - Precipitation: Environmental Measurements Limited ARG100 tipping bucket gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: CS 107 thermistors.
- Time reference: Time stamps refer to the middle of the half-hour period (e.g., 00:15 = 00:00–00:30).

## Observed Variables and Outputs
- Environmental and micrometeorological variables:
  - Air temperature (T_air), soil temperatures (T_soil_10cm, T_soil_20cm, T_soil_30cm), relative humidity (RH), vapour pressure deficit (VPD), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), monin-obukhov stability (MO), etc.
- Fluxes and related quantities:
  - CO2 flux (Fc) and gap-filled Fc (Fc_Filled), CO2 flux quality control (Fc_QC) flags.
  - Latent heat flux (LE) and gap-filled LE (LE_Filled), latent heat QC (LE_QC).
  - Sensible heat flux (H) and gap-filled H (H_Filled), sensible heat QC (H_QC).
  - Modelled respiration (Resp) and u* friction velocity (ustar).
- Quality control and data processing:
  - QC flags derived from gas analyser and anemometer diagnostics; basic reality checks via radiation-binned QC with 15 populated bins.
  - Data with QC=0 are best; QC=1 marginal; QC=2 or QC=3 poor/very poor.
  - Data gaps filled using the REddyProc R gap-filling package, applying QC=0 data.
  - Respiration modelled by Lloyd & Taylor 1994 fit to nocturnal QC=0 CO2 flux data (monthly).

## Data Processing, Quality Assurance, and Gaps
- Processing steps:
  - WPL corrections for fluxes; storage term corrections for CO2 fluxes.
  - Flux QC based on diagnostic flags and basic sanity checks.
  - Bin-based QC to identify outliers within radiation bins.
  - Gap filling using REddyProc on QC=0 data.
  - Respiration modeled from nocturnal QC=0 data per month.
- Data gaps:
  - Caused by sensor malfunction or power loss.
  - NA cells indicate no data.

## File Formats and Metadata
- Primary format: CSV.
- Dataset field descriptions and metadata:
  - Includes a wide range of fields (e.g., Year, Month, Day, Hour, Minute; T_air; T_soil_10cm; T_soil_20cm; T_soil_30cm; RH; Net_rad; PAR; Precip; Wind_Spd; Wind_Dir; VPD; LE; LE_Filled; LE_QC; Fc; Fc_Filled; Fc_QC; H; H_Filled; H_QC; Resp; ustar; MO).
  - Header and row-number conventions provided; location codes (Essex AH, etc.), habitat types (Mudflat, Saltmarsh), site and quadrat details, scale classifications (A–D), and seasonal codes (Winter, Summer).

## Practical Relevance for Data Support
- Enables end users to self-serve with:
  - Cleaned flux data with QC flags and gap-filled estimates.
  - Modelled respiration and energy balance components for saltmarsh ecosystems.
  - Timely, half-hourly to minute-level environmental context to support cross-dataset analyses within CBESS.
- Facilitates data discovery, combination with other sites/datasets, and the development of data products (dashboards, reports) for policy and science communication.
- Documentation supports data quality assessment, provenance, and reuse (instrumentation, processing steps, and metadata structure).