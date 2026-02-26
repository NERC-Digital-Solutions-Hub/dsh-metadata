# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

- Purpose and site
  - An NH3 enhancement experiment in a Birch plantation at Glencorse woodland (55.8539°N, -3.2151°W; altitude 200 m) near Edinburgh to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
  - Enhancement system is wind-controlled, releasing NH3 only when wind is from 275–345° direction at threshold speeds ≈0.31 m/s.

- Measurements and data collection
  - NH3 concentrations measured at 1.5 m height along monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from Sept 2021 to Dec 2022.
  - Vertical NH3 concentrations measured at every 25 cm interval from 5 to 3.5 cm above the ground at 4, 10, and 16 m distances from the enhancement system.
  - Data used to drive a four-layer canopy compensation point model to estimate deposition (and emission) across soil, understory vegetation, tree trunks, and tree canopy.

- Modeling approach
  - Deposition flux modeled with a bi-directional resistance framework accounting for stomatal and soil re-emission processes.
  - Core deposition flux: Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance to dry deposition (inverse of deposition velocity, Vd).
  - Soil deposition flux uses soil surface quasi-laminar boundary layer resistance (Rbg); trunk and canopy fluxes use respective quasi-laminar and stomatal/cuticular parameterizations.
  - Parameterizations include:
    - Soil boundary layer, trunk boundary layer, stomatal resistance Rs (with LAI dependency; RsMax = 5000 s m-1, RsMin = 35 s m-1, α = 180 W m-2).
    - Cuticular deposition: multiple parameterizations (Massad et al., 2010; Jones et al., 2007; DEPAC module van Zanten et al., 2010; Sutton et al., 1998) with LAI dependencies and day/night adjustments.
    - A DEPAC-based module and Haarweg LAI for specialized parameterizations.
  - Complete methodology and model details are described in Deshpande et al. (2024).

- Data structure and variables
  - 126 measurements of 17 parameters stored in a CSV file.
  - Key columns include:
    - Distance (m) from NH3 source; Month
    - NH3_conc_measured (µg m⁻³): monthly mean NH3 at 1.5 m
    - NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc (modelled NH3 concentrations at soil, understory, trunk surfaces, and canopy)
    - Deposition fluxes: Fg (soil), Fs_us (understory stomatal), Fw_us_Massad/DEPAC/Jones (understory cuticular), Fd_us (understory cuticular, Sutton), Ftt (trunk deposition), Fs_tc (canopy stomatal), Fw_tc_Massad/DEPAC/Jones (canopy cuticular), Fd_tc (canopy cuticular, Sutton)
    - Negative flux values indicate emission rather than deposition
  - Distance sign convention: negative distances indicate southwest direction; positive indicate northeast.

- Quality control and data availability
  - Data visually checked; obvious instrument issues and power-related gaps removed.
  - Regular-interval missing values due to scheduled power cuts; additional gaps from sensor replacements.

- Funding and references
  - Funded by UKRI GCRF South Asian Nitrogen Hub.
  - Model foundations and parameterizations draw on Chamberlain (1968, 1984), Fowler (1978), Nemitz et al. (2000), Massad et al. (2010), Jones et al. (2007), Sutton et al. (1998), van Zanten et al. (2010), and related works; detailed methodology in Deshpande et al. (2024).

- Potential use for analysts
  - Identify relationships between ambient NH3 concentrations at multiple canopy layers and total deposition flux.
  - Compare deposition parameterizations (Massad, Jones, DEPAC, Sutton) and assess their suitability for forest ecosystems.
  - Calibrate or validate bi-directional NH3 exchange models at fine-scale, local sites.
  - Investigate spatial and temporal patterns of deposition vs. emission within the forest canopy and soil-vegetation interfaces.