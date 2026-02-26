# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

## Overview
- Time series dataset of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil physics data.
- Collected at five eddy covariance (EC) flux tower sites across southeast England.
- Subset extracted from longer-term data for the HyTES_Campaign_Summer_2019_Calibration Dataset during the Copernicus High Spatio-Temporal Resolution Land Surface Temperature Monitoring mission.
- Flight campaign: HyTES airborne imaging spectrometer flown over EC sites on a UK Twin Otter aircraft on 2019-06-28 to 2019-06-29.
- Primary use: calibration/validation context for remote sensing data and surface flux studies.

## Study sites
- Five EC sites included: three croplands (two on clay soils, one drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
- Coordinates are not provided in the dataset for security reasons; can be obtained by contacting the dataset author.
- Sites linked to ASSIST and UK-SCAPE flux tower programs; additional COSMOS-UK meteorological/soil data contributed for one site.

## Sampling regime
- Automated measurements of fluxes, meteorology, and soil physics from 2019-06-22 00:30 to 2019-07-06 00:00.
- Flux data: open-path EC systems measuring three wind components, sonic temperature, and CO2/H2O mixing from a LI-7500 IRGA at 20 Hz, logged with a CR3000 logger.
- Measurement heights vary by site (2.0–5.0 m) with specified offsets between sensor centers.
- Ancillary data: air temperature, relative humidity, barometric pressure, net radiation and components, soil heat flux, soil moisture and temperature, precipitation, all logged at 0.1 Hz and averaged to 30-minute means.

## Flux data processing
- Processing with EddyPRO v6.1, including quality control, coordinate rotation, tilt corrections, cospectral corrections, and density corrections for heat/moisture fluxes.
- Wind speed and direction computed at EC measurement height.
- QC includes removal of outliers, tests for EC method validity, footprint analysis to ensure representativeness (>80% flux originating from target ecosystem), and manual checks via weekly plots.
- Footprint evaluation performed using the ART Footprint Tool and a non-neutral atmosphere model (Kormann & Meixner 2001).
- Data gaps and quality flags documented for each flux.

## Data gap-filling and flux partitioning
- Gap filling for LE and H using Marginal Distribution Sampling (MDS) via REddyProc in R.
- Gap filling performed on the complete site time series before extracting HyTES campaign data.

## Details of data structure
- Time series provided as separate CSV files per site.
- Time range: 2019-06-22 00:30 to 2019-07-06 00:00.
- Missing records denoted by -9999.
- Variables include LE, H, G1/G2 (soil heat flux), TA, VPD, RNET, SWIN/LWIN/SWOUT/LWOUT, PA, P, RH, WS, WD, TS, VWC, etc., with corresponding QC flags.
- QC flags indicate data quality: 0 = high quality observed, 1 = gap-filled good quality, 2 = gap-filled acceptable, 3 = gap-filled poor.

## Nature and units of recorded values
- Fluxes: LE and H in W/m^2; G1/G2 in W/m^2.
- Meteorology/soil: TA (°C), VPD (hPa), RNET (W/m^2), SWIN/LWIN/SWOUT/LWOUT (W/m^2), PA (kPa), P (mm per 0.5 hour), RH (%), WS (m/s), WD (degrees), TS (°C), VWC (% vol), etc.
- TIME_START/TIME_END mark observation window; included as part of the dataset metadata.

## Acknowledgments
- Data collection supported by UK Natural Environment Research Council (NERC) awards NE/R016429/1 and NE/N018125/1; ASSIST and COSMOS-UK contributions acknowledged.
- Dataset authors thank landowners and site managers for access and permission.

## References
- Key methodological and data processing sources for QC, eddy covariance processing, footprint analysis, and REddyProc gap-filling are cited (e.g., Foken et al., Reichstein et al., Moncrieff et al., Schotanus et al., Webb et al., etc.).