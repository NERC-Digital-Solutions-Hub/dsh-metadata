This document describes the dataset submitted under filename BW_NXA_2018-2020.csv

## Dataset overview
- Continuous half-hourly time series of heat fluxes (sensible H and latent LE) and greenhouse gas fluxes (co2_flux and ch4_flux) obtained by eddy-covariance.
- Accompanied by gas concentrations and ancillary meteorological data (air temperature, relative humidity, pressure, PAR, total and incoming radiation, wind speed and direction).
- Location: Nxaraga, south edge of Chief's Island, Okavango Delta, Botswana.
- Time period: 01/01/2018 to 31/12/2020.
- Missing data are coded as -9999.

## Study area: The Okavango Delta
- One of the world’s largest inland deltas (approx. 40,000 km2).
- Flooding driven by pulsed river discharge; annual water inputs from Cubango and Quito rivers and rainfall.
- Flood duration and extent governed by discharge and rainfall; evapotranspiration dominates water loss.
- Four physiographic zones: Panhandle (entry channel), permanent swamp, seasonal swamp, occasional swamp.
- Vegetation and habitat vary across zones; seasonal swamps flood 3–6 months/year.
- Floodplain vegetation includes reed grasses and papyrus; large herbivores commonly interact with the area.

## Instrumentation and measurements site
- Eddy-covariance system: Campbell Scientific IRGASON (3D ultrasonic anemometer + open-path CO2/H2O), LI-COR 7700 CH4 analyzer.
- Meteorology: Vaisala WXT520 weather station (temperature, pressure, humidity, wind speed/direction).
- Radiation sensors: Skye SKS1110 pyranometer (total radiation) and SKP215 PAR detector.
- Data logging: Campbell Scientific CR3000 (10 Hz for EC variables; 10 s for meteorology).
- Deployment: 3 m mast with effective measurement height ~2.5 m; flux footprint mainly in wind sector 60°–190° for EC and 130°–270° for the seasonal floodplain.
- Site context: floodplain bounded by a water channel with papyrus vegetation; wildlife and vegetation influence soil and flux dynamics.

## Data processing and quality
- Raw data processed into half-hourly fluxes using EddyPro software (v7.0.6).
- Quality control performed by Dr. Helfter.
- Output variables include:
  - H (sensible heat flux, W/m2) with QC flag qc_H (0 good, 1 fair, 2 poor)
  - LE (latent heat flux, W/m2) with QC flag qc_LE
  - co2_flux (μmol m^-2 s^-1) with qc_co2_flux
  - ch4_flux (μmol m^-2 s^-1) with qc_ch4_flux
  - co2_mole_fraction (ppm), h2o_mole_fraction (ppthou), ch4_mole_fraction (ppm)
  - VPD (Pa)
  - wind_speed (m s^-1), wind_dir (deg)
  - ustar (m s^-1), stability (dimensionless)
  - PAR (μmol m^-2 s^-1), Rg (W m^-2), RH (%), Pair (hPa), Tair (°C)
- Missing data indicated by -9999 in the dataset.

## Variables (summary)
- Fluxes: H, LE, co2_flux, ch4_flux
- Gas concentrations: co2_mole_fraction, h2o_mole_fraction, ch4_mole_fraction
- Meteorology: VPD, wind_speed, wind_dir, ustar, stability, PAR, Rg, RH, Pair, Tair
- Quality flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux

## Footprint and usage notes
- Flux estimates are valid primarily within defined wind sectors to ensure spatial homogeneity assumptions hold (EC: 60°–190°; floodplain: 130°–270°).
- Outputs may be affected by patchy data coverage and sector-specific limitations; users should consider footprint when aggregating or comparing with other sites.

## Provenance and personnel
- Instrumentation installed by Dr. Carole Helfter (UK Centre for Ecology and Hydrology).
- Monthly maintenance and data collection by Dr. Mangaliso Gondwe (Okavango Research Institute, University of Botswana).
- Data processed and quality-checked by the researchers using EddyPro.

## References
- Gumbricht et al., Channels, wetlands and islands in the Okavango Delta and their relation to hydrological and sedimentological processes. Earth Surf Proc Land. 2004.
- Krah et al., Airborne dust deposition in the Okavango Delta, Botswana, and its impact on landforms. Earth Surf Proc Land. 2004.
- Gumbricht et al., The topography of the Okavango Delta, Botswana, and its tectonic and sedimentological implications. S Afr J Geol. 2001.
- Gondwe & Masamba, Spatial and temporal dynamics of diffusive methane emissions in the Okavango Delta. Wetl Ecol Manag. 2014.
- McCarthy et al., Observations on hydrology and geohydrology of the Okavango Delta. S Afr J Geol. 1998.
- Bonyongo et al., Floodplain vegetation in Nxaraga Lagoon area, Okavango Delta. S Afr J Bot. 2000.