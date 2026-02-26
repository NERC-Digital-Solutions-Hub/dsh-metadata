# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- A 2022 ammonia (NH3) enhancement experiment in a tropical sub-montane forest at Queensberry Estate, central Sri Lanka, to study NH3 effects on vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate (approx. 6.9693° N, 80.5911° E), altitude 1645 m.
- Data types: NH3 concentrations and bi-directional deposition flux estimates across distances from the NH3 source and monthly intervals (April–December 2022).

## Data collection and flux calculations
- NH3 enhancement system is wind-controlled, releasing NH3 only when wind direction favors monitoring quadrats and at threshold speeds (0.3–10 m/s).
- NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analyzed monthly from April to December 2022.
- Deposition (and emission) are estimated with a four-layer canopy compensation point model using a bi-directional resistance framework that accounts for stomatal and soil re-emission processes.
- Deposition flux concepts include contributions from soil surface, understory vegetation, tree trunks, and tree canopy (with respective resistances such as Rbg, Rb(tt), Rs, and Rd for cuticular pathways).
- Multiple parameterizations for cuticular deposition flux (Rw) are used, including Massad et al. (2010), Jones et al. (2007), DEPAC module, and a capacitance-based approach (Rd). Parameters consider leaf area index (LAI), time of day (day/night), relative humidity, temperature, solar radiation, and other factors.
- Complete methodology and calculations are described in Deshpande et al. (2024).

## Data structure and fields
- Dataset: 144 measurements across 13 parameters.
- CSV columns (Distance in meters from NH3 source; Month) and 13 NH3-related fields:
  - NH3_conc: NH3 concentration at 1.5 m height (µg m^-3)
  - Fg: soil deposition flux (kg ha^-1)
  - Fs_us: understory stomatal deposition flux (kg ha^-1)
  - Fw_us_Massad: understory cuticular flux (Massad et al. 2010) (kg ha^-1)
  - Fw_us_DEPAC: understory cuticular flux (DEPAC) (kg ha^-1)
  - Fw_us_Jones: understory cuticular flux (Jones et al. 2007) (kg ha^-1)
  - Fd_us: understory cuticular flux (Sutton et al. 1998) (kg ha^-1)
  - Ftt: tree trunk deposition flux (kg ha^-1)
  - Fs_tc: tree canopy stomatal deposition flux (kg ha^-1)
  - Fw_tc_Massad: tree canopy cuticular flux (Massad et al. 2010) (kg ha^-1)
  - Fw_tc_DEPAC: tree canopy cuticular flux (DEPAC) (kg ha^-1)
  - Fw_tc_Jones: tree canopy cuticular flux (Jones et al. 2007) (kg ha^-1)
  - Fd_tc: tree canopy cuticular flux (Sutton et al. 1998) (kg ha^-1)
- Notes: Negative flux values indicate emission rather than deposition.

## Quality control
- Data visually checked; obvious instrument malfunctions and datalogger/power issues removed.
- Regular-missed values due to scheduled power cuts; additional gaps from sensor replacement.

## Data provenance, usage, and funding
- Complete experimental design, methodology, analysis, and findings detailed in Deshpande et al. (2024).
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Data readiness: CSV format suitable for self-serve analysis, visualization, and integration with other environmental datasets to compare NH3 concentration and deposition across sites or parameterizations. Potential outputs include dashboards of NH3 concentrations and deposition flux by distance and time, and cross-parameterization comparisons (Massad, Jones, DEPAC, etc.).