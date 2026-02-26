# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

- Three CSV files capture time series of surface–atmosphere exchanges and ancillary observations from INCOMPASS Land Surface Stations in India (Berambadi, Dharwad, Kanpur) over 2016-01-01 00:30 to 2018-01-01 00:00.
- Key fluxes and variables include sensible heat (H), latent heat (LE), momentum (τ), and net ecosystem CO2 exchange (NEE), plus meteorology and soil physics data, turbulence metrics, and observation quality indicators.
- Observations were collected using open-path eddy covariance systems and standardized instrumentation, with data processed to 30-minute flux averages.

## INCOMPASS Land Surface Stations (sites)

- Berambadi, Southern Karnataka
  - Location: agricultural land on Deccan Plateau; 2 km from Western Ghats foothills; ~, 873 m amsl
  - Climate: semi-arid tropical monsoon (Aw)
  - Mean annual temp ~24.4°C; rainfall ~600 mm
  - Soils: Alfisol; mixed agriculture around site
- Dharwad, Northern Karnataka
  - Location: UAS Dharwad campus; ~692 m amsl
  - Climate: semi-arid tropical monsoon (Aw)
  - Mean annual temp ~24.3°C; rainfall ~885 mm
  - Soils: Vertisol; agricultural field with crop rotations
- Kanpur, Uttar Pradesh
  - Location: semi-natural grassland at IIT Kanpur; ~129 m amsl
  - Climate: humid subtropical (Csa)
  - Mean annual temp ~25.6°C; rainfall ~820 mm
  - Soils: Fluvisol; vegetation a Phragmites–Saccharum–Imperata grassland; seasonal flooding potential

## Sampling regime and measurements

- Measurements
  - Automated fluxes, meteorology and soil physics via open-path eddy covariance (EC) systems at all three stations
  - 10 m tall masts; sonic anemometers for turbulence components; LI-7500A for H2O/CO2; barometer; temperature, humidity, net radiation, wind speed/direction; tipping-bucket rain gauge
  - EC data: 20 Hz; logged with CR3000 Micrologger; fetch-optimized deployment
- Data cadence
  - Sensors scanned at 0.1 Hz; data aggregated to 1-minute means; flux calculations performed on 30-minute intervals
  - Fluxes computed for H, LE, τ, and NEE; density corrections and other standard EC processing applied

## Data processing and quality control

- Processing
  - EddyPRO software (v6.1) used for flux calculation
  - Corrections included: angle-of-attack, 2D rotation, co-spectral corrections, humidity-density effects, and CO2 storage terms
  - Sign convention: positive flux from surface to atmosphere
- Quality control (flux data)
  - Outliers removed via median absolute deviation
  - Tests: Stationarity and Integral Turbulence (flags 0–2); require overall flag ≤ 1
  - Additional checks: signal strength of LI-7500A > 80%; flux within site ranges; NEE not negative at night
  - Footprint assessment using Kormann & Meixner analytical model (via ART Footprint Tool)
  - Weekly visual checks; manual removal of clearly erroneous values
- Quality control (ancillary data)
  - Range checks and spike/dropout checks; cross-checks between paired soil observations
  - Large soil moisture changes cross-checked with rainfall and observed flooding
- Data structure and formats
  - Time series provided as CSV files per station; complete series from 2016-01-01 00:30 to 2018-01-01 00:00
  - Missing data denoted by -9999
  - Timestamps refer to the end of each 30-minute period
  - Table references for structure and variable definitions (Table 2 and Table 3 in the source)

## Nature and units of recorded values (key variables)

- DateTime: yyyy-mm-dd HH:MM (Indian Standard Time, UTC+5:30)
- H: sensible heat flux density (W m^-2); H_unc (random error); H_strg (storage term)
- LE: latent heat flux density (W m^-2); LE_unc; LE_strg
- Tau: momentum flux (kg m^-1 s^-2); Tau_unc
- NEE: net ecosystem CO2 exchange (μmol CO2 m^-2 s^-1); NEE_unc; CO2_strg
- Pa: barometric pressure (kPa)
- Ta: air temperature (°C); RH: relative humidity (%)
- SWin, SWout, LWin, LWout, Rnet: radiative components and net radiation (W m^-2)
- G1, G2: soil heat flux at 0.03 m (W m^-2)
- Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_3: soil temperatures at specified depths (°C)
- VWC_0.05_1, VWC_0.15_1, VWC_0.05_2, VWC_0.15_2: soil volumetric water content (%)
- Precipitation: total and 0.5-hour rate (mm and mm h^-1)
- WS_EC, WS_10m: wind speeds (m s^-1); WD_EC, WD_10m: wind directions (degrees)
- Ustar: friction velocity (m s^-1); TKE: turbulent kinetic energy (m^2 s^-2)
- Tstar, L, zL: stability-related parameters (K, m, dimensionless)
- x_peak, x_10, x_30, x_50, x_70, x_90: upwind distances contributing to flux (meters)

## Access, use and interpretation notes

- Data are suitable for investigating surface energy balance, CO2 exchange, and meteorological/soil drivers across three contrasting land surfaces (agricultural and grassland) in India.
- Users should account for site-specific differences (climate, soil, land use) and the footprint context when comparing flux values.
- Be mindful of data gaps and site-specific QC flags; consult the footprint and QC documentation when interpreting flux reliability.

## Acknowledgments and references

- INCOMPASS project funding from UK NERC and Indian MoES; additional support acknowledged for authors and collaborators
- References cited relate to flux processing, QC methods, footprint analysis, and climate data sources used in dataset creation

- Datasets and related methodological references include: EddyPRO processing steps, QC procedures (e.g., Papale 2006; Mauder et al. 2013; Moncrieff et al. 1997, 2004; Naiman et al.), and footprint modeling work (Kormann & Meixner 2001)