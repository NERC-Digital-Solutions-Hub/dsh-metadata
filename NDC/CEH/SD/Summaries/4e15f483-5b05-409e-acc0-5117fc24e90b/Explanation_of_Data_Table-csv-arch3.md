# Explanation of column headings in Data_Table.csv

- Column A: Order
  - Taxonomic order to which each avian species belongs.

- Columns B/C: Genus and species
  - Generic and specific (Linnaean) names for each avian taxon.

- Column D: BCEV (mm3)
  - Brain Cavity Endocranial Volume measured in cubic millimetres.
  - Derived from voxel segmentation of the whole brain cavity space.

- Column E: FFV (mm3)
  - Floccular Fossa Volume measured in cubic millimetres.
  - Derived from voxel segmentation of the bony pocket in the brain cavity that houses the cerebellar flocculus.
  - Values for the left and right flocculi are summed to obtain these values.

- Column F: %BCEV
  - Percentage value of the whole brain cavity volume represented by the total flocculus fossa volume: (FFV/BCEV) × 100.

- Column G: Fossa Type
  - Flocculus fossa morphology coded as Type 1 to 5.
  - Morphology is strongly determined by vascular occupancy (mainly the loop of the floccular artery), shape of the proximal region of the fossa, elongation, and rostrocaudal compression.
  - Type 1: Arterial loop enclosed within fossa; fossa dome-shaped with a single distal foramen; walls show no vascular impressions.
  - Type 2: Arterial loop enclosed; dome-shaped base, rostrocaudally compressed region that twists into a partial spiral; fossa elongate or truncated with a single distal foramen.
  - Type 3: Arterial loop enclosed; base not markedly domed, minimal torsion; elongated main section, tapering to a single distal foramen or a blunt distal end.
  - Type 4: Arterial loop not enclosed; arteries exit the fossa and converge distally into a paperclip shape with a single distal foramen.
  - Type 5: Arterial loop leaves a distinct surface trace; lacks twisted base of Types 2 and 4 but is rostrocaudally compressed; a bone sheet may create a fenestra in the endocast; variability in arterial traces or foramina can obscure the distal extent of neural flocculus occupancy.