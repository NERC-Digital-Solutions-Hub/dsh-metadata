# Fluvial hydrochemistry, CO2  efflux and delta   13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Overview and scope
- Dataset from the NERC-funded project addressing atmospheric CO2 efflux in karst fluvial systems (NE/N002806/1).
- Measures CO2 efflux from streams, springs, reservoirs and ponds in the Houzhai karst catchment (SW China).
- Data types include CO2 fluxes, water velocity, water chemistry (temperature, pH, dissolved oxygen, electrical conductivity, total alkalinity), dissolved inorganic carbon (DIC), and δ13C of DIC.
- Sampling cadence: most sites monthly, with intensified monitoring during rainfall events.
- Stable isotope data collected concurrently with CO2 flux measurements.
- Data structure centers on a single CSV file flux_and_13C_data; site information provided in Table 1.

## Study area and sites
- Houzhai catchment area: 73.4 km2, Guizhou Province, China.
- Climate: humid subtropical monsoon; typical annual precipitation ~1140 mm, average temperature ~20.1°C.
- Topography: altitudes 1,220–1,400 m above sea level.
- Geology: Middle Triassic limestone and dolomite.
- Monitoring locations encompass multiple site types: streams, springs, sinkholes, reservoirs/ponds.
- Site coordinates and types are detailed in Table 1, with numerous site IDs (e.g., springs, sinkholes, streams, reservoirs) across the catchment.

## Data collected and variables
- CO2 flux data: F_CO2 (μmol CO2 m^-2 s^-1) and F_sd (standard deviation across measurements).
- Water chemistry: temperature (T, °C), pH, electrical conductivity (EC, μS cm^-1), dissolved oxygen (DO, mg L^-1), water depth, depth-averaged flow velocity (Flow_velocity, m s^-1), total alkalinity (TA, mmol L^-1), dissolved inorganic carbon (DIC, mmol L^-1).
- Isotopic data: δ13C-DIC (per mil, ‰).
- Derived metrics: pCO2_DIC (from measured DIC; μatm) and pCO2_TA (from TA-derived DIC, μatm).
- Data unit notes: F_CO2 and F_sd in μmol m^-2 s^-1; TA and DIC in mmol L^-1; others with respective units as stated.

## Sampling and analytical methods
- CO2 flux measurement: floating chamber method using a 0.0028 m^3 chamber; CO2 accumulation measured over 4 minutes with three repeats per site to obtain mean flux.
- Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)), with variables defined accordingly.
- Flow velocity measurement: depth-averaged velocity ṽ using a flow meter with an impeller; averaging appropriate depths based on water depth.
- Water chemistry: measure T and pH at deployment; collect water samples within 15 minutes of flux measurement for [DIC], δ13C-DIC, and TA using headspace methods and titration; [DIC] sometimes estimated from TA, pH, and equilibrium constants.
- pCO2 calculation: derived from DIC with pH and temperature (Henry’s law); pCO2_DIC and pCO2_TA represent pCO2 calculated from measured DIC and from DIC estimated from TA, respectively.

## Quality control and data processing
- CO2 flux QC: fluxes derived from three repeated four-minute measurements per site.
- DIC and δ13C-DIC QC: headspace method with calibration against three isotopically distinct inorganic carbon standards; instrument drift corrected by a standard every 10 samples.
- Documentation notes provide calibration details and reference methods to ensure measurement accuracy and comparability.

## Data structure and access
- Core dataset: a single CSV file named flux_and_13C_data with 19 columns: Sequence, ID, Type, Date, Time, F-CO2_, F_sd, TA, T, pH, EC, DO, Water_depth, Flow_velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC.
- Column descriptions: F-CO2 (CO2 flux), F_sd (flux SD), TA (total alkalinity), DIC (dissolved inorganic carbon), DIC_TA (DIC estimated from TA), pCO2_DIC and pCO2_TA (partial pressures derived from DIC and TA), d13C-DIC (δ13C of DIC).
- Units are specified for each variable in the dataset documentation.
- Site-level details (lat/long and Type) are provided in Table 1, covering a variety of hydrological features.

## References and provenance
- Project: Addressing a significant knowledge gap in fluvial system atmospheric CO2 efflux: the contribution from karst landscapes (NE/N002806/1).
- Related methodological references:
  - Waldron et al., 2014 on precision and accuracy of DIC stable isotope measurements using continuous-flow IRMS.
  - Zhang et al., 2019 on storage dynamics and connectivity in karst catchments.

## Reuse and considerations for data leaders
- Data discovery and interoperability:
  - Clear linkage between flux data, water chemistry, and isotopic data facilitates integration with broader catchment datasets.
  - Metadata includes sampling cadence, site types, and measurement methods, supporting reuse across platforms.
- Data quality and governance:
  - Documented QC procedures (instrument calibration, drift correction, standard checks) aid assessment of data reliability.
  - Some DIC values are estimated from TA, introducing potential additional uncertainty; users should account for estimation methods in analyses.
- Collaboration and extended use:
  - The dataset supports cross-site and cross-catchment comparative studies in karst systems and can inform models of CO2 efflux and carbon cycling in heterogeneous hydrological networks.
  - Potential opportunities for linking with regional data communities focusing on karst hydrology, CO2 flux, and stable isotope applications.