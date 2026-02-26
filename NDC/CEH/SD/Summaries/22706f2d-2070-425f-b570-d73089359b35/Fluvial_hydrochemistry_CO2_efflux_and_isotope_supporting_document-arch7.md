# Fluvial hydrochemistry, CO2 efflux and delta 13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Brief description
- Dataset from the NERC project addressing CO2 efflux from karst-influenced fluvial systems in the Houzhai catchment, SW China (2016–2018).
- Includes measurements of CO2 efflux (F_CO2) from streams, springs, sinkholes, reservoirs/ponds, plus water chemistry and stable isotope data.
- Variables collected per site and time: CO2 flux (and uncertainty), flow velocity, water temperature, pH, electrical conductivity, dissolved oxygen, water depth, and various DIC-related metrics.
- Isotopic data: δ13C of dissolved inorganic carbon (δ13C-DIC).
- Sampling generally monthly with intensified measurements during rainfall events.
- Data organized in a single CSV file with 19 columns, enabling map-based visualization of spatial patterns and relationships with hydrological features.

## Study area and site information
- Location: Houzhai catchment, 73.4 km², Guizhou Province, China.
- Climate: Humid subtropical monsoon; typical annual precipitation ~1140 mm; mean temperature ~20.1°C.
- Elevation: 1,220–1,400 m above sea level.
- Geology: Middle Triassic limestones and dolomite.
- Site types and locations: Monitoring sites include streams, springs, sinkholes, reservoirs/ponds; coordinates provided for each site.
- Site list provided in Table 1 with lat/long and type (e.g., Spring, Sinkhole, Stream, Reservoir, Pond), including multiple identifiers per feature (e.g., 109-1 to 109-8, 131-1 to 131-2, 65/65-DTS, etc.).

## Sampling and analytical methods
- CO2 flux measurements: Floating chamber method (volume 0.0028 m³), CO2 accumulation tracked over 4 minutes, three replicates per site to obtain mean flux.
  - Flux calculation: F_CO2 = (ΔCO2/Δt) × (V / (R × T × S)).
  - Units: F_CO2 in μmol CO2 m⁻² s⁻¹; chamber surface area S in m²; V in m³; T in K.
- Flow velocity: Depth-averaged velocity obtained with a flow meter (impeller); method varies with depth to compute a representative velocity.
- Water chemistry and DIC isotopes: At deployment, measure water temperature and pH; collect water samples within 15 minutes of flux measurement.
  - DIC concentration, δ13C-DIC, and total alkalinity (TA) measured using headspace method and titration.
  - pCO2 estimated from DIC (pCO2_DIC) using pH and temperature; pCO2_TA calculated from TA-derived DIC (pCO2_TA).
  - In cases where DIC is not measured, DIC estimated from TA, pH, and equilibrium constants.
- Quality control for chemistry: Calibration with three distinct inorganic carbon standards; a blank/standard every 10 samples to correct instrument drift.
- Documentation: Detailed procedural notes and references to established methods (Waldron et al., 2014; related isotopic standard references).

## Data structure and qualifications
- Data file: flux_and_13C_data.csv containing 19 columns.
- Columns include: Sequence, ID, Type, Date, Time, F_CO2, F_sd, TA, T, pH, EC, DO, Water_depth, Flow_velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC.
- Key definitions:
  - F_CO2: mean CO2 flux from 3 measurements; F_sd: associated standard deviation.
  - DIC_TA and pCO2_TA: DIC estimated from TA and pCO2 estimated from TA, respectively.
  - pCO2_DIC: pCO2 estimated from measured DIC.
- Units: F_CO2 and related CO2 metrics in μmol m⁻² s⁻¹; TA and DIC in mmol L⁻¹; T in °C; EC in μS cm⁻¹; DO in mg L⁻¹; water depth and flow velocity in m and m s⁻¹; d13C-DIC in per mil (‰).

## Relevance for GIS specialists
- The dataset provides geolocated measurements across a karst catchment, enabling spatial visualization of CO2 flux and hydrochemical properties.
- Site-level attributes (Type, coordinates) facilitate layering of flux data with hydrological features (streams, springs, sinkholes, reservoirs) and topographic context.
- Suitable for creating map-based data products to explore spatial patterns of CO2 efflux, DIC isotopic composition, and water chemistry in relation to catchment structure and geology.
- Data supports analyses across multiple resolutions, with monthly sampling and higher-frequency events, requiring careful aggregation or downscaling for GIS visualization.

## Quality and limitations
- DIC not measured at all sites/time points; some DIC values estimated from TA and pH, introducing additional uncertainty.
- DIC measurement and CO2 flux procedures follow standardized methods with calibration standards and drift corrections; QA details provided.
- Site coverage includes diverse karst features, but overlap and density may vary by location, potentially affecting spatial interpolation.

## References
- Zhang, Z., et al. (2019). Storage dynamics, hydrological connectivity and flux ages in a karst catchment: conceptual modelling using stable isotopes. Hydrology and Earth System Sciences, 23(1), 51-71.
- Waldron, S., et al. (2014). Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry. Rapid Communications in Mass Spectrometry, 28(10), 1117-1126.