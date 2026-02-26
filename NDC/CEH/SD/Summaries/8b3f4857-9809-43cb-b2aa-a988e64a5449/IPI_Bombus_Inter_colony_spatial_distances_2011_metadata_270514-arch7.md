# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

## Overview
- Study of geographic distances between all pairs of wild bumblebee colonies across a 1950 ha agricultural landscape around the Hillesden Estate, Buckinghamshire, UK.
- Five Bombus species examined: B. terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Inter-colony distances range from 7 to 5264 metres.
- Data generated as part of the Insect Pollinators Initiative, led by the Centre for Ecology and Hydrology.

## GIS workflow and data processing
- Worker locations recorded with GPS; non-lethal DNA sampling from workers (June–August 2011).
- Workers genotyped and assigned to full-sib groups (colonies) using COLONY v.2.0.
- Colony locations estimated per sibship by computing the mean centre of worker coordinates, then snapping to the nearest land-use/land-cover class representing potential nesting habitat.
- Only colonies represented by two or more workers were included.
- Geographic (Euclidean) distances calculated between all possible colony pairs.

## Data creation and structure
- Spatial data were mapped in ArcGIS; results stored as Excel files and as a CSV file for sharing.
- Main data file: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv, with 48,423 rows.
- Key fields (examples):
  - FROM_FID, FROM_Colony, FROM_X, FROM_Y
  - TO_FID, TO_Colony, TO_X, TO_Y
  - DISTANCE (in metres)
  - species (four-letter codes)
- Units: distances in metres; colony coordinates in OS Easting/Northing.
- Data file structure is designed to enable pairwise distance analysis across colonies.

## Experimental design and scope
- Area details: 1,950 hectares centered on the Hillesden Estate, Buckinghamshire (UK); coordinates 1°00'01"W, 51°57'16"N.
- Sampling window: June–August 2011.
- Data generation method: ArcGIS-based mapping, mean-centre colony estimation, and snapping to land-use classes.

## Data quality and provenance
- DNA sampling followed recognized standard protocols; non-lethal collection with proper storage and handling.
- QA performed at multiple stages by the Centre for Ecology and Hydrology and the Institute of Zoology.
- Analyses based on these data have undergone peer review and were accepted for publication in Molecular Ecology.

## Species coding
- Four-letter species codes used in the dataset:
  - bter = Bombus terrestris
  - blap = B. lapidarius
  - bpas = B. pascuorum
  - bhor = B. hortorum
  - brud = B. ruderatus

## Additional context and references
- The data are linked to standard methods for sibship reconstruction from genetic data (Wang 2004) and are part of a broader project examining pollinator spatial structure in agricultural landscapes.