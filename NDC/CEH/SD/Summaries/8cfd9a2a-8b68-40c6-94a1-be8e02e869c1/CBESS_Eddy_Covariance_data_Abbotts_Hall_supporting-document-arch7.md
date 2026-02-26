# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- Eddy covariance flux measurements collected at the Abbotts Hall site in Essex, part of the CBESS dataset.

## Location and Site Description
- Location: Essex, Abbotts Hall (AH); coordinates 51°47'9"N, 0°52'1"E.
- Site context: Abbotts Hall salt marsh in Salcott channel, near the Blackwater Estuary; small, restricted embayment salt marsh sheltered from SW and NE winds, connected to a network of marshes; highly dissected with dendritic drainage channels, clay and organic sediments, and evidence of internal marsh fragmentation.

## Monitoring Period
- Half-hourly mean values collected from 15 December 2012 to 27 January 2015.

## Variables Observed (Key Parameters)
- Microclimate: Air temperature (T_air), soil temperature (T_soil_10cm, T_soil_20cm, T_soil_30cm), relative humidity (RH), vapour pressure deficit (VPD).
- Radiation and energy: Net radiation (Net_rad), photosynthetically active radiation (PAR).
- Hydrology: Precipitation (Precip).
- Meteorology: Wind speed (Wind_Spd), Wind direction (Wind_Dir), Monin-Obukhov stability (MO).
- Fluxes: CO2 flux (Fc) with filled version (Fc_Filled) and quality flag (Fc_QC); Latent energy flux (LE) with filled (LE_Filled) and QC (LE_QC); Sensible heat flux (H) with filled (H_Filled) and QC (H_QC); Respiration (Resp); u* friction velocity (ustar).
- Derived/modelled: Modelled respiration (Resp) and related parameters.
- Quality control: QC flags accompany flux variables to indicate data quality levels.

## Instruments, Data Acquisition, and Processing
- Field hardware: Campbell Scientific (CS) dataloggers; CS Closed Path Eddy Covariance (CPEC200) system; CSAT3A anemometer on a 4.3 m tower.
- Data rates: Fluxes and wind velocity at 10 Hz; remaining variables at 1/60 Hz (every minute).
- Sensors: Vaisala HMP155A for air temperature/humidity; EdiRe and Matlab for flux processing; net radiation with Kipp and Zonen NR Lite; PAR with Skye Instruments SKP215; soil temperatures with CS 107 thermistors.
- Time reference: Middle of the half-hour period (e.g., 00:15 represents 00:00–00:30).
- Data processing: Half-hour means calculated in Matlab; corrections applied include frequency loss (WPL) corrections and, for CO2 fluxes, storage term corrections.
- Reference processing: Fluxes corrected for instrument biases and basic reality checks; data binned by radiation into 15 populated bins for QC.

## Quality Control, Gap Filling, and Modelling
- QC framework: Flux QC flags based on diagnostic flags from the gas analyser and anemometer; additional reality checks:
  - Within each radiation bin, fluxes more than 3.5 SD from bin mean flagged (QC = 1); more than 5 SD flagged (QC = 2).
  - Data affected by tower wind shadow flagged (QC = 3).
  - QC = 0 represents the best quality data; QC = 1 marginal; QC = 2 or 3 poor or very poor.
- Gap filling: Gaps filled using the REddyProc R package, applied to QC = 0 data.
- Modelling: Nocturnal CO2 fluxes (QC = 0) modelled using Lloyd & Taylor (1994) respiration model, applied monthly.
- Data gaps: Indicate sensor malfunction or power loss; NA cells indicate no data.

## Data Formats and Dataset Metadata
- File format: CSV.
- Data content: Includes standard fields with dataset metadata and detailed field descriptions (e.g., seasonal codes, site/habitat identifiers, spatial scales, and time components).
- Time and indexing: Row numbers provided to preserve original input order; fields include Year, Month, Day, Hour, Minute; Season and Location codes; Site and Habitat descriptors; spatial scale categories (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100 m to upper limit).
- Data caveats: Gaps due to sensor failure or power loss; NA entries indicate missing data.

## Access and Contact
- Staff responsible: Timothy Hill.