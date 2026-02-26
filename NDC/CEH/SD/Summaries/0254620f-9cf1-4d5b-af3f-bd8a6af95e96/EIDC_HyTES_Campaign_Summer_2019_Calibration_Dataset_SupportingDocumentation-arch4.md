# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

## Purpose and context
- Calibration dataset for the Net-Sense/HyTES campaign under the Copernicus Candidate High Spatio-Temporal Resolution Land Surface Temperature Monitoring (LSTM) mission.
- Captures time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE) plus supporting meteorological and soil physics data.
- Campaign conducted in June 2019 (June 28–29) with the HyTES airborne imaging spectrometer flown over five eddy covariance (EC) sites on a BAS Twin Otter aircraft.

## Study sites and data collected
- Five EC flux tower sites across southeast England.
- Land cover: three croplands (two on clay soils, one drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
- Site coordinates not provided in the dataset for security reasons; can be obtained by contacting the dataset authors.
- Instruments and sensor suites summarized in Table 1, covering flux towers and ancillary meteorological/soil sensors at each site.

## Sampling regime and instrumentation
- Automated measurements span 2019-06-22 00:30 to 2019-07-06 00:00.
- Flux data: turbulent flux densities of H and LE measured above canopy with open-path EC systems (high-frequency data at 20 Hz); measurement heights vary by site (2.0–5.0 m).
- Ancillary data: air temperature, relative humidity, barometric pressure, net radiation and components (SWin, SWout, LWin, LWout), soil heat flux at 0.03 m, soil moisture (VWC) and temperature (Ts) at 0.1 m, precipitation, and wind characteristics.
- Data are scanned at 0.1 Hz and summarized as 30-minute means, with -9999 indicating missing data.

## Data processing and quality control
- Flux processing with EddyPRO Version 6.1, including:
  - QC of raw 20 Hz data
  - Angle-of-attack correction for sonic anemometers
  - 2D coordinate rotation to align with local terrain
  - Corrections for cospectral attenuation and density effects
  - Height-matching of wind variables
- QC procedures:
  - Outlier removal via median absolute deviation
  - Non-stationarity filtering
  - Footprint assessment; fluxes considered representative if >80% originate within the target ecosystem
  - Weekly visual checks; clearly erroneous values removed
- Data gap-filling and partitioning:
  - Gaps in EC data (LE, H) filled using Marginal Distribution Sampling via REddyProc
  - Gap-filling performed on complete site time series before HyTES data extraction

## Data structure and metadata
- Data delivered as five separate CSV files, one per EC site.
- Time range: 2019-06-22 00:30 to 2019-07-06 00:00.
- Missing records denoted by -9999.
- Variables (examples): TIME_START, TIME_END, LE (W/m^2) with LE_qc, H (W/m^2) with H_qc, G1 (W/m^2), TA (°C) with TA_qc, VPD, RNET, SWIN, SWOUT, LWIN, LWOUT, PA (kPa), P (mm/0.5 h), RH (%), WS (m/s), WD (degrees), TS (°C), VWC (%vol), TS, etc., each with corresponding QC flags. A full description of variables and units is provided in Table 2.
- Metadata and data lineage documented, including processing steps and references for algorithms and tools used.

## Data quality, provenance, and access
- Acknowledgments note NERC award support (NE/R016429/1; ASSIST/UK-SCAPE) and COSMOS-UK data contributions.
- Coordinates withheld for security; access to location information available via author contact.
- The dataset is presented as a calibration resource for the HyTES campaign, with detailed provenance from raw flux and ancillary data through QC, processing, and gap-filling to the final time-series outputs.