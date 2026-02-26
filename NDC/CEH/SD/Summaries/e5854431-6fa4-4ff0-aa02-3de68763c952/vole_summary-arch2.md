# The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis

- Purpose and scope
  - Use data to demonstrate environmental health and immunodynamics over time in wild voles.
  - Focus on standardised collection, processing, and analysis to enable monitoring of environmental health and policy performance.

- Study design and sampling regime
  - Location: Kielder Forest, Northumberland, UK.
  - Timeframe: 2015–2017.
  - Sampling regime: longitudinal and cross-sectional components across seven sampling sites within forest clear-cuts.
  - Trapping: 46 sessions (Mar–Oct, every ~2 weeks); at each session, traps at four sites (approximately 1 km apart); grid of 197 Ugglan traps per site, ~5 m between traps; 3-day sessions with checks morning and afternoon.
  - Marking: unique PIT tags for individuals.
  - Field data collected on first capture per session: sex, reproductive status, body measurements (snout-vent length, body mass), and tail blood sampling for RNA storage.

- Data collection and structure
  - Primary data file: long_blood_qpcr_FV.2.csv with fields including:
    - Metadata: bloodNum, blood tube ID, site, dateCapt, session, gridTreat, trapsOut, trapsWorking, operator, timeGrid, timeOut, trap, year.
    - Biological data: species, chip ID, NRW (new capture/recapture), alive, age, sex, repro, scrotal, pregnAnt, perforate, lact.
    - Morphology: bodyW (mass in g), bodyLen (mm), pelvCond, dorsALCond, bodyCond.
    - Parasitology: miteLaela, miteListro, miteMyo, tick, flea.
    - Treatments: treat, frontline dose, profender dose, etc.; treatment status (treatDue, totTreatTotal, prevTreat).
    - qPCR immunology data: gene expression markers across plates (AR, CD8A, FOXP3, GATA3, IL10, IL17, IL1B, IL4, INFG, ORAI1, etc.) and additional genes (CD86, CD99L2, COL1A1, CTGF, FIZZ1, GPX1, IL1RN, IRF9, TGFB, TXNDR2, APOBR, BAB, BAR, IL1RAP, INSR, IRF2, MPR2, NOS2, SENS3, TOLLIP).
  - Calibration and normalization: qPCR using SYBR Green; endogenous controls Ywhaz and Actb; data quantified as relative expression (RQ) via ∆∆Ct; plateauing and run controls included.
  - Pathogen testing: detection of Babesia microti (18S) and Bartonella spp. (16S) by SYBR Green qPCR; validation against RNA-Seq pathogen reads showing strong correlation (B. microti r^2=0.81; Bartonella spp. r^2=0.81).

- Laboratory methods and calibration
  - Sample processing: RNA extracted from splenocytes preserved in RNAlater; DNase treatment; cDNA synthesis with reverse transcription kit; cDNA diluted 1/20 for assays.
  - qPCR setup: 384-well plates, robot-assisted pipetting (Pipetmax), QuantStudio 6-flex; 10 µl reaction volumes with PrecisionFAST qPCR Master Mix.
  - Plate design and controls: three standard plate layouts per panel; duplicates for unknown samples; triplicates for calibrator samples; no template controls per plate.
  - Calibrators and reference samples: main calibrator created from pooled splenocyte cDNA from multiple volunteers; additional synthetic calibrators for under-represented genes ( Tollip, Il1rap, Irf2 ).
  - Assay validation: primer design in-house with validation confirming target specificity and 100 ± 10% PCR efficiency; melting curves and amplification plots reviewed for each well replicate.

- Data quality assurance and interoperability
  - Cross-plate dispersion: samples from different field groups distributed across plate triplets to avoid plate-sampling confounding.
  - Data processing: expression values computed with ΔΔCt against calibrator; supervisory checks on amplification curves and melting curves.
  - Data storage and sharing: datasets stored and uploaded to appropriate portals to support broader access.

- Outputs and outputs formats
  - Standardised formats (datasets, reports, maps, charts) suitable for environmental health monitoring and policy scrutiny.
  - Gene expression data provide immunodynamic profiles across individuals, time, and population contexts.
  - Pathogen burden data integrated with host immune markers for holistic health assessments.

- Relevance and related work
  - Builds on prior methodology for immunological profiling in wild animals (e.g., The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis, Molecular Ecology 2011).
  - Linked to subsequent studies on early-life immune expression and fitness, and gene-immune associations in wild rodents (references to 2011 Molecular Ecology, 2019–2021 preprints).

- Particular challenges and opportunities for data use
  - Challenge: increasing the value of datasets by integrating with additional data sources for broader environmental interpretation.
  - Challenge: enabling access to underlying data used to generate final outputs to support transparency and reuse.