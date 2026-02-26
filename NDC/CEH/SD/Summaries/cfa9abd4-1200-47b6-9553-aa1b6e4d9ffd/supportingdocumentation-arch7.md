# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

- Purpose and scope
  - Provides barium concentration and stable Ba isotope ratio measurements from controlled laboratory batch experiments and Himalayan river samples (Nepal) for adsorption–desorption processes.
  - Aims to understand Ba isotope fractionation between dissolved and adsorbed phases and validate lab results with field data (PRESSurE project).

- Data collection overview
  - Laboratory experiments (Riverine Series): partitioning and kinetic subseries using river water and groundwater with clay minerals (kaolinite, montmorillonite) and iron-oxyhydroxides (goethite, ferrihydrite).
  - Estuarine series: desorption of Ba from river-derived suspended sediment into seawater, with re-equilibration in river water.
  - Post-reaction processing: separation of water and adsorbent, followed by displacement of adsorbed Ba for complete phase measurements.
  - Himalayan river field samples: 12 river-water samples from Sunkoshi and Saptakoshi (Nepal) as part of PRESSurE; sampling across multiple seasons with in-situ filtration and sediment-water separation.

- Analytical methods
  - Ba concentrations: ICP-OES (Agilent 5100) with certified standards; matrix matching and drift control.
  - Barium isotopes: TIMS (TRITON Plus) with a double-spike for mass-fractionation correction; co-precipitation steps for seawater samples; use of NIST/NBS standards for long-term accuracy.
  - Uncertainty: ~7% (2σ) for Ba concentrations by ICP-OES; ~2% (2σ) for TIMS isotope ratios; isotopic measurement uncertainty as low as ~0.03 ‰ using standards.

- Key procedures and measurements
  - Displacement of pre-existing adsorbed Ba from minerals to obtain a clean baseline.
  - Mineral–water reactions under controlled durations, with variable adsorbent concentrations or durations.
  - Extraction of adsorbed Ba post-reaction to quantify both dissolved and adsorbed phases.
  - Field sample processing includes filtration, acidification, desorption of adsorbed cations, and subsequent Ba measurements.

- Data structure and files
  - Two CSV data files:
    - BaIsoExperimentData.csv: laboratory experiment data.
    - BaIsoNepalRivers.csv: field river data.
  - Laboratory data fields (examples):
    - ID, Series, Subseries, Water, Adsorbent, Adsorbent ID, Water mass, Adsorbent mass, Reaction duration, Pretreatment, Ba diss, Ba ad, d138Ba diss, d138Ba ad.
  - Field data fields (examples):
    - ID, Date, River, Loc, SSC, Discharge, Ba diss, Ba ad, d138Ba diss, d138Ba ad.
  - Some fields are NA or NM when not applicable.

- Data processing and workflow (laboratory and field)
  - For lab: prepare adsorbents, conduct mineral–water experiments, separate phases, quantify Ba in dissolved and adsorbed forms, and measure Ba isotopes.
  - For field: collect river samples, filter, dry sediments, desorb adsorbed Ba, and measure Ba concentrations and isotopes using the same analytical pipeline as labs.

- Spatial and GIS relevance
  - Field data supply spatially linked samples from Nepalese rivers (Sunkoshi, Saptakoshi) with temporal context (seasonal sampling), enabling GIS mapping of Ba concentrations and isotope distributions across river systems and during different hydrological conditions.
  - Data can be joined with GIS layers for rivers, basins, and sediment sources to explore spatial patterns of Ba cycling and isotope fractionation.

- Related references and data context
  - Knight et al. PRESSurE River Chemistry Time Series (Nepal), 2024.
  - Double-spike Ba isotope methodology (Rudge et al., 2009).
  - Ba stable isotopes in the global ocean (Hsieh & Henderson, 2017).
  - Methodological notes on Ba and isotope analyses (Foster et al., 2004).

- Usage notes and caveats for GIS users
  - Some fields may be NA or NM depending on experiment type or measurement availability.
  - River sampling captures only the first meter of the water column due to high flow, which may influence representativeness for certain analyses.
  - Data are designed for linking isotope and concentration measurements to adsorbed vs dissolved phases, enabling spatial visualization of fractionation processes alongside hydrological variables (discharge, suspended sediment concentration).

- Access and documentation
  - Data and accompanying documentation are provided in CSV format within the repository.
  - Complementary data and methodologies are referenced, enabling integration with broader datasets and Publications.