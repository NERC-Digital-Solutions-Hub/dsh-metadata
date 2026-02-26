# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Eddy covariance flux measurements collected at the Cartmel Sands site in Morecambe, as part of the CBESS dataset.
- Focus on coastal biodiversity and ecosystem service sustainability through flux data.

## Location and site context
- Cartmel Sands salt marsh at the mouth of the Leven estuary, eastern bank.
- Exposure to dominant south-westerly winds; marsh length ~3.2 km, width ~1 km; landward edge bounded by a railway embankment.
- Underlain by fine sandy sediments with a dendritic creek system; saltmarsh pans scattered throughout higher areas.

## Temporal coverage and sampling
- Half-hourly mean values.
- Observation window: 31 May 2013 to 26 Jan 2015.

## Variables observed and derivatives
- Atmosphere and soil: Air temperature (T_air), soil temperature at 5 cm (T_soil_5cm), soil temperature at 10 cm (T_soil_10cm), relative humidity (RH), vapour pressure deficit (VPD).
- Radiation and meteorology: Net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), Monin-Obukhov stability (MO).
- Fluxes: CO2 flux (Fc) with filled value (Fc_Filled) and quality flag (Fc_QC); latent heat (LE) with filled value (LE_Filled) and QC (LE_QC); sensible heat (H) with filled value (H_Filled) and QC (H_QC); respiration (Resp); u* friction velocity (ustar).
- Data quality and processing: Basic QC flags for fluxes (0 best to 3 very poor), WPL corrections, CO2 storage term corrections, radiation-based binning, and gap filling (REddyProc).
- Modeling: Modelled respiration (Resp) and nocturnal data used for Lloyd & Taylor 1994 respiration model with tidal-depth modification.

## Data collection and instrumentation
- Datalogger: Campbell Scientific CR5000.
- Flux instrumentation: enclosed LI-7500 and collocated CSAT3; fluxes and wind measurements at 10 Hz on a 4.3 m lattice tower.
- Data processing: EdiRe and Matlab; half-hour averages computed in Matlab.
- Supporting sensors: Vaisala MP103A for air temperature/humidity; EML ARG100 tipping-bucket rain gauge for precipitation; Kipp and Zonen NR Lite for net radiation; Skye Instruments SKP215 for PAR; T-type thermocouples for soil temperatures.
- Time reference: mid-point of the half-hour period (e.g., 00:15 for 00:00–00:30).

## Data handling, quality control, and gap filling
- Flux data corrected for frequency losses (WPL) and CO2 data corrected for storage terms.
- Data binned by radiation into 15 bins; outliers within bins flagged (QC=1 or 2); data affected by tower wind shadow flagged (QC=3); QC=0 indicates best data.
- Gaps filled using REddyProc R package, applied to QC=0 data.
- Respiration modeled from nocturnal QC=0 CO2 flux data with modification for tidal depth.

## Data formats and metadata
- File format: CSV.
- Dataset includes a comprehensive field description dictionary detailing variable names, units, and data types (e.g., Year, Day, Month, Hour, T_air, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD, LE, Fc, H, Resp, u*, MO, QC flags, and filled counterparts).

## Spatial and dataset scope for GIS use
- Spatial scope limited to Cartmel Sands, Morecambe, with explicit site location coordinates provided for Cartmel Sands.
- Data suitable for map-based visualisations of energy and carbon fluxes, land-atmosphere interactions, and coastal wetland processes.
- Includes quality flags and gap-filled values to support reliable spatial analyses and temporal trend mapping.