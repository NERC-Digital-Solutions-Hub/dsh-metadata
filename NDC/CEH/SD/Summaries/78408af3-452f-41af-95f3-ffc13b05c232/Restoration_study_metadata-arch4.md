# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

## Overview
- A 2014 study sampling arthropods across 52 arable grassland restoration sites and 5 target National Nature Reserve communities in calcareous soils of Southern England.
- Data encompass species across detritivores, herbivores, predators, and pollinators, with functional trait information (body mass, dispersal ability, trophic group).
- Associated plant community data, landscape context, and site/environment metadata are included to support analyses of restoration success and arthropod responses.

## Study design and scope
- Sites: 52 arable reversion sites (age 1–30 years) plus 5 pristine target grassland communities.
- Habitat context: Variation in restoration age, sward structure, floral similarity to targets, management (cutting/grazing), and surrounding landscape.
- Geographic focus: Calcareous soils in Southern England, including areas surrounding South Downs ESA and South Wessex Downs ESA.

## Data collection methods
- Arthropod sampling methods (applied to multiple taxonomic groups): pollinator transects, suction sampling, and pitfall trapping.
- Taxa targeted: bees (Apoidea), ants (Formicidae), butterflies (including Zygaenidae), hoverflies (Syrphidae), beetles (selected families), plant/leaf hoppers (Auchenorrhyncha), true bugs (Heteroptera), spiders (Araneae), woodlice (Isopoda), and millipedes (Diplopoda).
- Sampling protocol: 
  - Pollinator transects: single 2 × 100 m transect per site, walked three times from July to August 2014; each occasion involved two passes; conducted 10:00–16:00 under standard weather conditions.
  - Suction sampling: two visits per site (June and July 2014) using a Vortis suction sampler; each visit yielded 55 subsamples along transects.
  - Pitfall traps: five traps per site along a 20 m transect, left for ~4 weeks (June–mid July 2014).
- Data handling: species identified to species where possible; juveniles excluded; some taxa provisionally identified to genus due to observational limitations.
- Plant community sampling: ten 1 × 1 m quadrats per site to quantify vascular plant cover; sward height measured with drop disk method before any sward cuts.

## Data structure and variables
- Presence/absence matrices: primary output across methods (binary data at the site level).
- Abundance data: site-level abundances summed across all sampling methods (transects, pitfall, suction).
- Functional traits (Species_x_trait.csv): for each arthropod species, including Grassland_specialist, Low.Mobility, Body Mass (Mass), and trophic group (Detri., Mono., Olig., Poly., Poll., Pred.).
- Plant data (Species_x_sites_plants.csv): plant species presence and/or percent cover per site.
- Related trait and taxonomic context (Species_x_trait.csv): higher taxonomic group and family classifications.
- Site-level environmental and landscape context (Site_x_environment.csv):
  - Spatial coordinates (X_OSGB, Y_OSGB) with anonymity considerations.
  - Age of restoration, site area, number of sward cuts, presence of sheep grazing, sward structure (height), and floristic similarity metrics (J.plant; Jaccards_invert).
  - Proximity to surrounding species-rich grassland within 1000 m (Prox_1000_ave_2km).
  - Historical habitat changes (Perc_change_ExtGrass_2km; change in grassland cover since 1930).
  - Chao1 richness estimates for overall and subgroups (all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1).
  - Management history descriptor (Hist_manag).
- Landscape and ecological metrics: derived from UK Land Cover Map 2015 at 25 m resolution; proximity index increases as surrounding grassland patches become closer and more contiguous.

## Data processing and analysis-ready features
- Richness estimation: Chao1 estimators calculated for overall and functional groups (all, detritivores, herbivores, predators, pollinators).
- Community similarity: Jaccard's similarity between overall arthropod communities and target grassland examples.
- Integrated dataset design: combines species occurrence/abundance, functional traits, plant/community data, and landscape context for cross-scale analyses of restoration outcomes.

## Data availability and file describe-ables
- Species_x_sites.csv: presence/absence of each arthropod species per site.
- Species_x_sites_combined.csv: abundance of each arthropod species per site (summed across methods).
- Species_x_sites_pitfall.csv: abundances from pitfall sampling per site.
- Species_x_sites_suction.csv: abundances from suction sampling per site.
- Species_x_sites_transect.csv: presence/absence from transect-based observations per site.
- Species_x_sites_plants.csv: plant species cover percentages per site.
- Species_x_trait.csv: species-level trait information and taxonomic grouping.
- Site_x_environment.csv: site-level environmental and landscape variables (detailed field list described above).

## Quality, limitations, and governance
- Multi-method sampling introduces differing resolution scales; results presented as presence/absence at the site level to harmonize data across methods.
- Juvenile arthropods excluded; some taxa identified only to genus due to observational constraints.
- Anonymization of precise locations included in coordinates within Site_x_environment.
- Data derived metrics (Chao1, Jaccard) provide robust comparisons across restoration ages and landscape contexts.

## Relevance for data leadership and governance
- Demonstrates a comprehensive, multi-layer data collection schema integrating taxonomy, functional traits, plant communities, and landscape context for restoration assessment.
- Provides clear data structures, file schemas, and metadata descriptors that support discoverability, interoperability, and reuse.
- Highlights the importance of documenting sampling design, methods, and processing steps to enable reproducibility and cross-study integration.
- Illustrates opportunities to align similar restoration datasets under standardized schemas (e.g., trait matrices, presence/absence matrices, site-level metadata) to support scalable data governance and collaborative analysis.