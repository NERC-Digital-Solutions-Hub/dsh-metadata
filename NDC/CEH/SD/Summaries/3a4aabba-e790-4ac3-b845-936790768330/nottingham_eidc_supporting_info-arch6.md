# Seedling growth declines in warmed tropical forest soils

## Overview
- Describes growth parameters for tree seedlings in a lowland tropical forest in Panama under experimental soil warming (SWELTR) on Barro Colorado Island.
- Entire soil profile heated by 4°C; surface soils heated ~3°C.
- Seedling community includes six species (three N-fixers: Inga laurina, Ormosia macrocalyx, Tachigali versicolor; three non-N-fixers: Lacmellea panamensis, Protium pittieri, Virola surinamensis).
- Data types collected: relative growth rates (RGRs), height change, herbivory index, light-saturated photosynthesis (Amax), leaf chlorophyll concentration, photosynthetic photon flux density (PPFD); soil nutrient mineralisation (N and P) via in situ resin membranes monthly.
- Data span 2016–2022, with seedling data mainly 2016–2019 and chlorophyll measurement in 2022; soil resin data collected monthly over the study period.

## Experimental design
- Soil warming experiment (SWELTR): 10 paired control and heated plots over 1 ha.
- Heated plots: average +4°C soil-profile warming (to ~1.5 m depth); surface soils ~+3°C.
- Plot structure: circular plots (internal diameter ~3.5 m; external footprint ~5 m), 16 heating rods forming a ring around each plot.
- Seedling plots inside each experimental plot: 36 seedlings per plot (6 species × 6 replicates), totaling 360 seedlings across all plots.
- Seedling establishment: seeds collected in 2015, germinated in shade house, transplanted in early wet season 2016.
- Experimental layout: five paired sets (A–E) of heated/control plots; randomised planting within seedling plots.
- Species stratification: six shade-tolerant species; three known N-fixers and three non-N-fixers.

## Data collection and transformation methods
- Temporal scope: data collected 2016–2019 for seedling measurements; resin mineralisation measured monthly for three years; chlorophyll measured Sept 2022.
- Seedling measurements:
  - Height: measured from soil surface to shoot apex with a tape measure.
  - PPFD: monthly measurements above each seedling for overcast and clear-day conditions (two metrics per month).
  - Asat: light-saturated photosynthesis measured with LI-COR LI-6400 system.
  - Herbivory: continuous scale (0–3) assessing leaf damage.
- Soil nutrient measurements:
  - In situ mixed-bed ion-exchange resin membranes to estimate mineralised N and P (PO4-P, NH4-N, NO3-N).
  - Resin deployed monthly at 5 cm depth; extraction by 0.5 M HCl; analysis with Lachat Quickchem 8500.
- Leaf chlorophyll:
  - Chlorophyll Content Index (CCI) measured in Sept 2022 using a chlorophyll meter; n = 10 leaves per species per plot.
- Growth analysis:
  - Relative Growth Rate (RGR) computed using a first-order power-law model: dh/dt = t^β, with RGR derived from slope of log(height) vs log(time) across relative months.
  - β (growth rate parameter) used to assess warming effects on growth.
- Quality control:
  - Data quality checks in R for outliers and correct seedling IDs; verification against blanks/standards.

## Data files and structure
- Data are provided in five separate CSV files:
  - SWELTR_seedlings_RGRs.csv — plant growth parameters by species and plot (RGR_power, RGR_power_post/pre, Nfix, etc.).
  - SWELTR_seedlings_gasex.csv — seedling gas-exchange parameters (Amax, stomatal conductance, Ci, transpiration, VPD, PPFD, leaf area, etc.) with treatment, species, plot, and timing details.
  - SWELTR_seedlings.csv — seedling height and herbivory measurements (HEIGHT, HERBIVORY, LEAVES, PREPOST, etc.).
  - SWELTR_chlorophyl.csv — leaf chlorophyll data (CCI) by plot and species.
  - SWELTR_soilresins.csv — soil resin nutrient data (pre/post, Rmonth, Plot, plotpair, Sample, season, treatment; P, NH4, NO3, total inorganic N; units provided; NA denotes missing data).
- Variable and field details:
  - Key identifiers: PLOT, PLOTPAIR, SPECIES, REPLICATE, SUBPLOT, PLOT_CODE.
  - Temporal markers: RMONTH (relative month since warming began), MONTH, YEAR, PREPOST/POST.
  - Environmental and analytical measures: TREAT, Nfix, LUZ_SUN, LUZ_CL, PPFD, Amax, CHLOROPHY, HERBIVORY, etc.
- Notes:
  - Data include missing values denoted as NA.
  - File descriptions indicate explicit data structure for cross-dataset integration (e.g., linking by PLOT, SPECIES, TREAT).

## Analytical methods and usage
- Analytical approach outlined in methods:
  - Use RGR as a key growth metric and compare between warmed and control treatments using the β parameter from the power-law growth model.
  - Integrate gas exchange and PPFD data to interpret photosynthetic responses to warming.
  - Examine resin-derived nutrient availability in relation to plant uptake under warming.
  - Correlate leaf chlorophyll content with photosynthetic performance and nutrient status.
- Potential data products:
  - Dashboards or pivot-table style summaries enabling self-serve exploration across species, treatments, and time.
  - Visualizations of growth trajectories, photosynthetic performance, herbivory, and nutrient availability under warming.
- Scope for data synthesis:
  - Cross-dataset analyses linking growth metrics (RGR, height) with gas exchange, chlorophyll, PPFD, and soil nutrient dynamics to assess warming effects on seedling establishment and resilience.

## Accessibility and notes
- Data are organized into clearly named CSV files with explicit field definitions to support data reuse.
- Emphasis on reproducibility through described collection, measurement, and QC procedures.
- Users should account for temporal gaps (e.g., focused seedling growth data 2016–2019 vs. chlorophyll measurement in 2022) and missing data (NA) when integrating datasets.