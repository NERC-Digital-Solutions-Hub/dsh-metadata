# Growth rates of grass species with contrasting photosynthetic pathways and life histories

## Overview
- Plant growth dataset from controlled-environment experiments in Sheffield, collected across 2016 and 2017 in three parts.
- Aims: compare growth among grasses with C3 vs C4 photosynthesis and annual vs perennial life histories; includes weekly harvests over five weeks.
- Data components: dry biomass of roots and leaves, counts of roots/leaves/shoot branches; leaf anatomical characteristics from herbarium-derived data; phylogenetic relationships among species.
- Funded by NERC standard grant NE/N003152/1; relates to Wade et al. (2020) New Phytologist.
- Dataset available under Open Government Licence (OGL); citation required.

## Access and licensing
- Licence: Open Government Licence (OGL).
- DOI and citation instructions provided:
  Wade, R.N.; Seed, P.; McLaren, E.; Wood, E.; Christin, P .A.; Thompson, K.; Rees, M.; Osborne, C.P. (2020). Growth rates of grass species with contrasting photosynthetic pathways and life histories. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/cb0d7a37-45c5-4645-b5ef-ba097d92fc20

## Experimental design and scope
- Phylogenetic comparative analysis of 74 grass species from across BOP (C3 only) and PACMAD lineages.
- Sampling strategy: stratified sampling to capture diversity of C4 and annual grasses using seeds from public germplasm collections; included multiple pairs of annual vs perennial within lineages.
- Coverage: 12 independent C4 lineages and 20 monophyletic annual groups (nine annual lineages include C4 species).
- Plant material and setup: seeds germinated under pre-dormancy treatments, transferred to 2 L pots with vermiculite/sand, randomised block design within eight chambers.
- Growth conditions: 14 h photoperiod, 30/25 C day/night, ~80% humidity, PPFD ~1056 μmol m^-2 s^-1; controlled watering (deionised water) and nitrate-type nutrient solution applied biweekly.

## Data collection and measurements
- Three time-staggered experiments; germination date recorded; pre-transplant non-destructive measurements on 10 seedlings per species; daily counts of root tips and leaves until transplanting.
- Post-transplant measurements: leaves, leaves on main tiller, tillers counted three times weekly; main stem height measured weekly.
- Harvest protocol: four plants per species harvested weekly for five weeks; roots washed; biomass separated into leaves, stems, roots; fresh masses recorded; leaf detachment and tiller counts performed.
- Morphometrics and imaging: leaf area measured by image analysis; root architecture quantified (total length, surface area, diameter, forks, tips) using WinRHIZO; total leaf area per plant measured with WinDIAS; primary roots counted from root images.
- Derived metrics: shoot/root phytomer sizes, number of seminal/primary and secondary roots, etc.
- Tissue and anatomy: structural tissue investments (veins, fibres) quantified from leaf cross-sections; additional measures include epidermis, bundle sheath, fibre tissue areas per segment; per-leaf values scaled by total leaf veins; leaf width measured on cleared/stained leaves.
- Leaf anatomy dataset: additional data from 86 species using published transverse sections; per-segment tissue areas normalized by veins and scaled to whole leaf.

## Analytical methods and phylogeny
- Phylogeny construction: chloroplast markers (trnK-matK, rbcL, ndhF, trnL-trnF) obtained from NCBI or sequenced; alignment with MUSCLE; concatenated; time-calibrated tree with BEAST v1.8.4 using GTR+G+I, Yule prior, relaxed clock; monophyly of BOP and PACMAD enforced.
- Cross-study phylogeny: for LEAF_SUPPORT_DATASET, used phylogeny from Christin et al. (2013).
- Data organization and files:
  - SPECIES_INFORMATION.CSV: species, seed_source, germplasm_accession, photosynthetic_pathway, clade, life history.
  - GROWTH_ANALYSIS_DATASET.CSV: fields include block, unique_code, experiment, species_name, germination_date, date_measured, no_days_growing, no_Leaves, no_Leaves_Main_Tiller, shoot_Length, no_tillers, root_depth, leaf_DM, Leaf_Area, SLA, shoot_DM, total_root_DM, total_plant_biomass_DM, yield_DM, total_root_length, total_root_surface_area, total_root_diameter, total_root_forks, total_root_tip, shoot_FM, total_root_FM, yield_FM, total_biomass_FM, total_seminal_roots, total_second_roots, life_history, photosynthetic_pathway, clade, lineage.
  - LEAF_SUPPORT_DATASET.CSV: Species, LH, Phototype, Total_vein_no., Leaf_width_mm, segment_nb_veins, E, F, M, OS, IS, V, extensions.
  - Phylogeny files: concatenated_combined.tre (for growth dataset), gpwg4.tre (for leaf support dataset).
- Data provenance: measurements spanning germination to weekly harvests; controlled environment protocol supports reproducibility and cross-study comparison.

## Data quality, governance and reuse
- Metadata-rich structure with explicit fields for species identity, photosynthetic pathway, life history, experimental blocks, dates, and multiple derived metrics.
- Phylogenetic context integrated to support comparative analyses.
- Clear licensing and citation requirements facilitate attribution and reuse within Open Government Licence terms.
- Designed to address common stewardship challenges: large, multi-system data collection; standardized metadata; integration of morphometric, anatomical, and phylogenetic data to enable reuse in broader datasets and analyses.

## References
- Christin, P.-A., Osborne, C.P., Chatelet, D.S., et al. (2013) Anatomical enablers and the evolution of C4 photosynthesis in grasses. Proceedings of the National Academy of Sciences, USA, 110, 1381-1386.
- Wade, R.N., Seed, P., McLaren, E., et al. (2020) The morphogenesis of fast growth in plants. New Phytologist, accepted.