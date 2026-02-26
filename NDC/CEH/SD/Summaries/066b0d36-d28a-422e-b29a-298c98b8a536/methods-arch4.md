# Impact of Pinus contorta invasion on Patagonian grassland productivity

- Purpose and scope
  - Quantify the impact of invasive Pinus contorta on Patagonian grassland productivity and sheep carrying capacity.
  - Use a gradient of invasion across five NW Patagonia sites to assess how pine density and canopy affect grassland output and forage value.

- Study area and design
  - Location: northwest Patagonia, Argentina; five plantations (A1, A2, A3, C1, C2) established ~30 years ago, replacing native grasslands.
  - Environment: mean annual precipitation ~900 mm; mean temperature ~8.3 °C; native grasslands dominated by Pappostipa speciosa and Festuca pallescens.
  - Experimental design: five transects per site radiating from the plantation edge toward the invasion front; transect lengths vary by site (A1/A3: 500 m; A2/C2: 200 m; C1: 350 m).
  - Sampling along transects: circular plots at 0, 25, 50, 75, 100, 150, 200, 350, 500 m (depending on transect reach); each plot has six subplots for canopy and productivity measures.
  - Invasion status: control plots (no invasion) vs invaded plots with increasing pine density.

- Pine abundance metrics
  - Density: trees per hectare.
  - Basal area: sum of cross-sections of pines per hectare (m2/ha).
  - Canopy cover: percent sky blocked by pine crowns, estimated from hemispheric photos in subplots.

- Grassland productivity and forage metrics
  - Total productivity: aboveground green biomass (kg/ha/year) at peak production (early summer).
  - Palatable productivity: biomass of species forageable by sheep (kg/ha/year).
  - Vegetation use factor (UF): portion of forage effectively grazed without compromising sustainability (site-specific, in Table 1).
  - Sheep stocking rate: sustainable number of sheep (OLU-based; 1 OLU = Merino 40 kg; 365 kg dry forage/year); expressed as sheep_ha_year.
  - Data sources and species coding: palatable vs non-palatable classification based on Patagonia grassland condition handbook.

- Data collection and quality control
  - Field verification: GPS checks; position/direction validation of hemispheric photos.
  - Biomass processing: harvest, oven-dry at 60°C for 48 h, precise weighing.
  - Data integrity: post-collection review to identify missing samples or inconsistencies; exclusion of transects lacking control plots to enable impact assessment.

- Data structure and variables
  - Dataset: a single CSV file named Database with 22 columns.
  - Key columns (examples): wypt (waypoint), site, transect, plot, distance, pinus_cover (canopy %), pinus_cover_average, productivity_total (kg/ha), productivity_total_plot_average, productivity_palatable (kg/ha), productivity_palatable_plot_average, proportion_palatable, proportion_palatable_average, es_total_productivity, es_palatable_productivity, es_stocking_rate, use_factor, sheep_ha_year, sheep_ha_year_average_plot, density_ha, total_ba_ha.
  - Data notes: 'na' indicates missing data; average values for plots are taken from the first subplot row per plot.

- Analytical methods
  - Standardization to account for site variability: compute stride-specific effect sizes (log-response ratios) for each subplot.
  - Three impact measures (three ES):
    - EStp: effect of invasion on total grassland productivity (ln Bi/Bc).
    - ESpp: effect of invasion on palatable productivity (ln Pi/Pc).
    - ESsr: effect of invasion on sustainable sheep stocking rate (ln Si/Sc).
  - Averaging: per plot, average the six subplots to obtain plot-level ES values; positive ES indicates invasion increases productivity or carrying capacity, negative indicates decrease.
  - Interpretation: magnitude is absolute value of ES; direction indicates positive or negative impact of pine invasion.

- Exclusions and limitations
  - Five transects were excluded from analyses due to lack of a control plot (insufficient baseline for comparison): three in A2, one in A3, one in C2.
  - Data are cross-sectional along invasion gradient; growing-season timing and site-specific UF influence results.

- Practical implications and use
  - Enables cross-site comparison of invasion impacts on grassland productivity and livestock carrying capacity.
  - Supports data-driven decisions on land management, grazing strategies, and potential control of pine invasion in Patagonia.
  - Metadata and structure designed to support reuse, reproducibility, and integration with broader data on Patagonian rangelands.