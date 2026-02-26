# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Purpose and scope
- Investigates the impact of elevated atmospheric ammonia (NH3) on tropical forest vegetation, bryophytes, lichens, and soil.
- Establishes an NH3 enhancement system in a tropical sub-montane forest site (Queensberry Estate, Sri Lanka) to study deposition and emission processes.
- Extends an earlier dataset (2022) with improvements to deposition modelling and time-resolved concentration peaks.

## Data collection and flux calculations
- Enhancement system controlled by wind conditions to release NH3 only when wind direction targets monitoring quadrats (5–75° and 185–255°) and at threshold speeds (0.3–10 m s−1).
- NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analyses conducted monthly from January 2023 to December 2024.
- Deposition and emission from different surfaces estimated via a four-layer canopy compensation point model and a bi-directional resistance framework, accounting for stomatal, soil, trunk, and canopy processes.
- Deposition flux to each surface calculated using respective resistances:
  - Soil: quasi-laminar boundary layer resistance (Rbg)
  - Tree trunks: quasi-laminar boundary layer resistance around trunks (Rb(tt))
  - Stomatal deposition: stomatal resistance (Rs) with LAI dependency
  - Cuticular deposition: multiple parameterizations (Rw) with LAI dependence; includes four parameterizations (Massad et al. 2010; Jones et al. 2007; DEPAC module; Haarweg LAI)
  - Capacitance-based parameterization (Rd) for cuticular processes
- Deposition flux formulations (e.g., Fχ(z) = χa / Rt) integrate ambient NH3 concentrations with resistances to estimate fluxes to soil, understory, and canopies.

## Modelling improvements and time resolution
- Introduces a time-resolved approach: NH3 concentration peaks during release periods drive deposition estimates, while ambient NH3 concentrations drive deposition outside release periods.
- Improves upon earlier methodology that used mean monthly NH3 for all time intervals, enabling more accurate peak deposition estimates during NH3 release.

## Data products and structure
- Dataset comprises 816 measurements across 13 parameters.
- Stored in a CSV with the following columns:
  - Distance (m; positive = northeast, negative = southwest relative to source)
  - Month (monthly granularity)
  - NH3_conc (µg m−3; monthly average at 1.5 m)
  - Fg (soil deposition flux; kg ha−1; negative indicates emission)
  - Fs_us (stomatal deposition to understory; kg ha−1; negative indicates emission)
  - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (cuticular understory deposition; kg ha−1)
  - Fd_us (cuticular understory deposition; kg ha−1)
  - Ftt (tree trunk deposition; kg ha−1)
  - Fs_tc (stomatal deposition to tree canopy; kg ha−1)
  - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones (cuticular canopy deposition; kg ha−1)
  - Fd_tc (cuticular canopy deposition; kg ha−1)
- Data allow negative values to indicate emission and positive values to indicate deposition; distance sign indicates direction relative to NH3 source.

## Quality control and data management
- Visual quality checks performed; obvious instrument/method errors removed.
- Missing values largely due to scheduled power cuts; additional gaps from sensor replacement.
- Dataset constitutes an extension of the 2022 dataset, with enhanced modelling and time-resolved deposition estimates.

## Data access and governance
- Funded by the UKRI GCRF South Asian Nitrogen Hub.
- Data described and made accessible via external data centres (e.g., NERC EDS Environmental Information Data Centre) with formal references and DOIs.

## Key methodological details and references
- Bi-directional exchange and resistance modelling grounded in established literature (e.g., Chamberlain; Massad et al.; Nemitz et al.; Sutton et al.; DEPAC module).
- Four-layer canopy compensation point model integrates stomatal, soil, trunk, and canopy resistances to estimate deposition fluxes.
- Multiple parameterizations for cuticular deposition allow cross-comparison and sensitivity analysis (Massad 2010; Jones 2007; DEPAC 2010; Haarweg LAI).
- References provide foundational equations for boundary-layer resistances, deposition velocities, and parameterizations used in the dataset.

## Implications for monitoring frameworks
- Demonstrates integration of field experiments, mechanistic atmospheric chemistry modelling, and transparent data sharing to support policy-relevant monitoring.
- Highlights importance of time-resolved deposition estimates (not just monthly means) for accurately assessing emission/ deposition dynamics.
- Emphasizes data governance aspects (metadata clarity, openness, and reproducibility) by publishing full dataset and modelling approach, while acknowledging practical data collection challenges (power outages, sensor maintenance).
- Provides a replicable framework for monitoring NH3 deposition to forest ecosystems in other regions, with adaptable parameterizations and explicit data structures.

## Funding
- UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).