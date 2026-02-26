# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

## Overview
- Ammonia (NH3) enhancement experiment conducted in a Birch plantation at Glencorse woodland near Edinburgh (Birch plantation coordinates 55.8539°, -3.2151°, altitude 200 m) to study NH3 impacts on forest vegetation, bryophytes, lichens, and soil.
- Established in 2022; data reported for January 2023 to December 2024.
- Aimed at estimating NH3 deposition and emission across soil surface, understory vegetation, tree trunks, and tree canopy using a bi-directional resistance model.

## Data collection and measurement
- NH3 enhancement system controlled by wind conditions measured below the canopy; NH3 released only when wind blows from 275–345 degrees toward monitoring quadrats at threshold speeds of 0.31 m/s.
- NH3 concentrations measured at 1.5 m height along monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analysed monthly.
- Monitoring includes multiple vertical/horizontal sampling zones: soil surface (0.05 m), understory (0.5 m), trunk surfaces (1.75 m), and canopy (3.5 m).

## Modelling approach and flux calculations
- Uses a four-layer canopy compensation point model and a bi-directional resistance framework incorporating stomatal compensation point and soil re-emission potential.
- Deposition flux F is computed as F = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance to dry deposition.
- Deposition to soil (Rbg) and to tree trunks (Rb(tt)) are parameterized with established resistance formulations, plus stomatal (Rs) and cuticular (Rw) resistances.
- Cuticular deposition fluxes are evaluated with four parameterizations (Massad et al. 2010; Jones et al. 2007; DEPAC module; Sutton et al. 1998), all LAI-dependent. Stomatal deposition uses Rs with LAI dependency. A capacitance-based parameterization (Rd) is also used.
- Key resistance components:
  - Soil: Rbg (quasi-laminar boundary layer resistance)
  - Tree trunks: Rb(tt) (quasi-laminar boundary layer around trunks)
  - Stomatal: Rs
  - Cuticular: Rw (several parameterizations)
  - Capacitance: Rd
- Overall deposition velocity Vd is the inverse of Rt.

## Model improvements and time dynamics
- Current model version simulates NH3 concentration peaks during release periods to estimate deposition, while ambient NH3 drives deposition when releases stop.
- This is an improvement over the previous version that used mean monthly NH3 concentrations for all time intervals, enabling better capture of release-driven deposition peaks.

## Data structure and contents
- Dataset: 108 measurements across 17 parameters.
- Format: CSV with columns including:
  - Distance (m; negative = southwest, positive = northeast)
  - Month (year-month)
  - NH3_conc_measured (µg m-3; 1.5 m height)
  - NH3_conc_soil (µg m-3; soil surface, 0.05 m)
  - NH3_conc_us (µg m-3; understory 0.5 m)
  - NH3_conc_ts (µg m-3; trunk surfaces 1.75 m)
  - NH3_conc_tc (µg m-3; canopy 3.5 m)
  - Fg (kg ha-1; cumulative soil deposition flux)
  - Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us (kg ha-1; various understory deposition components; negative values indicate emission)
  - Ftt (kg ha-1; trunk deposition)
  - Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc (kg ha-1; canopy deposition components)
- Notes:
  - Negative flux indicates emission.
  - Distance sign indicates direction relative to NH3 source.
- Data source references include the enhanced, extended 2023–2024 dataset, with links to 2022 data for comparison.

## Quality control and data availability
- Visual quality control performed; obvious instrument/malfunction errors removed.
- Some regular-interval gaps due to scheduled power cuts; additional gaps during sensor replacement.
- Data were validated and curated to be suitable for correlation analysis, model validation, and comparison of deposition parameterizations.

## Scope for analysts
- Enables analysis of spatial and vertical variation in NH3 concentrations and deposition across soil, understory, trunks, and canopy.
- Supports comparison of multiple deposition parameterizations (Massad, Jones, DEPAC, Sutton) within a consistent experimental framework.
- Facilitates exploration of the relationship between ambient NH3 concentrations, release-driven peaks, and actual deposition flux across different forest compartments.
- Provides a dataset to test and calibrate bi-directional exchange models and canopy deposition resistance approaches.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Key references underpinning the modelling framework and parameterizations include works by Chamberlain, Fowler, Massad et al., Nemitz et al., Jones et al., Sutton et al., van Zanten et al., and related 2010–2017 literature; Deshpande et al. (2024a, 2024b) provide complete methodology, analysis, and dataset integration.