# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

- Overview
  - Purpose: Investigate effects of elevated ambient NH3 on forest vegetation, bryophytes, lichens, and soil using a wind-controlled NH3 enhancement system.
  - Location: Birch plantation in Glencorse woodland near Edinburgh (55.8539°, -3.2151°; altitude 200 m).
  - Time frame: Enhancement established in 2022; NH3 concentrations measured monthly from September 2021 to December 2022.
  - Data products: Concentrations of NH3 at multiple heights, vertical concentration gradients, and multiple NH3 deposition components across forest strata, plus modeled deposition/emission fluxes using a four-layer canopy framework.

- Data collection and flux calculations
  - Experimental control: NH3 release triggered by wind direction (275–345°) and threshold speeds (0.31 m/s) relative to monitoring quadrats.
  - Measurement heights and schemes:
    - Primary NH3 concentration measured at 1.5 m height along the monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; data collected monthly.
    - Vertical profiling: NH3 concentrations measured at every 25 cm between 5 cm and 3.5 cm above ground at 4-, 10-, and 16-m distances from the enhancement source.
  - Deposition modeling:
    - Four-layer canopy compensation-point model with bi-directional resistance to estimate deposition fluxes to soil surface, understory vegetation, tree trunks, and tree canopy.
    - Deposition flux at height z follows Fχ(z) = χa / Rt (inverse of total resistance Rt).
    - Parameterizations used to estimate resistances for soil, trunks, stomatal, and cuticular deposition, including LAI dependencies and diurnal/phenological variation.
  - Key parameterizations and components:
    - Soil deposition resistance (Rbg) using quasi-laminar boundary layer expressions.
    - Tree trunk deposition resistance (Rb(tt)) based on boundary layer concepts and Reynolds/Schmidt numbers.
    - Stomatal deposition resistance (Rs) with LAI dependence and bounds (RsMax, RsMin, alpha, Rad).
    - Cuticular deposition flux (Rw) with multiple parameterizations and LAI dependence; includes day/night, DEPAC module, Haarweg LAI, and other published forms.
    - Deposition flux components: cumulative soil (Fg), understory stomatal (Fs_us), understory cuticular (Fw_us) via multiple parameterizations (Massad 2010, Jones 2007, DEPAC 2010, Sutton 1998), trunk (Ftt, Fw_tc, Fd_tc) and canopy fluxes (Fs_tc, Fw_tc) with multiple parameterizations.
  - Completeness: Full methodology and findings detailed in Deshpande et al. (2024); this document provides the data and modeling framework description.

- Data structure and fields
  - Dataset size: 126 measurements across 17 parameters.
  - File format: CSV with the following core columns:
    - Distance (m): distance from NH3 enhancement source; negative = southwest, positive = northeast.
    - Month: month/year of observation.
    - NH3_conc_measured (µg m-3): monthly average NH3 concentration at 1.5 m along transect.
    - NH3_conc_soil (µg m-3): modeled monthly average NH3 concentration at soil surface (0.05 m) via vertical sampler array.
    - NH3_conc_us (µg m-3): modeled monthly average NH3 concentration in understory layer (0.5 m).
    - NH3_conc_ts (µg m-3): modeled monthly average NH3 concentration at trunk surfaces (1.75 m).
    - NH3_conc_tc (µg m-3): modeled monthly average NH3 concentration in tree canopy (3.5 m).
    - Deposition flux columns (example): Fg (kg ha-1, soil), Fs_us (kg ha-1, understory stomatal), Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (kg ha-1, understory cuticular; multiple parameterizations), Fd_us (kg ha-1, understory cuticular from Sutton et al.), Ftt (kg ha-1, trunk deposition), Fs_tc (kg ha-1, canopy stomatal), Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones (kg ha-1, canopy cuticular), Fd_tc (kg ha-1, canopy cuticular from Sutton), including alternative variants (1/2) for some columns.
  - Notes: Data quality reflects visual QC; missing values arise from scheduled power cuts and sensor replacement periods.

- Quality control and data quality
  - Visual checks conducted; clearly erroneous data from instrument faults or logging issues removed.
  - Data gaps mainly due to scheduled power interruptions; some gaps also from sensor replacements.

- Provenance, usage, and context
  - Funding: UKRI GCRF South Asian Nitrogen Hub supported facility establishment.
  - References and context: Core deposition modeling framework and parameterizations drawn from Chamberlain; Fowler; Jones et al.; Massad et al.; Nemitz et al.; Sutton et al.; van Zanten et al.; and related deposition literature.
  - Where to find full methodology: Deshpande et al. (2024) provides complete experimental design, methodology, analysis, and findings.
  - Relevance for data leadership:
    - Demonstrates end-to-end data workflow from field collection through complex, multi-layer deposition modeling.
    - Illustrates integration of observed concentrations with modeled fluxes across canopy strata, enabling evaluation of data interoperability and model suitability for decision-support in forest nitrogen management.
    - Highlights data challenges: scattered data sources, need for robust metadata, and the importance of clear provenance for complex biogeochemical datasets.

- Key takeaways for data strategy
  - Comprehensive data structure: clearly defined, multi-parameter dataset capturing concentrations and deposition across canopy layers and flux components.
  - Robust quality control: explicit acknowledgement of instrument/power-related gaps; need for transparent documentation of data corrections and gaps.
  - Rich metadata and provenance: multiple parameterizations and references embedded to support reproducibility and cross-study comparability.
  - Potential for networked use: data designed to be integrated with broader atmospheric deposition studies and used to calibrate/validate deposition models across forests and regions.