# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

## Aim
- Use mass spectrometry to measure cytokinin and ABA concentrations in soil and hydroponic solutions, examining effects of earthworms and plants and enabling data to be compared over time.

## Study design and treatments
- Experimental setups include:
  - Hydroponic solutions (42 days) with four treatments: earthworms plus plants, earthworms only, plants only, neither.
  - Soil experiments (42 days) using sandy loam soil with three earthworms per jar in earthworm-present treatments; five plant-containing replicates per condition.
- Plant species:
  - Hydroponics: Sinapis alba (white mustard).
  - Soil: Sinapis alba; initial establishment before earthworm addition to limit burrowing effects.
- Earthworm species:
  - Hydroponics: Eisenia fetida.
  - Soil: Lumbricus terrestris.
- Replication and measurements include shoot biomass, soil moisture, and earthworm biomass (pre/post).

## Sample preparation and extraction (soil vs hydroponic)
- Soil samples:
  - Phytohormones spiked with authentic standards in soil to establish recovery.
  - Extraction with a 15:4:1 methanol:water:formic acid (v:v:v) mixture; performed over multiple time points, with a final 24 h extraction to prevent degradation.
  - Internal standards: isotopically labelled phytohormones added before extraction.
  - Clean-up via solid-phase extraction (MCX cartridges) to separate acidic, cytokinin ribosides, and cytokinin free bases fractions.
- Hydroponic solutions:
  - Recovery straightforward; isotopically labelled standards added for internal calibration.
  - No solvent extraction required.

## Solid phase extraction and fractionation
- Cartridge: 60 mg, 3 mL Oasis MCX (mixed-mode cation exchange).
- Conditioning and loading performed under acidic conditions (formic acid, pH ~1.4).
- Fractions eluted:
  - Fraction 1: acidic compounds (methanol).
  - Fraction 2: cytokinin ribosides (0.35 M NH4OH).
  - Fraction 3: cytokinin free bases (0.35 M NH4OH in 60% methanol).
- Fraction 2 archived for future analysis; Fractions 1 and 3 used for analysis.

## Identification and quantification by mass spectrometry
- Identification:
  - FT-ICR-MS (solariX XR) with ESI, negative mode for Fraction 1 and positive mode for Fraction 3.
  - High mass accuracy (<1 ppm) used to determine empirical formulae prior to quantification.
- Quantification:
  - Internal-standardized MRM on a TSQ Endura triple quadrupole with LC separation.
  - Compounds quantified: IAA and ABA (Fraction 1), zeatin (Z), adenosine (Ade), and isopentenyladenosine (iP) (Fraction 3).
  - Isotopically labelled internal standards used: for IAA, ABA, Z, Ade, iP (e.g., 13C6-IAA, 2H6-ABA, 2H6-Z, 2H6-Ade, 2H6-iP, etc.).
  - LC separation on a Kinetex C18 column with a 95:5 water:methanol starting mix and gradient to 100% methanol; detailed gradient timings provided for Fractions 1 and 3.
  - Specific transitions and instrument settings optimized for each compound (collision energies, Q1/Q3 transitions, and ionization modes).

## Data handling and analysis
- Internal standards enable correction for extraction and analysis variability.
- Data processing includes:
  - Correlating FT-ICR-MS identifications with subsequent MRM quantification.
  - Handling of non-detects and limits of detection (as detailed in supplementary data).
- Statistical analysis:
  - Outliers identified via interquartile range and excluded.
  - Plant biomass and hydroponic solution pH tested with t-tests (normal data).
  - FDH (fluorescein diacetate hydrolysis) activity and phytohormone concentrations analyzed via two-way ANOVA (factors: presence/absence of earthworms and plants); Holm-Sidak post hoc tests used for multiple comparisons.
  - Hydroponic phytohormone data, not normally distributed, still analyzed with two-way ANOVA due to robustness of ANOVA to violations of normality and equal variance for interaction effects.
- FDH assay in soil as a proxy for biological activity; pH of hydroponic solutions measured at experiment end to assess earthworm influence on solution chemistry.

## Molecular biology analyses
- Goal: determine whether earthworms/microbial context influence ABA biosynthesis gene expression in Sinapis alba.
- Approach:
  - Use Brassica napus genome as a guide to design primers for ABA biosynthesis (NCED3, NCED5) and abiotic-stress response genes (CIPK6, NHX1, RD29A).
  - Validate primers on Sinapis alba; BLAST against earthworm genomes to confirm specificity.
  - qPCR performed on RNA from shoots and roots; cDNA synthesized and normalized to Actin7 using the ΔΔCt method.
- Data include gene expression changes relative to internal control and references for selected genes (Tables S5–S6 of supplementary information).

## Data availability and supplementary information
- All data available from the EIDC data catalogue (High et al., 2019).
- Supplementary information includes:
  - Table 1: Concentrations of target compounds detected in all samples (including LOD handling and outliers).
  - Tables 2–4: Biomasses, FDH activity, pH values.
  - Tables S5–S6: Molecular biology primers and target genes.
- The study integrates metabolite data with plant and earthworm biology to assess environmental samples using standardized workflows.

## Relevance to environmental monitoring
- Demonstrates a standardized, multi-matrix approach to monitor phytohormones and related metabolic activity in soil and hydroponic systems.
- Combines robust QA/QC (internal standards, SPE cleanup, FT-ICR-MS for identification, and targeted MRM) to produce comparable datasets over time.
- Data sharing via EIDC supports reuse and integration with other environmental health datasets; aligns with goals of increasing dataset value and enabling access to underlying data for broader scrutiny of environmental health and policy performance.