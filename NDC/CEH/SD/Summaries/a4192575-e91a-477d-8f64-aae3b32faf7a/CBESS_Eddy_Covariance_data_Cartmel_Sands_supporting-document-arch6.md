# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- A dataset of eddy covariance flux measurements for the Cartmel Sands salt marsh near Morecambe, UK, covering late May 2013 to January 2015.
- Site context: Cartmel Sands salt marsh at the mouth of the Leven estuary, exposed to dominant SW winds, ~3.2 km long and 1 km wide.
- Staff: Timothy Hill.

## Observations and measurements
- Sampling cadence:
  - Fluxes: processed to half-hourly mean values.
  - Other variables: recorded every 15 minutes.
- Instruments and setup:
  - Fluxes measured with a Campbell Scientific CR5000 datalogger, using a collocated LI-7500 and CSAT3; measurements at a 4.3 m tower with 10 Hz sampling.
  - Air temperature and humidity measured with Vaisala MP103A; data converted to Vapour Pressure Deficit (VPD).
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: type T thermocouples at depths of 5 cm and 10 cm.
  - Precipitation: Environmental Measurements Limited ARG100 tipping bucket rain gauge.
- Variables observed or modeled:
  - T_air, T_soil_5cm, T_soil_10cm
  - RH, VPD
  - Net_rad, PAR, Precip, Wind_Spd, Wind_Dir
  - Latent Energy (LE), LE_Filled, LE_QC
  - CO2 Flux (Fc), Fc_Filled, Fc_QC
  - Sensible Heat (H), H_Filled, H_QC
  - Modelled Respiration (Resp)
  - U* friction velocity (ustar)
  - Monin-Obukhov stability (MO)

## Data processing and quality control
- Data processing:
  - Flux corrections: frequency losses and WPL corrections; CO2 fluxes corrected for storage terms.
  - Time alignment: half-hourly period midpoints used (e.g., 00:15 for 00:00–00:30).
  - Respiration modelling: Lloyd & Taylor 1994 model fitted to nocturnal QC=0 CO2 flux data, with a tidal-depth modification.
  - Gap filling: performed with REddyProc (R) using QC=0 data.
- Quality control (QC) framework:
  - Flux QC flags: 0 = best, 1 = marginal, 2 = poor, 3 = very poor.
  - Data binned by radiation into 15 populated bins; outliers (>3.5 SD) flagged as QC=1, (>5 SD) QC=2.
  - Wind shadow effects flagged as QC=3.
- Data reliability:
  - Only QC=0 data used for gap filling and primary analyses; gaps can occur due to sensor malfunction or power loss.
- Documentation of methods:
  - Detailed dataset field descriptions cover variable definitions, units, and coding.

## Data formats and structure
- File formats: CSV for data files.
- Data organization:
  - Dataset includes explicit headers and a row-number field to preserve original input order.
  - Metadata and field descriptions cover seasonal, locational, site, and habitat qualifiers, plus measurement and QC fields.
- Data notes:
  - Gaps and NA cells indicate missing data due to sensor issues or power interruptions.
  - Time references and units are standardized across variables.

## Coverage, location, and site details
- Location: Cartmel Sands, Morecambe (CS) – 54°10'40"N, 003°00'05"W.
- Habitat: Saltmarsh at the mouth of the Leven estuary; exposed to prevailing SW winds; includes saltmarsh pans and a crested drainage network.
- Site scope: Cartmel Sands site; related fields in dataset include broader site/habitat qualifiers and quadrat-level descriptions (e.g., quadrat numbers, scale categories).

## Additional information and usage notes
- Dataset field descriptions provide structure for parsing and analysis, including headers, cell formats, and descriptive metadata for each field.
- Data management notes emphasize the importance of considering data gaps and QC flags when using the dataset for analyses or data-product development.