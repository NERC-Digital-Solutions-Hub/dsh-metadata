# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

## Purpose and study design
- Investigates how soil concentrations of cytokinin and ABA-related phytohormones (zeatin, iP, IAA, ABA, adenosine) change under four conditions: earthworms present with plants, earthworms present without plants, plants present without earthworms, neither present.
- Comparative analysis across two environments: soil and hydroponic solutions, over a 42-day period.
- Plant model: Sinapis alba; earthworms: Eisenia fetida (hydroponics) and Lumbricus terrestris (soil); multiple replicates and controlled biomass across treatments.

## Data management and sharing
- All data are available from the EIDC data catalogue (High et al., 2019), supporting transparency and future re-use.
- Internal standards (isotopically labelled phytohormones) are used for quantification to ensure traceability and comparability across datasets.

## Experimental setup and samples
- Hydroponic experiments:
  - 580 mL jars with silica sand and hydroponic solution; 42-day cultivation with four plant/earthworm treatment combinations.
  - Earthworms added for 24 hours at the end, with aeration, to minimize stress.
- Soil experiments:
  - 300 g soil per jar in sandy loam Eutric Cambisol; 42 days; five replicates per treatment.
  - Three mature L. terrestris per earthworm-present jar; plants established for 17 days prior to earthworm addition to reduce burrowing effects.
- Plant biomass and soil properties measured at the end; soil moisture used to normalize hormone concentrations.

## Analytical methods
- Extraction and cleanup:
  - Soil: tested phytohormone extraction conditions; 24-hour passive extraction at -20°C after spiking with isotopically labelled standards; MCX solid-phase extraction fractions to separate acidic compounds, cytokinin ribosides, and cytokinin bases.
  - Hydroponic solutions: straightforward recovery; internal standards added for calibration.
- Identification and quantification:
  - FT-ICR-MS (mass accuracy < 1 ppm) for preliminary identification of target analytes in Fractions 1 and 3.
  - Targeted quantification via MRM on a TSQ Endura triple quadrupole mass spectrometer with LC separation:
    - Fraction 1 (acidic compounds) analyzed in negative mode.
    - Fraction 3 (cytokinin bases) analyzed in positive mode.
  - Chromatography performed on a Kinetex C18 column with short, rapid gradients (total ~7.5 minutes per fraction).
  - Isotopically labelled internal standards used for all five target compounds (IAA, ABA, Ade, iP, Z) to enable accurate quantification.
- Statistical design:
  - Two-way ANOVA to test for effects of plants and earthworms (and their interaction) on phytohormone concentrations and FDH activity.
  - Normality assessed; non-normal hydroponic data analyzed with ANOVA robust to non-normality; Holm-Sidak post hoc tests used where appropriate.
- Biological activity and environmental context:
  - FDH assay used as a proxy for soil biological activity.
  - pH of hydroponic solutions measured to monitor earthworm influence on solution chemistry.

## Molecular analyses and data provenance
- Gene expression focused on ABA biosynthesis (NCED3, NCED5) and abiotic stress response genes (CIPK6, NHX1, RD29A) using qPCR.
- Brassica napus genome guided primer design; Sinapis alba orthologues amplified with cross-species validation to avoid non-target amplification.
- Expression data normalized to Actin7; relative changes calculated by ΔΔCt method.
- Attempted to identify earthworm capability for direct phytohormone biosynthesis via BLAST searches using ABA synthesis enzyme genes against earthworm genomes (Eisenia fetida and Lumbricus terrestris).

## Quality controls and data interpretation
- Extraction time optimization to minimize compound degradation while ensuring recoveries; 24-hour extraction chosen based on recovery data.
- Internal standards and calibration steps documented to support reproducibility and cross-study comparisons.
- Data handling includes explicit outlier identification/removal using IQR-based criteria prior to analysis.

## Implications for monitoring frameworks
- Demonstrates a comprehensive workflow for detecting environmentally relevant plant hormone signals in soil and biotic contexts, integrating chemical analytics with molecular biology.
- Highlights the importance of:
  - Standardized extraction and cleanup protocols to ensure data comparability across studies and monitoring programs.
  - Use of internal standards and robust QC measures to improve data reliability.
  - Open data deposition (EIDC) to support data sharing and policy-relevant evaluation.
  - Considering multiple matrices (soil and hydroponic solutions) and biotic interactions (plants and earthworms) for a holistic assessment of soil health and biogeochemical signaling.

## Supplementary information and references
- Supplementary tables include detailed concentration data, gene primer sequences, and experimental metadata.
- The study builds on a broad set of methodological references for phytohormone extraction, MS analytics, and plant stress genetics to support monitoring-ready protocols.