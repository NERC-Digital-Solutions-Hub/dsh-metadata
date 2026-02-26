# Flower density values of common British plant species [AgriLand]

- Purpose and scope
  - A dataset of flower density values for common British plant species collected during field surveys in 2011–2012, with dataset creation completed in 2015.
  - Designed to support GIS-based analyses of floral resources for pollinators and related ecological studies.

- Data structure and formats
  - 3 CSV spreadsheets:
    - AgriLand_FlowerDensity_herbs.csv (herbs and shrubs, 2D)
      - 1380 observations, 169 species, 22 columns
      - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency
      - Flower metrics include counts of buds, opened, and fruited floral units; flowers per opened floral unit; cross-points for vegetative cover; flowers per m2 and total flowers per m2
    - AgriLand_FlowerDensity_trees.csv (trees, 3D)
      - 85 observations, 10 species, 27 columns
      - Key fields: species, date, hour, location, habitat, FU.category, year, quadrat.no.independency, distance.m, top.tree.height, top.trunk.height, bottom.tree, height.of.tree
      - Flower metrics include counts within a 0.5m x 0.5m x 0.5m cube, height extrapolation along tree foliage, and distribution of flowers within foliage
    - AgriLand_FlowerDensity_perspecies.csv (per-species)
      - 179 species, 15 columns
      - Metrics per species: mean, variance, and n for flowering metrics (e.g., nb.of.open.flowers.per.floral.unit; nb.of.total.flowers.per.floral.unit); mean/var/n for flowers per m2 of vegetative cover (overall and at peak flowering)
  - Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott

- Field survey design and sampling regime
  - Timeframe: Field surveys conducted Feb–Oct 2011–2012; sites mainly in southern England (e.g., Bristol region).
  - Species selection: Based on Countryside Survey 2007 data; targeted insect-pollinated plants plus some additional locally important species, totaling about 270 species initially; 220–270 species surveyed with 50 extra locally important species added.
  - Sampling intensity:
    - 5 quadrats per population to estimate flowers per square meter of vegetative cover
    - 2 populations per species when possible
    - Total sampling per species: median 10 quadrats (range 1–20)
    - For herbs: one floral unit counted per quadrat to estimate flowers per floral unit

- Data collection and transformation methods
  - Herbs and shrubs (2D):
    - Quadrat size: 0.5 m × 0.5 m
    - Vegetative cover estimated via cross-point method (0.25 m² reference, up to 36 cross-points)
    - Floral units counted in buds, opened, and fruited states
    - Floral unit definitions used to derive numbers of buds, opened, and fruited flowers; derived metrics include opened flowers per floral unit and total flowers per floral unit
  - Trees (3D):
    - Flowering units counted within a 0.5 m × 0.5 m × 0.5 m cube placed at outer canopy
    - Extrapolated to whole tree using height measurements (inclination-based estimates) and distribution of flowers along foliage
    - Flower distribution classes (0–20% biased to 80–100% homogeneous) recorded; mean distribution calculated
  - Vegetative cover and density:
    - Vegetative area calculated from cross-points: area = cross-points × 0.25 / 36
    - Density metrics include flowers per opened floral unit, total flowers per floral unit, and flowers per m² of vegetative cover
  - Height and forest structure (trees):
    - Height calculation uses inclinometer readings (top, trunk, bottom) and distance to derive tree foliage height
  - Aggregation and summaries:
    - For each species, per-quadrat data aggregated to compute mean, variance, and sample size for flower density per m² of vegetative cover
    - Species-level summaries include mean/variance/n for flowers per floral unit and per m² cover, including peak flowering season estimates

- Units and measurement details
  - 2D herb/short-plant data: flowers per square meter of vegetative cover; cross-point-based vegetative cover area; counts of buds, opened, and fruited floral units
  - 3D tree data: density estimates extrapolated to whole tree using cube sampling and height distribution, expressed as flowers per m² of vegetative cover and per floral unit
  - Floral unit concepts: buds, opened, and fruited units; opened flowers per floral unit; total flowers per floral unit

- Spatial relevance and GIS applications
  - Provides spatially explicit data on floral resources across multiple species and habitats
  - Suitable for mapping species-specific flower densities, habitat-level floral resource availability, and temporal changes in nectar resources
  - Can be joined with location and habitat attributes to support pollinator resource assessments and conservation planning

- Data quality, limitations, and considerations
  - Data spread across three spreadsheets with different spatial scales (2D herbaceous vs 3D trees) and derived metrics
  - Extrapolation to whole-tree density relies on height and distribution estimates, introducing potential uncertainties
  - Quadrat-based sampling with variable number of quadrats per species; potential limitations in comparability across species and sites
  - Field sites concentrated in southern England; geographic coverage may affect broader UK generalizations

- References and provenance
  - Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators, in preparation)
  - Carey et al. 2008 (Countryside Survey: UK Results from 2007)
  - Data linked to UK IPI AgriLand project and related publications

- Potential GIS outcomes and next steps
  - Create species-specific density maps and hotspot analyses for pollinator planning
  - Develop habitat-based floral resource layers for policy and outreach
  - Integrate with other biodiversity and land-use datasets to support integrated landscape management
  - Apply quality checks and metadata standardization to enable cross-study interoperability