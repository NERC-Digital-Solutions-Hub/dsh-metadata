# Explanation of column headings in Data_Table.csv

- Column A: Order – Taxonomic order to which each avian species belongs.
- Column B/C: Genus and species – Linnaean genus and species names for each avian taxon.
- Column D: BCEV (mm3) – Brain Cavity Endocranial Volume, measured in cubic millimetres; derived from voxel segmentation of the whole brain cavity space.
- Column E: FFV (mm3) – Floccular Fossa Volume, measured in cubic millimetres; derived from voxel segmentation of the bony pocket housing the cerebellar flocculus; values for left and right flocculi are summed.
- Column F: %BCEV – Percentage of the brain cavity volume represented by the total flocculus fossa volume (FFV/BCEV × 100).
- Column G: Fossa Type – Morphology of the flocculus fossa coded as Type 1 to Type 5; morphology reflects vascular occupancy and structural features, with the following types:
  - Type 1: Arterial loop enclosed within fossa; fossa dome-shaped; no vascular impressions on walls; single distal foramen.
  - Type 2: Arterial loop enclosed; dome-shaped base; rostrocaudal compression with partial spiral; elongated or truncated; single distal foramen.
  - Type 3: Arterial loop enclosed; base not domed; elongated, approximately circular; single distal foramen or blunt distal end.
  - Type 4: Arterial loop not enclosed; arteries exit distal extent forming a “paperclip” shape; single distal foramen.
  - Type 5: Arterial loop leaves distinct surface traces; lacks twisted base of Types 2 and 4; may have a fenestra caused by a bone sheet; variability in arterial sulci/foramina can obscure distal occupancy.

- Additional context for interpretation:
  - Column D and E are measured volumes (mm3) derived from imaging/segmentation methods.
  - Column F provides a derived proportion to compare brain and floccular fossa investment across taxa.
  - Column G encodes a qualitative morphology class that can inform vascular and endocast interpretation, with implications for cross-study comparability and metadata needs.