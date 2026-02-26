# Supporting documentation for bird ringing data

## Overview
- Describes a long-term population monitoring dataset from Wytham woods, Oxfordshire, UK, collected in 2020 and 2021 to study breeding biology and behaviour of birds.
- Birds were captured at nests during April–June and fitted with a BTO metal ring; Great tits and blue tits additionally received RFID/PIT tags. All nestlings were tagged at 2 weeks old.
- Autumn and winter ringing continued; immigrants were tagged. Birds were released after processing.
- Data were entered into the EBMP (Edward Grey Institute Bird data Management Project) with quality checks.

## Data Collection & Lifecycle
- Fieldwork period:
  - Primary capture: April–June (nest-based trapping at nests).
  - Additional ringing: autumn and winter across the woodland.
- Procedures:
  - Captures used mistnets; biometrics recorded (mass, wing length, tarsus length, fat score, bill length).
  - Members of the team (notably Keith McMahon and Sam Crofts, with others assisting) entered data into EBMP.
  - Immigrants to the population were tagged; all birds released after processing.
- Data governance:
  - Data undergo multiple quality checks within EBMP (e.g., identifying erroneous nestbox identities).

## Data Structure & Semantics
- File: a single CSV named Ringing_data containing 23 columns.
- Key column groups and examples:
  - Capture type: Record.type (physical vs diurnal), Retrap (new capture or retrapped).
  - IDs: Bto.ring (BTO ring number), Pit.tag (alphanumeric PIT-tag or blank if none).
  - PIT-tag status: Pit.tag.state with codes 0–6 (e.g., 0 no tag, 1 new tag, 2 tag present but not scanned, 3 tag scanned, 4 tag replaced, 5 tag removed and not replaced, 6 faulty tag removed and replaced).
  - Species and demographics: Bto.species.code, Age (codes with external reference), Sex (NA, F, M), Sexing method (pl, bp, cp, ib, ip).
  - Date/Location: Date.time; Location (e.g., nestbox code like 20201B100).
  - Morphometrics: Wing.length (mm), Weight (g); Bill.length/depth with respective measurement methods (Bill.length.method: s, f, n; Bill.depth.method: d, f); Tarsus.length with method (M or S).
  - Health/condition: Pox (NA/TRUE/FALSE), Leg.condition.description, Tick.description, Comments.
- Metadata references:
  - Species codes and age codes are defined in external PDFs provided by BTO (links included in the dataset documentation).

## Data Quality & Governance
- Data quality controlled within the EBMP system, including checks for data entry consistency and correctness of nestbox identities.
- Data entry primarily performed by named individuals (e.g., Keith McMahon and Sam Crofts) with involvement from additional field workers, enabling traceability and accountability.
- The structure uses standard, externally referenced coding schemes for species and age, aiding interoperability and future reuse.

## Access, Documentation & Reuse
- Dataset stored and managed in an internal Bird data Management Project (EBMP); access likely restricted to collaborators.
- Comprehensive field definitions and coding conventions are documented within the dataset description, including external references to BTO code lists for species and age.
- The documentation supports reuse by outlining data collection methods, tagging schemes, measurement variables, and data integrity checks.

## Relevance to Data Leaders
- Demonstrates end-to-end data lifecycle management: from field collection and tagging to centralized data entry, quality checks, and storage in a dedicated data management system.
- Highlights alignment with standard data practices:
  - Use of standard species and age codes with external reference resources.
  - Clear data lineage: who collected and entered data, and how quality was ensured.
- Shows data governance considerations for small, field-based datasets:
  - Importance of metadata, data provenance, and versioning.
  - Need for ongoing data stewardship and documentation to support discovery and reuse.
- Practical insights for improving data systems:
  - The value of maintaining external code lists to support interoperability.
  - The benefit of documenting data collection context (timing, locations, tagging schemes) to facilitate cross-project collaboration and broader data sharing.