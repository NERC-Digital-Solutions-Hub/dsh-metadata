# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS land surface stations in India, 2016 to 2017

- The dataset provides time series observations of surface-atmosphere exchanges, including sensible heat (H), latent heat (LE), momentum (τ), and net ecosystem CO2 exchange (NEE), recorded at three INCOMPASS Land Surface Stations in India from 2016-01-01 00:30 to 2018-01-01 00:00.
- Ancillary meteorological and soil physics observations accompany flux data, along with variables describing turbulence and data quality.
- Data were collected under the INCOMPASS project, with stations located in Berambadi (Southern Karnataka), Dharwad (Dharwad, Karnataka), and Kanpur (Uttar Pradesh).
- Observations were gathered using open-path eddy covariance systems, standardized instrumentation, and processed with established micrometeorological methods to support environmental monitoring and model validation.

## Sites and context

- Berambadi, Southern Karnataka
  - Location: 11.760633°N, 76.585361°E, 873 m amsl
  - Land use: Mixed agriculture
  - Climate: Aw (semi-arid tropical monsoon)
  - Soils: Alfisol
  - Mean annual temperature ~24.4°C; mean annual rainfall ~600 mm

- Dharwad, Southern Karnataka
  - Location: 15.498393°N, 74.985730°E, 692 m amsl
  - Land use: Agriculture
  - Climate: Aw (semi-arid tropical monsoon)
  - Soils: Vertisol
  - Mean annual temperature ~24.3°C; mean annual rainfall ~885 mm
  - Surrounding field management with crop schedule (maize, horse gram, soybean + intercropping, etc.)

- Kanpur, Uttar Pradesh
  - Location: 26.509072°N, 80.223765°E, 129 m amsl
  - Land use: Semi-natural grassland
  - Climate: Csa (humid subtropical)
  - Soils: Fluvisol
  - Mean annual temperature ~25.6°C; mean annual rainfall ~820 mm
  - Vegetation includes Phragmites-Saccharum-Imperata grassland; periodic flooding observed

## Data collection and instrumentation

- Flux measurements
  - Method: Open-path eddy covariance (EC) at all three stations
  - Height: 10 m masts supporting EC systems
  - Sensors: Wind components and sonic temperature (Windmaster sonic anemometer), water vapor and CO2 (LI-7500A), barometric pressure
  - Sampling: 20 Hz, logged with CR3000 Micrologger
  - Flux variables: H (sensible heat), LE (latent heat), τ (momentum), NEE (net CO2 exchange)
  - Processing: Fluxes computed with EddyPRO v6.1; 30-minute averaging; quality control applied

- Meteorology
  - sensors and placement consistent across sites
  - Barometric pressure (Pa), air temperature (Ta), relative humidity (RH)
  - Radiation: Net radiation (Rnet) and components (SWin, SWout, LWin, LWout)
  - Wind: Speed and direction at 10 m
  - Precipitation: Tipping-bucket rain gauge (aperture height 1 m)

- Soil physics
  - Duplicated measurements at two depths near the radiometer
  - Soil heat flux (G) at 0.03 m
  - Soil temperature (Tsoil) at 0.05 and 0.15 m
  - Volumetric water content (VWC) at 0.05 and 0.15 m
  - Instruments: HFP01-SC flux plates for G; ACC-SEN-SDI sensors for Tsoil and VWC
  - Data scanned at 0.1 Hz and aggregated to 30-minute means

## Data processing and quality control

- Processing details
  - EddyPRO used for flux calculation with detrending, 30-minute averaging, and necessary corrections
  - Corrections included: angle of attack, double rotation to local terrain, spectral attenuation, humidity effects on H, density corrections for LE and NEE
  - Sign convention: micrometeorological, positive fluxes are surface-to-atmosphere

- Quality control (EC data)
  - Outliers removed using median absolute deviation
  - Tests: Stationarity and Integral Turbulence; data flagged with a quality index; data with flag > 1 rejected
  - Additional criteria: LI-7500A signal < 80% raises data exclusion; fluxes outside site ranges; nighttime NEE negativity flags
  - Footprint assessment: Kormann & Meixner analytical footprint model via ART Footprint Tool to ensure representativeness
  - Weekly visual QC with manual removal of clearly erroneous values

- Quality control (ancillary data)
  - Basic range checks and spike/dropout visual checks
  - Cross-checks between paired soil sensors and against rainfall/flooding events
  - Clearly erroneous meteorological and soil data removed

## Data structure and contents

- Format and time coverage
  - Data provided as three CSV files, one per station
  - Time range: 2016-01-01 00:30 to 2018-01-01 00:00
  - Time stamps refer to the end of each 30-minute period
  - Missing data denoted by -9999

- Variables and columns
  - Fluxes: H (W m-2), LE (W m-2), τ (kg m-1 s-2), NEE (μmol CO2 m-2 s-1)
  - NEE and related terms: NEE_unc, H_unc, LE_unc, CO2_strg (CO2 storage term)
  - Atmospheric and environmental: Pa (kPa), Ta (°C), RH (%), SWin, SWout, LWin, LWout, Rnet (W m-2)
  - Turbulence and stability: u*, TKE, T*, L (Obukhov length), z/L, x_peak, x_10, x_30, x_50, x_70, x_90 (upwind distance metrics)
  - Surface and soil: G1, G2 (soil heat flux at two locations), Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2, VWC_0.05_1, VWC_0.15_1, VWC_0.05_2, VWC_0.15_2, Precipitation, WS_EC, WD_EC, WS_10m, WD_10m
  - Descriptive and metadata: DateTime (IST), plus uncertainty fields for several variables

- Data quality flags and gaps
  - -9999 indicates missing data after QC
  - QC flags and site-specific quality assessments accompany the data

## Access, documentation, and usage considerations

- Data are organized per site in CSV format with standardized columns and units
- Documentation includes detailed site descriptions, instrument configurations, data processing steps, QC procedures, and references
- Suitable for inter-site comparison, model validation, and long-term environmental monitoring related to surface energy balance and carbon fluxes in tropical-to-subtropical India

## Acknowledgments and references

- Funding and collaboration: INCOMPASS Project, supported by NERC (UK) and MoES (India) under various grants
- Additional support acknowledged for team members and site hosts
- References include methodological and foundational papers on eddy covariance processing, QC, footprint analysis, and climate classifications, among others