# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

- Purpose and scope
  - Provides a dataset to understand fractionation of stable barium isotopes during adsorption-desorption between environmental mineral adsorbents (kaolinite, montmorillonite, goethite, ferrihydrite) and surface waters (river, groundwater, seawater).
  - Includes controlled laboratory batch experiments and field samples from Himalayan rivers (Saptakoshi and Sunkoshi, Nepal) for validation.
  - Data support from the PRESSurE project and related methodological references.

- Experimental design (Laboratory Experiments)
  - Riverine Series:
    - Partitioning subseries: varying adsorbent concentration, constant 2000 min reaction, to quantify Ba partitioning between dissolved and adsorbed phases; ensures detectable Ba in both phases for isotope analysis.
    - Kinetic subseries: fixed adsorbent concentrations, reaction durations from 10 minutes to ~1 month, to assess time-dependent isotope fractionation.
  - Estuarine Series:
    - Quantifies desorption of Ba from river-derived sediments in estuarine conditions; clay minerals equilibrated with river-water analogue (HS50) then seawater; some experiments re-equilibrated with river water.
  - Post-reaction processing:
    - Separation by centrifugation; displacement of adsorbed Ba from surfaces for both dissolved and adsorbed phase analyses.

- Field sampling (Himalayan River Samples)
  - 12 river water samples from Sunkoshi and Saptakoshi rivers in Nepal (PRESSurE time series).
  - Sampling across seasons (pre-monsoon, monsoon, post-monsoon, dry season); 0.22 µm filtration to separate sediment and water; adsorbed cations desorbed using NH4Cl or CoHex; samples kept cold and filtered as needed.
  - Data include dissolved and adsorbed Ba concentrations and Ba stable isotope ratios for field samples, enabling comparison with laboratory results.

- Analytical methods
  - Concentrations:
    - Ba measured by ICP-OES (Agilent 5100) with certified standards; calibration matrix-matched; quality controls to minimize drift.
    - Isotopes measured by TIMS (Thermo Fisher Triton Plus) using a Ba double spike to correct for mass-dependent fractionation.
  - Isotope preparation and purification:
    - Samples processed through two-stage ion-exchange chromatography to isolate Ba from matrix elements; special steps for seawater (CaCO3 co-precipitation) to improve Ba/Ca ratios.
    - Post-purification oxidation and loading onto Re filaments for TIMS analysis.
  - Quality and blanks:
    - TIMS procedural blank ~0.07 ± 0.06 ng (very small relative to sample mass).
    - 1 M NH4Cl blanks for Ba measurement characterized; long-term accuracy validated with NIST/NBS standards.
    - Uncertainties: ~7% (2σ) for Ba concentrations by ICP-OES; ~2% (2σ) for TIMS concentrations; isotopic uncertainties ~0.03 ‰ (long-term with standards).

- Data structure and availability
  - Two CSV data files included:
    - BaIsoExperimentData.csv: laboratory batch experiment data.
    - BaIsoNepalRivers.csv: field data from Himalayan rivers.
  - Key fields (examples):
    - Laboratory data: experiment ID, series/subseries, water and adsorbent details, masses, reaction duration, pretreatment, Ba concentrations (dissolved and adsorbed), and d138Ba for both phases.
    - Field data: sample ID, date, river, station location, suspended sediment concentration, discharge, Ba concentrations (dissolved and adsorbed), and d138Ba for both phases.
  - Metadata and data descriptions:
    - Tables define parameters, units, and data structure; NM/NA labeling for unavailable data.
    - Documentation references methods, QA, and references for foundational Ba isotope work.

- Data quality and provenance
  - Long-term method validation via standards (NIST 3104a; NBS 127); external standards (SPS-SW2, SLRS-6) used for ICP-OES.
  - Comprehensive description of sample processing, including displacement of pre-existing adsorbed Ba, mineral-water reaction procedures, and adsorbed-phase extraction.
  - Data are tied to the PRESSurE Nepal river time series for field validation and to the referenced literature for methodological context.

- Reuse and relevance for data leadership
  - Enables tracing Ba inputs and isotope fractionation signatures across aquatic phases and mineral surfaces, aiding development of tracers for Ba sources and cycling in freshwater to estuarine systems.
  - Provides a well-documented data pipeline from sample collection to isotope measurement, enabling reproducibility and integration with other data networks.
  - Relevant for building broader data systems that emphasize complete metadata, data provenance, and cross-domain linkage (lab experiments with field validation). Links to the broader PRESSurE dataset and related Ba isotope literature.