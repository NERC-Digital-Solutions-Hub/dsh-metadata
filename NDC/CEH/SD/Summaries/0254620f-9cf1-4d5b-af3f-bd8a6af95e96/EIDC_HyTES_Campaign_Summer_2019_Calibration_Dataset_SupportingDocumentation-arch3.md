# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

- Overview of dataset
  - Calibration dataset for the Net-Sense/HyTES campaign under the Copernicus Candidate High Spatio-Temporal Resolution Land Surface Temperature Monitoring (LSTM) mission.
  - Five eddy covariance (EC) flux tower sites in southeast England; June 2019 flight campaign with HyTES hyperspectral imaging over EC sites.
  - Time period: flux, meteorological, and soil physics observations collected around 2019-06-22 to 2019-07-06; subset extracted from longer-term time series.
  - Data include turbulent fluxes of sensible heat (H) and latent heat (LE) and supporting ancillary data.

- Study sites
  - Five EC sites: three croplands (two on clay soils, one on drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
  - Site coordinates are not provided in this document for security reasons.
  - Site instrumentation summarized in a dedicated table, including soil type and sensors.

- Sampling regime
  - Automated measurements of fluxes, meteorology, and soil physics.
  - Fluxes measured above canopy with open-path EC systems (Windmaster sonic anemometer and LI-7500 IRGA) at 20 Hz; 30-minute interval means.
  - EC measurement heights: 2.0–2.6 m for most sites, 5.0 m at one site.
  - Sensor separations between sonic anemometer and IRGA specified; data logged with a CR3000.

- Ancillary data acquisition
  - Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure; net radiation (Rnet) and components (SWin, SWout, LWin, LWout); soil heat flux (G) at two locations; soil water content (VWC) and soil temperature (Ts) at 0.1 m; precipitation via tipping-bucket gauges.
  - Data scanned at 0.1 Hz and aggregated to 30-minute means; missing data marked as -9999.

- Flux data processing
  - Fluxes calculated with EddyPRO software (v6.1) using QC, coordinate rotation, tilt corrections, and cospectral attenuation corrections; density corrections for LE.
  - Quality control includes outlier removal, stationarity checks, footprint evaluation (target ecosystem representativeness >80% using ART Footprint Tool), and visual inspection.
  - All flux and ancillary data undergo weekly review; clearly erroneous values removed.

- Data gap-filling and flux partitioning
  - Gaps in LE and H filled using Marginal Distribution Sampling (Reichstein et al. 2005) with REddyProc in R; gap-filling performed on complete time series for each site before extraction for HyTES campaign.

- Data structure and units
  - Time series provided as separate CSV files per site; time stamps in TIME_START and TIME_END (YYYYMMDDhhmm); data cover 2019-06-22 00:30 to 2019-07-06 00:00.
  - Variables include LE, H, G1/G2 (soil heat flux), TA, VPD, RNET, SWIN, LWIN, SWOUT, LWOUT, PA, P, RH, WS, WD, TS, VWC, with corresponding QC flags (LE_qc, H_qc, TA_qc, etc.).
  - QC flags: 0 = high quality observed, 1 = gap-filled good quality, 2 = gap-filled acceptable quality, 3 = gap-filled poor quality.

- Data interpretation and quality considerations
  - Data are a calibration subset extracted from longer-term records; QC and gap-filling introduce derived data with quality flags indicating reliability.
  - Footprint analysis ensures data representativeness of target ecosystems; multiple quality control steps reduce risk of biases in downstream analyses.

- Acknowledgments and references
  - Data acquisition supported by Natural Environment Research Council funding; ASSIST and UK-SCAPE affiliations; COSMOS-UK data contributions.
  - References listed for QC, processing, and methodological foundations (e.g., EddyPRO, REddyProc, footprint modeling, and established flux processing procedures).