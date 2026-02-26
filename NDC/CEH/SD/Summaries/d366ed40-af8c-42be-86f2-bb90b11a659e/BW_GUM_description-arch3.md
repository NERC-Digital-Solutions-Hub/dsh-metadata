# This document describes the dataset submitted under filename BW_GUM_2018_2020.csv

- Purpose and scope
  - Provides a continuous time series of heat fluxes (latent and sensible) and trace gas fluxes (CO2 and CH4) derived from eddy-covariance measurements, plus gas concentrations and ancillary meteorological data.
  - Aims to quantify greenhouse gas fluxes over a Cyperus papyrus stand in Guma Lagoon, Okavango Delta, Botswana.
  - Data are reported at a half-hourly interval for 01/01/2018 to 31/12/2020.
  - Missing data are indicated with -9999.

- Study area: The Okavango Delta
  - One of the world’s largest inland deltas in northern Botswana, with about 40,000 km2 surface area.
  - Flooding driven by pulsed discharge from Cubango and Quito rivers; most water input lost to evapotranspiration.
  - Four physiographic zones: Panhandle entry channel, permanent swamp, seasonal swamp, and occasional swamp.
  - Vegetation and hydrology are linked to flooding extent and regime, with reed grasses and Cyperus papyrus dominating certain zones.

- Instrumentation and measurements site
  - Eddy-covariance system: Campbell Scientific IRGASON (3D ultrasonic anemometer + open-path CO2/H2O analyser) and LI-COR 7700 open-path CH4 analyser.
  - Additional sensors: Vaisala WXT520 weather station (air temperature, pressure, humidity, wind), Skye pyranometer (PAR) and SKP215 detector (PAR), data logger CR3000.
  - Deployment: system on a 3 m tripod on a 3 m platform; effective measurement height 5.5 m; located ~30 m west of a floating papyrus mat, canopy ~2.5 m above water.
  - Flux footprint: focused in wind sector 60°–190°; data from other sectors cautioned due to roughness elements.
  - Maintenance and processing: installed by Dr. Carole Helfter; monthly data collection by Dr. Mangaliso Gondwe; raw data processed to half-hourly fluxes using EddyPro v7.0.6; quality controlled by Dr. Helfter.

- Data contents and processing
  - Key variables (with units and descriptions):
    - H (W m-2): sensible heat flux; qc_H (quality flag; 0 good, 1 fair, 2 poor)
    - LE (W m-2): latent heat flux; qc_LE
    - co2_flux (μmol m-2 s-1): CO2 flux; qc_co2_flux
    - ch4_flux (μmol m-2 s-1): CH4 flux; qc_ch4_flux
    - co2_mole_fraction (ppm)
    - h2o_mole_fraction (ppthou)
    - ch4_mole_fraction (ppm)
    - VPD (Pa)
    - wind_speed (m s-1)
    - wind_dir (deg)
    - ustar (m s-1)
    - stability (dimensionless)
    - PAR (μmol m-2 s-1)
    - Rg (W m-2)
    - RH (%)
    - Pair (hPa)
    - Tair (°C)
  - Data processing: half-hourly fluxes derived from raw measurements; quality flags indicate data reliability.
  - Metadata and measurement context (instrument heights, footprint, and sector considerations) documented to support data interpretation.

- Data quality, gaps, and governance considerations
  - Missing data due to instrumentation downtime; represented as -9999.
  - Quality control applied during processing to assign qc_flags for each flux and related measurements.
  - Documentation provides context on instrument maintenance and site-specific conditions that affect data quality and interpretation.
  - The description highlights potential governance considerations for environmental monitoring data, such as metadata completeness, data sharing of underlying measurements, and ensuring standardised quality assurance procedures.

- References and context
  - The document includes references on the hydrology, geomorphology, and vegetation of the Okavango Delta, underpinning the environmental context for the dataset.