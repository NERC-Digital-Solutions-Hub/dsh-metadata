Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

- Overview
  - Study of intercolony geographic distances for five Bombus species in a 1950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
  - Intercolony distances ranged from 7 to 5264 metres.
  - Data support understanding of bumblebee spatial structure for ecological monitoring and policy-relevant decision-making.

- Measures and data types relevant to monitoring
  - Spatial distances between colonies (Euclidean; metres) derived from worker foraging locations.
  - Colony locations inferred from genetic sibship analysis of workers (full-sib groups) and mean-centre spatial estimation, then snapped to nearby land-use/land-cover for habitat context.
  - Five species analyzed: Bombus terrestris (bter), B. lapidarius (blap), B. pascuorum (bpas), B. hortorum (bhor), B. ruderatus (brud).

- Data collection and generation methods
  - Non-lethal DNA sampling from workers (June–August 2011) across potential habitat patches in the study landscape.
  - Genetic assignment to colonies using COLONY v2.0 to group workers into full-sib families.
  - Worker locations recorded with GPS; colony coordinates derived by averaging worker locations per sibship and snapping to land-use features.

- Analytical approach
  - Map-based estimation of colony locations; include only colonies represented by two or more workers.
  - Compute all pairwise colony distances; report distances in metres.
  - Data-backed by land-use context to reflect potential nesting habitat.

- Data products and structure
  - Dataset: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv
  - Format: CSV with 48,423 rows, each row a pairwise distance between two colonies.
  - Key columns:
    - FROM_FID, FROM_Colony, FROM_X, FROM_Y
    - TO_FID, TO_Colony, TO_X, TO_Y
    - DISTANCE (metres)
    - species (four-letter codes: bter, blap, bpas, bhor, brud)

- Metadata, quality assurance, and governance
  - Quality statement: non-lethal sampling; standard protocols; spatial data produced in ArcGIS; backed up in Excel; data checks at CEH and Institute of Zoology.
  - Analyses peer-reviewed and published in Molecular Ecology.
  - Data storage and sharing: ArcGIS, Excel, CSV; submitted to EIDC; open data sharing can be a barrier in some contexts; explicit metadata is provided with dataset.
  - Data provenance and methods aligned with established standards (reference: Wang 2004 for sibship reconstruction).

- Relevance for monitoring frameworks
  - Demonstrates a robust workflow for deriving spatial ecological measures from genetic and GIS data, including:
    - Designing data collection to support policy-relevant metrics (intercolony distances).
    - Ensuring data quality through non-lethal sampling, QC checks, and peer-reviewed analyses.
    - Providing clear data products with comprehensive metadata and standardized formats (CSV with explicit column definitions).
    - Linking spatial measures to habitat context via land-use snapping.

- Limitations and considerations for replication
  - Data reflect a snapshot from 2011; temporal dynamics and landscape changes may affect applicability to current monitoring.
  - Colony location estimation depends on the quality and representativeness of worker sampling; colonies must have at least two workers represented.
  - Potential barriers to data sharing and metadata completeness require careful governance and documentation to enable reuse.

- Practical implications for policy and decision-making
  - Available as a high-resolution, policy-relevant metric of pollinator spatial structure that can inform habitat restoration, corridor design, and landscape planning.
  - Adds a replicable framework for integrating genetic, spatial, and land-use data to monitor pollinator populations across agricultural landscapes.