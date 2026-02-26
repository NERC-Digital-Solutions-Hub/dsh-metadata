# Collection methods

## Overview and aims
- Study investigates how invasion by Pinus contorta affects Patagonian grassland productivity and the sheep stocking rate that the grassland can sustain.
- Conducted across five plantations in northwest Patagonia, Argentina, forming a gradient of invasion abundance from plantation edges outward.
- Metrics include total grassland productivity, palatable productivity (species foraged by sheep), and sustainable sheep stocking rate, analyzed in relation to pine abundance.

## Study design and sampling framework
- Sites: five plantations labeled A1, A2, A3, C1, C2.
- Transects: five per site, radiating from the pine plantation toward the invasion front.
- Transect lengths: vary by site (200 m for A2 and C2; 350 m for C1; 500 m for A1 and A3) to reach beyond the invasion front.
- Plots: circular plots (10 m diameter) placed along each transect at distances from the plantation: 0, 25, 50, 75, 100, 150, 200, 350, and 500 m (last two distances only where transects reach them).
- Control vs invaded: for each subplot, productivity measured in invaded plots and in paired control plots without invasion, established as the most distant non-invaded site along the transect.
- Exclusions: transects where pine presence prevented a valid control (no invasion-free plot) were excluded; total excluded: 5 transects (A2:3, A3:1, C2:1).

## Pine abundance metrics (three measures)
- Density (trees/ha): count within 10 m diameter subplot plots.
- Basal area (m2/ha): sum of diameters at ground level per hectare.
- Canopy cover (%): estimated from hemispheric photographs in six 0.25 m2 subplots per subplot.

## Grassland productivity and livestock metrics (three impact measures)
- Total productivity: aboveground dry biomass of all grasses, forbs, and shrubs per hectare (kg/ha/year) at peak production.
- Palatable productivity: productivity of species grazed by sheep, per hectare (kg/ha/year).
- Sheep stocking rate: sustainable number of sheep (per hectare or per year) based on the palatable productivity, using an Ovine Livestock Unit (OLU) framework (Merino wether, 40 kg, 365 kg dry forage/year) and vegetation use factor (UF) per site to reflect consumable forage proportion.

## Data collection and quality control
- Field checks: GPS readings validated; hemispheric pictures checked for position and direction.
- Biomass processing: standardized harvesting, oven-drying at 60°C for 48 hours, precise weighing.
- Post-collection checks: recounts to ensure no missing samples; checks for data inconsistencies (e.g., palatable < total productivity).

## Data structure and content
- File: a single csv named Database containing 22 columns.
- Key columns include: wypt (waypoint name), site, transect, plot, distance from plantation, pinus_cover (canopy cover for subplots), pinus_cover_average, productivity_total, productivity_total_plot_average, productivity_palatable, productivity_palatable_plot_average, proportion_palatable, es_total_productivity, es_palatable_productivity, es_stocking_rate, use_factor, sheep_ha_year, density_ha, total_ba_ha, and others.
- Data notes:
  - 'na' indicates missing data for a given subplot.
  - Average values across subplots within a plot are stored in the first subplot row; subsequent subplots show '-'.
- Three effect sizes (for each subplot) calculated:
  - EStp: effect of invasion on total grassland productivity.
  - ESpp: effect of invasion on palatable productivity.
  - ESsr: effect of invasion on sheep stocking rate.
- Effect sizes are averaged across the six subplots per plot; positive values indicate neutral-to-positive effects of invasion, negative values indicate detrimental effects.

## Measurements, units, and standardization
- Productivity measured as kg/ha/year (_total and palatable, at peak growing season December–March in Patagonia).
- Distance, transect lengths, and plot spacing designed to capture variation in invasion density, especially near the seed source.
- Palatable productivity linked to sheep foraging preferences; UF per site used to adjust sustainable forage calculations.

## Analytical approach
- To account for site-to-site productivity variability, authors standardize impact measures by computing log-response ratios (effect sizes) per subplot:
  - EStp = ln(Bi/Bc)
  - ESpp = ln(Pi/Pc)
  - ESsr = ln(Si/Sc)
  - Bi, Pi, Si refer to invaded subplots; Bc, Pc, Sc refer to corresponding control plots.
- For each plot, average the three effect sizes across its six subplots; interpret positive vs. negative values as increases or decreases in productivity or stocking rate due to pine invasion.

## Data governance and provenance considerations
- Documentation includes explicit methodological details, measurement protocols, and units to support reproducibility and interoperability.
- The dataset links ecological outcomes (productivity and stocking rate) to an explicit spatial layout (distance from plantation, transect, site) and to a measurable invasion metric (three abundance measures).
- Clear notes on data exclusions and quality checks aid data stewards in assessing data completeness and suitability for meta-analyses or data integration.
- References and site metadata (location, tree diameter, site palatable productivity, vegetation use factor) provide context for data interpretation and future data linking.

## Practical implications for data stewards
- Ensure metadata completeness to reflect measurement protocols, timing, and site-specific UF values.
- Maintain versioning and data lineage for the Database, including any re-calculations of effect sizes.
- Preserve the relationship between subplots, plots, transects, and site to support spatial analyses and reproducibility.
- Consider providing access to both raw measurements (e.g., individual subplot data) and derived metrics (e.g., ES values) to support diverse analyses.