# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

## Overview and aims from a Data Steward perspective
- Large-scale, site-centered dataset capturing arthropod communities and environmental context across 52 arable grassland restoration sites plus 5 National Nature Reserve targets in southern England (calcareous soils).
- Data span restoration ages from 1 to 30 years and include multiple management regimes (cutting, grazing) and landscape contexts to support governance of restoration biodiversity datasets and their reuse.
- Includes both species-level data (presence/absence and abundance across methods) and functional trait information for identified arthropods, enabling standardized data sharing and downstream analyses of ecosystem function.

## Data scope and structure
- Taxa and sampling scope
  - Arthropod groups monitored: bees, ants, butterflies, hoverflies, beetles (selected families), plant/leaf hoppers, true bugs, spiders, woodlice, millipedes.
  - Specimens identified to species where possible; some groups (bees, hoverflies) may be identified to genus due to sampling method.
  - Functional traits derived for species with references (e.g., Grassland specialist, Low mobility, Body mass, Trophic level including detritivore, herbivore, predator, pollinator).
- Plant and habitat context
  - Plant community: ten 1 × 1 m quadrats per site to quantify vascular plant cover; sward height measured with a drop disk.
- Landscape and historical context
  - Landscape metrics derived from 2015 UK Land Cover Map (LCM): proximity to species-rich grassland patches within 1000 m.
  - Historical change: percentage change in species-rich grassland cover from 1930 to 2015 within a 2 km radius to assess extinction debt considerations.
- Data products and formats
  - Per-site presence/absence matrices for arthropod species (Species_x_sites.csv) and per-method presence/absence or abundance matrices (Species_x_sites_pitfall.csv, Species_x_sites_suction.csv, Species_x_sites_transect.csv).
  - Combined abundance matrix across all sampling methods (Species_x_sites_combined.csv).
  - Plant data (Species_x_sites_plants.csv) with plant cover percentages.
  - Trait data (Species_x_trait.csv) detailing species group, family, and functional traits (Low.Mobility, Detri, Mono, Olig, Poly, Poll, Pred, Grassland_specialist, Mass).
  - Site-level environmental and landscape data (Site_x_environment.csv) including coordinates obfuscated for anonymity, restoration age, site area, management, sward structure, proximity metrics, historical change, plant similarity (J.plant), and biodiversity estimates (all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1).
- Data handling and metadata
  - Data descriptions accompany each file (columns include SITE, Description, Units) to support usability and interoperability.
  - Some analysis decisions noted due to differing resolutions among sampling methods; for example, focusing on binary presence/absence matrices for certain datasets.

## Methods and data quality considerations
- Sampling protocols
  - Pollinator transects: fixed 2 × 100 m transects walked three times per site between 10:00 and 16:00 during July–August 2014.
  - Suction sampling (Vortis) for sward-active arthropods: two sampling occasions per site (June and July 2014); 55 subsamples per occasion along a transect.
  - Pitfall traps: five traps per site along a 20 m transect, left out for four weeks (June–mid July 2014) with ethylene glycol solution.
- Data integration and limitations
  - Across-method differences necessitated converting to presence/absence matrices for some analyses; abundance data are provided in the combined per-site dataset.
  - Juveniles were excluded from analyses; some taxa identifications limited to genus due to sampling method.
  - Coordinates are obfuscated to protect landowners’ anonymity.
- Trait derivation
  - Functional traits compiled from multiple literature sources; includes habitat association, dispersal/mobility indicators, body mass, and trophic role classifications.
- Biodiversity metrics
  - Chao1 estimators calculated for overall arthropods and functional groups (detritivores, herbivores, pollinators, predators).
  - Jaccard similarity used to compare overall arthropod communities to target grassland communities.

## Practical implications for data stewardship and reuse
- Rich, multi-layer dataset suitable for analyses of restoration ecology, landscape context effects, and functional trait–community relationships in grassland arthropods.
- Well-documented data dictionary and file-level metadata facilitate discoverability, interoperability, and reproducibility for future stewardship and sharing.
- The dataset’s design supports reproducible integration with other grassland restoration datasets through standardized trait definitions, biodiversity metrics, and landscape context variables.
- Data governance considerations include anonymized spatial coordinates, explicit method documentation, and clear delineation between presence/absence and abundance data across sampling methods.

## How to access and use
- Primary data files are organized by data type (species per site, per method, combined abundances, plants, traits, and site environments) with accompanying metadata fields describing each column’s meaning and units.
- Useful for:
  - Assessing how restoration age and management influence arthropod communities.
  - Linking plant community structure and sward characteristics to arthropod diversity and trait composition.
  - Exploring landscape context effects such as proximity to other species-rich grasslands.
  - Meta-analytic projects combining restoration datasets across regions.