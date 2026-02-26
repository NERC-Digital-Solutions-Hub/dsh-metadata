# Pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK

## Overview
- Dataset of pollinator species caught in pan traps across habitats with differing floral cover, collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Part of a larger experiment investigating the effect of floral resources on pollination services to isolated plants.
- Data collected and interpreted by Evans, T.M., with supporting documentation available.

## Experimental design
- Four blocks of 100 ha each, separated by more than 500 meters.
- In each block, four experimental arrays placed at 50 m intervals along a 150 m transect that spans florally rich and florally poor habitats.
- Each block contains two arrays in florally rich habitat and two in florally poor habitat.
- Experimental arrays comprise three Eschscholzia californica plants arranged in a triangle (1 m apart); pan traps placed at the center of each array.

## Collection and measurement methods
- Pan traps: three circular plastic bowls (80 x 200 mm) in yellow, blue, and white, filled with water and a drop of unscented washing liquid to break surface tension.
- Deployment: 24 hours per array, across 16 arrays, with four surveys total; surveys conducted twice weekly on randomised days between 0930 and 1700.
- Processing: after 24 hours, traps strained and sorted into taxonomic groups; main pollinator groups identified to species level (Hymenoptera Apoidea, Diptera Syrphidae, Lepidoptera).
- Measurements: intertegular span (distance between wing bases) measured in millimetres using digital calipers.

## Data structure and content
- File: Pantrap_catches_from_Buckinghamshire_UK.csv
- Variables/columns include:
  - Pollinator species (species-level identifications; 'None' if no pollinators recorded)
  - Intertegular span (mm; 'NA' if no pollinators recorded)
  - Block (identification number for each of four 100 ha blocks)
  - Experimental array (identification for each of the four arrays per block)
  - Habitat (location category: florally rich or poor)
  - Treatment (context of the array location)
  - Survey date (deployment date of pan traps)
  - Grid references for each array
- Data structure notes:
  - All data are contained in a single CSV file.
  - Where no pollinators were recorded on a date, Pollinator species = 'None' and Intertegular span = 'NA'.

## Quality control and provenance
- Field collections and identifications conducted by Evans, T.M., with expertise in pollinator identification and field ecology.
- Identifications subsequently checked by a recognized expert in bee identification.
- Dataset described as complete; data were collected and interpreted by the named researcher.
- Supporting documentation provided for context and replication.

## Standards, reuse, and governance considerations
- Clear metadata and a defined data schema (including units and missing data conventions) support discoverability and reuse.
- Data are organized to relate pollinator records to specific experimental arrays, habitats, and dates, aiding data governance, provenance tracking, and interoperability with related studies.
- Documentation indicates the dataset is suitable for analyses linking floral resource availability to pollinator activity and morphology, while flagging potential use alongside broader datasets from the same experiment.