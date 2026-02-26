# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

- Overview: An ammonia enhancement experiment in a tropical sub-montane forest at Queensberry Estate (6.9693°, 80.5911°, altitude 1645 m) in central Sri Lanka, established in 2022 to study how elevated NH3 affects vegetation, bryophytes, lichens, and soil. The UKRI GCRF South Asian Nitrogen Hub funded the facility.

- Data collection and release control:
  - NH3 release is wind-direction controlled, occurring when winds come from directions 5-75° or 185-255° toward monitoring quadrats, at threshold speeds of 0.3-10 m/s.
  - NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
  - Measurements collected monthly from January 2023 to December 2024.
  - A four-layer canopy compensation point bi-directional resistance model estimates NH3 deposition (and emission) from soil, understory vegetation, tree trunks, and tree canopy.

- Modeling approach and deposition flux calculations:
  - Deposition flux Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance to dry deposition.
  - Soil deposition flux uses soil surface quasi-laminar boundary layer resistance Rbg, parameterized per Schuepp (1977).
  - Tree trunk deposition uses quasi-laminar boundary layer resistance Rb(tt), with a function of Reynolds number and conductance factors.
  - Stomatal deposition flux uses stomatal resistance Rs, with leaf area index (LAI) dependency; Rs has specified max/min bounds and temperature/radiation dependencies.
  - Cuticular deposition fluxes modeled with three or four parameterizations (and a capacitance parameter Rd), including LAI dependency to reflect phenology.
  - Four parameterizations for cuticular resistance (Rw):
    1) Massad et al. (2010) style with day/night adjustments,
    2) Jones et al. (2007) with ambient NH3 concentration weighting,
    3) DEPAC module (van Zanten et al., 2010) adjustments incorporating Haarweg LAI,
    4) Sutton et al. (1998) capacitance-based formulation.
  - Complete deposition to each surface (soil, understory, trunk, canopy) is computed with these resistances in a bi-directional exchange framework, including stomatal and cuticular pathways and phenology effects.

- Methodological improvements over prior work:
  - The current model simulates NH3 peaks during release periods to estimate deposition more accurately, while ambient concentrations drive deposition when NH3 is not released.
  - Previous versions used mean monthly NH3 concentrations for deposition at all times.

- Data quality and structure:
  - Quality control: visual checks; removal of obvious instrument malfunctions, datalogger issues, and power-cut artifacts; gaps occur during scheduled power cuts and sensor replacements.
  - Dataset size and content: 816 measurements across 13 parameters, provided in a CSV file.
  - Key columns:
    - Distance (m): distance from NH3 source; sign indicates direction (negative = southwest, positive = northeast).
    - Month: month and year.
    - NH3_conc (µg m-3): monthly average NH3 concentration at 1.5 m height along the quadrats.
    - Fg (kg ha-1): cumulative NH3 deposition flux to soil (negative = emission).
    - Fs_us (kg ha-1): stomatal deposition to understory vegetation.
    - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (kg ha-1): cumulative cuticular deposition to understory from Massad, DEPAC, and Jones parameterizations, respectively.
    - Fd_us (kg ha-1): cuticular deposition to understory from Sutton et al. parameterization.
    - Ftt (kg ha-1): deposition to tree trunks.
    - Fs_tc (kg ha-1): stomatal deposition to tree canopy.
    - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones (kg ha-1): cuticular deposition to tree canopy from Massad, DEPAC, and Jones parameterizations.
    - Fd_tc (kg ha-1): cuticular deposition to tree canopy from Sutton et al. parameterization.
  - Notes: Negative flux values indicate emission; distances are measured from the NH3 source.

- Dataset scope and accessibility:
  - Timeframe: January 2023 – December 2024.
  - Height: measurements at 1.5 m on two monitoring quadrats.
  - Data are available as a CSV with detailed metadata and units, enabling cross-comparison of deposition pathways and parameterizations.

- Funding and references:
  - Funded by UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
  - Core references underpinning the resistance-based deposition model include works by Chamberlain (1968, 1984), Fowler (1978), Jones et al. (2007), Massad et al. (2010), Nemitz et al. (2000), Sutton et al. (1998), and van Zanten et al. (2010), among others.