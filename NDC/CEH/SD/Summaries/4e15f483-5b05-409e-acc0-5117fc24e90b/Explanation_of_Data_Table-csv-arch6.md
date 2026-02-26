# Explanation of column headings in Data_Table.csv

## Overview
- Defines the meaning and derivation of each column in Data_Table.csv, focusing on taxonomic identification, brain metrics, and floccular fossa morphology.

## Column-by-column descriptions

- **A. Order**
  - Taxonomic order to which each avian species belongs.

- **B/C. Genus and species**
  - Generic and specific (Linnaean) names for each avian taxon.

- **D: BCEV (mm3)**
  - Brain Cavity Endocranial Volume in cubic millimetres.
  - Derived from voxel segmentation of the entire brain cavity space.

- **E: FFV (mm3)**
  - Floccular Fossa Volume in cubic millimetres.
  - Derived from voxel segmentation of the bony pocket housing the cerebellar flocculus; left and right values are summed.

- **F: %BCEV**
  - Percentage of the brain cavity volume represented by the total floccular fossa volume.
  - Calculated as (FFV / BCEV) × 100.

- **G: Fossa Type**
  - Flocculus fossa morphology coded as Type 1 to 5.
  - Morphology is influenced by vascular occupancy (primarily the floccular artery loop), the proximal fossa region, elongation, and rostrocaudal compression.

## Fossa Type definitions (Types 1–5)

- **Type 1**
  - Arterial loop enclosed within the fossa; no impression on fossa walls.
  - Fossa is dome-shaped with a single foramen exiting distally.

- **Type 2**
  - Arterial loop enclosed within the fossa; dome-shaped base tapering into a rostrocaudally compressed region.
  - Fossa elongated or truncated; distal portion tapers to a single distal foramen.

- **Type 3**
  - Arterial loop enclosed within the fossa; base not markedly domed and shows little torsion.
  - Main section elongates and is approximately circular, tapering to a single distal foramen or widening to a blunt distal end.

- **Type 4**
  - Arterial loop not enclosed within the fossa; rostral and caudal arteries exit the tapered distal extent.
  - Distally converges to form a 'paperclip' shape with a single smaller distal foramen.

- **Type 5**
  - Arterial loop leaves a distinct trace on the fossa surface.
  - Lacks the twisted base of Types 2 and 4 but is rostrocaudally compressed.
  - A bone sheet between arterial traces can create a 'fenestra' in the endocast.
  - Variability in arterial sulci or foramina may obscure the distal extent of floccular occupancy.

## Derived metrics and interpretation
- **Key derived metric:** %BCEV (FFV relative to BCEV) to compare relative floccular occupancy across species.
- **Data interpretation notes:** Morphology (Type 1–5) reflects vascular and structural variation in the floccular fossa, which may influence functional inferences drawn from the endocast data.