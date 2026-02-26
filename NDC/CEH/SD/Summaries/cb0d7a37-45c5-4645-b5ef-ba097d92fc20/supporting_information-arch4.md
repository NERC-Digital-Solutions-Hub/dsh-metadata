# Growth rates of grass species with contrasting photosynthetic pathways and life histories

- Purpose and scope
  - A dataset from controlled-environment growth experiments (2016–2017) to compare growth rates among grasses with C3 vs C4 photosynthesis and annual vs perennial life histories.
  - Includes sequential biomass harvests, above/below-ground biomass, and plant architectural traits, plus leaf anatomy and phylogenetic relationships.
  - Aimed at testing morphogenic bases for differential growth rates across lineages and life histories; linked to a New Phytologist publication (Wade et al., 2020).

- Data access and licensing
  - Available under the Open Government Licence (OGL).
  - Citation required: Wade et al. (2020). The growth rates study dataset; NERC Environmental Information Data Centre.
  - DOI provided for dataset access and reuse.

- Content and structure of the dataset
  - Growth data (GROWTH_ANALYSIS_DATASET.CSV)
    - Experimental blocks, species, germination date, dates of measurement, days grown.
    - Morphological measurements: leaves, leaves on main tiller, tillers, shoot length.
    - Biomass and mass metrics: leaf/ shoot/root fresh and dry masses, total plant biomass, flowering part biomass, root depth, root system metrics (length, surface area, diameter, forks, tips), total root and shoot biomasses, and related metrics (SLA, leaf area, etc.).
    - Additional derived metrics: seedling germination, developmental counts, and reproductive yield.
  - Species metadata (SPECIES_INFORMATION.CSV)
    - Species name, seed source, germplasm accession, photosynthetic pathway, clade, and life history.
  - Leaf support anatomy (LEAF_SUPPORT_DATASET.CSV)
    - Leaf-level anatomical and tissue measures per leaf segment: vein counts, leaf width, epidermis, fibers, mesophyll, bundle sheath areas, and related tissue areas normalized per vein.
  - Phylogeny and lineage notes
    - Phylogenetic trees: concatenated_combined.tre for growth analyses; gpwg4.tre for leaf-support analyses.
    - Linkages to clades: BOP (C3) and PACMAD (C4) lineages, with multiple independent C4 lineages and C3 sister groups.
  - Ancillary references
    - Cross-referenced datasets and prior phylogenetic work (Christin et al., 2013) for leaf anatomy and phylogeny context.

- Experimental design and sampling
  - Stratified sampling of 74 Poaceae grasses across:
    - BOP lineage (C3) and PACMAD lineage (including 22–24 independent C4 lineages and C3 sister species).
    - 12 independent C4 lineages and 20 monophyletic annual groups; nine annual groups include C4 members.
  - Seed sourcing from public germplasm collections; multiple within-lineage samples (annual vs perennial) with random draws where choices existed.
  - Seed germination → transplant to 2 L pots in vermiculite/sand, randomized blocks, and controlled-environment chambers.
  - Growth conditions: 14 h photoperiod, 30/25 C day/night, ~80% humidity, PPFD ~1056 μmol m^-2 s^-1, automated irrigation, nitrate feeding.

- Data collection and measurement schedule
  - Pre-transplant: non-destructive measurements on germinated seedlings; counts of root tips and leaves daily until transplant.
  - Post-transplant: periodic counts of leaves, leaves on main tiller, tillers; weekly main stem height.
  - Harvest regime: four plants per species per time point harvested weekly for five weeks; roots washed; biomass separated into leaves, stems, roots; fresh mass measured; dry mass after drying.
  - Root and leaf architecture: image-based analysis (WinRHIZO, WinDIAS) for root length, surface area, diameter, forks, tips, and total leaf area.
  - Additional structural data: primary vs secondary roots counted; tissue and vein investments assessed in cleared leaf sections.
  - Data integrity: some seedling mortality (~10%) with 30% replacement; standardised measurement protocols across experiments.

- Analytical and phylogenetic methods
  - Phylogeny reconstruction using chloroplast markers (trnK-matK, rbcL, ndhF, trnL-trnF); sequence retrieval, alignment (MUSCLE), concatenation, and time-calibrated BEAST analyses (GTR+G+I, Yule prior, relaxed clock).
  - Tree validation with convergence checks (Tracer), posterior tree sampling, and mapping of median ages onto a reference tree.
  - Leaf anatomy data linked to Christin et al. (2013) as supplementary phylogeny context for cross-section analyses.

- Data quality, standards, and reuse
  - Detailed variable definitions and units provided for robust reuse and cross-study comparability.
  - Clear separation of growth, leaf anatomy, and phylogeny datasets supports modular analyses and integration with other data sources.
  - Open licensing and explicit citation requirements promote traceability and attribution.

- Potential uses for data leaders
  - Assess data provenance, licensing, and metadata completeness in a high-quality, openly licensed dataset.
  - Integrate with internal data ecosystems to compare plant growth metrics across lineages, photosynthetic pathways, and life histories.
  - Use the phylogeny-informed framework to align organizational data products with external datasets, ensuring reproducibility (phylogenetic context, measurement protocols, and metadata).
  - Demonstrate governance best practices: licensing, data schemas, and cross-dataset linkage (growth metrics, leaf anatomy, and phylogeny) for complex data products.

- Related publications
  - Wade, R.N. et al. (2020). Growth rates of grasses with contrasting photosynthetic pathways and life histories. New Phytologist (dataset reference to the corresponding publication).
  - Christin, P.-A. et al. (2013). Anatomical enablers and the evolution of C4 photosynthesis in grasses. PNAS (leaf anatomy and phylogeny context).