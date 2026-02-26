# Explanation of column headings in Data_Table.csv

- Overview
  - Defines the meaning of each column in Data_Table.csv, focusing on avian taxonomy, brain measurements, derived metrics, and morphological classification of the flocculus fossa.
  - Measurements are derived from voxel segmentation of brain anatomy and standardized for comparison.

- Column-by-column description
  - Column A: Order
    - Taxonomic order to which each avian species belongs.
  - Columns B/C: Genus and species
    - Linnaean genus and species names for each avian taxon.
  - Column D: BCEV (mm3)
    - Brain Cavity Endocranial Volume measured in cubic millimetres.
    - Derived from voxel segmentation of the whole brain cavity space.
  - Column E: FFV (mm3)
    - Floccular Fossa Volume measured in cubic millimetres.
    - Derived from voxel segmentation of the bony pocket in the brain cavity that houses the cerebellar flocculus.
    - Values for left and right flocculi are summed to obtain FFV.
  - Column F: %BCEV
    - Percentage of the brain cavity volume represented by FFV.
    - Calculated as (FFV / BCEV) × 100.
  - Column G: Fossa Type
    - Flocculus fossa morphology coded as Type 1 to 5.
    - Morphology is influenced by vascular occupancy and structural features of the fossa.

- Fossa Type (Types 1–5) detailed meanings
  - Type 1
    - Arterial loop enclosed within fossa; no impression on walls.
    - Fossa dome-shaped with a single distal foramen.
  - Type 2
    - Arterial loop enclosed; base dome-shaped, tapering distally with rostrocaudal compression.
    - Fossa elongate or truncated; distal portion tapers to a single distal foramen.
  - Type 3
    - Arterial loop enclosed; base not domed with no torsion.
    - Main section elongate, approximately circular; tapers to a distal foramen or widens to a blunt distal end.
  - Type 4
    - Arterial loop not enclosed; rostral and caudal arteries exit distal fossa, forming a “paperclip” shape with a single distal foramen.
  - Type 5
    - Arterial loop leaves a distinct surface trace; lacks twisted base of Types 2 and 4.
    - A bone sheet may create a fenestra in the endocast; variability in arterial sulci/foramina may obscure distal occupancy.

- Data processing and quality notes
  - FFV values are obtained via voxel segmentation and summed across left and right floccular fossae.
  - BCEV is used as the reference brain cavity volume for calculating %BCEV.
  - Fossa Type classifications reflect morphological variation influenced by vascular occupancy and structural geometry.

- Practical relevance for environmental analysis
  - Enables standardized comparison of avian neuroanatomy across species, suitable for monitoring environmental effects on brain morphology.
  - Facilitates data integration and cross-study analyses through consistent column definitions and derived metrics (FFV, %BCEV, Fossa Type).