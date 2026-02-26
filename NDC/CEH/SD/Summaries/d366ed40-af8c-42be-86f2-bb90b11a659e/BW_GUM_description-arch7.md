# BW_GUM_2018_2020.csv

## Dataset scope
- Continuous time-series dataset of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes obtained via eddy-covariance, gas concentrations, and ancillary meteorological data.
- Measurements intended to quantify greenhouse gas fluxes over a Cyperus papyrus stand at Guma Lagoon, Okavango Delta, Botswana.
- Reported at half-hourly intervals for 2018-01-01 to 2020-12-31.
- Missing data are encoded as -9999.

## Spatial and temporal coverage
- Location: Guma Lagoon, Okavango Delta, Botswana (coordinates 18°57'53.01"S, 22°22'16.20"E).
- Habitat: Perennially flooded papyrus stand; flux footprint overlaps papyrus vegetation.
- Effective measurement height: 5.5 m (instrument mounted on a 3 m tripod on a 3 m platform).
- Flux footprint: Overlaps papyrus vegetation in wind sector 60°–190°; data from other sectors (notably 180°–360°) should not be used due to inhomogeneous roughness elements.
- Time period: 01 Jan 2018 – 31 Dec 2020.
- Data integrity: -9999 indicates missing values due to instrumentation downtime.

## Instrumentation and data collection
- Eddy-covariance core: IRGASON (3D ultrasonic anemometer + open-path CO2/H2O gas analyzer) and LI-COR 7700 open-path CH4 analyzer; crosswind placement with CH4 analyzer 0.3 m from the anemometer.
- Meteorology: Vaisala WXT520 weather station (air temperature, pressure, relative humidity, wind speed/direction).
- Radiation measurements: Skye Instruments pyranometer (total radiation) and quantum detector (PAR).
- Data logging: Campbell Scientific CR3000 datalogger; EC data at 10 Hz, meteorology at 10 s.
- Mounting/orientation: System oriented into prevailing wind direction; near a papyrus mat with land-water interface ~30 m west of the mat; canopy height ~2.5 m above water.
- Maintenance and processing: Monthly maintenance and data collection; raw data processed into half-hourly fluxes using EddyPro v7.0.6; quality control performed.

## Data processing, quality, and structure
- Processing: EddyPro software (v7.0.6) to compute fluxes from EC measurements.
- Quality flags (per variable):
  - H (sensibile heat flux): qc_H (0 = good, 1 = fair, 2 = poor)
  - LE (latent heat flux): qc_LE (0 = good, 1 = fair, 2 = poor)
  - co2_flux: qc_co2_flux (0 = good, 1 = fair, 2 = poor)
  - ch4_flux: qc_ch4_flux (0 = good, 1 = fair, 2 = poor)
- Variables included (examples with units and meanings):
  - H, LE: W m^-2 (sensibile and latent heat flux)
  - co2_flux: μmol m^-2 s^-1 (CO2 flux; negative values indicate flux toward the surface)
  - ch4_flux: μmol m^-2 s^-1 (CH4 flux; negative values indicate flux toward the surface)
  - co2_mole_fraction: ppm
  - h2o_mole_fraction: ppthou
  - ch4_mole_fraction: ppm
  - VPD: Pa
  - wind_speed: m s^-1
  - wind_dir: deg
  - ustar: m s^-1
  - stability: (dimensionless)
  - PAR: μmol m^-2 s^-1
  - Rg: W m^-2
  - RH: %
  - Pair: hPa
  - Tair: °C
- Notes:
  - Negative flux values denote fluxes toward the surface.
  - Data are half-hourly, aligned with the EC processing output.

## Contextual notes for GIS usage
- The dataset provides high-resolution, time-stamped flux measurements at a single monitoring site with a defined footprint. Suitable for time-series visualization, trend analysis, and integration with spatial layers (e.g., vegetation maps, hydrological features) to explore spatial-temporal patterns of GHG fluxes in the Okavango Delta.
- Care should be taken when combining with broader spatial datasets due to the specific measurement footprint (60°–190° wind sector) and the localized papyrus stand.

## The Okavango Delta context (optional GIS consideration)
- The Okavango Delta is a large, low-gradient inland delta (~40,000 km2) with seasonal to permanent wetlands and diverse vegetation.
- Hydrology is driven by pulsed river discharges and rainfall; flood extent and vegetation composition influence gas exchange processes.
- Four physiographic zones and variable vegetation (reeds, sedges, papyrus) affect spatial representativeness of single-point flux measurements.

## References
- Gumbricht et al. (various works on channels, wetlands, and hydrology of the Okavango Delta)
- Gondwe & Masamba (spatial and temporal methane dynamics in the Okavango Delta)
- McCarthy et al. (hydrology and geohydrology of the Okavango Delta)
- Bonyongo et al. (vegetation in the Okavango Delta)
- Additional methodological references for eddy-covariance and flux processing.