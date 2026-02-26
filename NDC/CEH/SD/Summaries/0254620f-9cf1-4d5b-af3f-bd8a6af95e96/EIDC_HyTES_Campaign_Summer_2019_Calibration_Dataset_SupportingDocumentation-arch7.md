# Subset of turbulent energy fluxes, meteorology and soil physics observations collected at eddy covariance sites in southeast England, June 2019

- Overview
  - Time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil physics data.
  - Collected at five eddy covariance (EC) flux tower sites in southeast England.
  - Dataset served as calibration data for the Net-Sense/HyTES campaign during the HyTES airborne flight in June 2019.

- Study sites
  - Five EC sites: three croplands (two on clay soils, one on drained lowland peat) and two managed grasslands (on chalk and drained lowland peat).
  - Site coordinates are not publicly provided for security reasons; coordinates available on request from the dataset author.
  - Site characteristics and instruments summarized in a table.

- Sampling regime
  - Automated flux, meteorological and soil-physics measurements span 2019-06-22 00:30 to 2019-07-06 00:00.
  - Measurements sampled at 20 Hz and aggregated to 30-minute means (precipitation sums).
  - EC measurement heights: generally around 2.0–2.6 m (2.0 m at some sites, 5.0 m at EF-SH); footprint considerations used to verify representativeness.

- Flux data processing
  - Fluxes (H and LE) computed with EddyPRO v6.1, including:
    - QC of raw 20 Hz data
    - Angle-of-attack correction for sonic anemometers
    - 2D coordinate rotation to align data to local terrain
    - Corrections for cospectral attenuation; humidity and density corrections
    - Wind speed/direction at measurement height
  - QC and gap-filling performed on the full site time series before extracting HyTES subset.
  - Data gap-filling for LE and H via Marginal Distribution Sampling using REddyProc in R.
  - Footprint analysis (ART Footprint Tool) ensures ≥80% of flux originates within the target ecosystem; flagged as representative when satisfied.

- Data structure and variables
  - Data provided as separate .csv files for each of the five sites.
  - Time span: 2019-06-22 00:30 to 2019-07-06 00:00.
  - Missing records denoted by -9999.
  - Variables include:
    - TIME_START, TIME_END
    - LE and LE_qc (latent heat flux and quality control flag)
    - H and H_qc (sensible heat flux and QC flag)
    - G1, G2 (soil heat flux at 0.03 m)
    - TA, TA_qc (air temperature at 2.0 m and QC)
    - VPD, VPD_qc (vapor pressure deficit and QC)
    - RNET (net radiation)
    - SWIN, LWIN (incoming shortwave, longwave)
    - SWOUT, LWOUT (outgoing shortwave, longwave)
    - PA (barometric pressure)
    - P (precipitation)
    - RH, RH_qc (relative humidity)
    - WS, WD (wind speed and wind direction at TC height)
    - TS, VWC (soil temperature at 0.1 m and volumetric water content)
  - Units follow LI-COR/Reichstein conventions where applicable.

- Data quality and caveats
  - QC flags indicate data quality: 0 = high quality observed; 1–3 denote gap-filled data with varying quality.
  - Non-stationary conditions lead to flux removal; outliers removed using median absolute deviation criteria.
  - Spatial representativeness checked via footprint model; only fluxes with adequate representation within the target ecosystem retained.
  - Data are a subset extracted from longer time series; complete site data exist beyond the HyTES window.

- Usage in GIS and potential data products
  - Ideal for creating map-based data products that link flux dynamics with HyTES-derived land surface temperature measurements.
  - Possible GIS applications:
    - Spatially referenced time series of H and LE to compare with HyTES flyover data.
    - Derivation of ancillary raster layers (RNET, TA, VPD, soil moisture, soil temperature) aligned to the EC site footprints.
    - Validation and calibration datasets for land-surface models and remote sensing products.
  - Important considerations for GIS work:
    - Coordinates are restricted; acquire from the authors for precise georeferencing.
    - Use 30-minute aggregated flux data and corresponding QC flags to filter or weight data in analyses.

- Access, Acknowledgments and references
  - Data acquisition supported by NERC awards; ASSIST and UK-SCAPE program contexts noted.
  - Acknowledges landowners and site managers.
  - Key references include EddyPRO processing details, footprint modelling, gap-filling methodologies, and HyTES/HyTES calibration context.