# BW_GUM_2018_2020.csv

- Overview
  - Dataset provides a continuous time series of heat flux (sensible H and latent LE) and trace gas fluxes (CO2, CH4) obtained by eddy-covariance, plus gas concentrations and ancillary meteorological data.
  - Location: Guma Lagoon, Okavango Delta, Botswana, near a Cyperus papyrus stand.
  - Coverage: 01/01/2018 to 31/12/2020; resolution: half-hourly; missing data encoded as -9999.

- Environment and site context
  - Okavango Delta: one of the world’s largest inland deltas with a pulsed flood regime driven by Cubango and Quito rivers; extensive water influx and evapotranspiration shaping vegetation and hydrology.
  - Delta zonation and vegetation influence flux dynamics: permanent vs seasonal swamps, papyrus stands, and associated plant communities.

- Instrumentation and site setup
  - Eddy-covariance system: Campbell Scientific IRGASON (3D ultrasonic anemometer + open-path CO2/H2O) and LI-COR 7700 CH4 analyser.
  - Weather and radiation: Vaisala WXT520; pyranometer (solar radiation) and PAR detector.
  - Data logging: Campbell Scientific CR3000; sampling at 10 Hz for EC variables, 10-s for meteorology.
  - Mounting: 3-m tripod on a 3-m platform (measurement height effectively 5.5 m); flux footprint focused on papyrus-dominated areas with wind sector 60°–190°; other sectors (notably 180°–360°) should not be used due to heterogeneity.

- Data processing and quality assurance
  - Raw data processed into half-hourly fluxes using EddyPro software (v7.0.6); quality controlled by designated researchers.
  - Outputs include fluxes and meteorological variables with associated quality flags.

- Variables and data structure
  - Fluxes and related variables:
    - H, LE: sensible and latent heat fluxes (W/m^2)
    - co2_flux: CO2 flux (μmol m^-2 s^-1; negative values indicate flux towards the surface)
    - ch4_flux: CH4 flux (μmol m^-2 s^-1; negative values indicate flux towards the surface)
  - Quality flags:
    - qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor)
  - Gas concentrations and environmental context:
    - co2_mole_fraction (ppm), ch4_mole_fraction (ppm), h2o_mole_fraction (ppthou)
    - VPD (Pa), wind_speed (m/s), wind_dir (degrees), ustar (m/s)
    - stability (dimensionless)
  - Meteorology and radiation:
    - PAR (μmol m^-2 s^-1), Rg (W m^-2), RH (%), Pair (hPa), Tair (°C)

- Data usage notes and caveats
  - Missing data represented as -9999.
  - Data are most appropriate for analyses within the specified footprint (60°–190°); cross-sectoral extrapolation is not advised.
  - The dataset reflects measurements at a papyrus-dominated stand and may be influenced by local vegetation structure and hydrology.

- Contextual references
  - Provides background on Okavango Delta hydrology, vegetation, and related geomorphology through cited references (1–6) detailing channels, wetlands, deposition, and ecology.