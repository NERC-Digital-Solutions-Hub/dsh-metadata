# Collection/generation methods

## Overview
- Wild-field vole study in Kielder Forest, Northumberland, UK (2015–2017).
- Seven sampling sites with traps laid in grids; traps spaced ~3–5 m; at least 1 km between some sites.
- 46 trapping sessions across March–October; sessions occurred about every two weeks.
- Approximately 197 Ugglan traps per site; trapping conducted over three days per session (checks in morning and afternoon).
- Individuals were marked with PIT tags; a range of morphometric, reproductive, and health data were collected; blood samples stored for molecular analyses.

## Sampling design and spatial framework
- Longitudinal component: individuals sampled multiple times.
- Cross-sectional component: individuals sampled following culling.
- Grid-based trapping across seven forest sites; each site is a distinct sampling location for spatial analyses.

## Data collected and data structure
- Primary dataset: long_blood_qpcr_FV.2.csv containing fields such as:
  - site, trapping details (dateCapt, session, gridTreat, trapsOut, trapsWorking, trap), operator, time on grid/out, trap ID.
  - species caught, chip ID, capture history (NRW, alive/dead), age, sex, reproductive state, body metrics (bodyW, bodyLen, fat scores), scrotal, pregnancy, lactation status.
  - parasite and ectoparasite counts (mites, ticks, fleas), treatment data (treat, frontline/profender doses, tail tissue ID), and comments.
  - qPCR-related data: gene expression targets (AR, CD8A, FOXP3, GATA3, IL10, IL17, IL1B, IL4, INFG, ORAI1, plus many more), and plate identifiers (qPCR.plate1/2/3) with relative expression values.
- The dataset integrates field capture information with molecular data (immune gene expression and pathogen detection).

## Experimental design (lab and field)
- Fieldwork: seven sites with live trapping; roughly 150–197 traps per site arranged in grids.
- Longitudinal sampling of individuals for immune expression profiling.
- Cross-sectional sampling after culling to compare across cohorts.
- Field data paired with laboratory measurements to link host traits with molecular data.

## Field and laboratory instrumentation
- Field: live traps deployed in grids; handling and processing performed on-site according to protocol.
- Laboratory: SYBR Green-based Q-PCR to quantify expression of immune-related genes in blood.
- RNA extraction from splenocytes preserved in RNAlater; DNAse treatment; cDNA synthesis with standard kits.
- Real-time PCR performed on QuantStudio 6-flex; 10 µl reaction volumes; plate automation for consistent handling.
- Endogenous controls: Ywhaz and Actb; unknown samples run in duplicates; calibrators run in triplicate; no-template controls included per plate.

## Calibration, data processing, and quality control
- Three standard plate layouts used to ensure consistency across plates.
- Unknowns in duplicate; calibrators in triplicate; main calibrator pool created from splenocyte cDNA across the study site.
- For underrepresented genes (e.g., Tollip, Il1rap, Irf2), synthetic 478 bp fragments used as additional calibrators.
- cDNA diluted 1/20 prior to assay.
- Data processed with ΔΔCt method to generate relative expression (RQ) values; melting curves and amplification plots checked for specificity.

## Pathogen detection and validation
- Pathogen screening: qPCR targeting Babesia microti (18S) and Bartonella spp. (16S) in longitudinal samples.
- Validation: comparisons with RNA-Seq-derived pathogen reads from a subset (n = 44) showed strong concordance (Babesia microti r^2 = 0.81; Bartonella spp. r^2 = 0.81; p < 0.001).

## References and provenance
- Methods and dataset described in:
  - Jackson et al. 2011. The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus Agrestis. Molecular Ecology.
  - Wanelik et al. 2019. IgE receptor polymorphism and inflammatory modes in a wild rodent. bioRxiv.
  - Wanelik et al. 2021. Early-life immune expression and later life health in a wild rodent. bioRxiv (doi linked in text).

## GIS-relevant considerations
- Data support spatial analyses of sampling effort, site-specific immune expression, and infection risk across seven forest sites.
- Rich attribute data per capture event enables map-based visualisations of host traits, qPCR results, and pathogen presence, aligned with environmental layers.
- Important notes for GIS integration: ensure consistent linking of field identifiers (site, dateCapt, session) to spatial coordinates and environmental context; account for missing values and cross-year comparability when modelling spatial patterns.