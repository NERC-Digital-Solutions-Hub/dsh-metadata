# Impact of Pinus contorta invasion on Patagonian grassland productivity

## Objective and study area
- Investigated how invasive Pinus contorta plantations affect grassland productivity and sheep forage in northwest Patagonia, Argentina.
- Five study sites (A1, A2, A3, C1, C2) with pine plantations ~30 years old, creating a gradient of invasion into adjacent native grasslands.
- Climate: mean annual precipitation ~900 mm; mean annual temperature ~8.3 °C. Native grasslands dominated by Pappostipa speciosa and Festuca pallescens, heavily used for sheep grazing.

## Spatial design and sampling
- Transects radiate from plantation edges toward the invasion front; length adjusted per site (A2 and C2: 200 m; C1: 350 m; A1 and A3: 500 m).
- Each site: five transects, with plots at distances from the plantation: 0, 25, 50, 75, 100, 150, 200, 350, 500 m (last two distances only where applicable).
- Plots are circular with 10 m diameter; transects spaced 50 m apart within a site.
- Excluded: five transects where pines were present in all plots (no control plot), leaving out those data from analyses.

## Measurements and variables
- Pine abundance metrics (per subplot):
  - Density: trees per hectare (trees/ha)
  - Basal area: cross-sectional area per hectare (m2/ha)
  - Canopy cover: percentage of sky blocked by pine crowns (estimated from hemispheric photos in six subplots per plot)
- Productivity metrics (per subplot and plot averages):
  - Total grassland productivity: green aerial biomass per hectare per year (kg/ha/year), measured at peak season
  - Palatable productivity: biomass of species forageable by sheep (kg/ha/year)
- Sheep stocking rate: sustainable number of sheep based on palatable biomass, using an Ovine Livestock Unit (OLU) benchmark (Merino 40 kg; 365 kg dry forage/year) and vegetation Use Factor (UF)
- Data collection details:
  - Biomass harvested at peak season, dried at 60°C for 48 h, weighed
  - Palatability classification based on Bonvissuto et al. (2008)
  - Canopy cover estimated from hemispheric photos
- Data structure: a single CSV file (Database) with 22 columns (e.g., wypt, site, transect, plot, distance, subplot, pinus_cover, productivity_total, productivity_palatable, sheep_ha_year, density_ha, total_ba_ha, pinus_cover_average, es_total_productivity, es_palatable_productivity, es_stocking_rate, use_factor, etc.)
- Table 1 provides site-level palatable productivity and vegetation use factor (UF)

## Analytical methods
- Standardized impact measures using log-response ratio effect sizes:
  - EStp: effect of pine invasion on total grassland productivity (ln(Bi/Bc))
  - ESpp: effect of pine invasion on palatable productivity (ln(Pi/Pc))
  - ESsr: effect of pine invasion on sustainable sheep stocking rate (ln(Si/Sc))
- For each plot, average the six subplots to obtain a plot-level ES for each measure.
- Interpretation: positive ES indicates invasion increases the corresponding productivity or stocking rate; negative ES indicates a decrease; magnitude reflects response strength.

## Quality control and data integrity
- In-field GPS checks to ensure accurate locations
- Validation of hemispheric photos for correct position/direction
- Standardized harvesting, drying, and weighing procedures
- Post-collection data checks (e.g., verifying palatable vs total productivity)
- Re-counts to confirm samples per transect; missing data flagged as 'na'

## GIS and data applicability
- Rich, georeferenced dataset across five sites with multiple transects, enabling:
  - Mapping of pine density, basal area, and canopy cover as spatial layers
  - Mapping of total and palatable grassland productivity, and sheep stocking rate
  - Creating gradient plots of invasion intensity and corresponding effect sizes (EStp, ESpp, ESsr)
- Useful datasets and attributes:
  - Site-level characteristics (Table 1): location, mean tree diameter, site area, palatable productivity, UF
  - Plot-level and subplot-level measurements along transects (distance from plantation, pine abundance metrics, productivity metrics, ES values)
- Potential GIS products:
  - Invasion gradient rasters or vector layers
  - Spatial layers of productivity losses/gains and stocking-rate changes
  - Distance-to-invasion-front analyses and proximity-based impact mapping

## Limitations and notes
- Some transects were excluded due to lack of a control plot, potentially biasing spatial coverage
- Variation in transect length by site; distances adapted to invasion gradient
- Data reflect peak-growing-season conditions and Patagonia-specific forage dynamics
- Some data entries marked as not applicable ('na') where measurements were unavailable