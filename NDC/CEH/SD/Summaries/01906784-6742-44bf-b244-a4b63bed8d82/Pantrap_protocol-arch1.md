# Pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK

## Overview
- A dataset listing pollinator species captured in pan traps across habitats with varying floral cover.
- Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Part of a larger experiment examining how floral resources influence pollination services to isolated plants.
- The dataset is complete and was collected and interpreted by Evans, T.M.

## Experimental design
- Four replicate blocks, each 100 hectares, separated by more than 500 meters.
- Within each block, four experimental arrays placed at 50 m intervals along a 150 m transect crossing the boundary between a florally rich wildflower patch and bare fallow ground.
- In each block, two arrays in florally rich habitat and two in florally poor habitat.
- Each experimental array contains three Eschscholzia californica plants arranged in a triangular formation, 1 meter apart.
- Pan traps located at the center of each array to measure pollinator activity density in relation to floral resources.
- Total of 16 arrays (4 blocks × 4 arrays).

## Collection methods
- Pan traps: three circular bowls (80 x 200 mm) with non-toxic fluorescent paint (yellow, blue, white).
- Bowls filled with water and a drop of washing-up liquid to reduce surface tension.
- Traps deployed for 24 hours at each of the 16 arrays; conducted twice weekly over a 16-day study period (four surveys in total).
- Surveys performed in random order, between 09:30 and 17:00.
- After 24 hours, traps were filtered, sorted into taxonomic groups, and main pollinator groups (Hymenoptera: Apoidea, Diptera: Syrphidae, Lepidoptera) identified to species level.
- Intertegular span (distance between wing bases) measured for each insect in the main pollinator groups using digital calipers.

## Data structure and units
- All data stored in a single CSV file: Pantrap_catches_from_Buckinghamshire_UK.csv.
- Grid references recorded for each experimental array.
- Intertegular span measured in millimetres.
- Missing data handling: if no pollinators observed on a survey date, Pollinator species = 'None' and Intertegular span = 'NA'.
- Key identifiers: Block (replicate block ID), Experimental array (array ID within block), Habitat, Treatment, Survey date.

## Quality control
- Field collections and identifications conducted by Evans, T.M., trained in pollinator identification.
- Identifications checked by an expert in bee identification.

## Usage context and metadata
- Dataset linked to supporting documentation on pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK.
- Data structure includes survey dates and locations across blocks and arrays, enabling analysis of pollinator abundance and body size (intertegular span) relative to floral resource availability.