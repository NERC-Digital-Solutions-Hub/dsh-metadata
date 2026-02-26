# Flower density values of common British plant species [AgriLand]

## Overview
- Purpose: standardized flower density data for common British plant species to monitor environmental health and pollinator resources over time.
- Source: UK IPI AgriLand project; field surveys conducted 2011–2012 in southern England; dataset creation in 2015.
- Stewardship: multiple institutions and researchers responsible for data collection and integrity (see Data responsibility).

## Data structure
- Three CSV spreadsheets:
  - AgriLand_FlowerDensity_herbs.csv (flower number in quadrats for herbs)
  - AgriLand_FlowerDensity_trees.csv (flower number in quadrats for trees)
  - AgriLand_FlowerDensity_perspecies.csv (flower density per species)
- Herb sheet (1360+ observations across 169 species, 22 columns) includes:
  - metadata: species, date, hour, location, habitat, FU.category, year
  - quadrat-level counts: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units
  - unit-level metrics: nb.of.buds.per.opened.floral.unit, nb.of.opened.flowers.per.opened.floral.unit, nb.of.fruited.flowers.per.opened.floral.unit
  - vegetation cover and density fields: cross.points, vegetative.area, nb.of.opened.flowers.per.m2, nb.of.total.flowers.per.m2
- Tree sheet (85 observations across 10 species, 27 columns) includes:
  - metadata: species, date, hour, location, habitat, FU.category, year
  - height data from inclinometer readings, distance, and top/bottom measurements
  - 3D cube counts: nb.of.floral.units.in.buds, nb.of.opened.floral.units, nb.of.fruited.floral.units
  - distribution and area metrics: flower.distribution, mean.flower.distribution, vegetative.area, nb.of.opened.flowers.per.m2, nb.of.total.flowers.per.m2
- Per-species sheet (179 species, 15 columns) includes:
  - species-level statistics: nb.of.open.flowers.per.floral.unit (mean, var, n), nb.of.total.flowers.per.floral.unit (mean, var, n), nb.of.open.flowers.per.m².of.vegetative.cover (mean, var, n), nb.of.open.flowers.per.m².of.vegetative.cover.at.the.peak..., nb.of.total.flowers.per.m².of.vegetative.cover (mean, var, n)

## Field survey and sampling regime
- Field period: February–October 2011 and 2012; most sites in southern England (e.g., Bristol region).
- Populations: one or two field populations per species, in one or two locations.
- Sampling design: 5 quadrats per population; 2 populations per species when possible; total per species typically median 10 quadrats (range 1–20).
- Floral counts: within each quadrat, count flowers from one floral unit to estimate flowers per floral unit.

## Measurements and units
- Quadrats for herbs and shrubs: 0.5 m × 0.5 m; vegetative cover estimated via cross-points (up to 36 points for 0.25 m²).
- Floral units: counts of buds, opened, and fruited floral units per quadrat; includes per-floral-unit flower counts.
- Trees: 3D cube method (0.5 m × 0.5 m × 0.5 m) placed on outer, flowering foliage; height extrapolated from inclinometer readings and foliage distribution.
- Vegetative cover: calculated from cross-points and surface area considerations; density metrics expressed as flowers per m² of vegetative cover.
- Flower density metrics: both per floral unit and per m² of vegetative cover; includes peak-season estimates.

## Calculations and transformations
- Vegetative area: cross.points × 0.25 / 36.
- Total flowers per floral unit: buds + opened + fruited.
- Total floral units: buds + opened floral units + fruited floral units.
- Flowers per m² of vegetative cover: total flowers divided by vegetative area.
- Tree height: derived from inclinometer readings (top, trunk, bottom) at known distance.
- Total flowers in whole tree column: (floral units counted × tree height / 0.5) × flower distribution percentage.
- Summary statistics: mean, variance, and sample size calculated for flower density (flowers/m²) per species.

## Species list and sampling rationale
- Initial list: 270 species (derived from Countryside Survey 2007) to cover species with substantial vegetative cover and pollinator relevance.
- Selection: 220 pollinator-relevant species (insect-pollinated and some wind/self-pollinated with flowers), plus 50 locally important species.

## Provenance and references
- Data provenance: AgriLand project data; field surveys 2011–2012; dataset creation 2015.
- Primary references:
  - Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators)
  - Carey et al. 2008 (Countryside Survey UK Results from 2007)

## Data responsibility
- Principal contacts: Mathilde Baude (mathilde.baude@univ-orleans.fr), Bill Kunin (W.E.Kunin@leeds.ac.uk), Jane Memmott (jane.memmott@univ-bristol.ac.uk)
- Data collection and validation aligned with project grant BB/H014934/1.

## Relevance for environmental monitoring analysts
- Delivers standardized, QA-supported floral resource data suitable for integrating with other environmental datasets.
- Provides detailed, site- and species-level measurements enabling temporal comparisons and policy performance assessments.
- Ensures data traceability through explicit definitions, units, and computational methods, facilitating reuse and interoperability.