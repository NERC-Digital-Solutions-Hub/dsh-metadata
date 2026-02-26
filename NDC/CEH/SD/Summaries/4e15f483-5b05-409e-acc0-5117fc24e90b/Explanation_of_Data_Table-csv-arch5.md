# Explanation of column headings in Data_Table.csv

- Purpose of document
  - Defines the meaning and data processing for each column in Data_Table.csv, enabling consistent interpretation, quality control, and reuse.

- Column A: Order
  - Taxonomic order to which each avian species belongs.

- Columns B/C: Genus and species
  - Generic and specific (Linnaean) names for each avian taxon.

- Column D: BCEV (mm3)
  - Brain Cavity Endocranial Volume measured in cubic millimetres.
  - Derived from voxel segmentation of the whole brain cavity space.

- Column E: FFV (mm3)
  - Floccular Fossa Volume measured in cubic millimetres.
  - Derived from voxel segmentation of the bony pocket housing the cerebellar flocculus.
  - Values for the left and right flocculi are summed to obtain the total FFV.

- Column F: %BCEV
  - Percentage of the whole brain cavity volume represented by the total flocculus fossa volume.
  - Calculated as (FFV / BCEV) × 100.

- Column G: Fossa Type
  - Flocculus fossa morphology coded as Type 1 to 5.
  - Morphology is strongly influenced by vascular occupancy (mainly the floccular artery loop), base shape, elongation, and rostrocaudal compression.
  - Type 1: Arterial loop enclosed within fossa; fossa dome-shaped; single distal foramen; walls show no vascular impressions.
  - Type 2: Arterial loop enclosed; dome-shaped base, rostrocaudally compressed region; elongated or truncated; distal foramen exits distally.
  - Type 3: Arterial loop enclosed with non-domed base; elongate main section; approximately circular cross-section; distal foramen exits distally or distal end widens to bulbous end.
  - Type 4: Arterial loop not enclosed; arteries exit distal extent; forms a paperclip shape with a single distal foramen.
  - Type 5: Arterial loop leaves distinct surface trace; lacks twisted base of Types 2 and 4; often a bone sheet between traces causing a fenestra; variability may obscure distal occupancy.

- Data lineage and processing notes (implied)
  - BCEV and FFV are derived from voxel segmentation, ensuring a standardized approach to volume measurement.
  - FFV is obtained by summing left and right measurements, then used to compute %BCEV.
  - Fossa Type is a qualitative morphology code with detailed criteria that reflect vascular and anatomical variation.

- Data governance implications for Data Stewards
  - Metadata needs to capture measurement methods, voxel segmentation protocol, and any software/tools used.
  - Maintain unit consistency (all volumes in mm3) and document how derived fields are calculated.
  - Record provenance for each row (taxon, genus/species, and associated measurements) to support reproducibility.
  - Document any limitations or potential ambiguities in morphology coding (Types 1–5) to aid data discovery and reuse.
  - Ensure clear handling of left/right FFV summation and transparency of any data exclusions or quality flags.