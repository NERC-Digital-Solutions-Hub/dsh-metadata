# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

- Purpose and scope
  - Provides time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE) plus supporting meteorological and soil physics data.
  - Collected at five eddy covariance (EC) flux tower sites in southeast England during June 2019.
  - Calibration data for the Net-Sense/HyTES campaign under the Copernicus LSTM mission; HyTES airborne campaign flown over EC sites 2019-06-28 to 2019-06-29.

- Study sites
  - Five EC sites: three croplands (two on clay soils, one drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
  - Site coordinates withheld for security; availability of coordinates upon request.

- Measurements and instrumentation
  - Fluxes: turbulent sensible heat (H) and latent heat (LE) measured above the canopy using open-path EC systems (Windmaster sonic anemometer and LI-7500 IRGA).
  - Micrometeorology: air temperature (TA), relative humidity (RH), barometric pressure (PA), net radiation (Rnet) and components (SWin, SWout, LWin, LWout), wind speed/direction, etc.
  - Soil physics: soil heat flux plates (G1, G2 at 0.03 m), soil temperature (TS) and volumetric water content (VWC) at 0.1 m, soil moisture sensors, rain gauges.
  - Dataloggers and sampling: 20 Hz data with 30-minute means; EC heights 2.0–5.0 m depending on site; measurement geometry specified (offsets between sonic anemometer and LI-7500).

- Sampling regime and data period
  - Automated measurements from 2019-06-22 00:30 to 2019-07-06 00:00.
  - Data include 30-minute averages; precipitation summarized as sums.

- Data processing and quality control
  - Flux calculation with EddyPRO v6.1, including:
    - QC of raw 20 Hz data
    - Angle-of-attack correction for sonic anemometers
    - 2D coordinate rotation for terrain
    - Corrections for high/low-frequency cospectral attenuation
    - Humidity-density corrections for H and LE calculations
    - Wind speed/direction at measurement height
  - QC protocol:
    - Removal of statistical outliers via median absolute deviation
    - Exclusion under non-stationary atmospheric conditions
    - Footprint analysis to ensure >80% flux originates within target ecosystem
    - Weekly visual checks; clearly erroneous values removed
  - Data gaps and gap-filling:
    - Gaps in LE and H filled with Marginal Distribution Sampling using REddyProc in R
    - Gap-filling performed on complete site time series before HyTES data extraction

- Data structure and metadata
  - Data delivered as five separate .csv files (one per EC site).
  - Time range: 2019-06-22 00:30 to 2019-07-06 00:00.
  - Missing data indicated by -9999.
  - Variables include: LE, H, G1/G2, TA, VPD, RNET, SWIN, SWOUT, LWIN, LWOUT, PA, P, RH, WS, WD, TS, VWC, TIME_START, TIME_END, and quality flags (e.g., LE_qc, H_qc, TA_qc, etc.).
  - Quality flags:
    - 0 = high quality observed
    - 1 = gap-filled data of good quality
    - 2 = gap-filled data of acceptable quality
    - 3 = gap-filled data of poor quality

- Variables and units (selected overview)
  - Fluxes: LE and H in W m-2
  - Atmospheric and micrometeorology: TA (°C), VPD (hPa), PA (kPa), RH (%), WS (m s-1), WD (degrees)
  - Radiation and energy balance: RNET (W m-2), SWIN/LWIN/SWOUT/LWOUT (W m-2)
  - Soil: G1/G2 (W m-2), TS (°C), VWC (%vol), P (mm per 0.5 h)
  - Precipitation: P (mm per interval)
  - Time metadata: TIME_START, TIME_END (YYYYMMDDhhmm)

- Data quality and limitations
  - Coordinates withheld; location-specific interpretation requires contact with the authors.
  - Gap-filled data are annotated with QC flags to indicate reliability.
  - Calibration dataset represents a subset of longer-term records; designed for HyTES campaign calibration.

- Access, acknowledgments, and references
  - Data acquisition supported by NERC awards NE/R016429/1 (UK-SCAPE) and NE/N018125/1 (ASSIST); COSMOS-UK contributed additional data.
  - Authors acknowledge landowners and site managers.
  - References include standard Eddy covariance processing and data quality literature (e.g., EddyPRO, Reichstein et al., Moncrieff et al., Papale et al., etc.).

- Potential uses for analysts
  - Validate and calibrate remote sensing products (HyTES) with ground-based fluxes and micrometeorology.
  - Develop or test data processing pipelines for eddy covariance data (QC, gap-filling, footprint analysis).
  - Investigate relationships between H and LE fluxes and environmental variables across different land covers and soil types.
  - Assess data quality, uncertainty, and the impact of gap-filling on flux estimates across short campaign windows.

- End notes
  - The dataset provides a tightly documented, QC-enabled, site-specific snapshot suitable for data-driven analyses, with clear metadata on processing steps, quality flags, and data gaps.