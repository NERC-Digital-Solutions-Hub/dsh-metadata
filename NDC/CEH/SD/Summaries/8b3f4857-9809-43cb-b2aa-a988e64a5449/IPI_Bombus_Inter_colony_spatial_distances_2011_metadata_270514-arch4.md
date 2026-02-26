# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

## Aim and scope
- Investigates geographic distances between intercolony pairs of five Bombus species across a 1950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Colonies are inferred from foraging worker samples genotyped and grouped into full-sib families.

## Data collected and methods
- Timeframe and location: June–August 2011; Hillesden Estate area, Southern England, UK.
- Species: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Sampling and processing:
  - Non-lethal DNA sampling from worker bees; tarsal tips removed and preserved in ethanol.
  - Genotyped and individuals assigned to full-sib groups (colonies) using COLONY v2.0.
- Geolocation and colony estimation:
  - Worker locations recorded with GPS.
  - Colony locations estimated as the mean center of workers within each sibship.
  - Mean centers snapped to the nearest land-use/land-cover class relevant for nesting habitat.
  - Colony locations only estimated for groups represented by two or more workers.
- Distances:
  - Euclidean distances calculated between all colony pairs, expressed in metres.

## Data structure and file details
- Data platform: ArcGIS for mapping; results stored in Excel; exported to CSV.
- Data file: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv
  - Format: CSV with 48,423 rows, each row a pairwise distance between two colonies.
- Key columns:
  - FROM_FID, FROM_Colony, FROM_X, FROM_Y
  - DISTANCE
  - TO_FID, TO_Colony, TO_X, TO_Y
  - species (codes: bter, blap, bpas, bhor, brud)
- Species codes:
  - bter = Bombus terrestris
  - blap = B. lapidarius
  - bpas = B. pascuorum
  - bhor = B. hortorum
  - brud = B. ruderatus

## Data quality, provenance, and governance
- Quality control: non-lethal sampling, storage, DNA extraction, genotyping, and colony assignment performed using recognised standard protocols; data checked at CEH and Institute of Zoology.
- Analytical validation: analyses peer reviewed and accepted for publication in Molecular Ecology.
- Provenance and backups: spatial locations stored in ArcGIS; backed up as Excel files; final dataset archived as CSV in EIDC.

## Context, usage, and relevance for data leadership
- Provides a structured, traceable dataset linking genetic data to spatial colony positions and intercolony distances.
- Supports studies on spatial structure, pollinator movement, and landscape connectivity within an agricultural landscape.
- Demonstrates data lifecycle: field collection, genetic analysis, geospatial processing, distance calculations, and formal data archiving with metadata and QA.

## Limitations and caveats
- Colony estimates are limited to sibships represented by two or more workers.
- Distances are Euclidean and do not account for potential landscape barriers beyond land-use snapping.
- Data are presented as pairwise distances across colonies within the studied landscape and time frame (2011).

## Reference to standard methods
- Wang J (2004) Sibship reconstruction from genetic data with typing errors. Genetics, 166, 1963-1979.