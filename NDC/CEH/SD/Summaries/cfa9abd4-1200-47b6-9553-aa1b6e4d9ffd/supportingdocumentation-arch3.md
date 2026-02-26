# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

- Purpose and scope
  - Provides barium concentration and stable isotope ratio measurements (δ138/134Ba) for both dissolved and adsorbed phases.
  - Combines controlled laboratory batch experiments with field river samples to understand Ba isotope fractionation during adsorption-desorption.
  - Laboratory work accompanies field samples from the PRESSurE project, along the Saptakoshi and Sunkoshi rivers in Nepal (2015–2016).

- Laboratory experiments
  - Riverine series:
    - Subseries: Partitioning and Kinetic.
    - Adsorbents: kaolinite, montmorillonite, goethite, ferrihydrite.
    - Goals:
      - Partitioning: assess how adsorbent concentration affects Ba distribution between dissolved and adsorbed phases (2000 min reaction duration; ~200 ng Ba needed in each phase).
      - Kinetics: assess effect of reaction duration (10 minutes to ~1 month) at fixed adsorbent concentrations.
  - Estuarine series
    - Purpose: quantify desorption of Ba from river-derived suspended sediments in estuarine conditions.
    - Protocol: clay minerals equilibrated with river-water analogue, then exposed to seawater; some runs re-equilibrated with river water.
  - Post-reaction processing
    - Separation of water and adsorbent by centrifugation.
    - Desorption of adsorbed Ba from surfaces for analysis.

- Himalayan River sediment and water samples
  - 12 river water samples from Sunkoshi and Saptakoshi in Nepal, part of the PRESSurE time series.
  - Field setup: hydrological stations installed after the 2015 Gorkha earthquake; sampling across multiple seasons.
  - Sample processing: sediment–water separation with 0.22 µm filters; adsorbed cations desorbed using NH4Cl or CoHex extraction; samples filtered and stored for analysis.
  - Measurements: Ba concentrations and isotope ratios measured using the same methods as laboratory samples.

- Analytical methods
  - Concentration measurements
    - Ba concentrations: ICP-OES (Agilent 5100) with certified standards; external standards and calibration lines matrix-matched.
    - Accuracy and precision: about 7% (2σ) for ICP-OES Ba concentrations.
  - Isotope measurements
    - Ba isotopes: TIMS (Thermo Fisher Scientific TRITON Plus) with a double-spike correction for mass-dependent fractionation.
    - Isotopic reference: δ138/134Ba relative to NIST 3104a standard.
    - Special preparation for seawater samples: CaCO3 co-precipitation to improve Ba signal relative to major ions.
    - Procedural blanks and standards
      - TIMS procedural blank: 0.07 ± 0.06 ng (n=6).
      - NH4Cl blanks: up to 4% of sample mass.
      - Long-term accuracy verified with NIST 3104a and NBS 127 standards; minimum isotopic uncertainty ~0.03 ‰.
  - Data handling and quality control
    - Reagents cleaned to reduce interference; samples pre-treated to remove NH4Cl effects on TIMS.
    - All samples processed under controlled clean-lab conditions (20 °C, 1 atm).

- Data structure and availability
  - Two CSV data files provided:
    - BaIsoExperimentData.csv: laboratory experiment data.
    - BaIsoNepalRivers.csv: field (river) data.
  - Data fields (examples)
    - Laboratory data: ID, Series, Subseries, Water, Adsorbent, Adsorbent ID, Water mass, Adsorbent mass, Reaction duration, Pretreatment, Ba diss (dissolved Ba), Ba ad (adsorbed Ba), d138Ba diss, d138Ba ad.
    - Field data: ID, Date, River, Loc, SSC (suspended sediment concentration), Discharge, Ba diss, Ba ad, d138Ba diss, d138Ba ad.
  - Field data notes
    - 12 Nepal river samples from Sunkoshi and Saptakoshi; field metadata in accompanying dataset Knight et al. 2024.
    - Sampling captured pre-monsoon and monsoon seasons; some post-monsoon/dry-season samples as well.

- Data quality, gaps, and governance
  - Metadata and data provenance documented; datasets are designed to support reproducibility and cross-study comparison.
  - Open data considerations highlighted: explicit notes on data sharing, standardization, and potential metadata gaps.
  - Verification against standard references and inter-lab consistency supported by long-term standard measurements.

- Relevance for monitoring frameworks
  - Demonstrates an end-to-end approach for generating, validating, and sharing environmental tracer data (Ba concentrations and isotopes) to evaluate adsorption-desorption processes in natural waters.
  - Shows integration of laboratory-derived processes with field measurements to ground-truth mechanistic understanding in real-world settings.
  - Emphasizes data governance practices: transparent methods, detailed metadata, and open sharing of datasets to enable policy-relevant monitoring and future decision-making.
  - Highlights common challenges for monitoring frameworks: data gaps, access and timeliness, inter-organisational data silos, metadata adequacy, data transformation needs, clear communication of complex isotope results, and establishment of robust data governance.

- References
  - Foster et al. (2004); Henderson et al. (2004); Hsieh & Henderson (2017); Knight et al. (2024); Rudge et al. (2009) – foundational methods and context for Ba isotope measurements and applications.