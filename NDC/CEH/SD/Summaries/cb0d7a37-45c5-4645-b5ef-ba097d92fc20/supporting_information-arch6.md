# Data access and terms of use

- The dataset is available under the Open Government Licence (OGL). Citation required: Wade et al. (2020) Growth rates of grass species with contrasting photosynthetic pathways and life histories. NERC Environmental Information Data Centre. Dataset. DOI provided in the license notice.
- Brief description: sequential biomass harvests from a plant growth experiment under controlled environmental conditions in Sheffield (2016–2017) to compare growth among grasses with C3/C4 photosynthesis and annual vs perennial life histories. Data include dry biomass for roots and leaves, counts of roots/leaves/branches, leaf anatomical characteristics, phylogenetic relationships, and related metadata. Related to Wade et al. (2020) in New Phytologist.

## What the data include

- Growth measurements from a controlled, multi-part experiment on 74 grass species across C3/C4 and annual/perennial groups.
- Datasets and analyses capture:
  - Biomass and morphology: leaf and shoot dry masses, leaf area, total root mass, root length/area/diameter, tiller counts, shoot length, and overall plant biomass.
  - Growth dynamics: daily/weekly counts and measurements across five weeks, including germination date, transplanting, partial mortality, and replacement of some seedlings.
  - Root architecture: primary/secondary roots, total root tips, forks, and root depth; image-based root metrics (WinRHIZO, WinDIAS).
  - Leaf anatomy: tissue areas per segment (epidermis, fibres, mesophyll, veins, bundle sheath tissues) with per-vein normalisation and leaf-wide scaling.
  - Phylogeny: relationships among species using chloroplast markers for downstream comparative analyses.

## Experimental design and sampling

- Species and sampling:
  - 74 grass species from BOP (C3) and PACMAD lineages; sampling includes 12 independent C4 lineages and 20 annual lineages (with many C4-annual combinations).
  - Seeds obtained from public germplasm collections; multiple pairs of annual vs perennial within lineages; short-lived perennials treated as annuals for this study.
- Growth conditions:
  - Controlled environment chambers with randomised block design (8 trolleys per chamber).
  - 14-hour daylength, 30/25°C day/night, ~80% humidity, PPFD ~1056 μmol m^-2 s^-1.
  - Automated watering and periodic nitrate-type nutrient supplementation.
- Plant handling:
  - Seeds germinated in Petri dishes; 20 seedlings per species grown to transplant stage; approximately 10% initial mortality with 30% replacement.
  - Post-transplant growth and periodic harvesting over five weeks; analyses include both destructive and non-destructive measurements.

## Data collection methods

- Pre-transplant non-destructive measurements for 10 germinated seedlings per species.
- Weekly/descriptive counts:
  - Pre- and post-transplant counts of leaves, tillers, and main stem height.
  - At each harvest: roots cleaned; leaves, stems, and roots weighed separately (FM and DM where applicable); leaf area measured.
  - Image analyses for root architecture and leaf area; manual counts for primary roots.
- Tissue and anatomical measurements:
  - Leaf transverse sections from 86 grass species analyzed for vein density, epidermis, bundle sheath, fibres, and other tissues; per-segment measures normalised by vein count and scaled to whole leaf.
- Replication and drying:
  - Four plants per species harvested weekly per time point; half dried at 70°C for dry mass.

## Data files and formats

- SPECIES_INFORMATION.CSV
  - Fields include: species, seed_source, germplasm_accession, photosynthetic_pathway, clade, life_history.
- GROWTH_ANALYSIS_DATASET.CSV
  - Fields include: block, unique_code, experiment, species_name, germination_date, date_measured, no_days_growing, no_Leaves, no_Leaves_Main_Tiller, shoot_Length, no_tillers, root_depth, leaf_DM, Leaf_Area, SLA, shoot_DM, total_root_DM, total_plant_biomass_DM, yield_DM, total_root_length, total_root_surface_area, total_root_diameter, total_root_forks, total_root_tip, shoot_FM, total_root_FM, yield_FM, total_biomass_FM, total_seminal_roots, total_second_roots, life_history, photosynthetic_pathway, clade, lineage.
- LEAF_SUPPORT_DATASET.CSV
  - Fields include: Species, LH (life history), Phototype (photosynthetic pathway), Total_vein_no, Leaf_width_mm, segment_nb_veins, E (epidermis area), F (fibres area), M (mesophyll area), OS (outer bundle sheath), IS (inner bundle sheath), V (vascular tissue), extensions (bundle sheath extension).
- Phylogeny data
  - For growth analysis: concatenated_combined.tre
  - For LEAF_SUPPORT analysis: gpwg4.tre
- Notes on provenance:
  - Phylogeny reconstruction used cpDNA markers trnK-matK, rbcL, ndhF, trnL-trnF; sequences sourced from NCBI or generated via Sanger sequencing; alignments with MUSCLE; BEAST v1.8.4 analysis with GTR+G+I, relaxed clock, Yule prior.
  - Cross-section leaf data linked to Christin et al. (2013) dataset for vein/mesophyll tissues.

## Provenance and licensing

- Data created from a formal plant growth experiment funded by NERC (NE/N003152/1) and linked to Wade et al. (2020) in New Phytologist.
- Licensing: Open Government Licence (OGL); proper citation required as specified above.
- Data references: Christin et al. (2013) for leaf anatomy reference; Wade et al. (2020) for growth morphogenesis analyses.

## Practical considerations for data support and reuse

- Reuse potential:
  - Suitable for phylogenetic comparative analyses of growth rates, morphogenesis, and tissue investment strategies in grasses.
  - Rich, multi-modal data: longitudinal growth, biomass components, root architecture, leaf anatomy, and phylogeny enable integrated analyses.
- Data quality and harmonisation:
  - Longitudinal measurements require careful alignment by date_measured and experiment block.
  - Unit consistency across datasets (DM, FM, cm, mm) is essential; verify cross-dataset joins via unique codes.
- Limitations and context:
  - Experimental conditions are controlled environments; extrapolation to field conditions should be done cautiously.
  - Mortality and seed replacement are documented; consider these factors in analyses of early growth stages.
  - Subsets of data (e.g., leaf anatomy) rely on external datasets and methods; align to referenced protocols when integrating.
- Citation and use:
  - Data users must cite Wade et al. (2020) and the dataset DOI; also acknowledge Christin et al. (2013) for leaf anatomy references where applicable.