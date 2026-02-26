# Data abstract

- What the dataset is
  - Information on species identity and frequency of all insect–flower interactions recorded in 10 birch-dominated woodland fragments in 2009 (May–August).
  - Data collected along two transects per site, within center of each wood, with a mix of grazed (cattle) and ungrazed sites.

- Sampling design and scope
  - Transects: 50 × 2 meters, 15 meters apart, at least 50 meters from woodland edge.
  - Disturbance: 5 sites grazed, 5 undisturbed; long-term grazing history; grazing intensity around 2007 documented.
  - One site (Brathens) excluded due to insufficient insect visitation data; final replication is 9 sites.
  - Location: River Dee catchment, Aberdeenshire, UK (latitude ~57.058–57.037, longitude ~−2.962 to −2.512).

- Dataset size and structure
  - 13 columns, 2,002 rows, 218 KB.
  - Core fields cover site metadata, environmental conditions, and interaction observations.

- Variables and data structure
  - Site name and geographic coordinates (latitude, longitude).
  - Disturbance status (grazed vs ungrazed) and environmental measures at sampling (wind speed, temperature).
  - Sampling date.
  - Taxonomic information: insect order, family, and species (binomial or recognisable taxonomic unit; RTU).
  - Interaction data: frequency of interaction between each insect (species/RTU) and visiting plant species, plus flowers per plant individual observed (flowers_N).
  - Plant species identity observed during visits.

- Provenance and funding
  - Data collection conducted in 2009; cofunded by British Ecological Society (SEPG 1563/1968) and NERC CEH Environmental Change Integrating Fund (NEC03463).
  - Subsequent paper development supported by CEH national capability projects (NEC04654 & NEC05106).

- Lineage and reuse
  - Data collected from May 20, 2009 to August 27, 2009 in 10 birch woods in Aberdeenshire.
  - Used to prepare two papers (references provided) and linked to ongoing research on plant–insect networks.
  - Metadata and data lineage documented (origin, sampling methods, and site-level details) to support reproducibility and secondary analyses.

- Metadata and documentation
  - Metadata fields defined for site, coordinates, date, wind, temperature, insect order and family, insect species, plant species, interaction frequency, and flowers observed.
  - Taxonomic references and supplementary materials available via linked publications and associated online resources.

- Data quality and limitations
  - One site excluded due to data scarcity, reducing replication to nine sites.
  - Taxonomic resolution may rely on RTUs where binomial names are not listed; supplementary material provides taxonomic authority references.
  - Environmental measurements (wind, temp) recorded with standardized equipment, but potential variability across sites and times.

- Implications for data strategy and reuse
  - Demonstrates structured, well-documented ecological interaction data with clear metadata, suitable for network analyses and cross-site comparisons.
  - Highlights the importance of documenting disturbance regimes (grazing) and environmental context when assessing interaction networks.
  - Provides a model for data governance: provenance, funding trails, and links to publications to facilitate discoverability and reuse by broader research communities.

- Actions for data leaders
  - Assess availability of similar datasets to enable broader meta-analyses on insect–flower networks.
  - Consider standardizing taxonomic units and metadata schemas to improve interoperability across studies.
  - Ensure clear notes on site inclusion/exclusion criteria and replication to support accurate interpretation in secondary analyses.