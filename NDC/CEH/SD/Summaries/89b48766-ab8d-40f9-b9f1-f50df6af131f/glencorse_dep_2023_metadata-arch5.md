# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

- Purpose and scope
  - NH3 enhancement experiment in a Birch plantation at Glencorse woodland (near Edinburgh) to study effects of high ammonia on vegetation, bryophytes, lichens, and soil.
  - Data cover January 2023 to December 2024; extension of the 2022 dataset from the same site.
  - Improvements over prior work: uses an improved bi-directional resistance model that simulates NH3 peaks during release periods to estimate deposition, rather than driving deposition with mean monthly concentrations.

- Location and setup
  - Site: Glencorse woodland, 55.8539°N, -3.2151°W, altitude 200 m.
  - Enhancement system is wind-controlled (activated when wind direction is 275–345° and at threshold speeds ~0.31 m/s).
  - NH3 measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses.

- Data collection and modelling
  - Measurements and flux calculations:
    - Deposition flux to multiple surfaces estimated via a four-layer canopy compensation point model and bi-directional exchange framework.
    - Components include soil surface, understory vegetation, tree trunks, and tree canopy.
    - Flux and deposition modeled using resistance parameters (e.g., soil boundary layer, trunk boundary layer, stomatal resistance, and cuticular pathways) with LAI dependencies.
  - Key modelling relationships:
    - Deposition flux Fχ(z) = χa / Rt (with Rt as total resistance).
    - Soil deposition via boundary layer resistance Rbg; trunk deposition via quasi-laminar resistance Rb(tt); stomatal deposition via Rs; multiple cuticular parameterizations (Rw) and a capacitance parameterization (Rd).
    - Several parameterizations and calibrations (Massad et al., Jones et al., DEPAC module, Sutton et al.) used to estimate deposition fluxes.
  - Data outputs include ambient NH3 concentrations at several heights and cumulative deposition fluxes to soil, understory, trunks, and canopy, with multiple parameterizations for cuticular deposition.

- Data structure and content
  - Dataset: 108 measurements across 17 parameters.
  - File format: CSV with clearly described columns.
  - Core columns and descriptions (examples):
    - Distance (m): distance from NH3 source; negative = southwest, positive = northeast.
    - Month: month and year.
    - NH3_conc_measured (µg/m3): monthly average NH3 concentration at 1.5 m height from ALPHA samplers.
    - NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc (µg/m3): modelled monthly NH3 concentrations at soil surface (0.05 m), understory (0.5 m), trunk surfaces (1.75 m), and tree canopy (3.5 m), respectively.
    - Fg, Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us: cumulative NH3 deposition flux to soil, stomatal deposition to understory, and various cuticular deposition parameterizations to understory (Massad, DEPAC, Jones, Sutton).
    - Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc: analogous fluxes for tree trunks and tree canopy.
    - Negative flux values indicate emission rather than deposition.
  - Metadata and provenance are embedded via full methodological references and dataset lineage.

- Quality control and data quality
  - Visual checks conducted; obvious instrument/malfunction and datalogger/power issues removed.
  - Gaps arise from scheduled power cuts and sensor replacements; some missing values reflect these operational realities.
  - Data represent a refinement over the 2022 dataset, with improved modelling to capture NH3 peaks during release periods.

- Data provenance and related works
  - Dataset extends the 2022 site dataset; current work enhances the deposition model to respond to on-site NH3 release dynamics.
  - Key references underpinning methods and parameterizations include Chamberlain (1968, 1984), Fowler (1978), Massad et al. (2010), Nemitz et al. (2000), Jones et al. (2007), Sutton et al. (1998), van Zanten et al. (2010), among others.

- Funding and access
  - Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
  - The document describes a data collection and modelling effort intended for integrated deposition estimation; explicit data sharing terms are not stated, but data are provided with detailed metadata and parameter definitions to enable reuse.

- Practical implications for data stewardship
  - Rich, multi-parameter dataset suitable for downstream analyses of NH3 deposition across soil and vegetation layers; clearly defined units, heights, and parameterizations aid interoperability.
  - The presence of multiple deposition parameterizations (and a newer deposition-peak-aware model) should be captured in metadata to allow users to understand modelling choices and uncertainty.
  - The dataset’s structure (108 measurements, 17 parameters) and the explicit treatment of emission vs. deposition (negative flux) are important for accurate data discovery, provenance, and reuse.
  - Quality-control notes should be linked to dataset-level quality statements and potential data gaps due to power cuts or sensor maintenance.

- Recommendations for data stewards
  - Ensure metadata captures: site details, sampling design, height levels, time period, measurement methods (ALPHA samplers), and modelling approach (bi-directional resistance model, parameterizations used).
  - Document data lineage: link to the 2022 extension, describe improvements over previous modelling, and provide references for all parameterizations.
  - Include data licensing and access terms; if not open, specify embargoes or restrictions and provide contact points.
  - Maintain data quality notes: report known gaps (e.g., power cuts), sensor replacement periods, and any data cleaning steps performed.
  - Align with data standards for environmental datasets (recommended: dataset title, authors, date range, methods, parameters with units, and provenance in a DataCite or similar schema).