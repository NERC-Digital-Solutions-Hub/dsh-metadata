# Collection/generation methods

- The dataset consists of 3D surface scans of beaks from chaffinches (Fringilla coelebs) and other passerine birds, all sourced from the Natural History Museum, Tring, UK.
- Scanning was performed with a calibrated MechScan macro structured light scanner and scans were aligned using FlexScan3D. Final files are saved in ply format with no additional post-processing.

## Nature and units of recorded values

- Scans are calibrated 3D files with distances between points recorded in millimetres.

## Quality control

- Scans were visually inspected for holes, misalignment, and missing regions.
- No post-processing beyond initial alignment.

## Details of data structure

- File naming convention: Genus_species_subspecies_n.ply
  - Examples: Aimophila_ruficauda_acuminata_1.ply, Anthus godlewskii_1.ply
- Subspecies names included when relevant; otherwise species only.
- File counts indicate the number of scans per taxon, e.g., numerous entries showing multiple scans per subspecies or species.

## Metadata file and data fields

- Metadata file: Passerine_scan_metadata.csv
- Key columns and meanings:
  - Specimen_id: matches the ply filename (Genus_species__subspecies_n)
  - Family, Genus, Species, Subspecies: taxonomic classifications
  - Mus_registration: museum accession data
  - Coll_date: collection date from museum labels
  - Country: country of collection (to be backfilled from Label_locality)
  - Label_locality: verbatim locality data
  - Sex: male, female, or unsexed
  - Bill_len, Bill_dep, Bill_wid: bill measurements (mm) with 0.01 mm precision
  - Tarsus, Wing, Tail: additional morphometrics (mm) with 0.1–1 mm precision
  - Scanner: abbreviation for the scanner used (MS = MechScan 3D Macro)
  - Notes: additional scan quality notes and transcription caveats

## Data management and governance considerations

- Data are raw ply scans with accompanying descriptive metadata intended to support future data sharing and discovery.
- Metadata completeness and accuracy are essential for integration into monitoring frameworks, including backfilling country data and ensuring consistent taxonomic labeling.
- The dataset highlights typical monitoring framework challenges: incomplete metadata, potential transcription errors, and the need for ongoing quality assurance and data governance (storage, sharing, and updates).

## Relevance for monitoring frameworks

- Provides a verifiable, high-resolution morphological dataset across multiple species and subspecies, suitable for comparative analyses and trend assessments over time and space (where collection dates and locations are available).
- Demonstrates a model for linking physical measurements (morphometrics) to specimen metadata to inform environmental health and biodiversity monitoring.
- Emphasizes the need for clear data standards, accessible raw data, and comprehensive metadata to overcome common barriers in monitoring data workflows (data gaps, access, silos, and governance).