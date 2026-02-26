# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

## Overview
- Dataset comprises three CSV files with time series observations of surface-atmosphere exchanges: sensible heat (H), latent heat (LE), and momentum (τ), plus net ecosystem CO2 exchange (NEE), at three INCOMPASS Land Surface Stations in India.
- Includes ancillary weather and soil physics data, turbulence descriptors, and observation quality metrics.
- Observation period: 2016-01-01 00:30 to 2018-01-01 00:00.
- Stations and locations:
  - Berambadi, Southern Karnataka (agricultural land)
  - Dharwad, Dharwad UAS campus, Northern Karnataka (agricultural land)
  - Kanpur, IIT Kanpur campus, Uttar Pradesh (semi-natural grassland)

## INCOMPASS Land Surface Stations
- Berambadi (11.760633°N, 76.585361°E; 873 m)  
  - Semi-arid Aw climate; Alfisol soils; mixed agriculture; crops include Maize, Turmeric, Sunflower, Marigold, Sorghum, vegetables.
- Dharwad (15.498393°N, 74.985730°E; 692 m)  
  - Aw climate; Vertisol soils; agricultural field on campus; crops include maize, horse gram, soybean + intercrops, intercropping systems.
- Kanpur (26.509072°N, 80.223765°E; 129 m)  
  - Csa climate; Fluvisol soils; semi-natural grassland with periodic flooding; vegetation typical of non-agricultural Indo-Gangetic plains; documented wildfires in 2016 and 2017.

## Data collection and instrumentation
- Flux measurements via open-path eddy covariance (EC) systems at all three sites on 10 m masts.
- Instruments:
  - Windmaster sonic anemometers for all three velocity components and sonic temperature.
  - LI-7500A infrared gas analyzers for H2O and CO2.
  - Barometric pressure sensor; HMP155 air temperature and RH; NR01 net radiometer; SBS314 tipping-bucket rain gauge.
- Data acquisition:
  - EC sampled at 20 Hz; logged with CR3000 Micrologger; flux calculations averaged to 30-minute intervals.
  - Sensor heights and site metadata detailed in site tables.

## Flux data processing
- Fluxes calculated with EddyPRO v6.1, using linear detrending and 30-minute averaging.
- Processing steps include:
  - Quality control of raw 20 Hz data
  - Angle-of-attack correction for sonic anemometers
  - 2D coordinate rotation to align to local terrain
  - Corrections for co-spectral attenuation, humidity effects on H, density fluctuations for LE and CO2
- Sign convention: positive fluxes transfer from surface to atmosphere.
- Additional outputs from processing: friction velocity (u*), Turbulent Kinetic Energy (TKE), temperature scaling (T*), Obukhov length (L), stability parameter (z/L), and upwind-connection metrics (x_peak, x_10, x_30, x_50, x_70, x_90).

## Quality control
- EC data QC:
  - Outliers removed using median absolute deviation.
  - Flags for Stationarity and Integral Turbulence tests; data rejected if combined QC flag > 1.
  - Fluxes rejected if LI-7500A signal < 80%, or outside site ranges, or nighttime NEE negative.
  - Footprint checks via ART Footprint Tool to assess representativeness.
  - Weekly visual QC with manual data cleaning as needed.
- Ancillary data QC:
  - Basic range checks, spike/dropout checks, cross-checks between soil measurements, rainfall checks for flooding periods, and removal of clearly erroneous values.

## Meteorological observations
- Variables collected at central masts with site-specific sensor heights:
  - Barometric pressure (Pa)
  - Air temperature (Ta) and relative humidity (RH)
  - Net radiation and components: SWin, SWout, LWin, LWout, Rnet
  - Wind speed (WS) and wind direction (WD) at 10 m
  - Precipitation (with 0.2 mm tip resolution)
- All sensors and data are logged at 0.1 Hz and aggregated to 30-minute blocks for flux calculations.

## Soil physics observations
- Duplicated soil measurements at two locations per site:
  - Soil heat flux (G) at 0.03 m depth
  - Soil temperature (Tsoil) and volumetric water content (VWC) at 0.05 m and 0.15 m depths
- Data logged at 0.1 Hz and aggregated to 30-minute resolution
- Used for QC and interpretation of surface exchanges

## Data structure and formats
- Time-series data provided as three CSV files (one per station), covering 2016-01-01 00:30 to 2018-01-01 00:00.
- Missing data denoted by -9999.
- DateTime stamps refer to Indian Standard Time (UTC+5:30).
- Column set described in Table 2 of the source document; key variables include H, LE, τ, NEE, Pa, Ta, RH, radiation components, soil variables, precipitation, and EC-derived metrics (u*, TKE, L, z/L, footprint metrics, etc.).

## Variables and units (highlights)
- Fluxes: H (W/m^2), LE (W/m^2), τ (kg m^-1 s^-2), NEE (μmol CO2 m^-2 s^-1)
- Atmospheric: Pa (kPa), Ta (°C), RH (%), SWin/SWout (W/m^2), LWin/LWout (W/m^2), Rnet (W/m^2)
- Turbulence and stability: u* (m/s), TKE (m^2 s^-2), T* (K), L (m), z/L (dimensionless)
- Soil and precipitation: G (W/m^2), Tsoil (°C), VWC (%), Precipitation (mm)
- Winds and footprints: WS_EC, WD_EC, WS_10m, WD_10m, x_peak and percentile-based upwind distances

## Data availability and GIS-oriented usage notes
- The dataset provides georeferenced flux and micrometeorological observations at three fixed sites, suitable for:
  - Mapping station locations and regional comparisons of energy and carbon fluxes
  - Linking fluxes with meteorology and soil conditions for spatially explicit analyses
  - Integrating with climate zones, soil types, and land cover to study spatial patterns in surface exchanges
  - Deriving 30-minute flux time series for visualization, historical mapping, and policy-relevant analyses
- Important GIS considerations:
  - Time dimension: 30-minute resolution; timestamps in IST
  - Site metadata (location, climate classification, soil order) essential for spatial analyses
  - Footprint analysis and representativeness should be considered when aggregating across sites or mapping regional fluxes

## Acknowledgments and references
- INCOMPASS project funded by UK NERC and MoES (Monsoon Mission); additional support from UPSCAPE/NERC and related Indian partners.
- Contributions from multiple institutions and researchers; references include methodology and data processing standards for eddy covariance and micrometeorology.