# Collection/generation methods

- Overview
  - 3D surface scans of beaks from chaffinches (Fringilla coelebs) and other passerine birds.
  - Specimens sourced from the Natural History Museum, Tring, Hertfordshire.
  - Scans produced with a calibrated MechScan 3D Macro structured light scanner and aligned using FlexScan3D.
  - Aligned scans saved in ply format with no additional post-processing.

- Data collection and processing
  - Scans captured using MechScan macro structured light technology.
  - Alignment performed in FlexScan3D; final files are ply format.
  - No subsequent post-processing applied.

- Nature and units of recorded values
  - Scans are calibrated 3D files; distances between points are recorded in millimetres.

- Quality control
  - Visual inspection of scans for holes, misalignment, and missing regions.
  - No further post-processing applied after alignment.

- Details of data structure
  - Each scan file name follows: Genus_species_subspecies_n.ply
    - Examples: Aimophila_ruficauda_acuminata_1.ply, Anthus_godlewskii_2.ply
  - Species and subspecies names are included in file names; the trailing number indicates the scan index for that taxon.
  - A comprehensive list pairs genus/species/subspecies with the number of scans (e.g., multiple entries per taxon).

- Metadata and data linkage
  - The meta-data file Passerine_scan_metadata.csv contains:
    - Specimen_id: matches the ply filename (Genus_species__subspecies_n)
    - Taxonomy: Family, Genus, Species, Subspecies
    - Collection data: Mus_registration (museum accession), Col_date (collection date)
    - Geography: Country, Label_locality (verbatim locality data)
    - Morphometrics: Bill_len, Bill_dep, Bill_wid, Tarsus, Wing, Tail (all in millimetres, with measurement methods)
    - Scanner: Abbreviation for scanner (MS = MechScan 3D Macro)
    - Notes: Additional scan quality notes and transcription notes
  - The Specimen_id field in metadata corresponds to the ply filename, enabling linkage between 3D geometry and associated descriptive data.

- How this data can be used in GIS
  - Import ply files as 3D point clouds or meshes for spatial and morphometric analyses.
  - Join ply data with Passerine_scan_metadata.csv on Specimen_id to enrich spatial analyses with taxonomy, locality, and measurement attributes.
  - Use Label_locality and Country for mapping specimen distribution and locality-level patterns (where georeferenced data exist or can be inferred).
  - Potential workflows include comparing beak morphology across taxa or geographic groups, integrating 3D morphology with existing GIS layers.

- Considerations and caveats for GIS use
  - Coordinate reference: Scans are in scanner space; georeferencing or transformation may be required before integration with other GIS layers.
  - Data provenance and quality: Visual QC performed; some scans may have holes or misalignments; no post-processing applied beyond initial alignment.
  - Metadata completeness: Some metadata fields may have missing values or partial entries; link via Specimen_id to maximize data usage.
  - Data organization: Data are distributed across ply geometry files and a separate metadata CSV; ensure consistent linking during integration.