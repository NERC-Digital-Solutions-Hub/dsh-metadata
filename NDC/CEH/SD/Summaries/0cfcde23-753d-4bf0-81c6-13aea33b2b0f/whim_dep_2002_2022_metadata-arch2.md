# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Long-term dataset (2002–2022) documenting ammonia (NH3) concentrations and dry deposition to mixed moorland vegetation at Whim Moss, Scotland.
- Experiment configured to study effects of elevated atmospheric NH3 on vegetation, bryophytes, lichens, and soil; NH3 release is wind-direction controlled to target monitoring quadrats.
- Data include both ambient/concentrated NH3 concentrations and calculated dry deposition fluxes using a concentration-dependent deposition model.

## Methods

- Study site and setup
  - Location: ombrotrophic bog at Whim Moss (55.76566°, -3.27155°; altitude 316 m), near Edinburgh.
  - Enhancement system releases NH3 only when wind is from 180–215° toward monitoring quadrats and above threshold wind speeds (>2.5 m s−1).

- NH3 concentration data collection
  - Instrument: UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
  - Sampling locations (lateral and vertical) changed over time to meet study requirements.
  - Measurement cadence: monthly analyses of NH3 concentrations; high-frequency (15-minute) concentrations derived during NH3 release periods.

- Deposition flux calculation
  - Deposition to vegetation estimated with a unidirectional resistance model: Fχ(z) = χa / Rt, where Rt is the total resistance (Ra + Rb + Rc).
  - Components:
    - Ra (aerodynamic resistance) derived from wind speed, friction velocity, and measurement heights.
    - Rb (boundary-layer resistance) parameterized from Reynolds number and Schmidt number.
    - Rc (canopy resistance) computed from daytime/night-time formulations, with constants from Jones et al. (2007).
  - During NH3 release: Rc(daytime) and Rc(night-time) computed using adjusted χ and constants; during no-release periods Rc is fixed (≈20 s m−1) and Rt uses monthly Ra and Rb with ambient NH3 concentrations.
  - Flux calculations performed for each 15-minute period and summed monthly.
  - Reference models and parameters drawn from related literature (Jones et al. 2007; Leith et al. 2004; Cape et al. 2008; etc.).

- Quality control
  - Visual checks; removal of data affected by instrument failure, sampler damage/loss, power outages.
  - Monthly NH3 concentrations below ambient values removed to avoid negative deposition flux.
  - Missing values occur where sampler locations changed or data were lost.

## Data structure and content

- Dataset size and contents
  - 6296 measurements across 6 parameters.
  - Data provided in a CSV with the following structured columns and descriptors:
    - Month: Month and year (format: Month).
    - ID: Sample identification label for ALPHA sampler (east/west; control/ambient).
    - Distance: Distance from NH3 source (meters); negative = upwind, positive = downwind.
    - Height: Measurement height above ground (meters).
    - NH3_conc: NH3 concentration; includes ambient and/or monthly average values.
    - Dep_kg_ha: Monthly dry deposition flux (kg ha−1 month−1); includes monthly total deposition.
  - Additional categorical descriptors:
    - E/W: East or West of main transect.
    - Con/Amb: Control or Ambient.
  - NA values indicate missing data due to sampler damage/loss or data gaps.

- Data access and format
  - CSV file available containing the full time series and associated measurements.
  - Missing data explicitly marked as NA in NH3_conc (concentration data) and Dep_kg_ha (deposition flux).

## Funding and references

- Funding: Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme delivering National Capability.
- Key references for methods and modelling components:
  - Cape et al. 2008; Fowler 1978; Garland 1977; Jones et al. 2007; Leith et al. 2004; Smith et al. 2000; Sutton et al. 1993; Tang et al. 2001; Wesely & Hicks 1977.

## Relevance for environmental monitoring and policy

- Demonstrates a complete data lifecycle for environmental monitoring:
  - Standardized data collection using established samplers.
  - Transparent, chemistry- and physics-based deposition modelling.
  - Rigorous quality control and clear data provenance.
  - Structured data storage and explicit metadata describing measurement context (location, height, distance, transect direction, release status).
- Enables cross-site or longitudinal comparisons by providing standardized NH3 concentration and deposition metrics over two decades.
- Supports integration with other environmental datasets to enhance value beyond single-use analyses, aligning with monitoring objectives to assess environmental health and policy performance over time.