# Collection/generation methods

## Overview
- 3D surface scans of beaks from chaffinches (Fringilla coelebs) and other passerine birds.
- Specimens originate from the Natural History Museum, Tring, Hertfordshire.
- Scans saved as ply files; no post-processing performed.

## Data collection and generation
- Scanning performed with a calibrated MechScan macro structured light scanner.
- Alignment to be performed with FlexScan3D (Polyga).
- Aligned scans saved directly as ply files.

## Data characteristics
- Scans are calibrated; point distances recorded in millimetres.

## Quality control and provenance
- Visual quality control conducted to check for holes, misalignment, and missing regions.
- No subsequent post-processing of scans.

## Data structure and naming
- Each ply file is named Genus_species_subspecies_n.ply (e.g., Aimophila_ruficauda_acuminata_1.ply).
- Subspecies included in naming; numbers indicate multiple scans per group.
- Examples illustrate naming for both subspecies and species-only entries.

## Metadata and discovery
- Metadata file: Passerine_scan_metadata.csv.
- Key columns include:
  - Specimen_id (matches ply filename), Family, Genus, Species, Subspecies
  - Mus_registration (museum accession), Coll_date (collection date)
  - Country, Label_locality (verbatim locality data)
  - Sex, Bill_len, Bill_dep, Bill_wid, Tarsus, Wing, Tail (all measurements in mm)
  - Scanner (MS = MechScan 3D Macro)
  - Notes (scan quality and transcription notes)
- Metadata links specimens to ply files and provides taxonomic, collection, and morphometric context.

## Data quality and limitations
- Metadata may include incomplete fields (e.g., country backfill gaps, some entries truncated or with missing subspecies data).
- Notes indicate possible errors in transcription of specimen label data.

## Data management and stewardship
- Data format: 3D ply point clouds with millimetre precision.
- Minimal post-processing; primary linkage between ply files and metadata through specimen IDs.
- Emphasis on discoverability via comprehensive metadata and standardized naming.

## Practical considerations for Data Leaders
- Ensure consistent, scalable naming conventions and complete metadata to improve discoverability.
- Maintain data quality through ongoing visual QC and address transcription/label data gaps.
- Plan for data governance: clear provenance, linkage between raw scans and descriptive metadata, and appropriate access/usage policies.