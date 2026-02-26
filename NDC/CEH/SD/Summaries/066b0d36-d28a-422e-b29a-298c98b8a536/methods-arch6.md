# Impact of Pinus contorta invasion on Patagonian grassland productivity

## Context and objective
- Quantify the impact of invasive Pinus contorta on grassland productivity along transects radiating from pine plantations in northwest Patagonia, Argentina.
- Compare grassland productivity in invaded plots vs. non-invaded control plots to assess three outcomes:
  - Total grassland productivity (all species)
  - Palatable grassland productivity (species foraged by sheep)
  - Sheep stocking rate sustainable by palatable forage
- Use three abundance metrics of pine: density (trees/ha), basal area (m2/ha), and canopy cover (%).

## Study design and data collection
- Five study sites: A1, A2, A3, C1, C2 with plantations of Pinus contorta established ~30 years ago.
- Transects: five per site, extending from plantation edge outward past the invasion front; transect lengths varied by site (A2 and C2: 200 m; C1: 350 m; A1 and A3: 500 m).
- Plots and distances: circular plots (10 m diameter) at multiple distances from plantation edge: 0, 25, 50, 75, 100, 150, 200, 350, 500 m (the last two only where feasible).
- Paired design: each invaded plot has a corresponding control plot at the same transect, located beyond the invasion front where pines are absent.
- Exclusions: five transects were not used in analyses due to lack of a valid control plot (A2: 3 transects; A3: 1; C2: 1).
- Data collected per subplot:
  - Pine abundance metrics: density, basal area, canopy cover
  - Grassland productivity: total green biomass and palatable biomass (harvested at peak season; dried and weighed)
  - Sheep stocking potential: derived from palatable biomass using an Ovine Livestock Unit (OLU) standard (40 kg sheep; 365 kg/year forage) and vegetation use factor (UF)

## Variables and data structure
- Dataset: one CSV file named Database with 22 columns.
- Key columns and meanings:
  - wypt, site, transect, plot, distance, subplot (identifiers)
  - pinus_cover, pinus_cover_average (canopy cover metrics)
  - productivity_total, productivity_total_plot_average (total grassland productivity, kg/ha)
  - productivity_palatable, productivity_palatable_plot_average (palatable productivity, kg/ha)
  - proportion_palatable, proportion_palatable_average (share of total productivity that is palatable)
  - es_total_productivity, es_palatable_productivity, es_stocking_rate (effect sizes)
  - use_factor (vegetation use factor)
  - sheep_ha_year, sheep_ha_year_average_plot (sheep stocking rate per hectare per year)
  - density_ha, total_ba_ha (density and total basal area for pines)
- Data quality notes:
  - 'na' denotes missing data
  - For plots with averaged values across subplots, the first row contains the average; subsequent rows show dashes

## Analytical methods
- Standardized effect sizes (log-response ratios) to compare invasion impacts across sites:
  - EStp = ln(Bi / Bc) for total grassland productivity
  - ESpp = ln(Pi / Pc) for palatable grassland productivity
  - ESsr = ln(Si / Sc) for sheep stocking rate
  - Bi, Pi, Si refer to invaded plots; Bc, Pc, Sc refer to corresponding control plots
- Per plot, six subplots are averaged to produce a plot-level ES for each outcome.
- Interpretation:
  - Positive ES indicates an increase due to pine invasion; negative ES indicates a decrease.
  - Magnitude reflects the strength of the response.

## Data quality and controls
- Field quality checks:
  - Regular GPS verification
  - Verification of hemispheric canopy images for correct position/direction
  - Standardized protocols for biomass harvest and drying
  - Post-collection re-counts to ensure data completeness
  - Consistency checks (e.g., palatable productivity not exceeding total productivity)

## Site context and environmental background
- Climate and ecology:
  - Mean annual precipitation ~900 mm; mean annual temperature ~8.3°C
  - Native grasslands dominated by Pappostipa speciosa and Festuca pallescens
  - Pine plantations have replaced native grasslands and act as sources of invasion
- Land use:
  - Extensive livestock grazing, mainly sheep, dependent on native rangelands for forage
- Link to management:
  - Outputs inform understanding of invasion impacts on forage availability and livestock carrying capacity

## Data records and supplementary details
- Table 1 (described): location, mean diameter of pines, plantation area, palatable productivity, and vegetation use factor (UF) for each site
- Figures (described):
  - Figure 1: maps and transect scheme showing invasion front
  - Figure 2: mean total productivity in control plots (non-invaded) by site
  - Figure 3: conceptual model of the measured impacts and contributing factors
- References provide context for methodology and regional ecology

## Potential uses for Data Support and downstream applications
- Cross-site comparisons of how pine invasion alters total and palatable grassland productivity
- Assessing changes in sustainable stocking rates and implications for sheep production
- Informing land management decisions to mitigate invasion impacts and maintain forage provision
- Enabling meta-analyses and reproducibility through a well-documented, standardized dataset with explicit effect-size calculations