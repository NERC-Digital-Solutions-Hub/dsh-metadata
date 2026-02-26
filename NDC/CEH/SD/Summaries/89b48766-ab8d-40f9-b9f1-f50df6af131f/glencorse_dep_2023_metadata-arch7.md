# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

## Objective and scope
- Study of ammonia (NH3) enhancement effects on forest vegetation, bryophytes, lichens, and soil using a wind-controlled release system.
- Measurements collected Jan 2023 – Dec 2024 at Glencorse woodland near Edinburgh (Birch plantation).
- Data extend the 2022 dataset; improved bi-directional resistance/deposition model to capture NH3 peaks during release periods.

## Study site and data collection
- Location: Glencorse woodland, near UKCEH, Edinburgh; coordinates 55.8539°N, -3.2151°W; altitude ~200 m.
- NH3 enhancement system: releases NH3 only when wind is directed toward monitoring quadrats (275–345 degrees) and above a threshold wind speed (0.31 m/s), controlled by wind conditions measured below the canopy.
- NH3 concentration measurements: at 1.5 m height along the monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses.
- Spatial/vegetation context: measurements across multiple canopy layers—soil surface, understory vegetation, tree trunks, and tree canopy.

## Modelling and calculation approach
- Deposition modelling: four-layer canopy compensation point model; bi-directional resistance model accounting for stomatal and soil re-emission processes.
- Deposition flux formulation: Fχ(z) = χa / Rt, where χa is ambient NH3 concentration and Rt is total resistance to dry deposition.
- Resistance components:
  - Soil surface boundary layer resistance (Rbg) for soil deposition.
  - Quasi-laminar boundary layer resistance around tree trunks (Rb(tt)).
  - Stomatal resistance (Rs) with Leaf Area Index (LAI) dependency.
  - Cuticular deposition flux with multiple parameterizations (Rw) and one capacitance (Rd) parameterization; LAI dependency included.
  - Several parameterizations for cuticular uptake (Massad et al. 2010; Jones et al. 2007; DEPAC module; Sutton et al. 1998).
- Deposition to different micro-environments (soil, understory, trunks, canopy) estimated with corresponding resistances and parameterizations.
- Peak deposition modelling: current model simulates NH3 concentration peaks during release; ambient NH3 concentrations drive deposition when NH3 is not released.

## Data structure and content
- Dataset size: 108 measurements across 17 parameters.
- Data format: CSV file with columns (Distance, Month, NH3_conc_measured, NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc, Fg, Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us, Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc — with some variants and duplicated entries for certain parameterizations).
- Distance: in meters from NH3 enhancement source; negative = southwest, positive = northeast.
- Height/locations: concentrations measured at specific transect heights (1.5 m for ambient NH3; soil 0.05 m, understory 0.5 m, trunk 1.75 m, canopy 3.5 m).
- Variables include:
  - NH3_conc_measured: monthly average NH3 concentration at 1.5 m along transect.
  - NH3_conc_soil/us/ts/tc: monthly average NH3 concentrations at soil surface, understory, trunk surfaces, and tree canopy, respectively.
  - Fg, Fs_us, Ftt, Fs_tc: cumulative NH3 deposition fluxes to soil, understory, tree trunks, and tree canopy (negative values indicate emission).
  - Fw_* and Fd_*: various deposition flux parameterizations (Massad 2010; DEPAC; Jones 2007; Sutton 1998) for cuticular deposition in understorey and canopy.
- Quality control: visual QC performed; obvious instrument/logger/power issues corrected; regular power cuts cause some missing values; sensor replacement caused gaps.
- Dataset origin: extension of the 2022 data at the same site; improved deposition modelling approach.

## Data quality and provenance
- Data quality checks include visual inspection and flagging of gaps due to power issues or sensor replacement.
- The improved model allows for deposition peak estimation during NH3 release periods, enhancing temporal resolution of deposition dynamics.

## Access, usage, and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Related literature and methodological basis include:
  - Chamberlain (1968); Chamberlain et al. (1984)
  - Fowler (1978)
  - Massad et al. (2010)
  - Nemitz et al. (2000)
  - Jones et al. (2007)
  - Sutton et al. (1998)
  - van Zanten et al. (2010)
  - Deshpande et al. (2024a, 2024b)
- Full methodology, data, and findings are described in Deshpande et al. (2024a, 2024b).