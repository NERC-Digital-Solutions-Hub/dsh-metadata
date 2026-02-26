# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Studies the effects of high ammonia (NH3) in the air on forest vegetation, bryophytes, lichens, and soil at the Queensberry Estate, central Sri Lanka (6.9693°, 80.5911°, altitude 1645 m).
- NH3 enhancement system is wind-controlled; NH3 released only when wind direction and speed meet specified conditions.
- NH3 concentrations measured at 1.5 m height along monitoring quadrats; monthly analysis from April to December 2022.
- Deposition (and emission) estimated for soil surface, understory vegetation, tree trunks, and tree canopy using a four-layer canopy compensation point bi-directional resistance model.
- Data collected and analyzed with a focus on map-based visualization and spatial interpretation of NH3 fluxes.

## Data collection and deposition modeling
- NH3 concentrations measured using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analysis conducted monthly.
- Deposition flux Fχ(z) calculated as χa / Rt, where Rt is the total resistance to dry deposition.
- Flux components estimated for:
  - Soil surface (Rbg parameterization)
  - Tree trunks (Rb(tt) parameterization)
  - Stomatal deposition (Rs with Leaf Area Index dependence)
  - Cuticular deposition (multiple parameterizations; with LAI-dependency)
- Cuticular deposition parameterizations include:
  - Massad et al. (2010)
  - Jones et al. (2007)
  - DEPAC module (van Zanten et al., 2010)
  - Sutton et al. (1998)
- Stomatal deposition includes maximum and minimum resistances with LAI scaling; Rs is influenced by radiation.
- Day vs. night parameterizations (based on solar radiation) and an additional DEPAC module for acidifying compounds.
- Complete methodological details available in Deshpande et al. (2024).

## Data structure and variables
- Dataset includes 144 measurements across 13 parameters.
- Data provided in a CSV with fields:
  - Distance (m): distance from NH3 enhancement source; negative = southwest, positive = northeast.
  - Month: month and year.
  - NH3_conc (µg m^-3): monthly average NH3 concentration at 1.5 m height.
  - Fg (kg ha^-1): cumulative NH3 deposition flux to soil.
  - Fs_us (kg ha^-1): cumulative stomatal deposition to understory vegetation.
  - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (kg ha^-1): cumulative cuticular deposition to understory from different parameterizations.
  - Fd_us (kg ha^-1): cumulative cuticular deposition to understory (Sutton/1998 parameterization).
  - Ftt (kg ha^-1): cumulative deposition flux to tree trunks.
  - Fs_tc (kg ha^-1): cumulative stomatal deposition to tree canopy.
  - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones (kg ha^-1): cumulative cuticular deposition to tree canopy (different parameterizations).
  - Fd_tc (kg ha^-1): cumulative cuticular deposition to tree canopy (Sutton/1998 parameterization).
- Negative flux values indicate emission; distance direction encodes spatial orientation.

## Quality control
- Data visually checked; obviously erroneous data due to instrument malfunctions, datalogger issues, or power cuts removed.
- Regular gaps are due to scheduled power outages; some gaps from sensor replacement.

## GIS-ready considerations and usage
- Spatial dimension represented by distance and direction from the NH3 source; enables conversion to geolocated map layers if source coordinates are defined.
- Temporal dimension with monthly NH3 concentrations and deposition fluxes supports time-enabled maps or animations.
- Multiple deposition parameterizations allow comparative visualization of soil, understory, trunk, and canopy contributions.
- Clear metadata on units, sign convention (negative = emission; positive = deposition) and directionality supports accurate map-based interpretation.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key references underpinning the deposition modeling and parameterizations (e.g., Chamberlain 1968; Fowler 1978; Massad et al. 2010; Nemitz et al. 2000; Sutton et al. 1998; Jones et al. 2007; van Zanten et al. 2010; Deshpande et al. 2024).