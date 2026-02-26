# BW_NXA_2018-2020.csv

## Overview
- Continuous time series (half-hourly) of heat fluxes (sensible H and latent LE) and trace gas fluxes (CO2, CH4) obtained by eddy-covariance, plus gas concentrations and ancillary meteorological data.
- Data period: 01/01/2018 to 31/12/2020.
- Location: Nxaraga, south edge of Chief's Island, Okavango Delta, Botswana.
- Purpose: quantify greenhouse gas fluxes from seasonal floodplains.
- Missing data: represented as -9999.
- Processing and QC: raw data processed into half-hourly fluxes using EddyPro v7.0.6; quality controlled.

## The Okavango Delta
- One of the world’s largest inland deltas (~40,000 km2); hydrology driven by pulsed discharge from Cubango and Quito rivers.
- Annual water input: ~9 billion m3 from rivers + ~6 billion m3 from rainfall; evapotranspiration ~1500 mm.
- Flood dynamics: flood peak typically in August; flood extent and annual inundation governed by discharge and rainfall.
- Four physiographic zones: Panhandle (entry channel), permanent swamp, seasonal swamp, occasional swamp.
- Vegetation zones: permanent swamps dominated by reed grasses and papyrus; seasonal swamps with Panicum repens and Oryza longistaminata.
- Floodplain ecology: papyrus mats, diverse fauna (hippos, elephants, impala, buffalo) influence soil and vegetation; grasses dominate floodplain flora.

## Instrumentation and site
- Measurement basis: eddy-covariance for fluxes between surface and atmosphere.
- Instruments: IRGASON (3D ultrasonic anemometer + open-path CO2/H2O analyzer) and LI-COR 7700 CH4 analyzer.
- Meteorological sensors: Vaisala WXT520 (air temperature, pressure, RH, wind), Skye pyranometer SKS1110 (total radiation), quantum detector SKP215 (PAR).
- Data logger: Campbell Scientific CR3000; EC data at 10 Hz, meteorology at 10 s.
- Site setup: 2.5 m mast height for a 3 m mast; footprint overlaps papyrus vegetation; designated wind sectors for flux computations: 60°–190° (overall) and 130°–270° (seasonal floodplain).
- Maintenance and processing: installed by Dr. Carole Helfter; monthly maintenance by Dr. Mangaliso Gondwe; data processed by EddyPro v7.0.6 with quality control by Helfter.
- Ecological context: the measurement area includes a seasonal floodplain bordered by a channel and papyrus mats; presence of large herbivores (hippos, elephants) and grazing pressure noted.

## Variables and data structure
- Fluxes: H (sensible heat, W m^-2), LE (latent heat, W m^-2), co2_flux (μmol m^-2 s^-1), ch4_flux (μmol m^-2 s^-1).
- Quality flags: qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor).
- Gas mole fractions: co2_mole_fraction (ppm), h2o_mole_fraction (ppthou), ch4_mole_fraction (ppm).
- Meteorology and soil- atmosphere metrics: VPD (Pa), wind_speed (m s^-1), wind_dir (deg), ustar (m s^-1), stability (dimensionless).
- Radiation and environment: PAR (μmol m^-2 s^-1), Rg (W m^-2), RH (%), Pair (hPa), Tair (°C).

## Data caveats and usage notes
- Missing data indicated by -9999.
- Footprint and heterogeneity considerations: data from wind sectors outside the designated ranges should be avoided due to roughness elements (trees, shrubs) affecting spatial homogeneity assumptions underlying eddy-covariance.
- Ecological factors: presence and activity of hippos, elephants, and grazing pressure may influence flux dynamics in the floodplain.
- Suitability: appropriate for standardized environmental monitoring and policy-performance assessment with transparent provenance and processing details.

## Data provenance and references
- Data submitted under filename BW_NXA_2018-2020.csv; instrumentation, processing, and QC teams noted (Helfter; Gondwe).
- References informing the contextual background of the Okavango Delta and measurement approach include:
  - Gumbricht et al. 2004
  - Krah et al. 2004
  - Gumbricht et al. 2001
  - Gondwe & Masamba 2014
  - McCarthy et al. 1998
  - Bonyongo et al. 2000