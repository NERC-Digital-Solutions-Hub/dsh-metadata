# Growth rates of grass species with contrasting photosynthetic pathways and life histories

## Overview
- A dataset from a controlled plant growth experiment examining growth differences among grasses with C3 vs C4 photosynthesis and annual vs perennial life histories.
- Contains sequential biomass harvests, including dry biomass of roots and leaves, and counts of roots, leaves, and shoot branches.
- Includes an independent dataset of leaf anatomical characteristics and phylogenetic relationships among species.
- Funded by NERC and connected to Wade et al. (2020) in New Phytologist.
- Available under the Open Government Licence (OGL); attribution required when cited.

## What data are included
- Growth and morphology data for 74 grass species grown under controlled conditions.
- Measurements cover: root and shoot biomass, leaf area, plant height, tiller counts, root architecture metrics, and leaf anatomical traits.
- Leaf anatomy dataset provides cross-sectional tissue areas (veins, epidermis, bundle sheath, mesophyll, fibers) normalized per leaf and scaled to total leaf vein counts.
- Phylogenetic data to support comparative analyses across species.

## Experimental design and sampling
- Phylogenetic comparative analysis across 74 species from Poaceae, spanning BOP (predominantly C3) and PACMAD lineages (includes many C4 lineages).
- Stratified sampling to maximize diversity of C4 lineages and their C3 sister groups; included multiple pairs of annual vs perennial within lineages.
- Seeds sourced from public germplasm collections; short-lived perennials treated as annuals for the study.
- 12 independent C4 lineages and 20 monophyletic annual groups; nine annual lineages included C4 lineages.
- Pre-germination treatments, germination in Petri dishes, transplantation into 2 L pots with vermiculite/sand mix.

## Data collection and measurements
- Growth conditions: controlled environment chambers with 14 h photoperiod, 30/25°C day/night, ~80% humidity, PPFD ~1056 μmol m^-2 s^-1.
- Watering: automatic deionised water irrigation; nitrate-type nutrient solution supplied regularly.
- Data collection timeline: three staggered experiments with weekly harvests over five weeks; germination date recorded; non-destructive measurements taken pre-transplant.
- Post-transplant measurements: total leaves, leaves on main tiller, number of tillers, main stem height.
- Harvesting: four plants per species per timepoint; roots washed; biomass weighed as fresh mass (FM) and dry mass (DM).
- Morphometrics: leaf area, specific leaf area (SLA), total root length, surface area, diameter, number of forks/tips; shoot and root biomass; total plant biomass and flowering part mass.
- Root architecture: analysis via WinRHIZO; primary vs secondary roots distinguished; seedling morphology recorded.
- Leaf anatomy: analysis of leaf veins, epidermis, bundle sheath, mesophyll, fibers; scaling to whole leaf using vein counts per leaf.
- Data processing: image analysis of leaf sections; normalization by vein number; leaf width measurements from cleared/stained leaves.

## Data processing and analysis
- Phylogeny reconstruction: chloroplast markers trnK-matK, rbcL, ndhF, trnL-trnF; sequences sourced from NCBI, amplified/sequenced as needed.
- Sequence alignment with MUSCLE; concatenated markers; time-calibrated phylogeny with BEAST 1.8.4 under GTR+G+I; Yule speciation prior; relaxed molecular clock; monophyly constraints for BOP and PACMAD.
- Two analyses run (10,000,000 generations; burn-in 5,000,000); convergence checked with Tracer; posterior trees combined for median ages on the reference tree.
- The cross-section leaf dataset uses a previously published phylogeny (Christin et al., 2013).

## Data structure and files
- SPECIES_INFORMATION.CSV: species name, seed source, germplasm accession, photosynthetic pathway, clade, life history.
- GROWTH_ANALYSIS_DATASET.CSV: block, unique plant code, experiment, species, germination date, measurement dates, days grown, leaf counts, shoot length, tillers, root depth, leaf/projected biomass and area metrics, SLA, total biomass, yield, root architecture metrics, tissue counts, life history, photosynthetic pathway, lineage.
- LEAF_SUPPORT_DATASET.CSV: species, life history, photosynthetic pathway, leaf vein counts, leaf width, vein segment details, area measurements for epidermis, fibers, mesophyll, vascular tissue, bundle sheath extensions.
- Phylogeny files used: concatenated_combined.tre (GROWTH_ANALYSIS_DATASET) and gpwg4.tre (LEAF_SUPPORT_DATASET).

## Access, use and licensing
- Data available under the Open Government Licence (OGL) at the provided DOI link.
- Users must cite: Wade, R.N.; Seed, P.; McLaren, E.; Wood, E.; Christin, P.A.; Thompson, K.; Rees, M.; Osborne, C.P. (2020). Growth rates of grass species with contrasting photosynthetic pathways and life histories. NERC Environmental Information Data Centre. Dataset. DOI.
- Dataset related to Wade et al. (2020) publication in New Phytologist.

## Provenance and references
- Christin, P.-A. et al. (2013) Anatomical enablers and the evolution of C4 photosynthesis in grasses. PNAS.
- Wade, R.N. et al. (2020) The morphogenesis of fast growth in plants. New Phytologist (dataset context).