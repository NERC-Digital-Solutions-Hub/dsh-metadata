# Flower density values of common British plant species [AgriLand]

## Overview
- Dataset documenting flower density values for common British plant species, part of the UK IPI AgriLand project (BB/H014934/1).
- Field data collected in 2011–2012; dataset created in 2015.
- Delivered as three CSV spreadsheets; data responsibility shared among Mathilde Baude, Bill Kunin, Jane Memmott, and others.
- Aimed at informing pollinator resource assessments and environmental monitoring, with clear definitions of variables and measurement methods.

## Dataset structure and contents
- Spreadsheet 1: AgriLand_FlowerDensity_herbs.csv
  - 1380 observations; 169 species; 22 columns
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency
  - Measurements per floral unit: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units
  - Derived metrics: vegetative.area, nb.of.opened.flowers.per.floral.unit, nb.of.total.flowers.per.floral.unit, nb.of.opened.flowers.per.m2, nb.of.total.flowers.per.m2
- Spreadsheet 2: AgriLand_FlowerDensity_trees.csv
  - 85 observations; 10 species; 27 columns
  - Measurements per quadrat/tree: distance.m, top.tree.height, top.trunk.height, bottom.tree, height.of.tree, flower.distribution, mean.flower.distribution
  - Counts per floral unit and extrapolated totals: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units, nb.of.buds.per.opened.floral.unit, nb.of.opened.flowers.per.opened.floral.unit, nb.of.total.flowers.per.m2, nb.of.opened.flowers.per.m2
- Spreadsheet 3: AgriLand_FlowerDensity_perspecies.csv
  - 179 species; 15 columns
  - Per-species metrics: nb.of.open.flowers.per.floral.unit (mean, var, n), nb.of.total.flowers.per.floral.unit (mean, var, n), nb.of.open.flowers.per.m².of.vegetative.cover (mean, var, n), nb.of.open.flowers.per.m².of.vegetative.cover.at.the.peak (mean, var, n), nb.of.total.flowers.per.m².of.vegetative.cover (mean, var, n)

## Field survey and scope
- Field surveys conducted February–October in 2011 and 2012.
- Study area mainly in southern England (e.g., Bristol).
- For each species: one or two field populations in one or two locations were monitored.

## Species list and sampling plan
- Initial list built from UK Countryside Survey 2007; focused on species likely rewarding pollinators.
- 270 species targeted (approximately 220 insect-pollinated and related), plus 50 locally important species.
- Sampling regime: 5 quadrats per population; 2 populations per species when possible.
- Total sampling per species: median 10 quadrats (range 1–20).
- Flower counts conducted on one floral unit per quadrat.

## Data collection, generation and transformation
- Vegetative cover estimated using 0.5 m x 0.5 m quadrats; cross-point method (up to 36 points for 0.25 m²).
- Floral units: counts of buds, opened, and fruited units within each quadrat; floral units defined as an entity comprising one or more flowers accessible to insects.
- Trees: flowers counted in a 0.5 m x 0.5 m x 0.5 m cube on outer foliage; extrapolated to whole tree using height measurements from an inclinometer and distribution estimates along the canopy.

## Analytical methods and metrics
- Vegetative cover area calculated as cross-points × 0.25 / 36.
- Total flowers per opened floral unit = buds + opened + fruited flowers.
- Total floral units = buds + opened + fruited units.
- Flowers per m² of vegetative cover = total flowers divided by vegetative area.
- Tree height estimated with inclinometer data: height = [(a+c)/100] × d − [(b+c)/100] × d (where a, b, c are inclinometer readings and d is distance).
- Total flowers in the whole tree column estimated from 3D cube counts, height, and estimated distribution.
- For each species: compute mean, variance, and sample size of flower density (flowers per m²) across quadrats.

## Data quality, metadata and accessibility
- Metadata included in spreadsheet descriptions (variable definitions, data units, and measurement context).
- Data responsibilities and project funding clearly identified; dataset creation date provided.
- Data are presented as CSV files suitable for reuse in monitoring analyses and dashboards.

## Relevance for policy monitoring and environmental health evaluation
- Provides standardized, transparent measures of floral resource availability critical for assessing pollinator resources and habitat quality.
- Facilitates cross-site comparability via defined quadrat methods, floral unit concepts, and density calculations.
- Supports trend analysis and scenario evaluation in monitoring frameworks, with explicit data collection procedures and derived metrics.

## References
- Baude et al. 2015. Britain in bloom: national-scale changes in nectar resources for pollinators (in revision).
- Carey et al. 2008. Countryside Survey: UK Results from 2007. NERC/CEH.