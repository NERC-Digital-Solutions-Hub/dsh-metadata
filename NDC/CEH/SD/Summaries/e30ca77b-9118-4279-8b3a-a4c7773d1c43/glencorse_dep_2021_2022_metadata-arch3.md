# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Provides data from an NH3 enhancement experiment in a Birch plantation at Glencorse woodland near Edinburgh (55.8539°, -3.2151°, altitude 200 m) to study how elevated ammonia affects forest vegetation, bryophytes, lichens, and soil.
- Combines measured concentrations with a four-layer canopy deposition model to estimate deposition fluxes to soil, understory, trunks, and canopy.
- Data are structured to support evaluation of ammonia deposition processes and to inform policy-relevant environmental health monitoring.

## Experimental design and measurements
- Enhancement system releases NH3 only when wind direction is between 275–345 degrees and above-threshold wind speeds (0.310 m s^-1), controlled by below-canopy wind measurements.
- NH3 concentrations measured at 1.5 m height along a monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analysis from Sept 2021 to Dec 2022.
- Vertical NH3 concentration gradients measured at multiple heights and distances (4, 10, 16 m from source) to drive canopy-wise deposition modeling.
- The study models deposition and emission fluxes across four canopy layers (soil surface, understory vegetation, tree trunks, tree canopy) using a bi-directional resistance framework.

## Modeling approach and key equations
- Deposition flux at height z: Fχ(z) = χa / Rt, where χa is ambient NH3 concentration and Rt is the total resistance to deposition (inverse of deposition velocity Vd).
- Soil deposition: governed by soil surface quasi-laminar boundary layer resistance Rbg with a specified parameterization.
- Tree trunks: modeled with quasi-laminar boundary layer resistance around trunks (Rb(tt)) depending on friction velocity and canopy/ Reynolds relationships.
- Stomatal deposition: modeled with stomatal resistance Rs, incorporating Leaf Area Index (LAI) and environmental factors.
- Cuticular deposition: evaluated using four parameterizations (with LAI dependency and phenological adjustments):
  - Massad et al. (2010) style resistance with RH and T adjustments.
  - Jones et al. (2007) daytime and nighttime formulations based on ambient NH3 concentration.
  - DEPAC module (van Zanten et al., 2010) adjustments with LAI Haarweg values.
  - Sutton et al. (1998) capacitance-based approach.
- Additional equations incorporate Schmidt number, Reynolds number, and related constants for gas exchange processes.
- Complete methodology and model integration are detailed in the associated Deshpande et al. (2024) publication.

## Data collection, quality control, and structure
- Quality control: visual checks for instrument errors, datalogger issues, and power outages; gaps attributed to scheduled power cuts or sensor replacements.
- Dataset composition: 126 measurements across 17 parameters.
- Data format: CSV with columns including distance from NH3 source, month, measured NH3 concentration at 1.5 m, modeled concentrations at soil/understory/trunk/canopy heights, and cumulative deposition fluxes for various compartments (soil, understory, trunk, canopy) using multiple parameterizations.
- Example variables include:
  - NH3_conc_measured (µg m^-3)
  - NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc (modelled concentrations at respective canopy layers)
  - Fg (soil deposition), Fs_us (stomatal understorey deposition), Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (cuticular understorey deposition, multiple parameterizations)
  - Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc (canopy deposition and related fluxes)
- Data organization: distance is in meters with sign conventions for directions; month field denotes time; deposition flux signs indicate emission when negative.

## Data governance, accessibility, and context
- The facility and data collection were funded by UKRI GCRF South Asian Nitrogen Hub.
- References underpinning the modeling approaches and parameterizations are provided (Chamberlain; Fowler; Jones et al.; Massad et al.; Nemitz et al.; Owen & Thomson; Schuepp; Sutton et al.; van Zanten et al.; Wesely & Hicks).
- Complete experimental design, methodology, analysis, and findings are reported in Deshpande et al. (2024).

## Relevance for monitoring frameworks
- Demonstrates an integrated approach to environmental health monitoring: coordinated field measurements, vertical profiling, and multi-layer canopy deposition modeling.
- Addresses data challenges common in monitoring frameworks: data gaps due to power/sensor issues, need for robust metadata and parameterization choices, and the importance of transparent data structure for policy evaluation.
- Supports decision-making by providing detailed deposition flux estimates across different forest components, enabling policy-relevant assessment of ammonia impacts on forest ecosystems.
- Highlights data governance considerations: openness of underlying data, need to attach comprehensive metadata, and the potential barriers related to sharing complex, model-derived outputs.