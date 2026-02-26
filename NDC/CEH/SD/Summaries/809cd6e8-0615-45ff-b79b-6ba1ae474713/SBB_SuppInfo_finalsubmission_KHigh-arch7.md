# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

- Purpose: Develop mass spectrometry–based methods to quantify phytohormones (IAA, ABA, zeatin [Z], isopentenyladenosine [iP], adenosine [Ade]) in soil and hydroponic solutions, assessing effects of earthworms and plants.
- Data outputs: Concentrations of target phytohormones, internal standard–normalized signals, and related soil/solution parameters; additional biological activity (FDH) and plant biomass data; gene expression related to ABA synthesis and abiotic stress responses.
- Data availability: All data accessible in the EIDC data catalogue (High et al., 2019).

## Experimental design and data types

- Treatments and setups
  - Hydroponic experiments: four treatments (earthworms present/absent; plants present/absent) with four replicates, over 42 days, using Sinapis alba and a defined hydroponic solution.
  - Soil experiments: same four treatment combinations, 42 days, using sandy loam soil; earthworms added after plant establishment; five replicates per condition.
- Measurements collected
  - Phytohormone concentrations in hydroponic solutions; FDH assay for soil biological activity; soil pH; plant biomass (above-ground parts); soil moisture and related characteristics.
  - Molecular biology: gene expression in ABA biosynthesis and abiotic-stress–responsive pathways (qPCR on plant roots and shoots).
- Data scope: Both chemical (phytohormones) and biological data across hydroponic and soil matrices, with multiple replicates and treatment combinations.

## Analytical workflow and data acquisition

- Sample preparation
  - Soil: phytohormone extraction with methanol:water:formic acid; four time-point extraction revealed 24 h as optimal to avoid degradation.
  - Hydroponic solutions: direct extraction with internal standards for calibration.
- Clean-up and fractionation
  - Solid phase extraction using MCX cartridges; three fractions generated (Fraction 1 acidic, Fraction 2 cytokinin ribosides, Fraction 3 cytokinin free bases); Fraction 2 archived, Fraction 1 and 3 analyzed.
- Identification and quantification
  - FT-ICR-MS (high-resolution) used for initial identification of target analytes in Fractions 1 and 3 (mass accuracy < 1 ppm).
  - MRM LC-MS/MS (Thermo TSQ) for quantification with isotope-labeled internal standards.
  - LC separation: Kinetex C18 core-shell column; detailed gradient conditions provided; 7.5-minute runs per fraction.
- Standards and calibration
  - Standards: IAA, ABA, Ade, iP, Z and corresponding isotopically labeled standards.
  - Transitions and collision energies optimized per compound (table of transitions provided).

## Target compounds and internal standards

- Analytes: Indole-3-acetic acid (IAA); Abscisic acid (ABA); Zeatin (Z); Isopentenyladenosine (iP); Adenosine (Ade).
- Internal standards: Isotopically labeled analogs for all five compounds (e.g., 13C6-IAA, 2H6-ABA, etc.).
- Analytical approach: Combination of FT-ICR-MS for identification and LC-MS/MS–MRM for precise quantification.

## Data processing, statistics, and quality control

- Statistical analyses
  - Two-way ANOVA with factors: presence/absence of earthworms and presence/absence of plants.
  - Post hoc Holm-Sidak tests for multiple comparisons.
  - For hydroponic phytohormone data (non-normal): ANOVA used with robustness considerations; outliers removed using IQR criteria.
- Data handling
  - Outlier handling and LOD considerations noted in supplementary information.
  - Normalization and internal standardization implemented to ensure comparability across runs and matrices.

## Molecular biology analysis

- Genomic context and primer design
  - Brassica napus genome used as guide to design primers for Sinapis alba orthologues in ABA synthesis and abiotic-stress response genes.
  - Genes targeted: NCED family (ABA synthesis) and stress-responsive genes (e.g., CIPK6, NHX1, RD29A).
- Expression profiling
  - qPCR on Brassica-related orthologues; normalization to Actin7; ΔΔCt method for relative expression.
  - Validation steps included in supplementary materials, with primer sequences provided.

## Data availability and supplementary information

- Data repository
  - All data associated with the study are available in the EIDC data catalogue (High et al., 2019).
- Supplementary materials
  - Tables detailing concentrations (MRM results), plant biomasses, FDH activity, and pH values.
  - Tables S5–S6 include gene targets and primer sequences for molecular analyses.

## GIS-relevant implications: data products and visualization

- Potential spatial data products
  - Map phytohormone concentrations and FDH activity by treatment and experimental unit (soil vs. hydroponic vessels).
  - Visualize temporal or replicate-based variation (if location/time metadata are captured) alongside soil properties (pH, moisture, organic matter).
  - Integrate molecular data (gene expression) with chemical/microbial activity metrics for multi-layer GIS analyses.
- Data integration considerations
  - Link chemical measurements to experimental units with robust metadata (treatment, matrix, replicate, biomass, moisture, pH).
  - Ensure traceability of internal standards and LC-MS/MS calibration to support spatial comparisons.
- Quality and standardization needs for GIS
  - Consistent naming conventions for treatments and matrices; documented LOD/LOQ and data cleaning steps.
  - Clear provenance for data processed through FT-ICR-MS and LC-MS/MS workflows; access to supplementary tables for full context.

## Key considerations for data management and interpretation (for GIS specialists)

- Complexity of data sources: multiple matrices (soil and hydroponic solutions), several analytical techniques (FT-ICR-MS, MRM LC-MS/MS), and molecular data.
- Proactive metadata capture: sample location within experimental setup, treatment group, replicate identifiers, extraction timepoints, instrument settings, and data processing parameters.
- Applicability to map-based visuals: while results are experimental, the structured data (concentrations, activities, biomass, pH, gene expression) are suitable for layered GIS dashboards that compare conditions and explore spatially explicit patterns across experimental units.