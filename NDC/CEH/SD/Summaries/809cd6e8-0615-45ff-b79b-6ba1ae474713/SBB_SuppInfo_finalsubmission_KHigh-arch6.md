# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

## Overview
- Investigates how earthworms and plants influence cytokinin and ABA levels in soil and hydroponic solutions using mass spectrometry.
- Combines plant and soil ecology with analytical chemistry to quantify phytohormones and assess soil biological activity.
- Data include phytohormone concentrations, soil and solution chemistry, plant biomass, earthworm performance, soil enzyme proxy (FDH), and gene expression related to ABA and abiotic stress.

## Data types and sources
- Phytohormone concentrations in soil and hydroponic solutions:
  - Target compounds: IAA, ABA, zeatin (Z), isopentenadenosine (iP), adenosine (Ade); quantified with internal standards.
  - Fractionation data from solid-phase extraction (SPE) into three fractions for analysis.
- Mass spectrometry data:
  - FT-ICR-MS for initial identification of analytes (Fraction 1 and Fraction 3).
  - LC-MS/MS (MRM) for quantification using internal standards and isotope-labeled standards.
  - Transition lists and instrument parameters (Table 1) and LC conditions (Fraction 1 and Fraction 3).
- Experimental outputs:
  - Plant biomass (above-ground), dry mass of soil, moisture content.
  - Hydroponic solution pH at the end of experiments.
  - Fluorescein diacetate hydrolysis (FDH) assay results as a proxy for soil biological activity.
- Molecular biology data:
  - qPCR gene expression for ABA synthesis pathway (NCED3, NCED5) and abiotic-stress responsive genes (CIPK6, NHX1, RD29A); primers listed; normalization to Actin7; delta-delta Ct analysis.
  - Cross-species primer validation against earthworm genomes to assess possibility of phytohormone biosynthesis by earthworms.
- Supplementary data:
  - Tables of raw/processed phytohormone concentrations, biomasses, FDH activity, pH values, and outliers.

## Data collection and workflow
- Experimental design:
  - Hydroponic experiments: 4 treatment combinations (earthworms present/absent; plants present/absent) with four replicates, total 42 days; Sinapis alba introduced for plant growth; Eisenia fetida earthworms added briefly at the end.
  - Soil experiments: four treatment conditions replicated five times each; 300 g soil per jar; 15 S. alba seeds per jar; earthworms (three mature L. terrestris) added to earthworm-present treatments; 42 days total with staged establishment before earthworm addition.
- Sample preparation and extraction:
  - Soil: phytohormone extraction based on plant tissue methods; tested extraction conditions due to soil complexity; 24-hour passive extraction at -20°C with a 15:4:1 methanol:water:formic acid solvent; internal standards added before extraction; extended extraction times tested but 24 h chosen to minimize degradation.
  - Hydroponic solutions: direct extraction with internal standards; no solvent extraction required.
- Clean-up and fractionation:
  - Solid-phase extraction (SPE) using MCX cartridges to separate acidic compounds (Fraction 1), cytokinin ribosides (Fraction 2, archived), and cytokinin free bases (Fraction 3); fractions prepared and dried; Fraction 1 and 3 reconstituted for analysis.
- Identification and quantification:
  - FT-ICR-MS (negative mode for Fraction 1, positive mode for Fraction 3) for broad identification with mass accuracy < 1 ppm.
  - MRM LC-MS/MS (TSQ Endura) with validated transitions and isotopically labeled internal standards for precise quantification of IAA, ABA, Z, iP, and Ade.
  - Chromatography on a C18 core-shell column with specified gradients for Fraction 1 and Fraction 3.
- Molecular biology:
  - RNA extraction from hydroponically grown plants; cDNA synthesis; qPCR to quantify ABA synthesis and stress-responsive genes; primers designed using Brassica napus orthologues and validated against earthworm genomes.
- Data processing and analysis:
  - Identification via FT-ICR-MS followed by targeted MRM quantification.
  - Statistical analyses: two-way ANOVA to assess effects of earthworms and plants (and their interaction) on phytohormone levels and FDH; t-tests for plant biomass and hydroponic solution pH; normality checks (Shapiro-Wilk) with robust ANOVA when necessary.
  - Outlier handling using interquartile range criteria; Holm-Sidak post hoc tests for multiple comparisons.
- Data accessibility:
  - All data available from the EIDC data catalogue (High et al., 2019).

## Key measurements and data interpretation
- Phytohormones:
  - Quantified IAA, ABA, Z, iP, and Ade in hydroponic solutions and soil extracts, with internal standardization and isotope-labelled standards for accuracy.
  - Data used to assess how earthworms and/or plants influence phytohormone dynamics in soil environments.
- Soil biology proxy:
  - FDH assay used to infer microbial and enzymatic activity in soils under different treatments.
- Soil and plant metrics:
  - Biomass measurements to determine growth responses to earthworms and plants.
  - Soil moisture content and pH of hydroponic solutions as potential confounding factors.
- Molecular responses:
  - Expression of ABA biosynthesis genes and abiotic-stress responsive genes to detect plant molecular responses to earthworm presence and soil conditions.
  - Cross-species primer validation to explore potential earthworm involvement in phytohormone biosynthesis pathways.
- Data governance and quality:
  - Use of internal standards and isotopically labeled controls for quantification.
  - Conservative data handling with outlier removal and non-normal data treated with robust ANOVA.
  - Supplementary data tables provide raw and processed concentrations, biomasses, and activity metrics for reproducibility.

## Data management, sharing, and reuse
- Data are curated and made publicly accessible via the EIDC data catalogue (High et al., 2019), enabling reuse for analyses of plant-soil-earthworm interactions, phytohormone dynamics, and methodological pipelines combining FT-ICR-MS and MRM-based quantification.
- Comprehensive documentation accompanies data (Tables S5–S6, supplementary tables) to support replication of molecular assays and data interpretation.
- The study provides a replicable workflow from sample preparation through advanced mass spectrometry to statistical analysis, suitable for adaptation in similar data-support contexts (e.g., dashboards or self-serve exploration of phytohormone dynamics in soil environments).