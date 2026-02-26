# Grassland arthropod trait and associated environmental data collected in arable reversion sites in southern England, 2014

- Overview
  - A 2014 study in southern England sampled a chronosequence of 52 arable grassland restoration sites plus five target National Nature Reserve grassland communities on calcareous soils.
  - Sites varied in restoration age (1–30 years), habitat quality (sward structure, floristic similarity to targets), management (cutting, grazing), and surrounding landscape (isolation, grassland cover).
  - Arthropods were identified across detritivores, herbivores, predators, and pollinators; functional traits (e.g., body mass, dispersal) were derived for species identified to species level.
  - The dataset supports analyses of how restoration, habitat quality, and landscape context shape grassland arthropod communities and functional trait distributions.

- Study design and sampling
  - Location: calcareous soils in southern England; restoration sites associated with ESA schemes and agri-environmental programs.
  - Sampling methods (covering broad taxonomic groups):
    - Pollinator transects: two fixed 2 × 100 m transects per site walked three times (July–August 2014) under suitable weather; taxa include bees, butterflies, hoverflies.
    - Suction sampling (Vortis): two sampling occasions per site (June–July 2014);主要 sward-active arthropods collected along transects with 55 subsamples per visit.
    - Pitfall trapping: five traps per site along a 20 m transect, left out for ~4 weeks (June–mid July 2014).
  - Data integration: samples from multiple methods were combined for analysis; due to differing resolutions, results are presented as presence-absence matrices at the site level for some analyses.

- Taxa and identification
  - Targeted groups: bees (Apoidea), ants (Formicidae), butterflies (including Zygaenidae), hoverflies (Syrphidae), beetles (several families), plant/leaf hoppers (Auchenorrhyncha), true bugs (Heteroptera), spiders (Araneae), woodlice (Isopoda), and millipedes (Diplopoda).
  - Most arthropods identified to species; some bees and hoverflies attributed to genus when necessary (e.g., Neoascia spp., Cheilosia spp., Hylaeus spp., Lasioglossum spp.).
  - Juveniles were excluded from analyses.

- Functional traits
  - Derived from literature to describe ecological roles and life-history characteristics:
    - Grassland specialist: habitat association with grassland (ISIS/SAT-based data).
    - Low dispersal ability: inferred from mobility data and wing development; flightless species typically considered poor dispersers.
    - Body mass: dry weight (mg) as a proxy for energetic and dispersal traits.
    - Overall trophic level: detritivore, herbivore (monophagous, oligophagous, polyphagous), pollinator, and/or predator (species may span multiple trophic roles).

- Plant community and structure
  - Vegetation sampling: ten 1 × 1 m quadrats per site to quantify percentage cover of vascular plants.
  - Sward structure: average height measured with a drop disk (30 cm diameter, 150 g) to describe structural condition during arthropod sampling.
  - Sampling window: June–July 2014, prior to sward cutting.

- Landscape context and environmental metrics
  - Landscape structure: derived from the 2015 UK Land Cover Map (25 m resolution).
  - Proximity to species-rich grassland: index representing surrounding grassland patch area relative to edge distance, calculated within 1000 m of each restoration site.
  - Historic change: percentage change in species-rich grassland cover from 1930 to 2015 within a 2 km radius to assess potential extinction debt effects.
  - Site attributes: age since restoration, area, management history, sward characteristics, grazing presence, and other local factors.

- Data files and key variables
  - Species_x_sites.csv: presence/absence of each arthropod species at each site.
  - Species_x_sites_combined.csv: abundance of each species at each site, summed across all sampling methods.
  - Species_x_sites_pitfall.csv: species abundances from pitfall traps by site.
  - Species_x_sites_suction.csv: species abundances from suction sampling by site.
  - Species_x_sites_transect.csv: species presence/absence from pollinator transects by site.
  - Species_x_sites_plants.csv: plant species' percent cover per site.
  - Species_x_trait.csv: species-level trait data, including group, family, dispersal/mobility traits, grassland specialist status, detritivore/monophagous/oligophagous/polyphagous/pollinator/predator indicators, and body mass.
  - Site_x_environment.csv: site-level environmental and landscape variables, including:
    - X_OSGB and Y_OSGB coordinates (with privacy protections),
    - Age, Area, J.plant (plant community similarity to targets; 0–1),
    - No.Cuts (sward cutting frequency), Sheep (grazing presence), Sward.Structure (height), Prox_1000_ave_2km (proximity to species-rich grassland),
    - Perc_change_ExtGrass_2km (historical loss of species-rich grasslands within 2 km),
    - Hist_manag (historic management), Jaccards_invert (arthropod community similarity to target),
    - all.chao1, det.chao1, herb.chao1, pred.chao1, Poll.chao1 (Chao1 richness estimates for overall and functional groups).

- Data quality, scope, and considerations
  - Multi-method sampling yields differing resolution; analysis emphasizes presence-absence matrices and richness estimators (Chao1) to compare communities.
  - Coordinates are anonymized to protect landowners.
  - Data enable correlation and modeling of arthropod community structure and functional trait distributions with restoration age, habitat quality, management, plant community structure, and landscape context.
  - Potential to explore extinction debt signals and restoration success by comparing to target grassland communities.

- Analytical opportunities and applications
  - Correlate restoration age and management with arthropod richness and functional trait composition.
  - Assess how landscape proximity to species-rich grasslands influences community similarity and trait distributions.
  - Compare observed arthropod assemblages to target grassland communities using Jaccard similarity and related metrics.
  - Explore multi-taxa responses across detritivores, herbivores, predators, and pollinators, leveraging trait data to interpret ecological functioning.
  - Utilize Chao1 estimates to evaluate sampling completeness and compare richness across habitats and restoration stages.

- References and data provenance
  - Includes methodological and ecological literature on grassland restoration, dispersal, biodiversity metrics (Chao1, Jaccard), and landscape connectivity, supporting trait derivations and analytical choices.