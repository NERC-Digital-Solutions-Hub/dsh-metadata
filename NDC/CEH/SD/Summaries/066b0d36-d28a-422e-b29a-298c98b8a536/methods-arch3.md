# Impact of Pinus contorta invasion on grassland productivity and sheep stocking rate in Patagonia

- This study quantifies how invasion by Pinus contorta affects native Patagonian grassland productivity and the capacity to sustain sheep stocking rates.
- It uses a gradient of invasion abundance established from five plantation sites (A1, A2, A3, C1, C2) in northwest Patagonia, with transects radiating from plantation edges to beyond the invasion front.

## Study area and design

- Location: Northwest Patagonia, Argentina; mean annual precipitation ~900 mm; mean temperature ~8.3 °C.
- Native grasslands are moderately covered and dominated by palatable tussock grasses (Pappostipa speciosa, Festuca pallescens).
- Experimental design: five transects per site (often 500 m long) extending from the plantation outward, with plots positioned at fixed distances from the plantation (0 to 500 m, depending on transect length).
- Invasion gradient: plots arranged to compare invaded vs. control (non-invaded) conditions along each transect.
- Exclusions: transects where pine occurred in all plots (no control) were not used in analyses; total excluded across sites: five transects (three at A2, one at A3, one at C2).

## Measurements and variables

- Pine abundance metrics (three metrics measured in circular subplots, 10 m diameter):
  - Density: pines per hectare (trees/ha).
  - Basal area: total cross-sectional area of pines per hectare (m2/ha).
  - Canopy cover: percent of sky blocked by crowns (estimated via hemispheric photos in six subplots per circle).

- Grassland productivity metrics (measured at peak growing season):
  - Total productivity: aerial green biomass per hectare (kg/ha/year) for all grassland species.
  - Palatable productivity: biomass for species palatable to sheep only (kg/ha/year).

- Livestock provisioning metric:
  - Sheep stocking rate: sustainable number of sheep per hectare/year, calculated using the Ovine Livestock Unit (OLU) framework (Merino wether, 40 kg; 365 kg dry forage/year) and vegetation Use Factor (UF) per site.

- Vegetation Use Factor (UF): a site-specific proportion of forage that is effectively consumable by sheep.

- Data are recorded per subplot and summarized per plot (six subplots per plot for canopy and productivity metrics).

## Data collection and processing methods

- Transects: five per site, following the main dispersal direction, extending beyond the visible invasion front.
- Plot layout: along each transect, plots located at 0, 25, 50, 75, 100, 150, 200, 350, and 500 m from the plantation (with some distances only present in longer transects).
- Sampling protocol:
  - Pine abundance: counts for density; diameter at ground level for basal area; canopy cover estimated via hemispheric photography.
  - Biomass: harvest green biomass at peak season; oven-dry at 60°C for 48 h; weigh with precision scale.
  - Palatability: classify species as palatable or non-palatable according to regional guidelines.
  - Stocking rate: compute based on palatable biomass and OLU requirements, incorporating UF.
- Quality checks: GPS verification; position/direction checks for hemispheric photos; consistency checks on biomass harvests; verification to avoid missing samples; check for data inconsistencies (e.g., palatable > total productivity).

## Data structure and availability

- Data file: a single CSV ("Database") with 22 columns capturing all measurements and derived metrics.
- Key columns include:
  - wypt, site, transect, plot, distance (from plantation), subplot
  - pinus_cover, pinus_cover_average
  - productivity_total, productivity_total_plot_average
  - productivity_palatable, productivity_palatable_plot_average
  - proportion_palatable, proportion_palatable_average
  - es_total_productivity, es_palatable_productivity, es_stocking_rate
  - use_factor
  - sheep_ha_year, sheep_ha_year_average_plot
  - density_ha, total_ba_ha
- Data flags: 'na' indicates missing data; averages are stored in the first row per plot with dashes in subsequent rows.

## Analytical methods

- Standardization across sites due to higher variability in grassland productivity: compute effect sizes (log-response ratios) for each subplot for three impacts:
  - EStp: invasion effect on total grassland productivity (ln(Bi/Bc))
  - ESpp: invasion effect on palatable grassland productivity (ln(Pi/Pc))
  - ESsr: invasion effect on sheep stocking rate (ln(Si/Sc))
- Definitions:
  - Bi, Pi, Si: invaded subplot values for total productivity, palatable productivity, and stocking rate, respectively.
  - Bc, Pc, Sc: corresponding control subplot values from the same transect (non-invaded).
- Calculation: for each plot, average the three effect sizes across the six subplots to obtain plot-level ES estimates.
- Interpretation: positive ES indicates increased productivity or stocking rate due to invasion; negative ES indicates detrimental effects.

## Quality control and data governance

- Field validation ensures data validity (GPS, plot position, sampling protocols).
- Post-collection checks include cross-validation of biomass measurements and plausibility checks (e.g., palatable biomass not exceeding total productivity).
- Metadata and data structure are explicit to facilitate reuse and cross-site comparability.
- The documentation provides clear definitions of all metrics and the calculations used for effect sizes, enabling consistent monitoring and replication.

## Challenges and considerations for monitoring frameworks

- Data gaps and quality barriers:
  - Occurrence of data gaps (missing metadata in some datasets) and the need for standardization across sites.
  - Variability in data completeness due to transects being excluded when control plots are absent.
- Data harmonization and comparability:
  - Use of multiple abundance metrics (density, basal area, canopy cover) to robustly characterize invasion.
  - Calculation of standardized impact metrics (ES) to enable cross-site comparison of invasion effects.
- Communication of complex findings:
  - Clear reporting of three concurrent impact pathways (total productivity, palatable productivity, and livestock support) and their effect sizes.
  - Presentation of results at plot, transect, and site levels to inform management decisions.
- Governance and openness:
  - The study includes clearly defined data structures and formulas, facilitating data sharing and governance, although actual data-sharing practices are not described here.