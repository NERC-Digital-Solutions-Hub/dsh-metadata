# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

## Overview
- Study of intercolony geographic distances among five Bombus species across a 1950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Location data and colony-level spatial structure derived from genotyped worker foraging locations sampled in summer 2011.
- Species studied: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Outputs include a comprehensive distance dataset used for ecological and spatial analyses; data collected under the Insect Pollinators Initiative.

## Data collection and sampling
- Non-lethal DNA sampling from worker bees across habitat patches (June–August 2011).
- Workers sampled/populations genotyped to assign individuals to full-sib groups (colonies) using COLONY v2.0.
- Only colonies represented by two or more workers included in analyses.
- GPS used to record precise worker locations; sampling encompassed all potential habitat patches within the landscape.

## Spatial estimation and colony localization
- Colony locations estimated per sibship by calculating the mean Easting/Northing of all workers within the sibship.
- Estimated colony coordinates were snapped to the nearest land-use/land-cover class that could serve as nesting habitat.
- Spatial analyses conducted in ArcGIS; Euclidean distances calculated between all colony pairs.

## Data structure and units
- Distances are reported in metres (m).
- Colony pairs derived from all colonies with at least two workers; intercolony distances range from 7 to 5264 m.

## Data processing, formats, and file details
- Data generated in ArcGIS, stored in Excel, and shared as a CSV file via EIDC.
- CSV file: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv
- 48,423 rows, each detailing a pairwise distance between two colonies.
- Key columns:
  - FROM_FID, FROM_Colony, FROM_X, FROM_Y
  - DISTANCE
  - TO_FID, TO_Colony, TO_X, TO_Y
  - species (four-letter codes)
- Species codes:
  - bter = Bombus terrestris
  - blap = B. lapidarius
  - bpas = B. pascuorum
  - bhor = B. hortorum
  - brud = B. ruderatus

## Experimental design and methods
- Landscape: 1950 ha in southern England, centered on Hillesden Estate (grid coordinates provided).
- Foraging worker locations mapped to land-use context; colony locations inferred from mean-centroid approach and habitat snapping.
- Data analysis supported by ArcGIS for spatial mapping and Euclidean distance calculations.

## Quality assurance and provenance
- Non-lethal sampling, storage, and DNA extraction followed recognized standard protocols.
- Locations and distances validated by staff at the Centre for Ecology and Hydrology and the Institute of Zoology.
- Analyses and results peer reviewed and published in Molecular Ecology.

## Data use and accessibility
- Dataset enables examination of spatial structure and intercolony distances across Bombus species in an agricultural landscape.
- Suitable for studies on colony dispersal, foraging ecology, and landscape connectivity; data shared in a standardized CSV format for reuse.