# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Long-term study at Whim Moss ombrotrophic bog near Edinburgh (May 2002–Dec 2022) investigating effects of elevated atmospheric NH3 on vegetation and soils.
- NH3 release is controlled by wind direction and threshold speeds; monitoring conducted along fixed quadrats.
- Ammonia concentrations measured with UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; deposition to vegetation estimated using a unidirectional resistance model.
- Data collection includes changes in lateral and vertical sampling locations over time; deposition flux calculated per 15-minute period and summed monthly.
- 6296 measurements across 6 parameters are provided in a CSV, enabling time-series analyses and data integration with other environmental datasets.

## Data collection and flux calculations
- NH3 enhancement experiment established in 2002 to study impacts on moorland vegetation, bryophytes, lichens, and soil.
- NH3 release occurs only when wind direction aligns with monitoring transects (180–215 degrees) and wind speeds exceed 2.5 m s-1.
- NH3 concentrations (15-minute periods during release) derived from monthly averages; ambient concentrations used to adjust deposition estimates.
- Deposition flux to vegetation computed using a unidirectional resistance framework with total resistance Rt = Ra + Rb + Rc; deposition flux Fχ(z) = χa / Rt.
- Component resistances:
  - Ra: aerodynamic resistance derived from wind speed and friction velocity at measurement height.
  - Rb: boundary-layer resistance computed from Reynolds number and Schmidt number (for NH3).
  - Rc: canopy resistance, calculated differently for day and night during NH3 release, using empirically derived constants; a constant Rc is used during non-release periods.
- Deposition flux is estimated for each 15-minute period and summed monthly; complete methodology described in related studies (Leith et al. 2004; Jones et al. 2007; Cape et al. 2008).

## Data structure and contents
- Dataset contains 6296 measurements of 6 parameters.
- Columns (with two related fields each where applicable):
  - Month: Month and year.
  - ID: Sample identifier for ALPHA sampler (location and type; e.g., East/West, Control/Ambient).
  - Distance: Distance from NH3 source (meters); negative = upwind, positive = downwind.
  - Height: Measurement height above ground (meters).
  - NH3_conc: 1) instantaneous NH3 concentration (µg m^-3); 2) monthly average NH3 concentration.
  - Dep_kg_ha: 1) monthly deposition flux (kg ha^-1 month^-1); 2) monthly total NH3 dry deposition flux.
- Data include NA values where data are missing due to sampler damage/loss or calibration/meteorological data gaps.
- Data provided as a CSV; sampling locations and numbers may have changed over time.

## Quality control and limitations
- Visual QA performed; obvious instrument failures, sampler damage, power outages, and data loss removed.
- Monthly NH3 concentrations lower than ambient values removed to avoid negative deposition values.
- Missing data reflect changes in sampler locations or periods without complete meteorological records.
- Outputs may be site-specific (Whim Bog) with methods dependent on release periods and canopy characteristics; cross-site comparability requires careful alignment of methodologies.

## Data usage and potential products
- Enables exploration of temporal trends in NH3 concentration and dry deposition at a peatland site.
- Can be combined with other environmental datasets (meteorology, vegetation responses, soil chemistry) to assess deposition effects.
- Useful for building dashboards or reports that show self-serve access to NH3 concentration and deposition flux data, as well as for reproducible analysis workflows.
- Potential to analyze the effects of data gaps and sampler changes on derived deposition metrics; supports methodological comparisons with other NH3 deposition studies.

## Provenance, funding, and references
- Funding: Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.
- Key references for methodology and prior results:
  - Leith et al. (2004)
  - Jones et al. (2007)
  - Cape et al. (2008)
  - Fowler (1978)
  - Garland (1977)
  - Sutton et al. (1993)
  - Tang et al. (2001)
  - Smith et al. (2000)

## Notes for data integration and reuse
- When integrating with other datasets, align time stamps to monthly aggregates or 15-minute periods as appropriate.
- Be aware of changes in sampler locations and measurement heights over the study period; document any spatial-temporal changes during analyses.
- Consider the assumptions of the deposition model (Ra, Rb, Rc) and the day/night Rc parameterization when interpreting deposition flux results.