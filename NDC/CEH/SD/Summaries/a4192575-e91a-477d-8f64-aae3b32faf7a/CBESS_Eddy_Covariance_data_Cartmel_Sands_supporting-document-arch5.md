# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Eddy covariance flux data collected at Cartmel Sands salt marsh, Morecambe, with staff responsible: Timothy Hill.
- Time period for flux measurements: half hourly means from 31/05/2013 to 26/01/2015.
- Site exposure: Cartmel Sands at Leven estuary mouth, with predominant south-westerly winds; marsh features include saltmarsh pans, tidal influence, and varied sediment.

## Observations and Location
- Location coordinates: Cartmel Sands (CS) – 54°10'40"N, 003°00'05"W.
- Site context: salt marsh, dynamic estuarine environment, exposed to tidal and wind conditions, with a 3.2 km long marsh and a 1 km width.

## Data Collection and Instruments
- Flux measurements: 10 Hz at 4.3 m on a lattice tower.
- Datalogger: Campbell Scientific CR5000.
- Gas and sonic sensors: enclosed CS LI-7500 and collocated CSAT3.
- Other measurements: 15-minute interval data for most variables; mean half-hour values calculated in Matlab.
- Environmental sensors: Vaisala MP103A for air temperature/humidity; EML ARG100 tipping bucket rain gauge for precipitation; Kipp and Zonen NR Lite for net radiation; PAR via Skye Instruments SKP215; soil temperatures with type T thermocouples.

## Variables Observed
- Air and soil temperatures: T_air, T_soil_5cm, T_soil_10cm.
- Humidity and energy/radiation: RH, Net_rad, PAR.
- Water/energy exchange: Precip, LE (latent heat flux), Fc (CO2 flux/NEE), H (sensible heat flux).
- Wind and stability: Wind_Spd, Wind_Dir, MO (Monin-Obukhov stability), u* (ustar).
- Quality and gap-filling: LE_QC, Fc_QC, H_QC, LE_Filled, Fc_Filled, H_Filled, Fc (NEE) modelled respiration (Resp).
- Data processing flags: QC flags based on gas analyser and anemometer diagnostics; data binned by radiation for QC checks; outliers flagged with QC codes.

## Data Processing, Quality Control, and Gaps
- Corrections: fluxes corrected for frequency losses and WPL; CO2 fluxes corrected for storage terms.
- QC methodology: data binned by radiation; within each bin, values beyond 3.5 SD from the mean marked; those beyond 5 SD given QC = 2; wind-shadow affected data flagged (QC = 3). QC = 0 denotes best quality data; QC = 1 marginal; QC = 2 or 3 poor/very poor.
- Gap-filling: missing data filled using the REddyProc R package, based on QC = 0 data.
- Respiration modelling: nocturnal QC = 0 CO2 flux data modelled with the Lloyd & Taylor 1994 respiration model, with a modification for tidal depth.
- Data gaps: gaps may result from sensor malfunction or power loss; NA cells indicate no data.
- Data timing: time stamps refer to the middle of the half-hour period.

## Data Formats and Structure
- Primary file format: csv.
- Dataset fields include a detailed data dictionary with: Year/Day/Month/Hour/Minute, T_air, T_soil_5cm, T_soil_10cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD, LE, LE_Filled, LE_QC, Fc, Fc_Filled, Fc_QC, H, H_Filled, H_QC, Resp, u* (ustar), MO; plus metadata like Season, Location, Site, Habitat, Quadrat Number, Scale, and additional descriptive headers.
- Field descriptions and units are specified for each variable, with sample columns for grid-like metadata (Season, Location, Site, Habitat, etc.) and measurement metadata (date/time, binning, and quality flags).

## Documentation and Metadata
- Comprehensive dataset description includes instrument types, measurement accuracies, data processing steps, QC criteria, and data provenance.
- Time conventions and data calibration details are specified to support reproducibility and reuse.

## Accessibility and Responsibilities (Data Steward Perspective)
- Clear assignment of staff responsible and explicit data processing workflows support governance and accountability.
- Detailed metadata and quality flags enhance discoverability and usability for data consumers.
- Use of standardized formats (CSV) and widely used processing tools (EdiRe, Matlab, REddyProc) facilitates interoperability across systems.
- Documentation of data gaps and corrective procedures helps users assess reliability and limitations.

## Considerations for Reuse and Limitations
- Flux data limited to May 2013–January 2015; site-specific conditions (tidal influence, marsh microtopography) may affect generalizability.
- Quality flags and gap-filled data should be used with awareness of the underlying QC processes and modeling steps.
- Data describe a complex estuarine marsh environment; users should consider spatial heterogeneity (Site/Habitat/Quadrat metadata) when aggregating or comparing with other datasets.