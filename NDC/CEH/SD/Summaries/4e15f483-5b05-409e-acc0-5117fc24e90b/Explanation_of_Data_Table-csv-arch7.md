# Explanation of column headings in Data_Table.csv

- Overview
  - Defines the attributes used in a CSV table of avian species brain anatomy, including taxonomic information, volumetric measurements, derived metrics, and morphological classification of the floccular fossa.
  - Units and derivations are specified to support data cleaning, joining with GIS datasets, and map-based analyses.

- Column A: Order
  - Taxonomic order to which each avian species belongs.

- Column B/C: Genus and species
  - Generic and specific (Linnaean) names for each avian taxon.

- Column D: BCEV (mm3)
  - Brain Cavity Endocranial Volume, measured in cubic millimetres.
  - Derived from voxel segmentation of the whole brain cavity space.

- Column E: FFV (mm3)
  - Floccular Fossa Volume, measured in cubic millimetres.
  - Derived from voxel segmentation of the bony pocket in the brain cavity that houses the cerebellar flocculus.
  - Values for the left and right flocculi are summed to obtain these values.

- Column F: %BCEV
  - Percentage of the whole brain cavity volume represented by the total flocculus fossa volume.
  - Calculated as (FFV / BCEV) × 100.

- Column G: Fossa Type
  - Flocculus fossa morphology coded as Type 1 to 5.
  - Morphology is strongly determined by vascular occupancy (mainly the loop of the floccular artery), shape of the proximal region of the fossa, elongation of the fossa, and degree of rostrocaudal compression.
  - Type 1: Arterial loop enclosed within fossa; no impression on fossa walls; dome-shaped with a single distal foramen.
  - Type 2: Arterial loop enclosed within fossa; dome-shaped base, rostrocaudally compressed region forming a partial spiral; elongated or truncated fossa; distal portion tapers to a single distal foramen.
  - Type 3: Arterial loop enclosed within fossa; base not strongly domed or twisted; main section elongated and approximately circular; tapers to a distal foramen or widens to a blunt distal end.
  - Type 4: Arterial loop not enclosed within fossa; rostral and caudal arteries exit the distal extent, forming a paperclip shape with a single smaller distal foramen.
  - Type 5: Arterial loop leaves a distinct trace on the fossa surface; lacks twisted base of Types 2 and 4 but is rostrocaudally compressed; a bone sheet may create a fenestra, and variability in arterial sulci/foramina may obscure the distal extent of floccular occupancy.