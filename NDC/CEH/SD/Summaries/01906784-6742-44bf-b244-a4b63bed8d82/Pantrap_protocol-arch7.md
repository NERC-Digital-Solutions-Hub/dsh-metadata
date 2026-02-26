# Pollinator data from pan traps located in habitats comprising different floral cover in Buckinghamshire, UK

- What the dataset contains
  - A list of pollinator species caught in pan traps, across habitats with different floral cover, collected at the Hillesden estate, Buckinghamshire, UK in June 2015.
  - Experimental context: four 100ha blocks with floral-rich and floral-poor habitats; four pan-trap arrays per block containing Eschscholzia californica plants.
  - Pan traps deployed in the center of each experimental array and sampled over four 24-hour surveys (twice weekly across 16 days).
  - Insects from main pollinator groups (Hymenoptera Apoidea, Diptera Syrphidae, Lepidoptera) identified to species; intertegular span measured for individuals.

- Experimental design and study area
  - Four 100ha blocks, each separated by more than 500 meters.
  - Within each block, four experimental arrays placed at 50-meter intervals along a 150-meter transect across a boundary between a florally rich wildflower patch and bare, fallow ground (two arrays in each habitat type per block).
  - Each array contains three E. californica plants arranged in a triangle; pan traps centered on the array.
  - Spatial references (grid references) captured for each array.

- Collection methods and timing
  - Pan traps: three circular plastic bowls (80 x 200 mm) with non-toxic fluorescent paint (yellow, blue, white), filled with water and a drop of washing liquid.
  - Deployment: 24 hours per array, across 16 arrays, with four surveys total; surveys conducted in randomised order between 09:30 and 17:00.
  - Post-collection: specimens sorted into taxonomic groups; main pollinator groups identified to species level; intertegular span measured with digital calipers.

- Data structure and units
  - Single CSV file: Pantrap_catches_from_Buckinghamshire_UK.csv.
  - Key fields: Block, Experimental array, Habitat, Treatment, Survey date, Pollinator species, Intertegular span.
  - Grid references recorded for each array; Intertegular span in millimetres.
  - Data encoding conventions: if no pollinators recorded on a survey date, Pollinator species = "None" and Intertegular span = "NA" (not applicable).

- Data quality control
  - Field collection and identifications conducted by Evans, T.M., with identification checks by an expert in bee identification.

- Temporal and contextual scope
  - Data collected in June 2015.
  - Part of a larger experiment examining the effect of floral resources on pollination services to isolated plants.

- Relevance for GIS and data analysis
  - Geolocated data at the level of experimental arrays within blocks, enabling spatial analysis of pollinator activity relative to floral resource availability.
  - Suitable for creating maps of species occurrences, abundance, and morphometrics (intertegular span) across habitat types and over time.
  - Can be integrated with habitat maps, land-cover layers, or floral resource datasets to assess spatial patterns and drivers of pollinator visitation.