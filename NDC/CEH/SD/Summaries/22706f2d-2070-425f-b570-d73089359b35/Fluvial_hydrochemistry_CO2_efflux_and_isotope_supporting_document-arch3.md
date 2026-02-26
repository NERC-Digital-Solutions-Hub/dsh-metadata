# Fluvial hydrochemistry, CO2  efflux and delta   13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Overview
- Dataset from the NERC-funded project addressing knowledge gaps in fluvial CO2 efflux from karst landscapes; measures CO2 efflux from streams, springs, reservoirs and ponds in the Houzhai karst catchment.
- Monitoring design: predominantly monthly measurements with intensive sampling during rainfall events.
- Variables include CO2 flux (F_CO2) with uncertainty (F_sd), flow velocity, water chemistry (temperature, pH, DO, EC, TA, DIC), calculated pCO2 from DIC or TA, and δ13C-DIC.

## Study area
- Houzhai catchment, 73.4 km2, Guizhou Province, SW China.
- Climate: humid subtropical monsoon; mean annual precipitation ~1140 mm, mean temperature ~20.1°C.
- Elevation: 1,220–1,400 m a.s.l.
- Geology: Middle Triassic limestone and dolomite; karst hydrology features.

## Data collected and variables
- CO2 fluxes: F_CO2 and F_sd; along with water velocity, water depth, and water chemistry (T, pH, EC, DO, TA, DIC).
- Gas and carbon isotopes: pCO2 estimates from DIC and from TA; δ13C-DIC values.
- Sampling design: site-level measurements across four site types (streams, springs, sinkholes, reservoirs/ponds); most sites sampled monthly, with additional intensive sampling during rainfall events.
- Site metadata: 19 listed site entries with coordinates and type (e.g., sinkhole, spring, stream, reservoir).

## Methods
- CO2 flux measurement: floating chamber (volume 0.0028 m3) with 4-minute measurements, three repeats; flux calculated from CO2 accumulation rate.
- Flow velocity: measured with a flow meter (impeller); depth-averaged velocity calculated for h > 0.2 m using 0.2h and 0.8h averages, or a single value at 0.4h for shallower sites.
- Water chemistry and isotopes: at deployment, measure T and pH; collect samples within 15 minutes of flux measurement for [DIC], δ13C-DIC, and TA using headspace methods and titration; pCO2 calculated from DIC using Henry’s law with pH and temperature; DIC sometimes estimated from TA when direct measurement unavailable.
- Quality control: calibration with three isotopically distinct carbon standards; drift correction using a standard every 10 samples.

## Data structure and accessibility
- Single CSV file flux_and_13C_data with 19 columns (Sequence, ID, Type, Date, Time, F-CO2_, F_sd, TA, T, pH, EC, DO, Water_depth, Flow_velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC).
- Units: F-CO2 and F_sd in μmol m-2 s-1; TA and DIC in mmol L-1; T in °C; EC in μS cm-1; DO in mg L-1; depth/velocity in m and m s-1; pCO2 in μatm; d13C-DIC in ‰.
- Site information (Table 1) lists coordinates and site type for each monitoring location (streams, springs, sinkholes, reservoirs).

## Data governance and quality considerations for monitoring frameworks
- Strengths: robust QA/QC including triplicate flux measurements, regular instrument calibration, and drift correction; clear metadata on site types and sampling times.
- Metadata and provenance: detailed site information and measurement methods support traceability and reproducibility.
- Potential challenges for monitoring programs:
  - Missing DIC data requiring estimation from TA, which introduces uncertainty.
  - Predominantly monthly sampling may miss short-term dynamics; event-based sampling helps but may require more resources.
  - Public sharing of data is emphasized but can be a barrier if datasets are not readily accessible or well-documented.
  - Ensuring data standardization across datasets (units, calculation methods for pCO2) is essential for policy-relevant use.

## Applications for policy and future decisions
- Provides empirical carbon flux data in a karst-fluvial system, contributing to regional carbon budgets and hydro-ecological policy decisions.
- Demonstrates end-to-end data collection, QA/QC, and metadata practices that inform monitoring framework development, data governance, and data-sharing policies.
- Supports evaluation of karst hydrology’s influence on CO2 evasion and dissolved inorganic carbon dynamics, informing management of water quality and carbon policy in karst regions.

## References
- Zhang, Z., et al., Storage dynamics, hydrological connectivity and flux ages in a karst catchment: conceptual modelling using stable isotopes. Hydrol. Earth Syst. Sci., 2019.
- Waldron, S., et al., Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry. Rapid Communications in Mass Spectrometry, 2014.