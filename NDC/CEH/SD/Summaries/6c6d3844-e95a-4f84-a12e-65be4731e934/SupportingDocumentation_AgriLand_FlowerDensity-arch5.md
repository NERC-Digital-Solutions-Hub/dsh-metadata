# Dataset information

- Data name: Flower density values of common British plant species [AgriLand]
- Data description: Flower density values of common British plant species
- Data format: CSV (3 spreadsheets)
  - AgriLand_FlowerDensity_herbs.csv
  - AgriLand_FlowerDensity_trees.csv
  - AgriLand_FlowerDensity_perspecies.csv
- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
- Project name: UK IPI AgriLand grant BB/H014934/1
- Data collection: 2011/2012
- Dataset creation: 2015

## Details of data structure

- Spreadsheet 1: flower number in quadrat herbs (AgriLand_FlowerDensity_herbs.csv)
  - 1380 observations, 169 species, 22 columns
  - Key fields and concepts: species, date, hour, location, habitat, FU.category (floral unit), year, quadrat.no.independency
  - Floral-unit related counts: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units
  - Flower counts per unit: nb.of.buds.per.opened.floral.unit, nb.of.opened.flowers.per.opened.floral.unit, nb.of.fruited.flowers.per.opened.floral.unit
  - Vegetation and density measures: nb.of.cross.points, vegetative.area, nb.of.opened.flowers.per.m2, nb.of.total.flowers.per.m2
- Spreadsheet 2: flower number in quadrats for trees (AgriLand_FlowerDensity_trees.csv)
  - 85 observations, 10 species, 27 columns
  - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency
  - Tree-height related measures: distance.m, top.tree.height, top.trunk.height, bottom.tree
  - Derived height: height.of.tree = [(a+c)/100]*d - [(b+c)/100]*d
  - Floral-unit counts and distribution: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units, flower distribution, mean.flower.distribution
  - Vegetation and density measures: nb.of.opened.flowers.per.m2, nb.of.total.flowers.per.m2
- Spreadsheet 3: flower density per species (AgriLand_FlowerDensity_perspecies.csv)
  - 179 species, 15 columns
  - Summary statistics per species for floral units and flowers: nb.of.open.flowers.per.floral.unit (mean, var, n), nb.of.total.flowers.per.floral.unit (mean, var, n)
  - Density metrics per vegetation cover: nb.of.open.flowers.per.m².of.vegetative.cover (mean, var, n), nb.of.open.flowers.per.m².of.vegetative.cover.at.the.peak..., nb.of.total.flowers.per.m².of.vegetative.cover (mean, var, n)

## Field survey and sampling design

- Field survey period: February–October 2011 and 2012
- Geographic focus: majority in southern England (Bristol, UK)
- Sampling regime per species:
  - 5 quadrats per population; 2 populations per species when possible
  - Total sampling per species: median 10 quadrats (range 1–20)
  - For each quadrat, count flowers from one floral unit to estimate flowers per floral unit
- Species list and selection:
  - 270 plant species initially selected (from Countryside Survey 2007 and pollinator relevance)
  - 220 species potentially rewarding for pollinators; 50 locally important species added
  - Focus on insect-pollinated plants and certain other flowering species

## Collection, generation, and transformation methods

- Quadrats and measurements (herbs/shrubs):
  - Quadrat size: 0.5 m x 0.5 m
  - Count floral units in buds, opened, and fruited states per quadrat
  - Estimate vegetative cover using cross-points (up to 36 points for 0.25 m²)
- Trees (3D extrapolation):
  - Floral units counted in a 0.5 m x 0.5 m x 0.5 m cube at outer foliage
  - Extrapolate to whole tree using tree height and distribution of flowers along foliage (0–20% to 80–100% distribution classes)
- Derived metrics and conversions:
  - Vegetative cover area: cross-points-based calculation
  - Flowers per opened floral unit; total flowers per floral unit; total floral units
  - Flowers per m² of vegetative cover
  - Tree height calculations using inclinometer readings (top, trunk, bottom) and distance
  - Whole-column flower estimates via height and distribution factor

## Analytical methods and formulas

- Vegetative cover area: cross-points × 0.25 / 36
- Total flowers in a column: as count per floral unit × height-based extrapolation
- Height calculation: H = [(a+c)/100]×d − [(b+c)/100]×d
- Whole-tree flower estimation: (number of floral units counted × tree height / 0.5) × percentage distribution
- Flower density per species: mean, variance, and n of flower density values from quadrats
- Reporting metrics: mean, variance, and sample size for density-related measures (per species and per floral unit)

## Provisions for governance, provenance, and references

- Data responsibility and team: multiple institutions and researchers listed (Baude, Kunin, Memmott)
- Project and grant references provided; data aligned with UK AgriLand and related projects
- References for methods and species selection:
  - Baude et al. 2015 (Britain in bloom)
  - Carey et al. 2008 (Countryside Survey UK results)
- Metadata scope evident in dataset documentation: detailed field descriptions, units, and column definitions across all sheets

## Considerations for data stewards

- Cross-sheet linkage: ensure consistent species naming, population identifiers, and quadrat numbering across herbs, trees, and per-species sheets
- Metadata completeness: maintain explicit definitions for all 22, 27, and 15 columns, including units and derivation notes
- Provenance tracking: capture data responsibility, collection dates, and transformation steps (especially height extrapolations and distribution assumptions)
- Access and re-use: dataset packaged with clear data responsibility and project context; verify licensing and sharing permissions for AgriLand-derived data
- Data quality and interoperability: address potential variations in measurement practices across populations and species; verify handling of incomplete or missing data
- Documentation continuity: preserve references and supplementary methods (Baude et al. 2015) for reproducibility and future reuse