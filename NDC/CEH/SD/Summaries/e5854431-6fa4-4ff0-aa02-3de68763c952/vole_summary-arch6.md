# Collection/generation methods

## Overview
- Live-trapping of wild field voles (Microtus agrestis) in Kielder Forest, Northumberland, UK, across 2015–2017.
- Seven sampling sites with grid-based trapping; sessions held March–October (46 sessions total) at roughly two-week intervals; each session lasted three days.
- Voles were marked with PIT tags; demographic data (sex, reproductive status) and morphometrics (body mass, body length) collected; blood samples taken for molecular analyses.

## Sampling design and data scope
- Longitudinal component: individuals sampled repeatedly over time.
- Cross-sectional component: individuals sampled after culling.
- Large grid per site: approximately 150–200 traps at each site, spaced 3–5 m apart; traps checked twice daily.
- Data collected include trap metrics (site, date, session, grid treatment, traps used/working), animal identifiers, species, sex, age, reproductive status, body measurements, fat scores, ectoparasite counts, and treatment histories.
- Primary data file: long_blood_qpcr_FV.2.csv, containing both field observations and laboratory results.

## Nature and units of recorded values
- Field data: bloodNum, blood tube ID, site, dateCapt, session, gridTreat, trapsOut, trapsWorking, trap, species, chip, NRW (new/recapture/within-week capture), alive, age, sex, repro, bodyW (g), bodyLen (mm), pelvicCond, dorsalCond, bodyCond, parasite counts (mites, ticks, fleas), and treatment details.
- Sampling metadata: enteredBy, entryDate, year, session2, treatDue, totTreatTotal, prevTreat.
- Pathogen data: qPCR targets for Babesia microti (18S) and Bartonella spp. (16S) with relative expression/read values validated against RNASeq-derived pathogen reads.
- Immunology/Molecular data: qPCR-based relative concentrations for gene panels across three plates, including genes such as AR, CD8A, FOXP3, GATA3, IL10, IL17, IL1B, IL4, INFG, ORAI1, CD86, CD99L2, COL1A1, CTGF, FIZZ1, GPX1, IL1RN, IRF9, TGFB, TXNDR2, APOBR, BAB, BAR, IL1RAP, INSR, IRF2, MPR2, NOS2, SENS3, TOLLIP; with endogenous controls Ywhaz and Actb.
- qPCR workflow details: plate layouts with fixed target sets, duplicates for samples, triplicates for calibrators, no-template controls, and a main calibrator pool created from splenocyte cDNA; additional synthetic calibrators used for underrepresented genes ( Tollip, Il1rap, Irf2 ).

## Laboratory methods and data generation
- Immunology assays: SYBR Green qPCR on 384-well plates to measure immune-related gene expression; cDNA synthesized from RNAlater-preserved splenocytes; RNA treated with DNase; reverse-transcribed to cDNA; samples run in duplicate; calibrators in triplicate.
- Calibration and normalization: endogenous controls (Ywhaz, Actb); ΔΔCt method used to generate relative expression (RQ) values; samples dispersed across plate triplets to avoid confounding plate with sampling group; melting curves checked for specificity.
- Pathogen identification: qPCR-based detection for B. microti and Bartonella spp.; validation against RNASeq pathogen reads showing strong concordance (r^2 ≈ 0.81 for both pathogens).

## Experimental design considerations and data integrity
- Aiming to minimize plate effects by distributing samples across plate triplets and maintaining consistent plate layouts.
- Validation steps include cross-method corroboration (qPCR vs RNASeq) for pathogen detection.
- Primer validation performed in-house with assay efficiency targeted at 100 ± 10%.

## Data provenance, references, and context
- Datasets and methods linked to prior work on immunodynamics in wild voles (e.g., Jackson et al. 2011; Wanelik et al. 2019, 2021) and related methodological papers.
- Primary papers describing the methods and dataset:
  - Jackson et al. 2011, Molecular Ecology
  - Wanelik et al. 2019, bioRxiv
  - Wanelik et al. 2021, bioRxiv
- These documents provide detailed protocols for immunological profiling and cross-validation with pathogen reads.

## How this data supports data use
- Provides a comprehensive, well-documented dataset linking field data (demography, morphometrics, parasitism) with molecular readouts (immune gene expression, pathogen presence).
- Includes explicit calibration, controls, and validation steps to support reuse in comparative analyses, meta-analyses, or explorations of immune dynamics in wild populations.
- Data are structured to enable self-serve exploration, with explicit file and field definitions and quality assurance procedures.