# Data overview

- Study and sampling scope
  - Plant community data collected in 100 plots of 1 m² across ten old-growth grasslands in the northern Cerrado, São Felix do Tocantins, Tocantins, Brazil.
  - Comparison between cattle-grazed and burned old-growth grasslands (50 plots) and ungrazed and unburned old-growth grasslands (50 plots); five grasslands per land-use category, with ten plots per grassland.
  - Fieldwork conducted in March–April 2022.
  - Data linked to two funded projects: “Ecological and economic evaluation of beef cattle on pastures in the Brazilian Cerrado” and “Optimising the long-term management of invasive species…,” funded by FAPESP and NERC respectively.

- Study area context
  - Location: Tocantins, Brazil, northern Cerrado; about 500 m altitude.
  - Climate: dry winter (May–Sept) and humid summer (Oct–Apr); annual rainfall ~1,400–1,500 mm; temperatures ~24–27°C.
  - Land-use history: traditional cattle ranching on old-growth grasslands for ~100 years; fire applied during the dry-to-wet transition, grazing mainly during the rainy season (Oct–Apr).
  - Environmental conditions: soils are predominantly arenosol (WRB/FAO); sites free of African invasive grasses and prior soil management.

- Sampling design and field methods
  - Transects: one 50-m transect per old-growth grassland, oriented North–South.
  - Plots: 10 plots of 1 m × 1 m per transect, systematically distributed.
  - Within-plot measurements:
    - All plant species identified; growth form categorized as graminoids, forbs, or shrubs.
    - Species presence and percent cover (0–100%) estimated; total cover may exceed 100% due to 3D structure.
    - Dead biomass cover and bare ground visually estimated.
  - Biomass sampling: within a 0.5 m × 0.5 m (0.25 m²) subplot per plot, aboveground vegetation biomass and litter were collected and separated into graminoid, forb, shrub, and dead biomass categories; samples dried at 80°C for 48 h and weighed to 0.1 g precision.
  - Data processing: biomass converted to g m⁻²; average site cover calculated across 10 plots; species absent at a site assigned a zero cover.

- Variables and data products
  - Calculated per-plot variables (from CattleGrazingCerrado1.txt):
    - total_richness, shrub_richness, graminoid_richness, forb_richness (species per 1 m²)
    - shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground (percent)
    - shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass (g m⁻²)
  - Site-level species abundance (from CattleGrazingCerrado2.txt):
    - 118 species with average cover per site; zeros indicate absence.
  - Location data (from CattleGrazingCerrado3.txt):
    - Latitude and longitude for each old-growth grassland site.

- Data structure and provenance
  - CattleGrazingCerrado1.txt: 100 rows (plots) with columns for site, land_use, plot, and the various richness, cover, and biomass metrics.
  - CattleGrazingCerrado2.txt: site-level matrix of average species cover across 118 species.
  - CattleGrazingCerrado3.txt: geographic coordinates (lat/long) for each site.
  - All data originate from two linked research projects and were collected with field verification (expert identification and herbarium support as needed).

- Implications for monitoring and governance
  - Provides a structured, multi-macetric baseline for assessing impacts of grazing and fire regimes on plant community diversity, structure, and biomass.
  - Enables comparative monitoring across land-use scenarios and over time.
  - Metadata and data organization facilitate integration into monitoring frameworks, with clearly defined units and sampling design.
  - Highlights typical monitoring challenges relevant to governance contexts (data availability, metadata clarity, and the need for careful data sharing and standardization).