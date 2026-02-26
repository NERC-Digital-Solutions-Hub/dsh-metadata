# Functional and epiphytic biodiversity differences between nine tree species in the UK

- Purpose and monitoring context
  - Provides a comprehensive, metadata-rich dataset to understand how tree species identity influences functioning and epiphytic biodiversity (lichens and bryophytes) across the UK.
  - Spurs environmental monitoring by linking tree biodiversity and ecosystem functioning to pest/pathogen concerns and potential ecological replacements.
  - Demonstrates an integrated approach to monitoring multiple biological and soil-chemical variables to inform policy and management decisions.

- Study design and scope
  - Locations: six sites across the UK (Knightshayes Court, Bodnant, Westonbirt, Crathes, Dinefwr, Mount Stuart).
  - Species: nine tree species including Quercus petraea, Q. robur, Fraxinus excelsior, Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Quercus cerris, Quercus rubra, and Tilia x europaea.
  - Sampling: 230 trees in total (roughly 35–40 per site); additional branch sampling for some species at certain sites.
  - Data are organized to support a relational database linking trees to site, species, and all measured attributes.

- Data collection and variables
  - Tree attributes: girth/DBH, height, site habitat context (semi-natural woodland, parkland, garden), canopy cover, and plant/neighbor context (distance and species to nearest tree within 30 m).
  - Biodiversity and epiphytes: presence/absence of bryophytes and lichens on trunk (ground level to 1.75 m) and on branches/twigs where reachable.
  - Bark and bark-related properties: bark pH, pattern (smooth, fissured, flaky, rugose, patterned), ridge/furrow measurements, bark hardness, water holding capacity.
  - Decomposition experiments: litter decomposition using four filter papers per tree buried 3 m south of the tree; monitored with litter bags and lollipop sticks; decay metrics recorded.
  - Soil analysis: eight soil samples per tree analyzed for mineralized nitrogen, total N and C, LOI, pH (water and CaCl2), and moisture-related properties; additional analyses include total N/C and NH4/N oxidation before and after incubation.
  - Spectroscopy and chemistry: FTIR spectra of ball-milled soil; bark chemistry including water holding capacity, pH, and conductivity; bark-related sampling and analyses.
  - Microbial/edaphic data: soil mineralization (N-min), and related metrics across samples.
  - Temporal and data capture: a central date field and per-tree collection events; use of iButton soil temperature loggers placed near litter decomposition experiments.

- Data management and structure
  - Relational database design with a central Trees table (ANS_Tree_code) linking to multiple auxiliary tables:
    - Habitat_structure
    - Decomposition
    - Temperature
    - Soil
    - FTIR
    - Bark_chemistry
    - Bark_plot
    - Bryophytes
    - Lichens
    - Bryophyte_names and Lichen_names (taxon reference tables)
  - Documentation and metadata
    - Each data file includes detailed metadata (Tables 3–14 describe content and fields for each file).
    - Data descriptions cover variable definitions, measurement methods, and data provenance.
  - Access and sharing
    - The dataset is structured to be stored in a relational database (e.g., Microsoft Access) with clear table relationships and documentation.
    - Emphasizes openness and data governance through metadata and standardized methods.

- Site details and sampling effort
  - Six sites with varying soil types, climates, and management histories; site-level climate data drawn from nearby meteorological stations.
  - Table-level breakdowns provide per-site counts of each tree species sampled and per-tree data capture specifics (e.g., when litter or canopy measurements were taken).

- Governance, quality, and standards
  - Emphasis on quality assurance: data are meant to be cleaned, transformed, analyzed, and presented clearly (reports, charts, dashboards).
  - Metadata completeness and dataset provenance are central, enabling verification of data quality and comparability across sites and species.
  - Data governance processes are implied through structured data sharing and clear linkage between datasets.

- Implications for monitoring frameworks
  - Demonstrates how to design an integrated biodiversity and ecosystem functioning monitoring program across multiple species and sites.
  - Highlights the importance of rich metadata, standardized measurement protocols, and robust data architectures to support policy-relevant environmental health monitoring.
  - Addresses potential data challenges by predefining data tables, metadata, and access pathways to avoid duplication and promote data reuse.

- Acknowledgments and references
  - Funded by Defra through the PuRpOsE project (BB/N022831/1) with additional Scottish Government support.
  - Methodological references underpin soil, bark, and decomposition analyses, and prior ecological work on oak ecosystems and pests.