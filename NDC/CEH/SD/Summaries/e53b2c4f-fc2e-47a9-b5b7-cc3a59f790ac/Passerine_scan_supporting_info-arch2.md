# Collection of 3D Surface Scans of Beaks of Chaffinches (Fringilla coelebs) and Other Passerine Birds

## Overview
- Data consist of 3D surface scans of beaks from chaffinches and other passerine birds.
- Specimens originate from the Natural History Museum, Tring, Hertfordshire.
- Scanning performed with a calibrated MechScan macro structured light scanner; alignments created with FlexScan3D; outputs saved as ply files with no post-processing.

## Collection/generation methods
- Scans generate calibrated point-distance data in 3D space.
- Distances between points are recorded in millimetres.
- Scans were visually inspected for holes, misalignment, and missing regions; no downstream post-processing applied.

## Data format and units
- Each scan is stored as a ply file containing calibrated 3D coordinates.
- Measurements are in millimetres.

## Data structure and naming
- File naming convention: Genus_species_subspecies_n.ply
  - Examples: Aimophila_ruficauda_acuminata_1.ply; Anthus_godlewskii_2.ply
- Subspecies and species names are included, followed by an index number.
- The dataset appears to include a long list of species/subspecies with corresponding scan counts; some entries contain inconsistencies or incomplete lines in the listing.

## Metadata and dataset contents
- Metadata file: Passerine_scan_metadata.csv
- Columns include: Specimen_id, Description, Family, Genus, Species, Subspecies, Mus_registration, Coll_date, Country, Label_locality, Sex, Bill_len, Bill_dep, Bill_wid, Tarsus, Wing, Tail, Scanner, Notes.
- Measurements: Bill length/dep/wid, Tarsus, Wing, Tail recorded with specified measurement tools and accuracies (e.g., 0.01 mm for some measurements, 1 mm for Wing/Tail).

## Quality control
- Visual QC performed on all aligned scans for holes, misalignment, and missing regions.
- No additional post-processing applied to scans.

## Data accessibility and reuse
- The dataset and its metadata are prepared for storage and upload to appropriate data portals.
- Metadata provide links between ply files and specimen provenance, taxonomy, collection data, and measurements.
- The dataset is suitable for integration with other environmental or biodiversity data to support broad monitoring initiatives.

## Relevance for Analysts Monitoring the Environment
- Enables standardized, time-based assessment of morphological data across bird taxa, useful for environmental health and policy performance analyses.
- Standardized data formats and metadata support cross-dataset integration and reproducible monitoring.
- The structured approach (data verification, standard naming, and metadata linkage) facilitates transparency and comparability over time.

## Challenges and considerations for analysts
- Ensuring data value through integration with other relevant datasets (e.g., ecological, climatic, or habitat data).
- Providing broad access to underlying data to maximize reuse and secondary analyses.
- Potential inconsistencies in the listing (e.g., incomplete or conflicting entries) require careful QA and validation before downstream analyses.