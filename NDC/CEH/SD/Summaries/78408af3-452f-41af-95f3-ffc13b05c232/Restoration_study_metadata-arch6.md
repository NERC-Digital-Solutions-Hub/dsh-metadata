# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

- Purpose and scope
  - A 2014 study across 52 arable grassland restoration sites and 5 pristine grassland communities in southern England on calcareous soils.
  - Sites varied in restoration age (1–30 years), habitat quality, management (cutting/grazing), and surrounding landscape; environmental variation was deliberately captured in the dataset.
  - Objective: characterize arthropod communities and derive functional trait information to support restoration assessment and biodiversity monitoring.

- Sampling design and periods
  - Arthropod groups targeted: bees, ants, butterflies, hoverflies, beetles, leafhoppers, true bugs, spiders, woodlice, millipedes ( sampled across multiple orders/guilds ).
  - Sampling methods (to cover diverse taxa):
    - Pollinator transects: a single 2 × 100 m transect walked at a constant speed on three occasions (July–August 2014); weather conditions followed Pollard & Yates standards.
    - Suction sampling (Vortis): conducted at two occasions in June–July 2014 along transects; 55 subsamples per visit.
    - Pitfall traps: five traps per site along a 20 m transect, left for four weeks (June–mid July 2014).
  - Data aggregation: samples combined across visits and methods for analyses; juveniles excluded; some genera identified to genus level for bees/hoverflies due to sampling constraints.
  - Plant data collected in June–July 2014, before any sward cutting.

- Plant and habitat measurements
  - Plant community: ten 1 × 1 m quadrats per site to quantify vascular plant cover.
  - Sward structure: average height measured with a drop disk (30 cm diameter, 150 g) to describe structural condition.

- Arthropod data and trait information
  - Species identification: majority to species; some bees/hoverflies identified to genus due to method; juvenile individuals ignored.
  - Functional traits for identified species (derived from literature):
    - Grassland specialist (habitat association)
    - Low dispersal ability
    - Body mass (dry weight, mg)
    - Overall trophic level (detritivore, herbivore, predator, pollinator)
  - Trait data allow multi-dimensional analyses of community function and restoration outcomes.

- Landscape and environmental context
  - Landscape metrics derived from the 2015 UK Land Cover Map (LCM 25 m resolution).
  - Proximity to species-rich grassland patches: index based on patch area and edge-to-edge distance within 1000 m.
  - Historical change: percentage change in species-rich grassland cover from 1930 to 2015 within a 2 km radius to assess potential extinction debt effects.
  - Site-level environmental variables collected (Site_x_environment.csv): coordinates (anonymized), age of restoration, site area, sward metrics, management history, proximity indices, and biodiversity similarity measures.

- Data files and structure
  - Species_x_sites.csv: presence/absence of each arthropod species by site.
  - Species_x_sites_combined.csv: abundance of each arthropod species by site (summed across all methods).
  - Species_x_sites_pitfall.csv: abundance by site (pitfall data).
  - Species_x_sites_suction.csv: abundance by site (suction data).
  - Species_x_sites_transect.csv: presence/absence by site (transect data).
  - Species_x_sites_plants.csv: plant cover percentages by site.
  - Species_x_trait.csv: species-level trait information (family, group, dispersal, mass, grassland specialization, etc.).
  - Site_x_environment.csv: site-level environmental and landscape variables (coordinates, age, area, sward structure, proximity indices, historic management, Jaccard similarity, all-chao1 richness estimates, and per-group richness estimates).
  - All richness estimates provided: all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1 (per species group).

- Data quality, processing notes
  - No single sampling method suffices for all taxa; data are thus harmonized to presence/absence matrices across sites for comparability.
  - Abundance data are provided per-method (pitfall, suction, transect) and combined for some analyses.
  - Some taxonomic resolution limitations (genus-level identifications for certain groups) acknowledged.

- Potential uses for data support and insights
  - Explore how restoration age, habitat quality, and landscape context influence arthropod richness and composition.
  - Assess functional trait responses (e.g., dispersal, feeding guilds, body mass) across restoration gradients.
  - Link plant community structure and sward characteristics with arthropod communities and functional traits.
  - Evaluate conservation value of restoration sites via proximity to other grasslands and historical grassland area changes.
  - Use presence/absence and abundance data to develop self-service data products (dashboards or summaries) for stakeholders such as local councils or private land managers.