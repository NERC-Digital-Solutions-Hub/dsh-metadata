# Growth rates of grass species with contrasting photosynthetic pathways and life histories

## Overview
- Publicly available dataset from plant growth experiments in Sheffield (2016–2017) to compare growth among grasses with C3 vs C4 photosynthesis and annual vs perennial life histories.
- Uses phylogenetic comparative analyses across 74 grass species to explore morphogenesis of fast growth.
- Related to Wade et al. (2020) in New Phytologist; funded by NERC.

## Experimental design and sampling
- Stratified sampling across BOP lineage (C3) and PACMAD lineage (includes C4 lineages).
- 74 species: 12 independent C4 lineages and 20 monophyletic annual grass groups; includes several C4/C3 and annual/perennial combos.
- Seeds from public germplasm collections; germinated and transplanted to 2 L pots in a controlled environment.
- Growth conditions: 14 h daylength; 30 °C day / 25 °C night; ~80% humidity; average PPFD ~1056 μmol m−2 s−1.
- Approximately 10% early mortality; 30% of dead seedlings replaced.
- Experimental structure included randomized block design across eight chambers/trolleys.

## Data collection and collection methods
- Three time-staggered experiments; germination date recorded.
- Pre-transplant: non-destructive measurements on 10 seedlings per species.
- Post-transplant: weekly counts of leaves and tillers; main stem height measured weekly.
- Harvests: four plants per species harvested weekly for five weeks; measurements include fresh and dry mass of leaves, stems, and roots; root washing and separation of plant parts.
- Morphometrics: leaf area, total root length, surface area, diameter, forks, tips; image analysis (WinRHIZO, WinDIAS) for root and leaf metrics.
- Phytomere metrics: shoot/root biomass per leaf/tiller counts.
- Structural anatomy: leaf cross-sections from herbarium-derived data to quantify vein, epidermis, bundle sheath, mesophyll, fibres; normalization per vein to scale to whole leaf.
- Data used to test relationships between mechanical support tissue investments and leaf size.

## Datasets and data structure
- SPECIES_INFORMATION.CSV: species name, seed source, germplasm accession, photosynthetic pathway, clade, life history.
- GROWTH_ANALYSIS_DATASET.CSV: plant-level measurements including experiment/block identifiers, germination date, dates of measurement, growth metrics (leaves, tillers, shoot/root measurements), biomass (fresh and dry), leaf area, SLA, yield, root system metrics, seminal/primary vs secondary roots, lineage and photosynthetic pathway.
- LEAF_SUPPORT_DATASET.CSV: leaf structural data per species including life history, photosynthetic pathway, vein counts, leaf width, epidermis, fibres, mesophyll, and vascular tissue areas.
- Phylogenies:
  - GROWTH_ANALYSIS_DATASET uses concatenated_phylogeny: concatenated_combined.tre
  - LEAF_SUPPORT_DATASET uses gpwg4.tre
- Related literature and datasets: cross-referenced with Christin et al. (2013) for leaf anatomy and Wade et al. (2020) for growth morphogenesis.

## Phylogenetics and analysis
- Phylogeny built from four chloroplast markers: trnK-matK, rbcL, ndhF, trnL-trnF.
- Data assembled from NCBI and Sanger sequencing where needed; alignments with MUSCLE; concatenated and time-calibrated with BEAST v1.8.4.
- Model: GTR+G+I; relaxed molecular clock; Yule speciation prior; monophyly of BOP and PACMAD enforced; divergence constrained with normally distributed prior.
- Two separate analyses (growth and leaf support) referenced to different phylogenies for downstream comparative analyses.

## Licensing and access
- Open Government Licence (OGL) for dataset access.
- Required citation: Wade, R.N.; et al. (2020). Growth rates of grass species with contrasting photosynthetic pathways and life histories. NERC Environmental Information Data Centre (Dataset). DOI provided.
- Data linked to the Wade et al. (2020) New Phytologist publication; funded by NERC NE/N003152/1.

## Data quality, governance, and workflow
- Rigorous experimental controls and replication (four plants per species per harvest; weekly measurements;ミortality managed with replacements).
- Pre- and post-transplant measurement regime ensures robust growth trajectories.
- Comprehensive metadata across species, experiments, and datasets to support reproducibility and cross-study comparability.
- Clear data governance through open licensing and explicit citation requirements.

## Relevance for monitoring, policy, and frameworks
- Demonstrates integration of multi-dimensional phenotypic data with phylogeny to interpret growth performance across lineages, informing indicators of plant productivity and structural investment.
- Provides openly available, well-documented datasets suitable for monitoring frameworks seeking transparent, reproducible environmental biology indicators.
- Highlights data provenance, cross-dataset interoperability, and governance practices needed to support monitoring decisions and future decision-making in plant and ecosystem health research.