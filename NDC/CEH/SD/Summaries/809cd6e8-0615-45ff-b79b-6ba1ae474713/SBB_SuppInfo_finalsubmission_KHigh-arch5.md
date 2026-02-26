# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

## Overview
- Investigates changes in phytohormones (cytokinins: zeatin, iP, adenosine; auxin: IAA; ABA) in soil and hydroponic systems in the presence of earthworms and/or plants.
- Experimental design includes plant presence/absence and earthworm presence/absence across soil and hydroponic matrices, with Sinapis alba as the plant model and two earthworm species (Eisenia fetida and Lumbricus terrestris).
- Data generation combines targeted mass spectrometry (MRM LC-MS/MS) for quantification, untargeted/targeted identification by FT-ICR-MS, and ancillary measurements (biomass, FDH soil activity, soil pH, and gene expression).
- All data are available from the EIDC data catalogue (High et al., 2019).

## Data types and assets
- Phytohormone measurements
  - Target compounds: IAA, ABA, zeatin (Z), isopentenyladenosine (iP), adenosine (Ade).
  - Quantification by MRM with isotopically labeled internal standards.
  - Fractionation data from solid-phase extraction (MCX) into three fractions (acidic, cytokinin ribosides, cytokinin free bases); Fraction 2 archived.
- Instrumentation data
  - FT-ICR-MS identification for Fractions 1 and 3 (negative/positive ion modes, m/z ranges, mass accuracy < 1 ppm).
  - LC-MS/MS (TSQ Endura) MRM method details, including transitions, collision energies, and internal standards (Table 1).
  - HPLC separation details (Kinetex C18 column, gradient conditions, flow rates).
- Biological and chemical measurements
  - Plant biomass: fresh/dry above-ground biomass (soil experiments).
  - FDH assay: soil biological activity expressed as µg fluorescein/g dry soil/30 min.
  - pH of hydroponic solutions at experiment end.
  - Soil/solution chemistry: soil moisture content, water-holding capacity adjustments.
- Molecular biology data
  - qPCR analysis for ABA synthesis pathway and abiotic stress-responsive genes (NCED3, NCED5, CIPK6, NHX1, RD29A) with primers designed against Sinapis alba orthologues guided by Brassica napus genome.
  - RNA extraction, cDNA synthesis, and ΔΔCt expression analysis (normalized to Actin7).
  - Supplementary primer sequences and gene targets (Tables S5–S6).
- Experimental design metadata
  - Treatments: Plants present/absent; Earthworms present/absent; Matrix (Soil vs Hydroponic); replicates (A, B, C, etc. for hydroponic/soil treatments); specific earthworm species used.
  - Growth conditions: hydroponic solution composition, soil type (sandy loam Eutric Cambisol), pH, organic matter; plant establishment period; earthworm depuration procedures; duration (42 days for plant experiments; 24-hour earthworm exposure in hydroponics).
  - Sample IDs and metadata conventions (e.g., Lterr X.X for Lumbricus terrestris soil experiments).

## Data collection and processing
- Sample preparation
  - Soil extraction tested and optimized; 24-hour passive extraction used to minimize degradation.
  - Hydroponic solution recovery straightforward; internal calibration with isotopically labeled standards.
  - Solid-phase extraction using MCX cartridges to separate acidic and basic/neutral fractions.
- Compound identification and quantification
  - FT-ICR-MS used for initial identification of target analytes in Fractions 1 and 3.
  - Quantification via MRM on a TSQ Endura instrument with internal standards; transitions and collision energies optimized per compound (Table 1).
  - HPLC separation precedes MS, with specific gradient profiles for Fractions 1 and 3.
- Experimental design
  - Hydroponic experiments: 4 replicates for each combination (earthworms + plants, earthworms only, plants only, neither) across treatments; 42 days total; 250 g soil-equivalent in hydroponic setups.
  - Soil experiments: 5 replicates per treatment, with three mature earthworms per earthworm-present jar; plants established for 17 days before earthworms added; total 42 days.
- Data analysis
  - Statistical tests: t-tests for biomass and pH; two-way ANOVA (earthworms x plants) for FDH activity and phytohormone concentrations; Holm-Sidak post hoc tests for non-normal hydroponic data.
  - Outlier handling: outliers identified via IQR method and removed prior to analysis.
  - Normalization: soil phytohormone data corrected to oven-dry soil mass; qPCR data normalized to Actin7 and analyzed via ΔΔCt.
- Data provenance and methods documentation
  - Detailed protocols for extraction, SPE, FT-ICR-MS settings, MRM transitions, chromatography, and qPCR primers.
  - References provided for methodological foundations (e.g., Farrow and Emery, 2012; Dobrev et al., 2005; supplementary tables).

## Data quality, provenance, and standards
- Quality and reproducibility
  - Internal standards and isotopologues ensure accurate quantification and instrument calibration.
  - Mass accuracy < 1 ppm for FT-ICR-MS identification supports reliable identification of analytes.
  - Replicated experimental design across matrices (soil and hydroponic) and treatments improves robustness.
- Metadata and documentation
  - Comprehensive experimental metadata: matrix, treatments, replicates, earthworm species, plant species, growth conditions, sampling times.
  - Detailed instrument settings, transitions, collision energies, and chromatographic parameters provided.
  - Supplementary information includes gene primers and gene targets enabling traceability of molecular analyses.

## Data storage, sharing, and accessibility
- Data repository
  - All data are available from the EIDC data catalogue (as High et al., 2019).
  - Data linkage to publications and supplementary materials ensures discoverability.
- Data governance implications
  - Clear data lineage from sample collection to final analyses (raw FT-ICR-MS data, MRM quantifications, FDH, pH, biomass, and qPCR results).
  - Need for consistent sample naming conventions (e.g., Lterr X.X, hydroponic treatment IDs) and stable identifiers to maintain traceability.
  - Documentation of data processing steps and scripts recommended to accompany datasets for reproducibility.

## Particular challenges relevant to data stewardship
- Complex, multi-matrix design (soil vs hydroponic) with multiple interacting factors (plants, earthworms) requiring rich metadata.
- Handling of large, multi-step MS datasets (FT-ICR-MS identities and LC-MS/MS quantifications) with precise instrument settings.
- Potential for matrix effects in soil extractions and detection limits for certain phytohormones; need for clear reporting of LODs and detected/undetected statuses.
- Integration of diverse data types (chemical measurements, biological activity, biomass, pH, gene expression) into a coherent, discoverable dataset.

## Key takeaways for Data Stewards
- Ensure comprehensive metadata schema that captures: matrix, treatments, species, replicates, growth conditions, sampling timelines, and sample IDs.
- Preserve both raw and processed data; include instrument parameters, calibration procedures, and data processing workflows.
- Maintain clear documentation of analytical methods (extraction, SPE, FT-ICR-MS, MRM, HPLC) and molecular biology protocols (RNA extraction, cDNA synthesis, qPCR primers, and normalization strategy).
- Link data to open-access repository (EIDC) with persistent identifiers; provide clear data dictionaries and unit conventions (e.g., µg/g for soil hormones, pH units, fluorescein µg/g soil/30 min).
- Include supplementary materials (Tables S5–S6, Tables 1–4, and associated figures) as part of the dataset to support reuse and reproducibility.
- Plan for data updates and versioning as analyses or supplementary data are expanded, ensuring end-to-end provenance from collection to final analysis.