# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Provides eddy covariance flux measurements at Cartmel Sands salt marsh to support studies of coastal biodiversity and ecosystem service sustainability.
- Location: Cartmel Sands, at the mouth of the Leven estuary, eastern bank; exposed to dominant southwest winds; 3.2 km long, 1 km wide; bounded by a railway embankment.
- Observation period and cadence: half-hour mean values from 31 May 2013 to 26 Jan 2015.
- Monitoring setup: fluxes and wind measured on a 4.3 m lattice tower; instruments include a Campbell Scientific CR5000 datalogger, a collocated LI-7500 provider, and a CSAT3 sonic anemometer.

## Observed variables and parameters
- Meteorological and environmental: Air temperature (T_air), soil temperature at 5 cm (T_soil_5cm) and 10 cm (T_soil_10cm), Relative Humidity (RH), Net Radiation (Net_rad), Photosynthetically Active Radiation (PAR), Precipitation (Precip), Wind Speed (Wind_Spd), Wind Direction (Wind_Dir), Vapour Pressure Deficit (VPD).
- Fluxes and processes: CO2 Flux (Fc) and Gap-Filled Fc (Fc_Filled), Latent Energy (LE) and Gap-Filled LE (LE_Filled) with quality flags (LE_QC), Sensible Heat (H) and Gap-Filled H (H_Filled) with quality flags (H_QC), Modelled Respiration (Resp), U* friction velocity (ustar), Monin-Obukhov stability (MO).
- Data quality and processing flags: Quality Control Flags for Fc (Fc_QC) and others as applicable (QC values: 0 best, 1 marginal, 2 poor, 3 very poor).

## Data collection, processing, and quality control
- Instrumentation and data collection: Fluxes and wind at 10 Hz; other variables typically at 15-minute intervals; data averaged to half-hour means (time reference is the middle of the half-hour period).
- Processing and corrections: Fluxes corrected for frequency losses and Webb-Peltier-Law (WPL) corrections; CO2 fluxes corrected for storage terms; respiration model fitted to nocturnal QC=0 data with Lloyd & Taylor (1994) framework, adapted for tidal depth.
- Data handling and QC: Flux data are binned by radiation; outliers beyond 3.5 SD within bins receive QC=1, beyond 5 SD receive QC=2; data affected by tower wind shadow receive QC=3; QC=0 denotes best data.
- Gap filling: Gaps filled using the REddyProc gap-filling package, applied to QC=0 data only.
- Data integrity: Gaps may occur due to sensor malfunction or power loss; NA indicates no data; time references and sensor calibration details are documented.

## File formats, metadata, and dataset structure
- Primary format: CSV.
- Metadata and field descriptions: Comprehensive dataset field descriptions and codes (Season, Location, Site, Habitat, etc.) included; header and row format details provided (e.g., Year, Day, Month, Hour, Minute; various sensor and flux fields with units).
- Time stamping: Mean values correspond to the middle of the half-hour period; explicit notes on units and encoding (e.g., PAR in μmol m^-2 s^-1, Net_rad in W m^-2).
- Observational gaps and data quality: NA cells indicate missing data; gaps reflect sensor malfunctions or power interruptions.

## Site context and habitat details
- Site: Morecambe – Cartmel Sands (CS); saltmarsh habitat with pans and a network of creeks.
- Environmental setting: Coastal marsh influenced by tidal and wind conditions; underlying fine sand and compacted sediments.

## Practical considerations for analysts
- Suitable for examining correlations between meteorological conditions and carbon/energy fluxes, validating or developing predictive models of NEE, LE, and H in coastal saltmarsh environments.
- Must account for QC flags and use gap-filled data appropriately; consider restricting analyses to QC=0 data or using gap-filled variants with awareness of their uncertainties.
- Rich metadata and structured field descriptions support reproducibility and cross-site comparisons within CBESS datasets.