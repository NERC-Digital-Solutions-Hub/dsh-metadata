# Overview

- Scope and purpose: Report concentrations of perfluorinated chemicals (PFCs) in gannet (Morus bassanus) eggs from two UK colonies (Bass Rock, Ailsa Craig) collected 1977–2013; samples frozen until analysis.
- Data products: Two CSV files named Results_Ailsa_Craig.csv and Results_Bass_Rock.csv containing 13 columns each (location, year, PFSAs 3–10, PFCAs 11–13; all in ng/g wet weight).

## Data collection and samples

- Samples: Whole eggs homogenised; 1 g wet weight per analysis; stored frozen until analysis.
- Colonies and timeframe: Bass Rock and Ailsa Craig; 1977–2013.

## Analytical method

- Extraction and cleanup:
  - Solid-liquid extraction with 18 h incubation at 4°C; internal standards 13C-PFOS and 13C-PFOA added.
  - Acetonitrile extraction, vortexing, ultrasonication (three cycles with no solvent change).
  - Centrifugation, evaporation, resuspension; cleanup with 25 mg activated carbon and 50 µL glacial acetic acid; final centrifugation.
- Instrumentation:
  - UPLC-MS/MS (ACQUITY UPLC with BEH C18 trap, RP-18e column) with negative electrospray ionisation.
  - Gradient: 70% A to 100% B; flow 0.4 mL/min.
  - Analytes: 10 PFCAs and 3 PFSs quantified.

## Quality control and performance

- QC: Blank in each batch; recoveries using 13C surrogates (PFOA and PFOS).
- Recovery: 72%–144% across compounds.
- Method detection limits (LOD):
  - PFCAs: mean LOD 0.060 ng/g; range 0.015–0.107 ng/g.
  - PFSs: PFDS 0.028; PFHxS 0.084; PFOS 0.137 ng/g.
- Data treatment: Target analytes recovery-corrected.

## Compounds analyzed (highlights)

- Perfluorinated sulfonates (PFSs): PFHxS, PFOS, PFDS.
- Perfluorinated carboxylic acids (PFCAs): PFBA, PFOA, PFNA, PFDA, PFUnA, PFDoA, PFTriDA, PFTeDA, PFPeDA, PFHxA (and related abbreviations listed in the document).

## Data structure and provenance

- Structure: Two CSV datasets with 13 columns; columns 1–2 identify location and year; columns 3–10 contain PFSAs; columns 11–13 contain PFCAs; all values in ng/g wet weight.
- Data provenance: Based on a method aligned with Fernandez-Sanjuan et al. (2010) for screening PFCs in aquatic organisms.

## Data governance considerations for Data Leaders

- Data discovery and integration:
  - Two separate colony datasets; plan for a unified data dictionary and harmonized schema.
  - Ensure consistent naming for analytes and units across both files.
- Metadata and documentation:
  - Capture sample-level metadata: exact colony, GPS if available, collection dates, sample type, storage conditions (frozen), and any pooling.
  - Document QA/QC details: batch IDs, surrogate standards, recoveries, LODs, and data correction methods.
- Data quality and reliability:
  - Acknowledge wide recoveries (72%–144%) and analyte-specific LODs; consider flagging or quality flags for low-recovery or near-LOD results.
  - Maintain traceability to the Fernandez-Sanjuan (2010) method reference; store method version and any deviations.
- Data stewardship and usability:
  - Establish versioned data releases and an auditable audit trail for updates or corrections.
  - Provide a machine-readable data dictionary and metadata schema to support discoverability and reuse.
  - Consider future data integration with broader monitoring datasets to enable trend analysis across time and colonies.

## End notes

- The document outlines a reproducible workflow for PFC measurement in eggs and provides a clear data structure, enabling downstream analysis of temporal and spatial trends, with explicit QC and metadata considerations suitable for data governance and stewardship.