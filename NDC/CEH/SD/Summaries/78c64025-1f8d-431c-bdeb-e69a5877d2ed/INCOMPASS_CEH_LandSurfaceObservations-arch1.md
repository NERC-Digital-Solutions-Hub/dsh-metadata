# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

- A three-site time-series dataset recording surface–atmosphere exchanges of sensible heat (H), latent heat (LE), momentum (τ), and net ecosystem CO2 exchange (NEE), plus extensive ancillary meteorology and soil physics data.
- Data span 2016-01-01 00:30 to 2018-01-01 00:00, at 30-minute resolution (observations aggregated to 30-minute means; missing periods flagged as -9999).
- Three INCOMPASS Land Surface Stations in India:
  - Berambadi, Southern Karnataka (agricultural land, mixed crops)
  - Dharwad, Dharwad (agricultural campus site)
  - Kanpur, IIT Kanpur (semi-natural grassland)
- Each site file includes turbulence measurements, atmospheric state, radiation, precipitation, soil heat flux, soil temperature, and soil moisture, as well as turbulence-related diagnostics and data quality indicators.

## Sites and environmental context

- Berambadi (11.7606°N, 76.5854°E; 873 m a.s.l.)
  - Semi-arid tropical monsoon climate (Aw)
  - Soils: Alfisol; 65% sand, 10% silt, 25% clay
  - Land use: mixed agriculture
  - Mean annual temp ~24.4°C; mean annual rainfall ~600 mm
- Dharwad (15.4984°N, 74.9857°E; 692 m a.s.l.)
  - Semi-arid tropical monsoon climate (Aw)
  - Soils: Vertisol
  - Land use: agriculture
  - Mean annual temp ~24.3°C; mean annual rainfall ~885 mm
- Kanpur (26.5091°N, 80.2238°E; 129 m a.s.l.)
  - Humid subtropical climate (Csa)
  - Soils: Fluvisol
  - Landscape: semi-natural grassland
  - Mean annual temp ~25.6°C; mean annual rainfall ~820 mm
- Site-specific context includes crop schedules near Dharwad and flood-prone conditions at Kanpur.

## Flux measurement and data collection

- Open-path eddy covariance (EC) systems configured at 10 m mast height at all sites.
- Measurements include:
  - Turbulent flux densities: sensible heat (H), latent heat (LE), momentum (τ)
  - Net ecosystem CO2 exchange (NEE)
  - Atmospheric turbulence components (u, w), sonic temperature
  - Meteorological: air temperature (Ta), relative humidity (RH), barometric pressure, net radiation (Rnet) and components (SWin, SWout, LWin, LWout), wind speed and direction
  - Precipitation (SBS314 tipping bucket, 1.0 m height)
  - Soil physics: soil heat flux (G), soil temperature (Tsoil), soil volumetric water content (VWC)
- Instrumentation (same EC suite repeated at all sites):
  - Windmaster sonic anemometer thermometers (Gill)
  - LI-7500A infrared analyzers (CO2 and H2O)
  - Barometer and temperature/humidity sensor suite
  - Net radiometer (NR01)
  - 20 Hz EC data logged at CR3000; 1-minute averages derived, then aggregated to 30-minute intervals
- Data collection period entirely within INCOMPASS project scope (2016–2017 operational window, with some data through early 2018).

## Data processing and quality control

- Flux processing using EddyPRO v6.1 with:
  - Linear detrending and 30-minute averaging
  - Corrections for angle-of-attack, planar rotation, high/low-frequency attenuation, density (H, LE, NEE), and storage heat terms
  - Sign convention: positive from surface to atmosphere
  - Additional metrics: friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and upwind contribution footprints
- Quality control (flux data):
  - Outlier removal via median absolute deviation
  - Tests for Stationarity and Integral Turbulence; reject if QC flag > 1
  - Exclude low signal strength (<80% for LI-7500A), implausible site-range fluxes, or NEE negative at night
  - Footprint analysis using ART Footprint Tool to assess representativeness
  - Weekly visual checks; clearly erroneous values removed
- Quality control of ancillary data (meteorology, soil):
  - Range checks and spike/dropout checks
  - Cross-checks between soil variables (e.g., G, Tsoil, VWC) and rainfall/flooding observations
  - Removal of clearly erroneous values

## Data structure and variables

- Data files: three CSVs (one per site: Berambadi, Dharwad, Kanpur)
- Time frame: 2016-01-01 00:30 to 2018-01-01 00:00
- Columns: as described in the dataset’s Table 2 and Table 3 (example variables)
  - Fluxes and flux-related terms: H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2), NEE (μmol CO2 m^-2 s^-1), CO2 storage term, storage flux
  - Atmospheric state: Pa (kPa), Ta (°C), RH (%)
  - Radiation: SWin, SWout, LWin, LWout, Rnet (W m^-2)
  - Turbulence and stability: u*, TKE, T*, L, zL, z/L, x_peak, x_10, x_30, x_50, x_70, x_90
  - Soil/ground variables: G (soil heat flux, W m^-2) at depths and locations, Tsoil (°C) at 0.05 and 0.15 m, VWC (%) at 0.05 and 0.15 m
  - Precipitation: Precipitation (mm per 0.5 h) and total precipitation
  - Wind: WS_EC, WD_EC; WS_10m, WD_10m
  - Quality flags and uncertainties for fluxes (e.g., H_unc, LE_unc, NEE_unc)
- Missing data: denoted as -9999
- Timestamp convention: end of each 30-minute period; DateTime provided in IST (UTC+5:30)

## Temporal coverage and data quality notes

- Continuous measurement period with gaps due to system issues or QC can occur; missing values are flagged with -9999.
- Data are provided with site-specific context, including location, climate, soil type, and management practices, enabling localized interpretation and cross-site comparisons.

## How this dataset supports analysis and modeling

- Enables examination of energy balance and carbon fluxes across three contrasting Indian ecosystems (agricultural and grassland) under monsoon-influenced climates.
- Facilitates:
  - Correlation analyses between fluxes (H, LE, NEE) and meteorological drivers (Ta, RH, Rnet, precipitation, wind, stability)
  - Evaluation of dependency of CO2 exchange on soil moisture and soil temperature dynamics
  - Development and validation of land-surface and ecosystem models for monsoon regions
  - Investigation of energy balance closure and the influence of storage terms
  - Site-specific assessments of footprint relevance and representativeness
- Important considerations for analysts:
  - Local site conditions (land use, soil type, flooding risk) strongly influence flux patterns
  - 30-minute resolution captures diurnal and weather-driven variability but requires careful aggregation for large-scale inferences
  - Data quality procedures (QC flags, footprint analysis) are essential for robust interpretation and model calibration

## Acknowledgments and references

- Funded by UK-NERC and Indian MoES under the INCOMPASS project; additional support acknowledged for specific researchers and collaborations.
- Key references cover flux processing (EddyPRO), QC methods, footprint evaluation, and methodological standards for eddy covariance data.