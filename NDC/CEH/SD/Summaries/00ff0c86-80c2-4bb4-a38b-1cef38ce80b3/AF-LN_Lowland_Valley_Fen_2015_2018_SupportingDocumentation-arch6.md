# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

- Purpose and content
  - Time series of land-surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ)
  - Turbulent fluxes measured with eddy covariance (EC) between 2015-01-01 00:30 and 2018-10-11 00:00
  - Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence

- Study site
  - AF-LN flux observation site, 53°18'37.18"N, 4°17'28.06"W, 63 m amsl, Cors Erddreiniog National Nature Reserve, Anglesey, North Wales
  - Habitat: conservation-managed valley-head fen with low-intensity pony grazing; high-quality for Natural Resources Wales
  - Climate: temperate maritime (mean 1981–2010: T = 10.4 ± 3.9 °C, P = 841 ± 41 mm year⁻¹)
  - Peat-dominated with shallow water table; peat depth up to ~2.5 m; low peat bulk density and high carbon content

- Sampling regime
  - Automated flux, meteorological, and soil measurements from 2015-01-01 00:30 to 2018-10-11 00:00

- Flux data acquisition
  - Open-path EC above grassland canopy at 2.0 m height
  - Fluxes: NEE (μmol CO2 m⁻² s⁻¹), τ (kg m⁻¹ s⁻²), H (W m⁻²), LE (W m⁻²)
  - Instrumentation: CSAT3 ultrasonic anemometer + LI-7500 IR gas analyser
  - Raw data: 20 Hz sampling of 3 velocity components, sonic temperature, and gas densities; logged with CR3000 Micrologger

- Ancillary data acquisition
  - Co-located meteorology and soil observations
  - Temperature (Ta, °C) and relative humidity (RH, %) at 2 m
  - Net radiation (Rnet, W m⁻²), incoming shortwave radiation (SWin), soil heat fluxes (G at two depths), soil temperature (Tsoil1 at 0.05 m), precipitation (0.5 h resolution and total)
  - Data logged as 30-minute means (and precipitation sums)

- Data processing
  - Turbulent flux densities computed from raw EC data with EddyPRO v6.1
  - Processing steps: QC of 20 Hz data; tilt/rotation corrections; coordinate rotation; spectral corrections; density corrections; random uncertainties via established methods
  - Output metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability z/L; flux footprints

- Quality control
  - Removal of statistical outliers (median absolute deviation) and non-stationary turbulence periods
  - Flux ranges: H (-200 to 500 W m⁻²), LE (-60 to 500 W m⁻²), NEE (-50 to 30 μmol CO₂ m⁻² s⁻¹)
  - NEE excluded at night and when u* below 0.18 m s⁻¹
  - Weekly visual checks with manual outlier removal as needed

- Data gap-filling and flux partitioning
  - Gap-filling of EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al., 2005)
  - Partitioning NEE into GEP and TER using Ta-driven approach (Reichstein et al., 2005)
  - Gap-filling and partitioning performed with REddyProc (R: Reichstein et al., 2016)
  - Where possible, missing meteorological data filled from a nearby second EC station (<1 km)

- Details of data structure
  - Single CSV file: AF-LN_Lowland_Valley_Fen_2015_2018.csv
  - Time span: 2015-01-01 00:30 to 2018-10-11 00:00
  - Missing data indicated by -9999
  - Table 1 (described in the dataset) defines variables, units, and descriptions

- Nature and units of recorded values (selected examples)
  - DateTime: dd-mm-yyyy HH:MM (UTC)
  - NEE: μmol CO₂ m⁻² s⁻¹ (baseline, before gap-filling)
  - NEE_filled: μmol CO₂ m⁻² s⁻¹
  - LE, H: W m⁻²
  - LE_filled, H_filled: W m⁻²
  - TER, GEP: μmol CO₂ m⁻² s⁻¹
  - Pa: kPa; Ta: °C; RH: %
  - VPD: hPa; SWin, Rnet: W m⁻²
  - G1, G2, Tsoil1: W m⁻², °C
  - Ustar (friction velocity): m s⁻¹; TKE, L, zL: various turbulence metrics
  - x_peak, x_70, x_90: meters (upwind flux contribution metrics)
  - NEE_sd, LE_sd, H_sd, etc.: standard deviations for flux uncertainties

- Acknowledgments and references
  - Funded by Natural Environment Research Council (NE/R016429/1) and Defra SP1210
  - Permissions from Natural Resources Wales to install the flux tower and access site
  - Key references for methods and processing tools (EddyPRO, REddyProc, standard EC QA/QC procedures)

- Practical notes for data use
  - The dataset supports self-service analysis of carbon, energy, and water fluxes from a peatland fen
  - Includes both raw and gap-filled/partitioned flux products for flexible use
  - Suitable for studies requiring turbulence metrics, footprint estimates, and data-quality-aware flux analyses