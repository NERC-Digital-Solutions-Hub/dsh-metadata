# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

- Overview
  - Study of effects of high NH3 on forest vegetation, bryophytes, lichens, and soil using a wind-controlled NH3 enhancement experiment in Glencorse woodland (Birch plantation), near Edinburgh.
  - NH3 release is triggered by wind direction (275–345°) and threshold wind speed (0.31 m/s); sampling occurs at 1.5 m height along a monitoring transect.
  - Data collected January 2023 to December 2024; used to estimate NH3 deposition and emission across soil, understory, trunks, and canopy via a bi-directional resistance model.

- Data Content
  - 108 measurements comprising 17 parameters.
  - Measurements and modeled concentrations/deposition fluxes across multiple spatial scales/heights:
    - NH3_conc_measured: monthly average NH3 concentration at 1.5 m.
    - NH3_conc_soil, NH3_conc_us (understorey), NH3_conc_ts (trunk surfaces), NH3_conc_tc (tree canopy): modeled NH3 concentrations at various heights.
    - Fg: cumulative NH3 deposition to soil.
    - Fs_us, Ftt, Fs_tc: stomatal deposition fluxes to understory, tree trunks, and tree canopy respectively.
    - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones: cuticular deposition fluxes to understory (three parameterizations).
    - Fd_us: cuticular deposition flux to understory (diffusive/other parameterizations).
    - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones: cuticular deposition fluxes to tree canopy (three parameterizations).
    - Fd_tc: cuticular deposition flux to tree canopy.
  - Distance from NH3 source (positive = northeast, negative = southwest); Month-year; units clearly specified.

- Methodology and Model
  - NH3 enhancement system relies on canopy-scale meteorology; deposition/emission estimated with a four-layer canopy compensation point bi-directional model.
  - Key deposition flux equation: Fχ(z) = χa / Rt, with Rt as total resistance to dry deposition.
  - Resistance components:
    - Soil surface: Rbg (quasi-laminar boundary layer)
    - Tree trunks: Rb(tt) (quasi-laminar around trunks)
    - Canopy/leaf interactions: Rs (stomatal resistance; LAI-dependent)
    - Cuticular deposition: multiple parameterizations for Rw (Massad et al. 2010; Jones et al. 2007; DEPAC module; Sutton et al. 1998)
    - Capacitance: Rd (epicuticular water film)
  - Parameterizations incorporate environmental drivers (LAI, RH, T, solar radiation) and plant/structure characteristics.
  - LAI-dependent adjustments applied to all cuticular parameterizations; day/night distinctions and phenological variation are included.
  - Improvements over previous work:
    - The current model simulates NH3 concentration peaks during release to estimate deposition, rather than using monthly mean concentrations for all periods.
    - Ambient NH3 concentration drives deposition when NH3 is not released.

- Quality Control and Provenance
  - Visual quality control; removal of obvious instrument/malfunction or datalogger/power-cut errors.
  - Regular gaps due to scheduled power cuts and sensor replacements; some gaps due to fault corrections.
  - Dataset extends a 2022 dataset from the same site; reflects a major modeling improvement.
  - Related publications provide complete methodology and analysis (Deshpande et al., 2024a; 2024b).

- Data Structure and Access
  - Data provided as a CSV file with clearly described columns (distance, month, NH3 concentrations at multiple heights, deposition fluxes across soil/understorey/trunk/canopy, multiple deposition parameterizations).
  - Each column includes unit and description to support discoverability and reuse.
  - Complete methodological and analytical details available in Deshpande et al. (2024a) and related dataset Deshpande et al. (2024b).

- Funding and References
  - Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
  - Key references cover deposition modeling and parameterizations (Chamberlain; Massad et al.; Nemitz et al.; Jones et al.; DEPAC module; Sutton et al.; others).

- Relevance for Data Leaders
  - Demonstrates end-to-end data workflow: experimental design, real-time/workflow-based data collection, multi-scale modeling, and multi-parameter deposition outputs.
  - Clear data structure with 17 parameters across 108 observations supports data discoverability, reuse, and cross-study comparison.
  - Model upgrades improve temporal accuracy by capturing release-period peaks, aiding prioritization and interpretation of deposition processes.
  - Data lineage and extension from a prior dataset highlight the importance of versioning and provenance in data strategy.
  - Metadata-rich, with explicit units and descriptive fields, facilitating interoperability and user-centered data product development.