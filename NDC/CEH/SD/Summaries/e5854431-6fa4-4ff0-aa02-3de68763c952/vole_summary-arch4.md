# Collection/generation methods

## Overview
- Live-trapping of wild field voles (Microtus agrestis) in Kielder Forest, Northumberland, UK, across 2015–2017.
- Sampling spanned 46 sessions, roughly every two weeks, at seven sampling sites (originally four per session with site reassignments).
- Voles were uniquely PIT-tagged; on first capture each session, researchers recorded sex, reproductive status, body measurements, and collected a small tail blood sample stored in RNAlater for short-term storage and later -80°C storage.

## Study design and sampling
- Longitudinal component: individuals sampled repeatedly while alive.
- Cross-sectional component: individuals sampled after culling.
- At each site, a grid of Ugglan traps was used; trapping and site logistics described to ensure broad spatial coverage.
- Field collection included demographic data, physical measurements, and blood/tissue sampling for downstream molecular assays.

## Field and laboratory instrumentation
- Immune gene expression measured by SYBR Green qPCR on blood-derived RNA from splenocytes preserved in RNAlater.
- Instrumentation included a 384-well plate format, robot-assisted pipetting (Pipetmax), and a QuantStudio 6-flex Real-Time PCR System.
- RNA extraction used the Mouse RiboPure Blood RNA Isolation Kit with DNase treatment; cDNA synthesized with the High-Capacity RNA-to-cDNA kit.
- Plate layouts used triplets with consistent target gene and endogenous control assays; samples assayed in duplicates; calibrators used across plates.

## Data collected and structure (Nature and Units of recorded values)
- Core data file: long_blood_qpcr_FV.2.csv with fields including:
  - Identification and sampling: bloodNum, Blood tube ID, site, dateCapt, session, gridTreat, trapsOut, trapsWorking, operator, timeGrid, timeOut, trap, year, etc.
  - Species and demographic: species, alive, age, sex, repro, scrotal, preg, perforate, lact, bodyW (g), bodyLen (mm), fat scores (pelvCond, dorsalCond, bodyCond).
  - Parasitic load indicators: miteLaela, miteListro, miteMyo, tick, flea.
  - Sample metadata: enteredBy, entryDate, comments, etc.
  - Molecular panel (gene expression): qPCR.plate1/2/3 IDs; genes (e.g., AR, CD8A, FOXP3, GATA3, IL10, IL17, IL1B, IL4, INFG, ORAI1, COL1A1, CTGF, FIZZ1, GPX1, IL1RN, IRF9, TGFB, TXNDR2, APOBR, BAB, BAR, IL1RAP, INSR, IRF2, MPR2, NOS2, SENS3, TOLLIP); relative concentrations.
  - Calibrators and processing: plate layouts, calibration references, duplications, and relative expression values.
- Additional details: extensive metadata on sample processing, plate management, and gene expression quantification.

## Experimental design, calibration, and data processing
- Gene targets chosen based on mouse immunology and prior vole data showing sensitivity to environment and host variables.
- Endogenous controls: Ywhaz and Actb.
- RNA extraction, DNase treatment, and cDNA synthesis followed standardized kits and manufacturer protocols.
- qPCR specifics:
  - Reaction: 10 µl with template 1 µl, Master Mix and SYBR Green; plate layouts included fixed target sets and endogenous controls across triplets.
  - Unknown samples assayed in duplicates; calibrators in triplicate; no-template controls included per plate.
  - Template cDNA diluted 1/20; calibrator created from pooled splenocyte cDNA; additional calibrator fragment used for certain genes (Tollip, Il1rap, Irf2).
  - Plate arrangement was balanced to avoid confounding plate effects with sampling structure.
- Expression quantification:
  - Relative expression values computed as ΔΔCt using machine software, indexed to plate-specific calibrators.
  - Quality control: melting curves and amplification plots inspected per well; cross-plate consistency ensured by matched triplets.
- Pathogen detection (microparasites):
  - qPCR targets: Babesia microti (18S) and Bartonella spp. (16S).
  - Validation: qPCR results corroborated with RNA-Seq pathogen reads from a subset of samples (n = 44); strong correlation (B. microti r^2 = 0.81; Bartonella spp. r^2 = 0.81; p < 0.001).

## Data provenance and references
- Methods and dataset described in:
  - Jackson et al. 2011, Molecular Ecology: “The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus Agrestis.”
  - Wanelik et al. 2019/2021 (bioRxiv): IgE receptor polymorphism, immune expression, and fitness outcomes in wild rodents.
- The dataset is complemented by cross-validation against RNA-Seq readouts and linked publications detailing the study design and analytical approach.

## Data quality, usability, and governance considerations (Data Leaders perspective)
- Data richness: combines detailed phenotypic data with longitudinal molecular measurements and pathogen load, enabling integrative analyses of immune dynamics in wild populations.
- Metadata completeness: extensive sample-level metadata and plate-level workflow information support reproducibility and data discoverability.
- Data integration potential: compatible with other datasets through standardized sample IDs, plate IDs, gene panels, and calibrators; supports cross-study meta-analyses of host immunity and fitness.
- Data quality controls: explicit QC steps (primer validation with defined PCR efficiency, duplicate measurements, calibrator-based normalization, plate triplet design, and manual review of amplification curves) increase reliability and cross-plate comparability.
- Accessibility considerations: dataset includes rich metadata and references; future updates should maintain standardized formats and consistent annotation to support efficient data sharing and re-use.