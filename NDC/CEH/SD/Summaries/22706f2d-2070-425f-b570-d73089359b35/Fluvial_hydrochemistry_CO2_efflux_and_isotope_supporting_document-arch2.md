# Fluvial hydrochemistry, CO2 efflux and delta 13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

- This dataset comes from the NERC-funded project addressing atmospheric CO2 efflux from fluvial systems in karst landscapes. It measures CO2 fluxes from streams, springs, sinkholes, and standing water bodies in the Houzhai catchment (SW China) to quantify karst-related CO2 emissions.
- The study area is the Houzhai catchment (73.4 km2) in Guizhou, China, with a humid subtropical monsoon climate, elevations 1,220–1,400 m, and limestone/dolomite geology.

Overview of data and variables

- Primary measurements:
  - CO2 efflux rate (F_CO2) with associated water velocity and water chemistry: temperature (T), pH, dissolved oxygen (DO), electrical conductivity (EC), total alkalinity (TA), dissolved inorganic carbon (DIC), and partial pressure of CO2 (pCO2, calculated from DIC and TA/pH).
  - Stable isotope data: δ13C of DIC (δ13C-DIC).
- Sampling cadence and scope:
  - Most sites monitored monthly; some intensive monitoring during rainfall events.
  - Sites include streams, springs, sinkholes, reservoirs/ponds (varied types listed in site table).
- Data file and structure:
  - One CSV file: flux_and_13C_data with 19 columns, including identifiers, date/time, F_CO2 and its standard deviation, TA, T, pH, EC, DO, water depth, flow velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, and d13C-DIC.
  - Units specified for each variable (e.g., F_CO2 in μmol m-2 s-1, DIC in mmol L-1, pCO2 in μatm, d13C-DIC in ‰).

Methods and quality control

- CO2 flux measurement:
  - Floating chamber method with a known volume (0.0028 m3); CO2 accumulation over 4 minutes, repeated three times to obtain mean flux.
  - Flux calculation formula provided: F_CO2 = (δCO2/δt) × (V / (R × T × S)).
- Hydrology and water chemistry:
  - Depth-averaged flow velocity (ū) measured with a flow meter; depth-based averaging rules for h > 0.2 m or a single value for shallower water.
  - At deployment, water temperature and pH measured; water samples collected within 15 minutes for [DIC], δ13C-DIC, and TA using headspace method and titration.
  - DIC sometimes estimated from TA, pH, and equilibrium constants; pCO2 calculated from DIC (pCO2_DIC) and from TA (pCO2_TA).
- Quality control and calibration:
  - DIC and δ13C-DIC measured with a headspace method and Thermo-Fisher Gas Bench/Delta V plus; calibration with three isotopically distinct inorganic carbon standards.
  - Standards included every 10 samples to correct for instrument drift.

Data management and accessibility

- Data structure details:
  - Column definitions include Sequence, ID, Type (site type), Date, Time, F-CO2, F_sd, TA, T, pH, EC, DO, Water_depth, Flow_velocity, DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC.
  - Explicit notes on units for each parameter.
- Site information:
  - Comprehensive table of site IDs, coordinates, and site types (e.g., Stream, Spring, Sinkhole, Reservoir) across Houzhai catchment.
- Data stewardship:
  - Data are presented with clear documentation of sampling times, methods, and QA/QC procedures.
  - Dataset is positioned for storage in appropriate data portals in line with monitoring/archiving practices.

Context and references

- References:
  - Zhang et al., 2019: conceptual modeling of storage dynamics and fluxes in karst catchments.
  - Waldron et al., 2014: methodology for quantifying DIC stable isotopes using continuous-flow isotope-ratio mass spectrometry.

Potential uses and alignment with the Analysts Monitoring the Environment archetype

- The dataset follows standardized monitoring and analytical protocols, enabling consistent cross-site comparisons and temporal trend analysis.
- Outputs are clearly tabulated and machine-readable, suitable for inclusion in environmental health dashboards, policy performance reviews, and long-term monitoring reports.
- The dataset emphasizes quality assurance, standardization, and traceability, aligning with the archetype’s emphasis on verifiable data used to assess environmental health over time.
- Challenge addressed: provides a framework for increasing dataset value through integration with related hydrological or atmospheric data to support broader analyses and data portal accessibility.