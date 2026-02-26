# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

- The dataset comprises three time-series files of surface-atmosphere exchanges (sensible heat H, latent heat LE, momentum τ) and net ecosystem CO2 exchange (NEE), plus ancillary meteorological and soil-physics observations, turbulence metrics, and observation quality indicators.
- Coverage: 2016-01-01 00:30 to 2018-01-01 00:00.
- Sites: Berambadi (Southern Karnataka), Dharwad (Dharwad University of Agricultural Sciences, Karnataka), and Kanpur (IIT Kanpur, Uttar Pradesh).
- Access scope: complete time series provided per station; data gaps and missing records denoted as -9999.

## Study sites

- Berambadi, Southern Karnataka
  - Location: semi-arid tropical monsoon climate (Aw); altitude ~873 m; Alfisol soils.
  - Land use: mixed agriculture; crops include maize, turmeric, sunflower, marigold, sorghum, vegetables.
- Dharwad, Southern Karnataka
  - Location: agricultural campus near Deccan Plateau; climate Aw; Vertisol soils.
  - Surroundings: large flat field under continual agricultural management; crop schedule includes maize, horse gram, soybean+pigeon pea intercropping, pigeon pea.
- Kanpur, Uttar Pradesh
  - Location: semi-natural grassland within IIT Kanpur; humid subtropical climate (Csa); Fluvisol soils.
  - Environment: periodic flooding from irrigation canals; grassland vegetation; notable wildfire events in 2016 and 2017 with rapid post-fire recovery.

## Data collection and instrumentation

- Flux measurements: open-path eddy covariance (EC) systems deployed on 10 m masts; three identical EC setups across sites.
- Instruments:
  - Wind: Windmaster sonic anemometers (m/s) for three velocity components and sonic temperature.
  - Gas and density: LI-7500A analyzers for water vapor and CO2; barometric pressure sensor.
  - Data logger: 20 Hz sampling with CR3000 Micrologger; data aggregated to 30-minute means.
  - Meteorology: LI-COR air temperature and humidity probe in aspirated shield; NR01 net radiometer for radiation components; SBS314 rain gauge.
  - Soil physics: duplicated measurements at two depths (0.03 m, 0.05–0.15 m for various sensors) including soil heat flux plates, soil moisture, and soil temperature.
- Data processing: EddyPRO Flux Calculation Software v6.1 used for QC, detrending, coordinate rotation, and flux calculations; fluxes expressed with micrometeorological sign convention (positive from surface to atmosphere).

## Data processing and quality control

- Processing steps: linear detrending, 30-minute averaging, corrections for humidity effects on H, density corrections for LE and NEE; angle-of-attack corrections for sonic anemometers; 2D rotation; co-spectral attenuation corrections; footprint assessment via ART Footprint Tool.
- Quality control (EC data): outlier removal (median absolute deviation), Stationarity and Integral Turbulence tests; data flagged (0, 1, 2) with rejection if QC flags exceed thresholds; additional checks: signal strength of LI-7500A, site-specific ranges, night-time NEE values; weekly visual reviews and manual data removal as needed.
- Ancillary data QC: range checks, spike/dropout detection, cross-checks between soil measurements and rainfall/flood events; removal of clearly erroneous values.
- Uncertainty and diagnostic outputs: includes Ustar (friction velocity), TKE, T*, Obukhov length L, stability parameter z/L, and upwind contribution metrics for fluxes; random uncertainties derived from covariance-based approaches.

## Data contents and structure

- Data format: three CSV files, one per station (Berambadi, Dharwad, Kanpur).
- Time coverage: 2016-01-01 00:30 to 2018-01-01 00:00; timestamps correspond to the end of each 30-minute period and are given in Indian Standard Time (UTC+5:30).
- Variables: time-stamped records for H, LE, τ, NEE, and CO2 storage, plus ancillary meteorological (pressure, air temperature, relative humidity, radiation components, wind speed/direction, precipitation) and soil physics variables (soil heat flux, soil temperature at 0.05 m and 0.15 m, soil moisture at 0.05 m and 0.15 m, precipitation, wind data from EC and 10 m). Each observation includes accompanying uncertainties (e.g., H_unc, LE_unc, NEE_unc) and quality flags.
- Data dictionary: Table 3-like mappings describe variable names, units, descriptions, and storage terms; -9999 marks missing data.

## Key variables and units

- Fluxes: H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2), NEE (μmol CO2 m^-2 s^-1); NEE also has a pre-gap-filling variant and CO2 storage term.
- Meteorology: Pa (kPa), Ta (°C), RH (%), SWin/SWin, SWout, LWin, LWout, Rnet (W m^-2); wind: WS_EC, WD_EC, WS_10m, WD_10m.
- Soil: G (W m^-2) at two depths/locations, Tsoil at 0.05 m and 0.15 m, VWC at 0.05 m and 0.15 m, Precipitation (mm per 30 min or total).
- Turbulence diagnostics: Ustar, TKE, Tstar, L, zL, x_peak, x_10, x_30, x_50, x_70, x_90 (upwind-distance metrics).

## Data quality, provenance and use

- Provenance: INCOMPASS project effort, with acknowledgments to funding bodies (NERC, MoES) and collaborating institutions.
- Data provenance: site owners and collaborators acknowledged; references provided for methodology and processing standards (e.g., Mauder et al., Foken et al., Moncrieff et al., Webb et al.).
- For data leaders: this dataset demonstrates rigorous QA/QC, standardized processing across multiple sites, detailed metadata (site characteristics, climate classification, soils, land use), and an openly formatted time-series data product suitable for cross-site analyses and governance of data assets.