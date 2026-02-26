# Collection/generation methods

- Scope
  - 3D surface scans of beaks from chaffinches (Fringilla coelebs) and other passerine birds.
  - Specimens sourced from the Natural History Museum, Tring, Hertfordshire.

- Data collection and generation
  - Scanned with a calibrated MechScan macro structured light scanner.
  - Aligned using FlexScan3D.
  - Aligned scans saved as ply files with no additional post-processing.

- Data format and structure
  - Distances recorded in millimetres within the ply files.
  - File naming convention: Genus_species_subspecies_n.ply (e.g., Aimophila_ruficauda_acuminata_1.ply; for species without subspecies: Genus_species_1.ply).
  - Aims to reflect subspecies groupings and the number of scans per group (e.g., multiple entries like 1, 2, 3 representing different scan sets).

- Metadata and linking data
  - The meta-data file Passerine_scan_metadata.csv includes:
    - Specimen_id (links to ply filename), Family, Genus, Species, Subspecies
    - Mus_registration, Coll_date, Country, Label_locality, Sex
    - Morphometrics: Bill_len, Bill_dep, Bill_wid, Tarsus, Wing, Tail
    - Scanner (e.g., MS for MechScan)
    - Notes (scan quality and transcription notes)
  - Specimen_id in metadata matches the ply filename, enabling data linkage.

- Measurements and units
  - Scans provide 3D spatial data with distances in millimetres.
  - Morphometric fields in metadata (e.g., bill length, bill depth, bill width, tarsus, wing, tail) are measured in millimetres, with specified measurement precision (e.g., calipers to 0.01 mm for some metrics; wing and tail to 1 mm accuracy per the metadata description).

- Quality control and processing
  - Scans were visually inspected for holes, misalignment, and missing regions.
  - No post-processing steps were applied after alignment.

- Data usage and considerations
  - Data are intended for morphometric and comparative analyses, potentially linking 3D beak morphology to taxonomic groups, collection data, and other measurements.
  - Data can be uploaded to portals with metadata for discoverability and reuse.
  - Potential limitations include incomplete metadata fields, country backfilling from locality data, and the fact that scans are raw (no post-processing corrections) which may influence downstream analyses.

- Typical challenges and context (as described in the broader archetype)
  - Access to and integration of datasets from multiple sources; ensuring dataset discoverability.
  - Handling data at multiple scales and ensuring consistent standardization across specimens.
  - Documentation of data provenance, measurement methods, and potential transcription issues to support robust analysis.