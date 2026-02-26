# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Provides eddy covariance flux measurements at Cartmel Sands salt marsh, Morecambe.
- Observation cadence: half-hourly means (some variables at 15-minute intervals; see details).
- Time coverage: 31 May 2013 to 26 January 2015.
- Aims to support understanding of coastal biodiversity and ecosystem service sustainability through flux data and related meteorological/soil variables.

## Location and Site Description
- Site: Cartmel Sands, Morecambe, at the mouth of the Leven Estuary on the eastern bank.
- Environmental context: exposed to dominant south-westerly winds; saltmarsh with pans scattered throughout higher areas.
- Physical characteristics: 3.2 km long, up to 1 km wide; underlain by fine sandy, compacted sediments; features a dendritic creek network and a railway embankment on the landward edge.

## Observed Variables and Data Content
- Meteorology and microclimate: air temperature (T_air), soil temperature at 5 cm (T_soil_5cm) and 10 cm (T_soil_10cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), vapour pressure deficit (VPD).
- Eddy covariance fluxes: CO2 flux (Fc) with gap-filled values (Fc_Filled) and quality control flag (Fc_QC); latent heat flux (LE) with filled values (LE_Filled) and QC (LE_QC); sensible heat flux (H) with filled values (H_Filled) and QC (H_QC); respiration (Resp) and modeled respiration components.
- Turbulence and stability: friction velocity (u* or ustar) and Monin-Obukhov stability (MO).
- Data organization: multiple dataset fields for site, habitat, season, and grid-like metadata; many variables have corresponding QC and gap-filled variants.

## Instrumentation and Measurement Details
- Datalogger: Campbell Scientific CS CR5000.
- Gas and flux instruments: collocated open-path CO2 flux measurements with a LI-7500 and a CSAT3 flux sensor.
- Measurement height and frequency: fluxes and wind at 4.3 m on a lattice tower; data captured at 10 Hz; other variables recorded at 15-minute intervals.
- Ancillary sensors: Vaisala MP103A for air humidity/temperature, EML ARG100 rain gauge for precipitation, Kipp and Zonen NR Lite for net radiation, Skye Instruments PAR sensor, type T thermocouples for soil temperature.
- Data processing: processing with EdiRe and Matlab; mean hourly/half-hourly values derived in Matlab.

## Data Processing, Quality Control, and Gap Filling
- Quality control: flux QC flags (0 = best; 1 = marginal; 2 = poor; 3 = very poor); QC applied to LE, Fc, and H.
- Data screening: data binned by radiation; within each bin, outliers beyond 3.5 SD flagged (QC=1) and beyond 5 SD flagged (QC=2); wind shadow data flagged (QC=3).
- Corrections: frequency loss corrections (WPL) applied; CO2 fluxes corrected for storage terms.
- Gap filling: missing fluxes filled using the REddyProc R package, based on QC=0 data.
- Flux modelling: nocturnal respiration modeled using Lloyd & Taylor 1994 model, with a tidal depth modification for Cartmel Sands.
- Data interpretation: basic reality checks and binning procedures applied to ensure data quality.

## Data Formats and Metadata
- File formats: CSV for data files.
- Dataset structure: detailed field descriptions covering date/time, location, site/habitat, and all measured variables (including multiple scale and season descriptors).
- Metadata features: explicit flags for quality (QC), filled values, and separate fields for observed vs. filled data; season and location codes to assist in comparative analyses.
- Data gaps: attributed to sensor malfunction or power loss; gaps explicitly noted in metadata.

## Data Availability, Limitations, and Governance
- Data are accompanied by systematic quality control measures and metadata to enable traceability and governance.
- Limitations include gaps due to instrument or power issues and the need to rely on modelled or gap-filled values for certain analyses.
- The dataset provides a transparent framework for monitoring coastal fluxes and supports integration into wider monitoring efforts (consistent with data governance and openness standards).