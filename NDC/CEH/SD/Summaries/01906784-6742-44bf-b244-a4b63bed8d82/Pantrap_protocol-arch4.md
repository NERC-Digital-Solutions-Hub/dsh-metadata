# Pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK

## Overview
- Records pollinator species caught in pan traps across habitats with varying floral cover on the Hillesden estate, Buckinghamshire, collected in June 2015.
- Experimental design centers around four 100-hectare blocks, each with experimental arrays placed to compare florally rich and florally poor habitats.
- For each survey, data include counts of main pollinator groups (Hymenoptera: Apoidea, Diptera: Syrphidae, Lepidoptera) and intertegular span (IT span) measurements.

## Experimental design
- Four replicate blocks (each 100 ha) separated by more than 500 meters.
- At each block centre, four experimental arrays placed along a 150 m transect (two arrays in florally rich habitat, two in florally poor habitat).
- Each array contains three Eschscholzia californica plants arranged in a triangle, 1 m apart.
- Pan traps are placed at the center of each array to assess pollinator activity density relative to floral resources.
- Surveys: 16 arrays total per survey, conducted twice weekly over 16 days (four surveys total) in random order, between 09:30 and 17:00.

## Collection methods
- Pan traps: three circular bowls (80 x 200 mm) with non-toxic fluorescent paint (yellow, blue, white); filled with water and a drop of unfragranced washing liquid.
- Traps deployed for 24 hours per array; 16 arrays per survey; two surveys per week across 16 days.
- After 24 hours, traps were strained, and insects from the main pollinator groups were counted and identified to species level under a dissecting microscope.
- Intertegular span measured for each pollinator using digital calipers.

## Quality control
- Field collections and identifications conducted by Evans, T.M., trained in pollinator identification and field ecology.
- Identifications checked by a recognised bee identification expert.

## Data structure and units
- Data stored in a single CSV: Pantrap_catches_from_Buckinghamshire_UK.csv.
- Grid references recorded for each array; IT span in millimetres.
- Missing data handling: if no pollinators recorded on a survey date, Pollinator species = None and Intertegular span = NA.
- Key columns include: Block, Experimental array, Habitat, Treatment, Survey date.
- Data fields include Pollinator species and Intertegular span, with location-based and experimental context metadata.

## Provenance and context
- Part of a larger experiment examining the effect of floral resources on pollination services to isolated plants.
- Data collected and interpreted by Evans, T.M.; supporting documentation available under “Pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK.”

## Potential uses and relevance for data leadership
- Demonstrates end-to-end data lifecycle: experimental design, field collection, taxonomic identification, trait measurement, QA, and structured metadata.
- Provides a well-described dataset with clear units, placement context, and repeatable survey methodology, useful for data governance, stewardship, and cross-dataset integration.
- Can inform organizational data strategy on capturing habitat context, species-level data, and functional traits (IT span) for biodiversity monitoring.
- Highlights importance of metadata completeness (grid references, block/array identifiers, habitat/treatment, survey dates) to enable discoverability and re-use across networks.