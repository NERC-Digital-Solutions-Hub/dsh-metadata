# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Eddy covariance flux dataset collected at Cartmel Sands salt marsh, Morecambe, as part of CBESS.
- Timeframe: 31 May 2013 to 26 January 2015 (half-hourly means for most variables; flux data at 10 Hz).
- Purpose: support monitoring of coastal biodiversity, ecosystem services, and climate-ecosystem interactions through standardized, quality-controlled data.

## Site and Observation Context
- Location: Cartmel Sands, Morecambe; at Leven estuary mouth, eastern bank; 3.2 km long marsh with a 1 km maximum width.
- Environmental setting: exposed to dominant south-westerly winds; marsh underlain by fine sands with a dentritic creek system; presence of saltmarsh pans.
- Instrumentation and deployment: 4.3 m lattice tower; Campbell Scientific CSCR5000 datalogger with a collocated LI-7500 and CSAT3 for fluxes; wind and flux measurements at 10 Hz; remaining variables recorded every 15 minutes.

## Variables and Measurements
- Meteorological and environmental variables: Air temperature (T_air), soil temperatures (T_soil_5cm, T_soil_10cm), Relative Humidity (RH), Net Radiation (Net_rad), Photosynthetically Active Radiation (PAR), Precipitation (Precip), Wind Speed (Wind_Spd), Wind Direction (Wind_Dir), Vapour Pressure Deficit (VPD).
- Fluxes and energy balance: CO2 Flux (Fc), CO2 Flux Gap Filled (Fc_Filled), Latent Heat Flux (LE) and Gap Filled (LE_Filled), Latent Heat Quality (LE_QC), Sensible Heat Flux (H) and Gap Filled (H_Filled), Sensible Heat Quality (H_QC), Net Ecosystem Exchange (NEE) equivalents.
- Data quality and modelling: Quality Control Flags (Fc_QC, LE_QC, H_QC), Modelled Respiration (Resp), U* Friction Velocity (ustar), Monin-Obukhov stability (MO), and associated processing notes (e.g., Rc/RC corrections, storage term corrections for CO2).
- Processing and time notation: half-hour mean values for non-flux variables; 10 Hz flux measurements; 15-minute cadence for most variables; time stamps refer to the middle of the half-hour period.

## Data Processing and Quality Control
- Processing tools: EdiRe and Matlab for flux processing; REddyProc R package for gap filling.
- Corrections applied: frequency losses (WPL corrections); CO2 flux corrections for storage terms; data binned by radiation with QC logic applied within bins.
- Quality flags and outlier handling:
  - QC = 0 indicates best quality data; QC = 1 marginal; QC = 2 poor; QC = 3 very poor (e.g., wind shadow effects).
  - Outliers detected within radiation bins: data outside 3.5 standard deviations set to QC = 1; data outside 5 standard deviations set to QC = 2.
  - Wind-shadow affected data flagged with QC = 3.
- Gap filling and modelling:
  - Gap filling applied to QC = 0 data using REddyProc.
  - Respiration model: Lloyd & Taylor (1994) nocturnal respiration model fit by month, with a modification for tidal depth.
- Calibration and data checks: consistent with standard monitoring practices; detailed metadata on sensor types and calibration is included, though explicit calibration procedure flags are listed as placeholders in the dataset description.

## Temporal Coverage and Data Structure
- Spatial and temporal metadata:
  - Site: Morecambe, Cartmel Sands (CS); related site components include other CBESS sites for context (e.g., Warton Sands, West Plain) but Cartmel Sands is the primary focus here.
  - Habitat: Saltmarsh (SM); quadrats numbered 1–22 across scales A–D (1 m to 100 m+ scale descriptors) and related location qualifiers.
- Data formats:
  - Primary data format: CSV.
  - Dataset includes comprehensive field descriptions and a header/row structure to support sorting and aggregation by Year, Day, Hour, Minute, etc.
- Data gaps: gaps caused by sensor malfunctions or power losses; NA cells indicate missing data.

## Practical Considerations for Analysts
- Standardised, quality-controlled observations enable cross-site comparisons and long-term environmental monitoring for policy performance.
- Data are designed to be stored in appropriate portals and are suitable for dashboards, maps, and reports that assess coastal ecosystem function, climate interactions, and ecosystem service provision.
- Awareness of limitations:
  - Gaps due to equipment downtime and occasional data losing power.
  - QC flags indicate varying data reliability; users should filter by QC level appropriate to their analysis.
  - Gas flux data include storage-term corrections and nocturnal respiration modelling with tidal adjustments, which introduce modelling assumptions.

## Relevance to Environmental Monitoring and Policy
- Provides a robust, openly described dataset for tracking coastal ecosystem responses to environmental change.
- Facilitates evidence-based assessments of coastal biodiversity, carbon fluxes, energy balance, and ecosystem service sustainability over time.
- Encourages data accessibility and transparency by detailing data collection, processing, quality control, and gap-filling methodologies.