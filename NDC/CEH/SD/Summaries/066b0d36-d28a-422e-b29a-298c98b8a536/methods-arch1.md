# Collection methods

## Overview
- Study in five sites (A1, A2, A3, C1, C2) in northwest Patagonia, Argentina, where Pinus contorta plantations (~30 years old) replace native grasslands.
- Objective: quantify how pine invasion affects grassland productivity and sheep grazing capacity.
- Invasion creates a gradient of pine abundance from plantation outward; productivity and grazing potential are assessed along transects radiating from the invasion source.

## Study design and field methods
- Transects: five per site, extending from plantation edge to beyond the invasion front; distance from plantation to sampling plots: 0, 25, 50, 75, 100, 150, 200, 350, 500 m (the last two distances used only on sites with longer transects).
- Transect lengths by site: A2 and C2 = 200 m; C1 = 350 m; A1 and A3 = 500 m; plots per transect spaced 50 m apart.
- For each independent transect, circular plots (10 m diameter) were placed at specified distances from the plantation.
- Control plots (no invasion) were paired with invaded plots on each transect; some transects were excluded if pines were present in all plots (no control).
- Excluded: 5 transects (3 in A2, 1 in A3, 1 in C2) due to absence of a true control.

## Pine abundance metrics
- Density: pines per hectare (trees/ha) within each circular plot.
- Basal area: sum of cross-sectional areas of pines per hectare (m2/ha), from diameter at ground level.
- Canopy cover: percent of sky blocked by pine crowns, estimated from hemispheric pictures taken in six 0.25 m2 subplots per plot using a fisheye lens.

## Grassland productivity and palatability measures
- Productivity metric: total aboveground green biomass at peak production (kg/ha/year), using peak green biomass as a proxy for annual productivity due to a short growing season (Dec–Mar).
- Palatable productivity: biomass considering only species palatable to sheep (foraged species).
- Palatability classification based on a regional handbook.
- Harvest method: harvest green biomass at peak, oven-dry at 60°C for 48 h, then weigh.
- Vegetation Use Factor (UF): site-specific factor representing the proportion of forage that can be grazed without compromising long-term forage production.
- Sheep stocking rate: sustainable number of sheep per hectare based on an Ovine Livestock Unit (OLU; Merino wethers ~40 kg; 365 kg dry forage per year) and UF.
- The stocking rate ties grassland productivity to grazing capacity; primary focus is on palatable biomass for grazing.

## Data structure and quality control
- Data file: one CSV named Database with 22 columns (e.g., wypt, site, transect, plot, distance, pinus_cover, productivity_total, productivity_palatable, proportion_palatable, es_total_productivity, es_palatable_productivity, es_stocking_rate, density_ha, total_ba_ha, pinus_cover_average, sheep_ha_year, UF, etc.).
- Data notes:
  - 'na' denotes missing data for a subplot.
  - Plot-average values are stored in the first subplot row for each plot; subsequent rows show dashes.
- Quality control procedures:
  - Real-time GPS checks in the field.
  - Verification of hemispheric photographs for position/direction.
  - Standardized harvesting and drying procedures.
  - Post-collection re-counts to ensure no missing samples.
  - Dataset checks to identify inconsistencies (e.g., palatable productivity exceeding total productivity).

## Analytical methods
- Standardization by effect sizes due to site-to-site variability in grassland productivity:
  - EStp: effect of invasion on total grassland productivity = ln(Bi/Bc).
  - ESpp: effect of invasion on palatable productivity = ln(Pi/Pc).
  - ESsr: effect of invasion on sheep stocking rate = ln(Si/Sc).
- For each subplot, three ES values are calculated; then averaged across the six subplots within each plot to obtain plot-level ES estimates.
- Interpretation:
  - Positive ES indicates a positive impact of invasion on the respective outcome; negative ES indicates a negative impact.
  - The magnitude is given by the absolute value of the ES.

## Context and references
- Study area characterized by extensive sheep grazing on native Patagonian rangelands and susceptibility of these grasslands to pine invasions.
- Key references provide context on regional grasses, forage use, and the ecological dynamics of Pinus contorta in Patagonia.

## Practical implications for analysts
- Rich, multi-metric dataset allows analysis of how different measures of pine abundance (density, basal area, canopy cover) relate to three distinct grassland outcomes (total productivity, palatable productivity, livestock grazing capacity).
- The standardized effect sizes enable cross-site comparisons and meta-analytic approaches despite local variation.
- The dataset supports exploring distance-from-source effects and invasion gradients on forage availability and grazing sustainability.