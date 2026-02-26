# The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis

## Overview
- Describes methods and dataset for measuring immune gene expression and pathogen infections in wild field voles to understand immunodynamics in natural populations.
- Integrates extensive field capture data with molecular assays and parasite surveillance to derive immune-related environmental health indicators.

## Study design and sampling
- Longitudinal (repeated live sampling of individuals) and cross-sectional (sampling after culling) components.
- Field site: Kielder Forest, Northumberland, UK, across seven forest clear-cut sites (2015–2017).
- Trapping: grid layout with ~150–197 Ugglan traps per site, spaced ~3–5 m apart.
- Sampling cadence: 46 sessions across March–October, roughly every two weeks.
- Individual tagging: unique PIT tag on first capture; recorded sex, reproductive status, body length, and body mass.
- Tissue collection: blood samples collected via tail puncture, stored in RNAlater, then -80°C for long-term storage.

## Field data collection (metadata and phenotypes)
- Site, trapping date, session, and grid/trap information (gridTreat, trapsOut, trapsWorking, trap ID).
- Species identification and animal status (alive/dead, age, sex, reproductive state: male A/D/S; female lactating/pregnant/perforate/non-perforate; scrotal status).
- Morphometrics: body mass (g), body length (mm), fat scores (pelvis, dorsal, body).
- Parasite and pathogen indicators: counts of ectoparasites (mites, ticks, fleas), and internal parasite data.
- Treatment data: anti-parasitic treatments and dosages (e.g., frontline, profender) with related fields.
- Sample identifiers: tube IDs, plate IDs for qPCR, and other lab-tracking fields.

## Molecular measurements and laboratory workflow
- Gene expression: SYBR Green qPCR to quantify a panel of immune-related genes in blood-derived RNA from longitudinal samples.
- Primer validation: de novo design with validation for specificity and ~100 ± 10% PCR efficiency.
- Normalization: endogenous controls Ywhaz and Actb; cDNA synthesized from RNAlater-preserved RNA; RT controls included.
- Plate setup: 384-well format with standard triplets of plate layouts; unknowns in duplicates; calibrators in triplicate; no-template controls included.
- Calibration and data processing: main calibrator created from pooled splenocyte cDNA; additional calibrator fragments used for underrepresented genes; data expressed as relative expression values (RQ) using ΔΔCt normalization.
- Pathogen detection: SYBR Green qPCR targeting Babesia microti (18S) and Bartonella spp. (16S) to quantify infections; validation against RNA-Seq pathogen reads (subset; n=44) showing strong concordance (r^2 ≈ 0.81 for both pathogens).
- Data quality: melting curves and amplification plots checked per well; samples distributed across plate triplets to avoid plate-sampling confounding.

## Data structure and content
- Primary dataset: long_blood_qpcr_FV.2.csv containing:
  - Demographics and capture metadata (site, dateCapt, session, year, etc.).
  - Trapping and environmental context (trapsOut, trapsWorking, gridTreat, treatDue, totTreatTotal, prevTreat).
  - Individual identifiers and status (species, chip, NRW, alive, age, sex, repro).
  - Morphometrics and condition scores (bodyW, bodyLen, pelvCond, dorsalCond, bodyCond).
  - Parasitology indicators (mite counts, tick counts, flea counts) and anti-parasitic treatments with dosages.
  - Molecular data: qPCR plate IDs (qPCR.plate1/2/...), gene targets with relative concentrations (AR, CD8A, FOXP3, IL10, IL17, IL1B, IL4, INFG, ORAI1, etc.), and additional markers (COL1A1, TGFB, NOS2, IRF9, etc.).
  - Reproductive and health notes (preg/test status, perforate, lact, scrotal, comments).
- Gene expression measures: relative concentrations (RQ) for a broad panel of immune-associated genes; two qPCR plate layouts used to assay a fixed gene set with matched animal triplets.

## Experimental design notes
- Longitudinal sampling enables within-individual immune expression dynamics over time; cross-sectional sampling informs population-level patterns.
- Field sites represent natural habitat conditions, with repeated measures across seven sites and multiple capture campaigns.
- Integration of host immune expression profiles with infection data provides a multifaceted view of environmental health indicators in wild populations.

## Data quality, validation, and governance
- Robust validation of molecular assays (primer efficiency, endogenous controls, calibrators) and cross-validated pathogen data with independent RNA-Seq reads.
- Transparent data structure with extensive metadata to facilitate reuse and comparability.
- Data sharing considerations highlighted (calibrators, standards, and plate design while ensuring data provenance and reproducibility).

## References and provenance
- Methods and dataset described in:
  - Jackson et al. 2011. The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis. Molecular Ecology.
  - Wanelik et al. 2019. IgE receptor polymorphism predicts divergent, sex-specific inflammatory modes and fitness costs in a wild rodent. bioRxiv.
  - Wanelik et al. 2021. Early-life immune expression profiles predict later life health and fitness in a wild rodent. bioRxiv.