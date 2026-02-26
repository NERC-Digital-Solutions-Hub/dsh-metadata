# Growth rates of grass species with contrasting photosynthetic pathways and life histories

## Overview
- A dataset of sequential biomass harvests from a controlled-environment growth experiment in Sheffield, comparing grasses with C3 vs C4 photosynthesis and annual vs perennial life histories.
- Includes belowground and aboveground biomass, root architecture metrics, leaf area, and related traits, plus leaf anatomical data and species phylogeny.
- Aims to understand morphogenesis and growth rate differences across 74 grass species using phylogenetic comparative analyses.

## Dataset contents and structure
- Three main data components:
  - GROWTH_ANALYSIS_DATASET.CSV: longitudinal measurements per plant (growth time, leaf count, tillers, stem height, biomass, leaf area, root metrics, etc.).
  - LEAF_SUPPORT_DATASET.CSV: leaf anatomical and tissue composition metrics (vein number, leaf width, epidermis, fibres, mesophyll, vascular tissues, bundle sheath, etc.).
  - SPECIES_INFORMATION.CSV: species-level metadata (seed source, germplasm accession, photosynthetic pathway, clade, life history).
- Phylogenetic context:
  - Phylogeny for growth analysis uses concatenated chloroplast markers; two related phylogenies referenced for respective analyses.

## Experimental design and sampling
- Stratified sampling of 74 Poaceae species across:
  - BOP (C3 lineage) and PACMAD (includes C4 lineages) clades.
  - 12 independent C4 lineages and 20 monophyletic annual grass groups, with several C4/C3 pairings for annuals.
- Seeds sourced from public germplasm collections; germination and transplantation conducted under controlled conditions.
- Experimental setup:
  - Randomised block design within eight chambers, 2 L pots with vermiculite/sand medium.
  - Growth conditions: 14 h photoperiod, 30/25°C day/night, ~80% humidity, ~1056 μmol m^-2 s^-1 PPFD.
  - Watering and nutrient regime standardized.

## Data collection and measurement methods
- Collection timeline:
  - Germination date recorded; pre-transplant non-destructive measurements on 10 seedlings per species.
  - Post-transplant: weekly harvests over ~5 weeks; destructive sampling of four plants per species per time point.
- Measurements:
  - Aboveground and belowground biomass: fresh and dry masses for leaves, stems, roots; total plant biomass and yield (flowering part).
  - Morphometrics: number of leaves, leaves on main tiller, tillers, main stem length, root depth.
  - Root architecture: total length, surface area, average diameter, forks, tips; primary vs secondary roots counted.
  - Leaf area and specific metrics: leaf area per plant, specific leaf area (SLA).
  - Imaging-based analyses: root system metrics via WinRHIZO; leaf area via WinDIAS.
  - Leaf anatomy: cross-sectional tissue areas (veins, epidermis, fibres, mesophyll, bundle sheath), normalized per vein and scaled to whole leaf using vein counts and leaf width.
- Phylogeny and comparative methods:
  - Four chloroplast markers used to construct a time-calibrated phylogeny (BEAST); marker sequences sourced from NCBI or newly sequenced.
  - Analyses constrained by clade monophyly and cross-clade priors; two separate phylogenies referenced for different datasets.

## Data files and schemas
- SPECIES_INFORMATION.CSV
  - Columns include: Species name, seed_source, germplasm_accession, photosynthetic_pathway, clade, life_history.
- GROWTH_ANALYSIS_DATASET.CSV
  - Key fields: block, unique_code, experiment, species_name, germination_date, date_measured, no_days_growing, no_Leaves, no_Leaves_Main_Tiller, shoot_Length, no_tillers, root_depth, leaf_DM, Leaf_Area, SLA, shoot_DM, total_root_DM, total_plant_biomass_DM, yield_DM, total_root_length, total_root_surface_area, total_root_diameter, total_root_forks, total_root_tip, shoot_FM, total_root_FM, yield_FM, total_biomass_FM, total_seminal_roots, total_second_roots, life_history, photosynthetic_pathway, clade, lineage.
- LEAF_SUPPORT_DATASET.CSV
  - Columns include: Species, LH (life history), Phototype (photosynthetic pathway), Total_vein_no., Leaf_width_mm, segment_nb_veins, E (epidermis area), F (fibres area), M (mesophyll area), OS (outer bundle sheath), IS (inner bundle sheath), V (vascular tissue), extensions (bundle sheath extension).
- References: Christin et al. (2013) on leaf anatomy; Wade et al. (2020) growth morphogenesis study (data source for the current dataset).

## Licensing and citation
- Open Government Licence (OGL) via https://doi.org/10.5285/cb0d7a37-45c5-4645-b5ef-ba097d92fc20
- Required citation: Wade, R.N.; Seed, P.; McLaren, E.; Wood, E.; Christin, P.A.; Thompson, K.; Rees, M.; Osborne, C.P. (2020). Growth rates of grass species with contrasting photosynthetic pathways and life histories. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/cb0d7a37-45c5-4645-b5ef-ba097d92fc20

## GIS-relevant applications
- Map-based trait integration:
  - Link species traits (photosynthetic pathway, life history) with geographic distribution datasets to produce maps of growth-potential or trait-rich grass assemblages.
  - Combine with environmental layers to explore how C3 vs C4 and annual vs perennial grasses may respond under different climates, using the phylogenetic context to inform trait evolution.
- Data fusion opportunities:
  - Augment field-based grass distribution products with mechanistic growth trait proxies derived from leaf and root morphology, enabling more nuanced habitat suitability or restoration planning maps.
- Visualisation and storytelling:
  - Create interactive maps showing species clusters by photosynthetic pathway and growth metrics across regions, incorporating uncertainty from phylogenetic analyses.

## Limitations and notes
- Data are generated from controlled-environment experiments, not field trials; environmental variability in natural settings is not captured.
- Measurements focus on short-term growth responses over five weeks and may not reflect long-term mature plant performance.
- Some metrics rely on image analysis and cross-sectional tissue data; exact replication may require specific software and equipment.

## References
- Christin, P.-A.; Osborne, C.P.; Chatelet, D.S.; Columbus, J.T.; Besnard, G.; Hodkinson, T.R.; Garrison, L.; Vorontsova, M.; Edwards, E.J. (2013) Anatomical enablers and the evolution of C4 photosynthesis in grasses. Proceedings of the National Academy of Sciences, USA, 110, 1381-1386.
- Wade, R.N.; Seed, P.; McLaren, E.; Christin, P.A.; Thompson, K.; Rees, M.; Osborne, C.P. (2020) The morphogenesis of fast growth in plants. New Phytologist, accepted.