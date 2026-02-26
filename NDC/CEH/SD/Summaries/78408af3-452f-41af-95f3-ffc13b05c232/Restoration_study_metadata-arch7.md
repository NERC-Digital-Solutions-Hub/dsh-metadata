# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

## Overview
- A 2014 study sampling 52 arable grassland restoration sites plus five target National Nature Reserve (NNR) grassland communities in southern England on calcareous soils.
- Sites vary by restoration age (1–30 years), habitat quality, management, and surrounding landscape, aiming to capture environmental variation relevant to grassland arthropods.
- Focus on arthropod communities across multiple trophic groups (detritivores, herbivores, predators, pollinators) with species-level identifications and derived functional traits.

## Study design and scope
- Geographic context: southern England, calcareous soils, largely part of the South Downs ESA, South Wessex Downs ESA, and related agri-environment schemes.
- Chronosequence approach: restoration age and landscape context used to assess recovery of arthropod communities and plant associations.
- Data products intended for GIS-based mapping and analysis to support conservation planning and restoration evaluation.

## Field sampling and taxonomic scope
- Taxa monitored: bees (Apoidea), ants (Formicidae), butterflies (including Zygaenidae), hoverflies (Syrphidae), beetles (selected Carabidae, Coccinellidae, Staphylinidae, Curculionidae, Apionidae, Chrysomelidae, Elateridae), plant hoppers (Auchenorrhyncha), true bugs (Heteroptera), spiders (Araneae), woodlice (Isopoda), millipedes (Diplopoda).
- Sampling methods to cover multiple taxa and resolutions:
  - Pollinator transects: single 2 × 100 m fixed transect per site, walked three times July–August 2014, weather conditions per Pollard & Yates (1993); two passes per date.
  - Suction sampling: sward-active arthropods using a Vortis sampler; two visits per site (June–July 2014); 55 suction captures per sample along transects.
  - Pitfall traps: five traps per site along a 20 m transect, 4 weeks (June–mid July 2014), preserved in 50% ethylene glycol with detergent.
- Data handling: due to varying resolutions across methods, analyses focus on binary presence/absence of species at each site; juveniles excluded; some genera-level identifications for bees and hoverflies noted.

## Plant and habitat measurements
- Plant community sampling: ten 1 × 1 m quadrats per site to quantify vascular plant cover; conducted June–July 2014 before sward cuts.
- Habitat structure: sward height measured with a drop disk to describe sward structure at arthropod sampling time.

## Spatial and environmental data
- Landscape metrics derived from the 2015 UK Land Cover Map (25 m resolution):
  - Proximity to species-rich grassland: index based on surrounding patches within 1000 m, higher values indicate closer, more contiguous grassland patches (0–5.54 observed).
  - Historical change in species-rich grassland cover: percent loss within a 2 km radius comparing 1930 land use data to 2015 (to assess extinction debt potential).
- Site-level environmental variables (Site_x_environment.csv):
  - X_OSGB, Y_OSGB coordinates (anonymized to protect landowner locations).
  - Age of restoration (years), site area (ha), sward-related metrics (No.Cuts, Sward.Structure), proximity metrics (Prox_1000_ave_2km).
  - Floristic similarity to target restoration sites (J.plant; 0–1 scale).
  - Historic management descriptor (Hist_manag) and Jaccard-based similarity (Jaccards_invert) to target communities.
  - Chao1-based estimates of arthropod richness by full set and by functional groups (all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1).

## Arthropod trait data
- Species trait dataset (Species_x_trait.csv) provides:
  - Group and Family classifications.
  - Low mobility trait (binary).
  - Detritivore, Monophagous/ Oligophagous/ Polyphagous herbivore, Pollinator, and Predatory traits (binary).
  - Body mass (Mass; continuous, mg).
  - Grassland specialist trait (binary) derived from habitat association data.
- Purpose: enable functional analyses of assemblage traits alongside taxonomic richness and community similarity.

## Data products and datasets
- Species-by-site matrices:
  - Species_x_sites.csv: presence/absence per site for each arthropod species.
  - Species_x_sites_combined.csv: abundance per species per site (sum across all sampling methods).
  - Species_x_sites_pitfall.csv: abundance per species per site for pitfall traps.
  - Species_x_sites_suction.csv: abundance per species per site for suction sampling.
  - Species_x_sites_transect.csv: presence/absence per species per site for pollinator transects.
- Plant and trait datasets:
  - Species_x_sites_plants.csv: plant cover percentages per species per site.
  - Species_x_trait.csv: species-level trait data as described above.
- Site and environment datasets:
  - Site_x_environment.csv: site-level environmental and landscape metrics, including richness estimators, proximity metrics, historical grassland change, and habitat descriptors.

## Data quality, limitations, and considerations for GIS work
- Resolution and sampling differences: integration uses presence/absence matrices due to differing method resolutions; abundance data available per method but cross-method comparability may be limited.
- Coordinate privacy: spatial coordinates are anonymized to protect landowner locations; precise mapping must account for reduced resolution.
- Taxonomic resolution: some taxa (notably bees and hoverflies) may be identified to genus level; juvenile specimens excluded.
- Temporal scope: data reflect a single year (2014) snapshot; use for temporal comparisons should account for annual variation and restoration age effects.
- Data fusion potential: combines arthropod data with plant cover, sward structure, and landscape context to examine relationships between habitat restoration, community composition, and functional traits.

## Practical GIS applications
- Map and analyze spatial patterns of arthropod richness and community composition across restoration ages and landscape contexts.
- Compare plant–arthropod associations and assess how habitat quality metrics (sward structure, management) influence trait distributions.
- Examine proximity effects of surrounding species-rich grassland patches on local arthropod communities.
- Explore extinction debt signals by relating historical habitat loss to current arthropod richness and community similarity.
- Develop data products for policy and conservation planning, such as prioritizing restoration sites with higher functional trait diversity or proximity to high-quality grassland patches.

## Endnotes and references
- Data and methods rely on established sampling and trait-assignment approaches from grassland arthropod ecology literature and contemporary landscape-genetic and richness estimators (e.g., Chao1, Jaccard similarity, FRAGSTATS-based landscape metrics).