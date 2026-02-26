# Collection/generation methods

- 3D surface scans of beaks from chaffinches (Fringilla coelebs) and other passerine birds; specimens sourced from the Natural History Museum, Tring, Hertfordshire.
- Scanning performed with a calibrated MechScan macro structured light scanner; alignment done in FlexScan3D; outputs saved as ply files with no post-processing.

## Nature and units of recorded values

- Scans are calibrated files; distances between points are recorded in millimetres.

## Quality control

- Scans visually inspected for holes, misalignment, and missing regions.
- No post-processing applied after alignment.

## Details of data structure

- Each scan file named by genus, species, subspecies, and a scan number: Genus_species_subspecies_n.ply.
  - Examples: Aimophila_ruficauda_acuminata_1.ply; Anthus_godlewskii_2.ply.
- Subspecies names included; numbers indicate multiple scans per taxon (e.g., various entries for a single taxon across multiple scans).

## Metadata and data columns (Passerine_scan_metadata.csv)

- Specimen_id and Description metadata map to the ply filename; taxonomic fields include Family, Genus, Species, Subspecies.
- Mus_registration and Coll_date capture museum accession and collection date.
- Location data: Country (to be backfilled from Label_locality) and Label_locality (verbatim locality).
- Sex of specimen (male, female, or unsexed).
- Morphometrics (in millimetres) with measurement precision:
  - Bill_len, Bill_dep, Bill_wid; Tarsus; Wing; Tail (Wing and Tail with precision to 1 mm; others to 0.01 mm in some cases).
- Scanner field indicates the scanner used (MS = MechScan 3D Macro structured white light scanner).
- Notes field records scan quality notes and potential transcription errors.

## Purpose and applicability

- The ply files provide detailed 3D beak morphology for cross-taxa analyses.
- Metadata enables filtering by taxon, subspecies, sex, and morphometrics; supports analyses of morphology-geography relationships and data provenance.
- Dataset designed to facilitate data discovery, visualization, and self-serve data exploration across researchers and institutions.