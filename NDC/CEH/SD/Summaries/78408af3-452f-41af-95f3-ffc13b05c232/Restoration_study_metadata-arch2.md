# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

- Purpose and scope
  - A chronosequence study across 52 arable grassland restoration sites and 5 target National Nature Reserve grassland communities in southern England (calcareous soils).
  - Sites span restoration ages from 1 to 30 years and capture variation in habitat quality, management (cutting/grazing), and surrounding landscape.
  - Objectives include documenting arthropod communities across multiple trophic groups, deriving functional traits for species, and linking community patterns to environmental context.

- Study design and sampling framework
  - Geographical focus: southern England, on calcareous soils; primarily ESA restoration sites and subsequent agri-environment schemes.
  - Arthropod sampling methods (used to cover diverse taxa and resolutions):
    - Pollinator transects: single 2 × 100 m transect per site, walked three times July–August 2014; observations restricted to 10:00–16:00 under suitable weather conditions.
    - Suction sampling: two visits in June and July 2014 using Vortis sampler; 55 subsamples per visit along transects.
    - Pitfall trapping: five traps per site along a 20 m transect; 4-week deployment June–mid July 2014.
  - Taxa targeted: bees (Apoidea), ants (Formicidae), butterflies (incl. Zygaenidae), hoverflies (Syrphidae), beetles (selected Carabidae, Coccinellidae, Staphylinidae, Curculionidae, Apionidae, Chrysomelidae, Elateridae), plant/leafhoppers (Auchenorrhyncha), true bugs (Heteroptera), spiders (Araneae), woodlice (Isopoda), millipedes (Diplopoda).
  - Identification level: primarily species-level; some bees/hoverflies classified at genus level due to direct observation constraints. Juveniles excluded.
  - Data harmonization: due to differing resolutions across methods, results presented as presence/absence matrices; also generated abundance data from the combined sampling.

- Functional trait data
  - Traits derived from literature to characterize species colonizing during restoration:
    - Grassland specialist (ISIs habitat association)
    - Low dispersal ability (mobility/flight data)
    - Body mass (mg)
    - Trophic group (detritivore, herbivore—monophagous/oligophagous/polyphagous, pollinator, predator)
  - Purpose: enable interpretation of functional community structure and potential restoration effects on ecosystem functions.

- Plant community and vegetation context
  - Plant sampling: ten 1 × 1 m quadrats per site to quantify vascular plant cover; conducted June–July 2014 before sward cutting.
  - Sward structure: height measured with a drop disk method to describe structural habitat conditions during arthropod sampling.

- Landscape and historical context
  - Landscape metrics derived from the 2015 UK Land Cover Map (LCM) at 25 m resolution.
  - Proximity to species-rich grassland: index describing surrounding patches within 1000 m, increasing as patches become closer/contiguous.
  - Historical change: percentage loss of species-rich grassland within a 2 km radius from 1930 to 2015, to assess potential extinction debt effects.

- Data products and variables
  - Species-by-site data files:
    - Species_x_sites.csv: presence/absence of each arthropod species per site.
    - Species_x_sites_combined.csv: abundance of each species per site (sum across sampling methods).
    - Species_x_sites_pitfall.csv: abundance per site (pitfall traps only).
    - Species_x_sites_suction.csv: abundance per site (suction sampling only).
    - Species_x_sites_transect.csv: presence/absence per site (pollinator transects).
    - Species_x_sites_plants.csv: plant cover data per site (percent cover).
    - Species_x_trait.csv: species trait mapping (taxonomic group, family, and trait presence/absence/values).
  - Site-environment dataset:
    - SITE_x_environment.csv: per-site environmental/contextual variables including coordinates (X_OSGB, Y_OSGB with anonymization), restoration age, site area, plant-based similarity to target communities (J.plant), management factors (No.Cuts), grazing (Sheep), sward structure (Sward.Structure), landscape proximity (Prox_1000_ave_2km), historical change (Perc_change_ExtGrass_2km), historic management descriptor (Hist_manag), community similarity metric (Jaccards_invert), and Chao1 richness estimates (all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1) for different arthropod groups.
  - Summary metrics
    - Overall and group-specific Chao1 richness estimates (global arthropods and subgroups: detritivores, herbivores, predators, pollinators).
    - Jaccard similarity between the study assemblage and target grassland reference communities.
    - Proximity and historical change indices to contextualize restoration outcomes.

- Analytical outputs and potential uses
  - Standardized datasets suitable for monitoring environmental health and restoration performance over time.
  - Enables cross-site comparisons of arthropod community richness, composition, and functional trait structure.
  - Supports linkage of arthropod community patterns to plant community structure, sward characteristics, and landscape context to inform management and policy decisions.
  - Data products can be uploaded to or integrated with environmental portals for broader access and reuse.

- Key challenges and archetype-aligned considerations
  - Value enhancement: combining this dataset with other relevant data to avoid single-use limitations and improve long-term ecological insight.
  - Data accessibility: ensuring underlying data are accessible to researchers and practitioners for validation and broader analysis.