# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Purpose and scope
- Investigates effects of high ambient ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Conducted as a wind-controlled NH3 enhancement experiment at Queensberry Estate, Sri Lanka (2022).
- Aims to quantify NH3 concentration and deposition fluxes to different ecosystem components (soil, understory vegetation, tree trunks, canopy).

## Study design and data collection
- Enhancement system is controlled by wind direction (5–75°, 185–255°) and threshold wind speeds (0.3–10 m s⁻¹).
- NH3 concentrations measured at 1.5 m height along two monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analysed monthly April–December 2022.
- Deposition and emission estimated using a four-layer canopy compensation point model (bi-directional resistance framework) accounting for stomatal and soil re-emission processes.
- Deposition flux components include soil surface, understory vegetation, tree trunks, and tree canopy, with multiple flux parameterizations for cuticular deposition.

## Modelling approach to deposition and fluxes
- Deposition flux to height z: Fχ(z) = χa / Rt, with Rt as total resistance to dry deposition.
- Soil deposition flux uses quasi-laminar boundary layer resistance (Rbg); trunk deposition uses quasi-laminar boundary layer around trunks (Rb(tt)).
- Stomatal deposition flux uses stomatal resistance (Rs) with LAI dependency.
- Cuticular deposition fluxes estimated using four parameterizations (Rw) plus one capacitance (Rd) parameterization:
  - Rw(min) variant (Massad et al., 2010) with LAI scaling
  - Rw(day) and Rw(night) parameterizations (Jones et al., 2007;  for day/night with LAI dependence)
  - DEPAC-based parameterization (van Zanten et al., 2010) with LAI Haarweg
  - Rw = function of LAI and other environmental factors
- Day-time vs night-time parameterizations chosen based on solar radiation thresholds.
- Complete methodological details and equations are provided in the associated Deshpande et al. 2024 publication.

## Dataset structure and content
- 144 measurements across 13 parameters.
- CSV structure with fields including:
  - Distance (m; negative = southwest, positive = northeast)
  - Month (year and month)
  - NH3_conc (µg m⁻³): monthly average NH3 concentration at 1.5 m
  - Deposition/flux components: Fg (soil), Fs_us (stomatal deposition to understory), Fw_us_Massad (cuticular to understory, Massad 2010), Fw_us_DEPAC, Fw_us_Jones, Fd_us (cuticular, Sutton 1998), Ftt (tree trunk deposition), Fs_tc (stomatal to canopy), Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc (canopy deposition)
  - Negative flux indicates emission
- Includes location data and metadata:
  - Coordinates: 6.9693° N, 80.5911° E
  - Altitude: 1645 m
- Dataset funding noted; broader methodology linked to Deshpande et al. (2024).

## Quality control and data handling
- Visual data checks to remove instrument malfunctions, datalogger issues, and power-cut-related errors.
- Regular missing values attributed to scheduled power cuts; additional gaps from sensor replacements.
- Data underwent cleaning, structuring, and preparation for deposition flux calculations.

## Metadata, accessibility, and governance
- Dataset described with detailed column metadata and parameter definitions to support reuse and verification.
- Underlying study funded by UKRI GCRF South Asian Nitrogen Hub, supporting transparency and open data principles.
- Full methodological detail and context available in Deshpande et al. (2024).

## Limitations and caveats
- Data limited to April–December 2022, with monthly NH3 concentration measurements at 1.5 m height.
- Flux estimates rely on multiple parameterizations; variability across models highlights uncertainty in deposition pathways (soil, understory, trunks, canopy, cuticular vs stomatal routes).
- Potential impacts of canopy structure, phenology, and local meteorology on deposition not exhaustively captured beyond the implemented models.

## Relevance for monitoring frameworks
- Demonstrates integration of field measurements with process-based deposition models to quantify NH3 exchange across ecosystem compartments.
- Shows practical data governance steps (QC, metadata, multiple parameterizations, clear data structure) that support evaluation of environmental health policies and decision-making.
- Provides a structured dataset suitable for benchmarking, meta-analysis, and informing future monitoring enhancements in tropical forest contexts.

## Funding
- UKRI GCRF South Asian Nitrogen Hub.

## References (key models and sources)
- Chamberlain (1968); Chamberlain et al. (1984)
- Fowler (1978)
- Jones et al. (2007)
- Massad et al. (2010)
- Nemitz et al. (2000)
- Owen & Thomson (1963)
- Schuepp (1977)
- Sutton et al. (1998)
- van Zanten et al. (2010)