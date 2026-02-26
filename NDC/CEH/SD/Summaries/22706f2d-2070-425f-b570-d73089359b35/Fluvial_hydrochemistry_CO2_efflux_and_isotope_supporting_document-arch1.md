# Fluvial hydrochemistry, CO2 efflux and delta 13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Overview
- Dataset from the NERC project NE/N002806/1 addressing knowledge gaps in atmospheric CO2 efflux from karst landscapes.
- Measurements cover CO2 efflux from streams, springs, reservoirs and ponds in the Houzhai karst catchment (SW China).
- Includes: CO2 efflux rate (F_CO2) with associated water velocity and water chemistry (temperature, pH, DO, EC, total alkalinity), calculated pCO2 from DIC and TA, and stable isotope data (δ13C-DIC).
- Data structure: a single CSV file (flux_and_13C_data) with 19 columns, including F_CO2, F_sd, TA, T, pH, EC, DO, water depth, flow velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, and d13C-DIC.
- Sampling: monthly monitoring at most sites, with intensified monitoring during rainfall events.
- Site types include streams, springs, sinkholes, reservoirs/ponds; sampling times and site information provided in accompanying table.

## Study area and site information
- Houzhai catchment: 73.4 km² in Guizhou Province, SW China.
- Climate: humid subtropical monsoon; average annual precipitation ~1140 mm; mean temperature ~20.1°C.
- Elevation: 1,220–1,400 m a.s.l.
- Geology: Middle Triassic limestones and dolomites.
- Sites: diverse features (streams, springs, sinkholes, reservoirs/ponds) with geographic coordinates and type listed in Table 1.

## Sampling and analytical methods
- CO2 fluxes measured using a floating chamber (volume 0.0028 m³); CO2 accumulation tracked over 4 minutes, three repeats per site.
- Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)).
- Flow velocity: depth-averaged (ū) measured with an impeller flow meter; depth handling per water depth.
- Water chemistry: measurement of water temperature, pH at deployment; water samples for [DIC], δ13C-DIC, and TA collected within 15 minutes of flux measurement.
- DIC and δ13C-DIC: measured via headspace method and analyzed with Thermo-Fisher Gas Bench/Delta V plus; TA via titration (0.2N HCl).
- pCO2: calculated from DIC (pCO2_DIC) using pH and temperature; additional pCO2_TA from TA-based DIC estimates.
- Quality control: calibration with three isotopically distinct inorganic carbon standards, inclusion of a standard every 10 samples to correct instrument drift; headspace method details per Waldron et al. (2014).

## Data structure and content
- File: flux_and_13C_data (CSV) with 19 columns:
  - Sequence, ID, Type, Date, Time
  - F_CO2, F_sd
  - TA, T, pH, EC, DO
  - Water_depth, Flow_velocity
  - DIC, DIC_TA
  - pCO2_DIC, pCO2_TA
  - d13C-DIC
- Units: F_CO2 and F_sd in μmol m⁻² s⁻¹; TA and DIC in mmol L⁻¹; T in °C; pH (unitless); EC in μS cm⁻¹; DO in mg L⁻¹; depth and velocity in m and m s⁻¹; pCO2 in μatm; d13C-DIC in ‰.
- Datasets support cross-site comparison and integration with isotopic and carbonate chemistry.

## Site information
- Table 1 provides site coordinates and types (e.g., sinkholes, springs, streams, reservoirs) across many locations (e.g., multiple entries for 109, 131, 294, HZ, MZ, etc.), indicating broad spatial coverage within the Houzhai catchment.

## Temporal scope
- Timeframe: 2016–2018.
- Monitoring regime: monthly measurements with intensified sampling during rainfall events to capture hydrological bursts and CO2 flux dynamics.

## Data quality and provenance
- QA/QC procedures include standardized flux measurement protocol, headspace DIC/isotope analyses with calibrated standards, and drift corrections via regular standards.
- Data are linked to published methodological references for flux and isotope measurements (Waldron et al. 2014; Zhang et al. 2019).

## References
- Zhang, Z., et al. Storage dynamics, hydrological connectivity and flux ages in a karst catchment: conceptual modelling using stable isotopes. Hydrol. Earth Syst. Sci., 2019.
- Waldron, S., et al., Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry. Rapid Communications in Mass Spectrometry, 2014.

## Potential uses for analysts
- Quantify and compare CO2 efflux across karst hydrological features (streams, springs, sinkholes, reservoirs) within a catchment.
- Investigate drivers of CO2 flux by relating F_CO2 to DIC, TA, pH, temperature, DO, and flow velocity.
- Use δ13C-DIC data to identify carbon sources and processes controlling inorganic carbon pools.
- Develop predictive models of CO2 efflux under different hydrological conditions and land-use scenarios.
- Facilitate spatial analyses of flux patterns by site type and location within the Houzhai catchment.