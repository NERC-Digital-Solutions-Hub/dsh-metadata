# This document describes the dataset submitted under filename BW_NXA_2018-2020.csv

## Overview
- A continuous time series (half-hourly) of heat fluxes (H, LE) and trace gas fluxes (co2_flux, ch4_flux), gas concentrations, and ancillary meteorological data collected to quantify greenhouse gas fluxes from seasonal floodplains.
- Time period: 01/01/2018 to 31/12/2020.
- Location: Nxaraga, on the south edge of Chief's Island, Okavango Delta, Botswana (coordinates 19°32'53"S, 23°10'45"E).
- Data quality: missing data encoded as -9999.

## Spatial and Temporal Scope
- Measurement site: 3 m EC mast on the SW edge of Chief's Island; effective EC measurement height 2.5 m.
- Flux footprint: floodplain data originate from wind sector 130°–270°; other sectors (e.g., 180°–360°) should not be used due to roughness elements.
- Data interval: half-hourly fluxes; raw sensors sampled at 10 Hz (EC) and meteorological sensors at 10 s.
- Geographic context: flux footprint and vegetation dynamics tied to the seasonal floodplain, with management and wildlife interactions affecting the littoral area.

## Instrumentation and Measurements
- Eddy-covariance hardware: Campbell Scientific IRGASON (3D ultrasonic anemometer + open-path CO2/H2O analyser) and LI-COR 7700 CH4 analyser; CH4 sensor mounted on a horizontal boom 0.3 m from the anemometer.
- Meteorology: Vaisala WXT520 for air temperature, pressure, relative humidity, wind speed and direction.
- Radiation: Skye Instruments pyranometer (SKS1110) and quantum detector (SKP215) for total incoming radiation and PAR.
- Data logging: Campbell Scientific CR3000, 10 Hz sampling for EC variables; 10 s for meteorological parameters.
- Site specifics: EC system mounted on a 3 m mast; canopy height ~2.5 m; papyrus/dense vegetation influence on wind and footprint.
- Data processing: raw data processed into half-hourly fluxes using EddyPro v7.0.6; quality controlled by Dr. Helfter.

## Variables and Quality Flags
- Primary fluxes and related variables (with units):
  - H (W m^-2); qc_H (quality flag: 0 good, 1 fair, 2 poor)
  - LE (W m^-2); qc_LE (0/1/2)
  - co2_flux (μmol m^-2 s^-1); qc_co2_flux (0/1/2)
  - ch4_flux (μmol m^-2 s^-1); qc_ch4_flux (0/1/2)
  - co2_mole_fraction (ppm)
  - h2o_mole_fraction (ppthou)
  - ch4_mole_fraction (ppm)
  - VPD (Pa)
  - wind_speed (m s^-1)
  - wind_dir (deg)
  - ustar (m s^-1)
  - stability (dimensionless)
  - PAR (μmol m^-2 s^-1)
  - Rg (W m^-2)
  - RH (%)
  - Pair (hPa)
  - Tair (°C)
- Notes:
  - Missing data represented as -9999.
  - Quality flags indicate data reliability for H, LE, CO2 flux, and CH4 flux.

## Data Processing and Quality Assurance
- Processing software: EddyPro v7.0.6 used to derive half-hourly fluxes from EC data.
- Quality control performed by Dr. Helfter.
- Data suitable for GIS-based visualization of spatial-temporal flux patterns, provided that sector and quality considerations are applied.

## Okavango Delta Context (Spatial Background)
- The Okavango Delta is a large inland delta (~40,000 km2) in northern Botswana with seasonal flooding from river discharge and rainfall.
- Flood regime and vegetation are shaped by a low topographic gradient and evapotranspiration losses; the delta comprises entry channels, permanent and seasonal swamps, and occasional swamps.
- Vegetation and hydrology influence flux measurements, including reed and papyrus-dominated zones and grazing by herbivores in floodplain areas.

## Practical GIS Considerations
- Map-based visualization opportunities: half-hourly H, LE, CO2 flux, CH4 flux, and gas concentrations across the Nxaraga site; relation to wind sector and footprint boundaries.
- Important caveats: apply sector masks to ensure data reflect homogeneous spatial sampling; respect quality flags; account for missing data (-9999) in analyses and visualizations.
- Coordinate and height context: site coordinates provided; measurement height 2.5 m; data are tied to a specific flux footprint orientation.

## References
- Gumbricht T, McCarthy J, McCarthy TS. Channels, wetlands and islands in the Okavango Delta, Botswana, and their relation to hydrological and sedimentological processes. Earth Surf Proc Land. 2004;29(1):15-29.
- Krah M, McCarthy TS, Annegarn H, Ramberg L. Airborne dust deposition in the Okavango Delta, Botswana, and its impact on landforms. Earth Surf Proc Land. 2004;29(5):565-77.
- Gumbricht T, McCarthy TS, Merry CL. The topography of the Okavango Delta, Botswana, and its tectonic and sedimentological implications. S Afr J Geol. 2001;104(3):243-64.
- Gondwe MJ, Masamba WRL. Spatial and temporal dynamics of diffusive methane emissions in the Okavango Delta, northern Botswana, Africa. Wetl Ecol Manag. 2014;22(1):63-78.
- McCarthy TS, Bloem A, Larkin PA. Observations on the hydrology and geohydrology of the Okavango Delta. S Afr J Geol. 1998;101(2):101-17.
- Bonyongo MC, Bredenkamp GJ, Veenendaal E. Floodplain vegetation in the Nxaraga Lagoon area, Okavango Delta, Botswana. S Afr J Bot. 2000;66(1):15-21.