# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- A 2022 ammonia (NH3) enhancement experiment at Queensberry Estate, central Sri Lanka (6.9693°N, 80.5911°E; altitude 1645 m) to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
- NH3 release is wind-controlled, directed toward monitoring quadrats (threshold speeds 0.3–10 m s^-1; wind direction 5–75° and 185–255°).
- NH3 concentrations measured at 1.5 m height along both quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from April to December 2022.
- Deposition (and emission) estimated with a four-layer canopy compensation point model, using a bi-directional resistance framework that includes stomatal compensation point and soil re-emission potential.
- Data support deposition flux estimates to the soil, understory vegetation, tree trunks, and tree canopy; allows comparison across multiple parameterizations of cuticular deposition and stomatal/soil pathways.

## Data collection and flux calculations
- Site details: Queensberry experimental site, central Sri Lanka; coordinates and altitude provided.
- Enhancement system: wind-controlled NH3 release tied to wind observations and speed thresholds.
- NH3 concentration measurement: performed at 1.5 m height along both monitoring quadrats with ALPHA samplers; monthly sampling cadence in 2022.
- Flux calculation framework:
  - Deposition flux Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is the total resistance to dry deposition.
  - Soil surface deposition uses quasi-laminar boundary layer resistance (Rbg).
  - Tree trunk deposition uses quasi-laminar boundary layer resistance (Rb(tt)).
  - Stomatal deposition uses stomatal resistance (Rs) with LAI dependency.
  - Four parameterizations for cuticular deposition flux (Rw) and one capacitance (Rd) parameterization for comparative purposes.
- Parameterizations for cuticular deposition flux:
  1) Rw (Massad et al., 2010): includes LAI dependency, with variable constants and environmental factors (RH, T).
  2) Rw (Jones et al., 2007): day/night parameterizations based on ambient NH3 concentration.
  3) Rw (DEPAC module; van Zanten et al., 2010): LAI Haarweg adjustment.
  4) Rd parameterization (Sutton et al., 1998): capacitance-based approach.
- Stomatal deposition (Rs) parameterization: Rs = min [ RsMax, RsMin(1 + α1/Rad) ] / (LAI)^0.5 with RsMax = 5000 s m^-1, RsMin = 35 s m^-1, α = 180 W m^-2, Rad = solar radiation.
- Notes: complete methodology and findings described in Deshpande et al. (2024).

## Data structure and content
- Dataset comprises 144 measurements across 13 parameters (capacity for multiple flux components and NH3 concentrations).
- Data format: CSV with columns including:
  - Distance (m; negative = southwest, positive = northeast)
  - Month
  - NH3_conc (µg m^-3) – monthly average NH3 concentration at 1.5 m height
  - Fg – cumulative NH3 deposition flux to the soil surface
  - Fs_us – cumulative stomatal deposition flux to understory vegetation
  - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones – cumulative cuticular deposition flux to understory vegetation (Massad 2010, DEPAC, Jones 2007)
  - Fd_us – cumulative deposition flux to understory vegetation (Sutton 1998 parameterization)
  - Ftt – cumulative deposition flux to tree trunks
  - Fs_tc – cumulative stomatal deposition flux to the tree canopy
  - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones – cumulative cuticular deposition flux to the tree canopy (Massad 2010, DEPAC, Jones 2007)
  - Fd_tc – cumulative deposition flux to the tree canopy (Sutton 1998)
- Negative flux values indicate emission rather than deposition.

## Quality control and limitations
- Data visually checked; obvious instrument or log issues removed.
- Regular-interval missing values due to scheduled power cuts; additional gaps from sensor replacements.
- Metadata notes provide transparency for data provenance and processing steps.

## Data usage and context
- Enables estimation and comparison of NH3 deposition pathways across soil, understory, tree trunks, and canopy in a tropical sub-mmontane forest.
- Supports cross-method comparisons for cuticular deposition parameterizations and validates bi-directional NH3 exchange modeling under tropical conditions.
- Complements analyses from similar wind-controlled NH3 enhancement experiments in Scotland and Sri Lanka, contributing to broader understanding of forest-NH3 exchanges.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key references underpinning methods and parameterizations, including Chamberlain (1968, 1984), Fowler (1978), Jones et al. (2007), Massad et al. (2010), Nemitz et al. (2000), Owen & Thomson (1963), Schuepp (1977), Sutton et al. (1998), van Zanten et al. (2010), and Deshpande et al. (2024).