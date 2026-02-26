# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

- Objective and scope
  - Study the spatial structure of five Bombus species by estimating intercolony distances across an agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
  - Reported intercolony distances range from 7 to 5264 metres.
  - Landscape area: ~1950 hectares; sampling conducted in 2011 (June–August).

- Species examined
  - Bombus terrestris (bter)
  - Bombus lapidarius (blap)
  - Bombus pascuorum (bpas)
  - Bombus hortorum (bhor)
  - Bombus ruderatus (brud)

- Methods: data collection and colony assignment
  - Non-lethal DNA sampling from worker bees; tarsal tip removed and preserved in 100% ethanol for DNA extraction.
  - Workers genotyped and assigned to full-sib groups (colonies) using COLONY v.2.0.
  - Worker geographic locations recorded with GPS.

- Location estimation and processing
  - Colony locations estimated as the mean Centre of all workers within each sibship.
  - Mean-centre locations snapped to the nearest land-use/land-cover class to reflect likely nesting habitat.
  - Only colonies represented by two or more workers were included.

- Distance calculation and data scope
  - Euclidean (geographic) distances calculated between all possible pairs of colonies (with two or more workers).
  - Distances are presented in metres.

- Data output and structure
  - Data stored in ArcGIS and exported to Excel; also submitted to EIDC as a CSV file.
  - File: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv
  - Columns include:
    - FROM_FID, FROM_Colony, FROM_X, FROM_Y
    - DISTANCE
    - TO_FID, TO_Colony, TO_X, TO_Y
    - species ( Bombus species code)
  - Total rows: 48,423 rows, each representing a pairwise inter-colony distance.

- Data quality and validation
  - Non-lethal sampling, proper storage, and DNA handling followed standard protocols.
  - Spatial data and colony assignments checked by staff at the Centre for Ecology and Hydrology and the Institute of Zoology.
  - Analyses reviewed and accepted for publication in Molecular Ecology.

- Experimental design and sampling regime
  - Landscape: 1950 ha agricultural area around Hillesden Estate, Southern England (coordinates provided in the study).
  - Sampling window: June–August 2011.
  - Habitat patches surveyed to cover potential foraging and nesting habitats across the landscape.

- Data accessibility and metadata
  - Location data, colony assignments, and pairwise distances backed up in Excel and CSV formats.
  - Metadata and dataset accessibility ensured via standard data management practices and portals (EIDC) with explicit column definitions and species codes.

- References and methods underpinning the analysis
  - COLONY v.2.0 for sibship reconstruction (Wang 2004) as the basis for colony assignment.