# Flower density values of common British plant species [AgriLand]

## Overview
- A dataset of flower density values for common British plant species collected during field surveys in 2011–2012, UK.
- Part of the UK IPI AgriLand project (grant BB/H014934/1); dataset creation completed in 2015.
- Data responsibility: Mathilde Baude, Bill Kunin, and Jane Memmott.
- Data format: CSV with three spreadsheets (herbs, trees, per-species) and accompanying metadata.
- Fieldwork largely conducted in southern England (e.g., Bristol area); one to two populations per species, five quadrats per population.

## Data structure and content
- Spreadsheet 1: AgriLand_FlowerDensity_herbs.csv
  - 1380 observations, 169 species, 22 columns.
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency.
  - Flower metrics per quadrat: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units, flowers per floral unit (buds/opened/fruited), cross-points, vegetative.area, flowers per opened floral unit, total flowers, flowers per m2 (opened and total).
- Spreadsheet 2: AgriLand_FlowerDensity_trees.csv
  - 85 observations, 10 species, 27 columns.
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency.
  - Tree height metrics: distance.m, top.tree.height, top.trunk.height, bottom.tree, height.of.tree.
  - Flower metrics: flower.distribution (subjective), mean.flower.distribution, nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units, extrapolated totals, vegetative.area, flowers per m2 (opened and total).
- Spreadsheet 3: AgriLand_FlowerDensity_perspecies.csv
  - 179 species, 15 columns.
  - For each species: FU.category; nb.of.open.flowers.per.floral.unit (mean, variance, n); nb.of.total.flowers.per.floral.unit (mean, variance, n); nb.of.open.flowers.per.m².of.vegetative.cover (mean, variance, n); nb.of.open.flowers.per.m².at peak flowering (mean, variance, n); nb.of.total.flowers.per.m².of.vegetative.cover (mean, variance, n).

## Field survey details
- Field period: February–October in 2011 and 2012.
- Location: predominantly south of England (including Bristol, UK).
- Sampling: for each species, 5 quadrats per population; 1–2 populations per species when possible.
- Total sampling per species: median 10 quadrats; range 1–20 quadrats.
- Floral units counted per quadrat to estimate flowers per floral unit.

## Species list and sampling regime
- Species list derived from the UK Countryside Survey 2007; focused on species likely rewarding pollinators.
  - Initial list: 270 species (270 total including locally important species).
  - 220 species selected as potentially pollinator-rewarding (insect-pollinated plus some wind/self-pollinated with flowers).
  - 50 additional locally important species included.
- Field sampling aimed to cover a representative subset of the surveyed flora per species.

## Data collection, generation, transformation, and analytical methods
- Field collection methods:
  - Herbs/shrubs: 0.5 m x 0.5 m quadrats; count floral units in buds, opened, and fruited states; estimate vegetative cover via cross-points (0.25 m² units; max 36 points).
  - Trees: 0.5 m x 0.5 m x 0.5 m cubic sample on outer foliage; estimate flowers per cubic sample; extrapolate to whole tree using tree height and distribution of flowers along the foliage.
- Calculations:
  - Vegetative cover area: cross-points × 0.25 / 36.
  - Total flowers per floral unit: buds + opened + fruited flowers.
  - Total floral units: buds + opened + fruited units.
  - Flowers per m² of vegetative cover: flowers ÷ vegetative area.
  - Tree height: height = [(a+c)/100] × distance − [(b+c)/100] × distance, using inclinometer measurements.
  - Total flowers in whole tree column: (number of floral units counted × tree height / 0.5) × percentage distribution across inner/outer foliage.
  - Species-level metrics: mean, variance, and sample size for density of flowers per m² (per quadrats), per species, computed from quadrat data.
- Data quality and transparency:
  - Clear definitions of floral units and distribution; explicit methods for extrapolation to whole trees.
  - Documentation of data sources and analytical steps; dataset associated with published references.

## Data quality, access, and usage notes
- Data responsibility and provenance documented (authors and grant).
- Measurements are interval-based with explicit units and calculation formulas; potential extrapolations (trees) noted.
- Field data limited to surveys from 2011–2012 in southern England; applicability to other regions may require caution.
- Datasets are structured to support analyses of pollinator nectar resources and cross-species comparisons of flower density.

## References
- Baude et al. 2015. Britain in bloom: national-scale changes in nectar resources for pollinators (in revision).
- Carey et al. 2008. Countryside Survey: UK Results from 2007. CEH/NERC, 105 pp.