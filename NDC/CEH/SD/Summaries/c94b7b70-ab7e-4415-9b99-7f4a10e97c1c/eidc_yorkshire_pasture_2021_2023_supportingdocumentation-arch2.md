# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

- What the dataset contains
  - 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes
  - Time period: 01/09/2021 to 01/01/2023 (approximately 1.5 years)
  - Additional weather and soil measurements accompanying flux data
  - Data structure center: Yorkshire_Pasture_2021_2023.csv

- Study site and management
  - Location: University of Leeds Research Farm, 53°51'58.64"N 1°19'11.08"W
  - Environment: temperate oceanic climate
    - Mean annual temp (1992-2022): 9.5 ± 1 °C
    - Precipitation: 885 ± 231 mm
  - Soil: loamy, calcareous brown earth, pH 6.8, bulk density 1.1 g cm-3
  - Soil properties: 0–30 cm soil carbon 27.7 g kg-1; nitrogen 2.3 g kg-1
  - Land management: agriculturally managed pasture
    - Grazed by sheep since 2012; periodic silage cutting (notably July 2022)
    - Rainfed; no fertiliser applied

- Collection methods and instrumentation
  - Flux measurements: automated eddy covariance (EC) above grass canopy, 2 m height
  - Core instruments:
    - CO2/H2O gas analyser: LI-7200RS
    - 3D sonic anemometer: Gill Windmaster
  - Data acquisition: 10 Hz sampling, 30-minute means
  - Ancillary measurements (30-minute means):
    - Energy fluxes: net radiation (Rnet), shortwave and longwave radiation components
    - Air temperature (Tair), relative humidity (RH), soil temperature (Tsoil at 5 cm), soil moisture
  - System and data handling: CR1000X datalogger; Smartflux 2 computer
  - Additional parameters captured: pressure (Pa), wind speed/direction, friction velocity (u*), etc.

- Data processing workflow
  - Processing software: EddyPro 7 (V7.0.6) with standard conditioning
  - Corrections applied:
    - Angle of attack correction for Gill anemometers
    - Time lag adjustment between sonic anemometer and high-frequency data
    - Correction for high- and low-frequency co-spectral attenuation
  - Uncertainty: random uncertainty estimates included for fluxes

- Quality control
  - Implemented in R (v4.1.3)
  - Criteria for data removal:
    - Statistical outliers
    - LI-COR signal strength > baseline by more than 10%
    - Non-representative footprint (more than 20% data outside site boundaries)
    - Unrealistic flux thresholds (H: 200–450 W m-2; LE: -50 to 400 W m-2; NEE: -60 to 30 μmol CO2 m-2 s-1)
    - friction velocity (u*) < 0.14 m s-1

- Gap-filling and flux partitioning
  - Missing periods gap-filled using marginal distribution sampling
  - Flux partitioning (NEE into GPP and Reco) performed
  - Uncertainty of filled values estimated from the data used to fill gaps

- Data structure and variables
  - Core time-stamped variables (in CSV units):
    - NEE (μmol CO2 m-2 s-1) and NEE_unc
    - LE (W m-2) and LE_unc
    - H (W m-2) and H_unc
    - Tau (momentum flux) and Tau_unc
    - CO2_strg, LE_strg, H_strg (storage terms)
    - Pa (kPa)
    - Tair (°C), RH (%)
    - VPD (two versions)
    - SWin, SWout, LWin, LWout, Rnet, PAR
    - G (soil heat flux)
    - Tsoil (°C); VWC (volumetric water content)
    - windspeed, winddir, Ustar
    - TKE, Tstar, L, (z-d)/L (stability), NEE_f (gap-filled NEE), NEE_f_sd
    - Reco (ecosystem respiration), GPP (gross primary productivity)
  - Note: NA indicates missing data

- Data usage and outputs
  - Provides a standardized, high-quality dataset for assessing pasture carbon balance and energy exchange
  - Suitable for environmental health monitoring, climate and land-surface interaction studies, and temporal trend analysis
  - Output available in the described CSV with explicit gap-filled NEE and partitioned components

- Acknowledgements and references
  - Funded by Leeds-York-Hull NERC DTP Panorama (grant NE/S007458/1)
  - Acknowledgement of the University of Leeds Research Farm and farm management information
  - References include methodological sources for data processing, quality control, gap-filling, and flux calculations used in the workflow