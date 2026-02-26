# Impact of Pinus contorta invasion on Patagonian grassland productivity and sheep stocking rate in northwest Patagonia, Argentina

## Overview
- Study area: five pine plantations (A1, A2, A3, C1, C2) in northwest Patagonia, Argentina, established ~30 years ago, replacing native grasslands.
- Objective: quantify how invasive Pinus contorta affects grassland productivity and the capacity to support sheep grazing.
- Approach: compare grassland productivity and sheep stocking potential along transects radiating from pine plantations, across a gradient of invasion abundance.

## Study Context and Site Description
- Climate: mean annual precipitation ~900 mm; mean annual temperature ~8.3 °C.
- Native grasslands: cover ~60%, dominated by Pappostipa speciosa and Festuca pallescens; important for extensive sheep grazing.
- Invasion gradient: pine density decreases with distance from plantations; transects extend from the plantation edge to beyond the invasion front.
- Sites and transects: five sites (A1, A2, A3, C1, C2) with five transects per site; transects lengths vary by site to reach beyond the invasion front (A2 and C2: 200 m; C1: 350 m; A1 and A3: 500 m).

## Methods: Experimental Design and Measurements
- Transect design: five transects per site radiating from the plantation; circular plots along each transect at fixed distances from the plantation.
- Distances sampled: 0, 25, 50, 75, 100, 150, 200, 350, 500 m (the last two used only where applicable).
- Plot layout: within each transect, six subplots per plot with 10 m diameter circular plots; distance between plots closer near the seed source to capture density variation.
- Pine abundance metrics (three measures):
  - Density: trees per hectare (trees/ha) from counts in 10 m diameter plots.
  - Basal area: total cross-sectional area of pines per hectare, from diameter at breast height measurements.
  - Canopy cover: estimated from six 0.25 m2 subplots per canopy assessment using hemispheric photos.
- Grassland productivity metrics (three measures):
  - Total productivity: aboveground green biomass (kg/ha/year) at peak production; included grasses, forbs, and shrubs.
  - Palatable productivity: aboveground green biomass of species palatable to sheep (kg/ha/year).
  - Sheep stocking rate: sustainable number of sheep per hectare based on an Ovine Livestock Unit (OLU) of a 40 kg Merino ewe consuming 365 kg dry forage/year; adjusted by vegetation Use Factor (UF) per site.
- Control plots: paired plots at the same transect distance from plantation but with no pine invasion.
- Exclusions: transects lacking a control plot or with pine presence across all plots were excluded from analyses (5 transects excluded: 3 in A2, 1 in A3, 1 in C2).

## Data Collection and Quality Control
- Data collection and checks:
  - GPS readings validated in the field.
  - Hemispheric pictures checked for correct position/direction.
  - Standardized harvesting, drying (60°C, 48 h), and weighing of biomass.
  - Post-collection re-counts to ensure data completeness; checks for inconsistencies (e.g., palatable productivity exceeding total productivity).
- Data structure: dataset stored as a single CSV file named Database with 22 columns.

## Analytical Approach
- Standardization across sites due to baseline productivity differences by calculating effect sizes:
  - EStp: effect of pine invasion on total grassland productivity; EStp = ln(Bi/Bc).
  - ESpp: effect on palatable grassland productivity; ESpp = ln(Pi/Pc).
  - ESsr: effect on sustainable sheep stocking rate; ESsr = ln(Si/Sc).
- Averaging: for each plot, average the three effect sizes across six subplots to obtain plot-level ES values.
- Interpretation: A positive ES indicates invasion increases the respective metric; a negative ES indicates a decrease; magnitude reflects response strength.
- Data presentation: Figure 2 (mean total productivity for control plots only) and Figure 3 (conceptual model of measured impacts) described in the study.

## Data Structure and Dataset
- Primary dataset: Database (CSV) with 22 columns capturing:
  - Spatial and plot identifiers: wypt, site, transect, plot, distance, subplot.
  - Pine metrics: pinus_cover, pinus_cover_average.
  - Productivity metrics: productivity_total, productivity_total_plot_average, productivity_palatable, productivity_palatable_plot_average, proportion_palatable, proportion_palatable_average.
  - Effect sizes: es_total_productivity, es_palatable_productivity, es_stocking_rate.
  - Vegetation and use metrics: use_factor.
  - Sheep stocking metrics: sheep_ha_year, sheep_ha_year_average_plot.
  - Pine density and structure: density_ha, total_ba_ha.
  - Data completeness: 'na' denotes missing data for a subplot.
- Note: Averages across subplots per plot are stored in the first subplot row; subsequent rows show dashes for averaged fields.

## Key Findings and Visualization (What to Expect)
- The study quantifies how pine invasion alters grassland productivity and sheep grazing capacity across a gradient of invasion intensity.
- Figures referenced:
  - Figure 2: Mean total productivity for control plots (baseline).
  - Figure 3: Conceptual model linking invasion factors, measured impacts, and underlying environmental/management factors.

## Limitations and Monitoring Implications
- Limitations:
  - Exclusion of five transects due to absence of a control or pervasive invasion along transects may affect spatial coverage.
  - Variability in transect length by site could influence comparability across sites.
- Implications for environmental monitoring:
  - Standardized metrics (density, basal area, canopy cover; total/palatable productivity; stocking rate) enable cross-site comparisons and temporal monitoring.
  - Use of log-response ratio effect sizes supports comparability across sites with different baselines.
  - Data management practices include quality control, installation of a structured dataset, and potential portal uploads for broader accessibility.

## Relevance for Policy and Management
- Provides a data-driven basis to assess how invasive conifers impact key provisioning services (grassland productivity and sheep grazing potential).
- Supports decisions on invasive species management, land-use planning, and sustainable grazing in Patagonian grasslands.