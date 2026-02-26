# Explanation of column headings in Data_Table.csv

## Overview
- Provides definitions for each column in Data_Table.csv, including measurements, derived metrics, and morphology coding related to avian brain anatomy.

## Column definitions
- Column A: Order
  - Taxonomic order to which each avian species belongs.
- Column B/C: Genus and species
  - Generic and specific (Linnaean) scientific names for each taxon.
- Column D: BCEV (mm3)
  - Brain Cavity Endocranial Volume, measured in cubic millimetres; derived from voxel segmentation of the whole brain cavity space.
- Column E: FFV (mm3)
  - Floccular Fossa Volume, measured in cubic millimetres; derived from voxel segmentation of the bony pocket housing the cerebellar flocculus; values for left and right flocculi are summed.
- Column F: %BCEV
  - Percentage of the brain cavity volume represented by the floccular fossa volume: (FFV/BCEV) × 100.
- Column G: Fossa Type
  - Flocculus fossa morphology coded as Type 1 to Type 5. Classification reflects how the arterial loop occupancy and skull morphology shape the fossa.

## Fossa Type details
- Type 1
  - Arterial loop fully enclosed within fossa; fossa dome-shaped with a single distal foramen; walls show no vascular impressions.
- Type 2
  - Arterial loop enclosed; dome-shaped base, distally tapering into a rostrocaudally compressed region with partial spiral; elongated or truncated fossa with a single distal foramen.
- Type 3
  - Arterial loop enclosed; base not domed or twisted; main section elongated and approximately circular, tapering to a distal foramen (or a blunt distal end).
- Type 4
  - Arterial loop not enclosed; rostral and caudal arteries exit the distal fossa, converging to form a “paperclip” shape with a single distal foramen.
- Type 5
  - Arterial loop leaves a distinct surface trace; lacks the twisted base of Types 2 and 4 but is rostrocaudally compressed; a bone sheet between arterial traces can create a fenestra in the fossa endocast; variability in arterial features may obscure distal occupancy of the flocculus.

## Measurement methods and data provenance
- BCEV and FFV are derived from voxel segmentation:
  - BCEV: total brain cavity volume.
  - FFV: volume of the floccular fossa; left and right values summed to produce the total FFV.
- FFV as a proportion of brain cavity is captured by %BCEV, enabling cross-species comparisons independent of absolute brain size.

## Notes for analysis
- FFV is a derived metric; ensure consistent voxel segmentation methodology when comparing across datasets or studies.
- The Fossa Type coding reflects morphological variation tied to vascular occupancy and skull structure; interpretations should consider potential variability in arterial anatomy.
- Data might include scale-related considerations and potential measurement uncertainty inherent in imaging-based segmentation.