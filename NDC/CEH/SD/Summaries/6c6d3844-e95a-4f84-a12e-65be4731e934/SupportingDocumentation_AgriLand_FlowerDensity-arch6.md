# Flower density values of common British plant species [AgriLand]

## Data overview
- Data name: Flower density values of common British plant species [AgriLand]
- Data format: CSV (three spreadsheets)
- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
- Project: UK IPI AgriLand grant BB/H014934/1
- Data collection period: 2011–2012; Dataset creation: 2015
- Field surveys conducted mainly in the south of England (Bristol, UK)
- Purpose: Estimate flower density and floral resources per species to support pollinator resource assessments
- Access and contact: Provided via project authors (emails listed in dataset description)

## Data structure and fields
- Spreadsheet 1: AgriLand_FlowerDensity_herbs.csv
  - Observations: 1380
  - Species: 169
  - Columns: 22 (example columns include species, date, hour, location, habitat, FU.category, year, quadrat.no.independency, counts of buds/opened/fruited floral units, flowers per floral unit, cross points, vegetative.area, opened/total flowers per m2, etc.)
- Spreadsheet 2: AgriLand_FlowerDensity_trees.csv
  - Observations: 85
  - Species: 10
  - Columns: 27 (example columns include species, date, hour, location, habitat, FU.category, year, quadrat.no.independency, distance.m, top.tree.height, top.trunk.height, bottom.tree, height.of.tree, flower.distribution, mean.flower.distribution, counts of buds/opened/fruited floral units, vegetative.area, flowers per m2, etc.)
- Spreadsheet 3: AgriLand_FlowerDensity_perspecies.csv
  - Species: 179
  - Columns: 15 (per-species statistics; FU.category; nb.of.open.flowers.per.floral.unit [mean, var, n]; nb.of.total.flowers.per.floral.unit [mean, var, n]; nb.of.open.flowers.per.m².of.vegetative.cover [mean, var, n]; nb.of.open.flowers.per.m².of.vegetative.cover.at.the.peak.of.flowering.season [mean, var, n]; nb.of.total.flowers.per.m².of.vegetative.cover [mean, var, n])
- Key data points cover:
  - Herbs: flower counts per floral unit, number of floral units in buds/opened/fruited states, vegetative cover, and derived densities (flowers per m2, total flowers, etc.)
  - Trees: 3D sampling unit (cube 0.5m x 0.5m x 0.5m), height and distribution estimates, counts of floral units, vegetative cover, and derived densities
  - Per-species: mean/variance/n for several density metrics per floral unit and per m² of vegetative cover, including peak-flowering-season estimates

## Methods and data collection
- Field surveys
  - Timeframe: February–October 2011–2012
  - Location: Predominantly south of England (Bristol area)
  - Design: For each species, 1–2 field populations in 1–2 locations; five quadrats per population; total per species: median 10 quadrats (range 1–20)
- Sampling regime
  - Herbs and shrubs: 0.5 m x 0.5 m quadrats; estimate vegetative cover via cross-points (36 points for 0.25 m²); count floral units in buds, opened, and fruited states; count flowers per floral unit
  - Trees: 3D cube sampling (0.5 m per side) around outer foliage with many flowers; extrapolate to whole tree using inclinometer height measurements and distribution class
- Collection/Transformation
  - Vegetative cover area calculated from cross-points
  - Floral unit tallies: buds, opened, fruited; total counts computed from unit counts and per-unit flowers
  - Height of trees derived from inclinometer readings (top, trunk, bottom) and distance
  - Whole-tree flower totals derived from counts in the 3D cube, tree height, and estimated distribution inside the foliage
- Analytical methods
  - Convert cross-point data to vegetative area (0.25 m² per plot, with 36 points)
  - Compute total flowers per opened floral unit and per floral unit
  - Derive flowers per m² of vegetative cover
  - For trees, estimate total flowers in the entire column using height and distribution percentage
  - Summary statistics (mean, variance, sample size) computed for flower density per species

## Data quality, provenance, and notes
- Data responsibility and project context provided (Baude, Kunin, Memmott; UK IPI AgriLand)
- Field collection methods and formulas explicitly described; includes supplementary methods referenced (Baude et al. 2015)
- Species selection based on UK Countryside Survey 2007 (454 species to survey; expanded with locally important species to 270 total)
- Data limitations
  - Field sampling uses a standardized but relatively sparse set of quadrats per species; some variability in habitat and location
  - Tree flower density relies on distribution estimates and inclinometer-derived height, introducing estimation variability
- References
  - Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators)
  - Carey et al. 2008 (Countryside Survey: UK Results from 2007)

## How to use and potential data products
- Self-serve data products
  - Species-level flower density summaries (per m² of vegetative cover and per floral unit)
  - Habitat- and location-based comparisons of flower density
  - Tree vs. herb/shrub floral resource comparisons across species
  - Peak-flowering-season estimates per species
- Data integration and reuse
  - Combine with pollinator visitation data or phenology data for ecosystem service analyses
  - Cross-wile sharing (CSV format facilitates integration with dashboards, pivot tables, or GIS outputs)
- Quality assurance and dissemination
  - Validate species-specific density metrics using per-species summary data
  - Share outputs with collaborators and policymakers to promote data reuse and visibility

## References
- Baude, M., et al. 2015. Britain in bloom: national-scale changes in nectar resources for pollinators (in revision)
- Carey, P.D., et al. 2008. Countryside Survey: UK Results from 2007. CEH/NERC, 105pp