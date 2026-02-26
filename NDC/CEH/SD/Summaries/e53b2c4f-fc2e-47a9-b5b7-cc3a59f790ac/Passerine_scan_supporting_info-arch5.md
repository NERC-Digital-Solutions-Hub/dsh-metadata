# Collection/generation methods

## Overview
- 3D surface scans of beaks of chaffinches (Fringilla coelebs) and other passerine birds.
- Specimens originate from the Natural History Museum, Tring, Hertfordshire.
- Scanned with a calibrated MechScan macro structured light scanner; alignment performed with FlexScan3D.
- Scans saved as ply files with no post-processing.

## Data capture and format
- Distances between points recorded in millimetres (calibrated files).
- All aligned scans are stored as ply files; no additional post-processing applied.
- File naming convention encodes taxonomic information and a scan index.

## Quality control and provenance
- Visual quality checks conducted to identify holes, misalignment, and missing regions.
- No post-processing performed after alignment, preserving raw scan state.

## Data structure and naming conventions
- Scan files named: Genus_species_subspecies_n.ply
  - Examples: Aimophila_ruficauda_acuminata_1.ply, Anthus_godlewskii_2.ply
- Subspecies and species are included in filenames; multiple scans per taxon are enumerated (n).
- A separate metadata file associates each ply with taxon and specimen metadata.

## Metadata schema (Passerine_scan_metadata.csv)
- Key columns:
  - Specimen_id: matches ply filename (Genus_species_subspecies_n)
  - Family, Genus, Species, Subspecies: taxonomic classification
  - Mus_registration: museum specimen accession number
  - Coll_date: collection date
  - Country: country of collection (backfilled from locality when possible)
  - Label_locality: verbatim collection locality
  - Sex: male, female, or unsexed
  - Bill_len, Bill_dep, Bill_wid: bill measurements (mm, precision 0.01 mm)
  - Tarsus, Wing, Tail: additional morphometrics (mm, Wing measured to 1 mm)
  - Scanner: abbreviation for scanner (e.g., MS = MechScan 3D Macro)
  - Notes: remarks on scan quality and transcription issues
- The metadata provides a direct linkage to each ply file and documents measurement methods and precision.

## Access, sharing, and updates
- Data are organized to allow discovery and reuse via the ply files and the accompanying metadata CSV.
- The Specimen_id linkage ensures traceability between 3D data and descriptive/morphometric metadata.
- The Notes field supports documenting scan quality and potential transcription errors, aiding data stewardship and updates.

## Governance considerations for Data Stewards
- Ensure tight alignment between ply files and metadata (_specimen_id_ consistency).
- Maintain metadata completeness and accuracy across all fields (taxonomy, collection data, locality, measurements, and scanner details).
- Enforce consistent units and measurement precision; document any deviations.
- Plan for updates as new scans are generated or existing records are corrected; implement versioning and provenance tracking.
- Address data transfer and storage considerations given potentially large ply files.
- Monitor for and document any data quality issues uncovered during reuse (e.g., holes, misalignments, or transcription errors) and update the Notes accordingly.
- Consider data interoperability by documenting the metadata schema and providing mappings to any relevant data standards or ontologies.