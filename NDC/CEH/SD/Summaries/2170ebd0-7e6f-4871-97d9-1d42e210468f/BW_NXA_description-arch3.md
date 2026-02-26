# BW_NXA_2018-2020.csv

- Overview
  - A continuous time series dataset of heat fluxes (sensible H and latent LE) and trace gas fluxes (CO2 and CH4) obtained by eddy-covariance, along with gas concentrations and ancillary meteorological data (air temperature, relative humidity, pressure, PAR, total incoming radiation, wind speed/direction).
  - Reported at half-hourly intervals for 2018-01-01 to 2020-12-31.
  - Location: Nxaraga, southern edge of Chief's Island, Okavango Delta, Botswana.
  - Missing data are encoded as -9999.

- What is measured
  - Fluxes
    - H (W m^-2)
    - LE (W m^-2)
    - co2_flux (μmol m^-2 s^-1; negative values denote fluxes towards the surface)
    - ch4_flux (μmol m^-2 s^-1; negative values denote fluxes towards the surface)
    - Quality flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor)
  - Gas concentrations and vapour
    - co2_mole_fraction (ppm)
    - ch4_mole_fraction (ppm)
    - h2o_mole_fraction (ppthou)
    - VPD (Pa)
  - Meteorological and derived variables
    - wind_speed (m s^-1)
    - wind_dir (deg)
    - ustar (m s^-1)
    - stability (dimensionless)
    - PAR (μmol m^-2 s^-1)
    - Rg (W m^-2)
    - RH (%)
    - Pair (hPa)
    - Tair (°C)

- Instrumentation and site
  - Eddy-covariance system: Campbell Scientific IRGASON (3D ultrasonic anemometer + open-path CO2/H2O analyzer) and LI-COR 7700 CH4 analyzer.
  - Orientation: IRGASON aligned with prevailing wind; CH4 analyzer mounted on a horizontal boom 0.3 m from the anemometer.
  - Meteorology: Vaisala WXT520 for air temperature, pressure, relative humidity, wind speed/direction.
  - Radiation: Skye Instruments pyranometer (PAR) and quantum detector.
  - Data logging: Campbell Scientific CR3000; EC sensors at 10 Hz; meteorological parameters at 10-s intervals.
  - Measurement height: effective 2.5 m, mounted on a 3-m mast on the SW edge of Chief’s Island.
  - Flux footprint and sectors
    - Over seasonal floodplain; footprint overlapped papyrus vegetation in wind sector 60°–190°. Data from other wind sectors (notably 180°–360°) should not be used due to inhomogeneous roughness.
    - Seasonal floodplain fluxes attributable to wind sector 130°–270°. Data from other wind sectors should not be used for these fluxes due to roughness elements (trees/shrubs).
  - Site context
    - Floodplain features a mix of channels, wetlands, and islands; papyrus-dominated vegetation; wildlife (hippopotamuses, elephants) influences soil and vegetation structure.
  - Maintenance and processing
    - Instrumentation installed by Dr. Carole Helfter (UK Centre for Ecology and Hydrology); monthly maintenance and data collection by Dr. Mangaliso Gondwe (Okavango Research Institute, University of Botswana).
    - Raw data processed to half-hourly fluxes using EddyPro software v7.0.6; quality controlled by Dr. Helfter.

- Data processing, quality control, and metadata
  - Processed fluxes produced with standard eddy-covariance methods and quality flags (H, LE, CO2 flux, CH4 flux) to indicate data reliability.
  - Metadata includes variable names, units, and descriptions (Table 1 in the document).

- Temporal and ecological context
  - Okavango Delta: one of the world’s largest inland deltas in northern Botswana; highly seasonal flooding driven by river discharge and rainfall; four physiographic zones (entry channel, permanent swamp, seasonal swamp, occasional swamp) with vegetation and hydrology influencing flux measurements.
  - Flood regime and vegetation influence the interpretation of GHG fluxes, particularly in seasonal vs. permanent wetlands and in areas with tall roughness elements.

- References
  - Supporting hydrology, sedimentology, and vegetation context for the Okavango Delta and related processes (Gumbricht et al., 2004; Krah et al., 2004; Gumbricht et al., 2001; Gondwe & Masamba, 2014; McCarthy et al., 1998; Bonyongo et al., 2000).