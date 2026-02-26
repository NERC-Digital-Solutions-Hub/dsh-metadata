# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Long-term study (2002–2022) of ammonia (NH3) enhancement and its dry deposition to mixed moorland vegetation at Whim Moss, near Edinburgh (55.76566°, -3.27155°, altitude 316 m).
- NH3 enhancement system is wind-controlled: release occurs only when wind direction is toward monitoring quadrats (180–215°) at speeds > 2.5 m s^-1.
- NH3 concentrations measured along monitoring transects using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analysis of samples.

## Methods: Data collection and deposition calculations
- Sampling approach:
  - 15-minute NH3 concentrations recorded during NH3 release periods.
  - Lateral and vertical sampling locations were adjusted over time to meet study needs.
  - NH3 deposition to vegetation estimated with a unidirectional resistance model (Rt = Ra + Rb + Rc).
- Key components:
  - Rt = total resistance to dry NH3 deposition (inverse of deposition velocity).
  - Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z.
  - Ra (aerodynamic resistance) computed from wind speed, friction velocity, and measurement/vegetation heights.
  - Rb (boundary-layer resistance) derived from Reynolds/Schmidt numbers and u*.
  - Rc (canopy resistance) calculated for NH3 release periods with daytime and nighttime formulations; constants are derived from prior work (Jones et al. 2007).
  - During non-release periods, Rc is held constant (20 s m^-1) with Ra and Rb monthly-averaged, making Rt independent of NH3 concentration.
- Concentration adjustments:
  - 15-minute concentrations during release periods (χ) derived from monthly-average NH3 concentrations and ambient concentrations, scaled by the proportion of release minutes in the month.
- Flux calculation:
  - Deposition flux is computed for each 15-minute interval and then summed over the month.
- References for methodology and models include Cape et al. (2008), Jones et al. (2007), Leith et al. (2004), and related foundational works.

## Quality Control
- Data visually inspected; errors from instrument failure, sampler damage, power outages removed.
- Monthly NH3 concentrations lower than ambient concentrations removed to avoid negative deposition values.
- Some missing values occur when ALPHA sampler locations were changed (removed/added) during a year.

## Data structure and contents
- Dataset size: 6296 measurements across 6 parameters.
- Data format: CSV file with the following structure:
  - Month: Month and year.
  - ID: Sample identifier (ALPHA sampler label).
  - Distance: Distance from NH3 source (positive downwind, negative upwind) in meters.
  - Height: Height above ground (meters) of measurement.
  - NH3_conc: 
    - NH3_conc,1 = 0.1 µg m^-3? (unit note in original: µg m^-3)
    - NH3_conc,2 = Monthly average NH3 concentration.
  - Dep_kg_ha:
    - Dep_kg_ha,1 = Monthly total NH3 deposition (kg ha^-1 month^-1)
    - Dep_kg_ha,2 = Monthly total NH3 deposition (same unit as above, clarified in dataset)
- Column details:
  - ID indicates transect position (E = East, W = West), sample type (Con = Control, Amb = Ambient).
  - Distance and height describe spatial context relative to the NH3 source.
- Data notes:
  - NA in NH3_conc indicates missing NH3 concentration data due to sampler damage/loss.
  - NA in Dep_kg_ha indicates missing deposition due to missing NH3 or meteorological data in a given month.

## Spatial and temporal details
- Location context:
  - Whim Moss peat bog (ombrotrophic) used to study NH3 deposition dynamics onto semi-natural vegetation.
- Spatial layout:
  - Monitoring along a transect with East/West designations; samples have a Distance value from the NH3 source indicating upwind/downwind position.
- Temporal scope:
  - Measurements collected and deposited values computed monthly, with 2002–2022 coverage.

## Data use and GIS considerations
- Ideal for map-based visualisations of NH3 concentrations and dry deposition flux across space (distance from source, transect direction) and time (monthly deposition).
- Important to handle data gaps due to sampler changes and to account for periods with no NH3 release (constant Rc and time-averaged Ra/Rb).
- Attributes to map:
  - NH3_conc (monthly and/or 15-minute-derived values), Dep_kg_ha (monthly deposition), Distance, Height, ID, E/W/Amb/Con classifications.
- Limitations:
  - Data gaps where samplers were moved or removed; potential variability in Rc formulation between day/night periods.
  - Monthly aggregation may mask short-term dynamics during release periods.

## Funding and references
- Funding: Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme delivering National Capability.
- References (selected):
  - Cape et al. 2008; Jones et al. 2007; Leith et al. 2004; Smith et al. 2000; Sutton et al. 1993; Tang et al. 2001; Wesely & Hicks 1977; plus related foundational works on dry deposition modelling.

## Summary for GIS Specialists
- A rich, long-term dataset combining spatially distributed NH3 concentrations and calculated dry deposition flux for a peatland site, suitable for spatial-temporal analysis and map-based visualization.
- Key spatial fields include Distance from source, Height, and transect orientation (E/W); temporal field is Month with monthly deposition totals.
- Data processing notes:
  - Use standard Rt = Ra + Rb + Rc deposition-velocity framework; Rc varies by day/night and NH3 concentration, with special handling when no release occurs.
  - Account for sampler changes when interpreting gaps and missing values.
- Data format: CSV with 6 primary parameters and 6296 measurements; NA values indicate missing concentration or deposition data.