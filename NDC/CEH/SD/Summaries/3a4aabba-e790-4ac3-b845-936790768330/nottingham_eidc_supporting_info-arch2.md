# Seedling growth declines in warmed tropical forest soils

- A comprehensive dataset from a soil warming experiment (SWELTR) in a seasonally moist lowland tropical rainforest on Barro Colorado Island, Panama.
- Objective: document how seedling growth and plant physiological parameters respond when the soil environment is warmed by 4°C across the soil profile.

## Experimental design and scope

- Location: Barro Colorado Island, Panama (9.1521° N, 79.8465° W).
- Design: 10 paired control and heated plots spanning 1 hectare, with heated plots warming the soil profile to ~4°C (surface soils ~3°C) using 16 heating rods extending to 1.2 m depth; seedling plots nested inside each circular plot.
- Seedling subplot layout: inside each experimental plot, seedling plots (1.5 x 1.5 m) containing 6 rows x 6 individuals, comprising 6 species (360 seedlings total per 5 plot pairs).
- Species: six shade-tolerant tropical tree species; three form nitrogen-fixing symbioses (Inga laurina, Ormosia macrocalyx, Tachigali versicolor) and three do not (Lacmellea panamensis, Protium pittieri, Virola surinamensis).
- Seed sources: seeds collected in 2015 nearby, germinated in shade house, transplanted during early wet season 2016.
- Duration: seedling data collected 2016–2019; resin nutrient measurements monthly over the same period (3 years); chlorophyll data collected specifically in September 2022 for leaf chlorophyll index.

## Data collected and key variables

- Seedling growth and condition
  - Relative growth rates (RGR) for each seedling
  - Seedling height changes
  - Herbivory index (0 = none to 3 = heavy damage)
  - Leaf chlorophyll concentration index (CCI)
- Physiological measurements
  - Light-saturated photosynthesis (Asat)
  - Light environment: photosynthetic photon flux density (PPFD) under overcast and sunny conditions
  - Gas-exchange parameters (e.g., stomatal conductance, internal CO2, transpiration)
- Soil nutrient availability
  - In situ resin-based measurements of mineralised nitrogen (NH4+, NO3−) and phosphorus (PO4−)
  - Expressed as extractable N and P per g resin per day
- Sampling regime
  - Seedling census every 3 months (6 species, 6 replicates per species per plot)
  - Resin measurements monthly (pre/post warming indicators included)
  - Chlorophyll measured for a subset of leaves in Sept 2022 following standard protocols

## Data collection and methods

- Height measurement: from soil surface to apical meristem with a tape measure.
- PPFD: monthly measurements above each seedling; two metrics (overcast and clear-day conditions).
- Asat: measured with a portable photosynthetic system (LI-6400) using a standard leaf cuvette and CO2 mixer.
- Resin-based soil nutrients: in situ resin membranes, extracted with 0.5 M HCl, analyzed for PO4, NH4, NO3 via flow injection analyzer; corrections using blanks.
- Chlorophyll: leaf chlorophyll content index (CCI) via reflectance (931/653 nm) on 10 leaves per seedling set.
- Herbivory: continuous 0–3 damage scale.
- Growth modeling: relative growth rate (RGR) estimated using a first-order power-law model from height data; warming effect assessed via the β parameter from log-log regression.
- Quality control: all data subjected to verification for seedling identification and data blanks/standards before statistical analyses in R.

## Data files and structure

- Seedling relative growth rates: SWELTR_seedlings_RGRs.csv
  - Key fields: SPECIES, PLOT, PLOTPAIR, TREAT, REPLICATE, RGR_power, RGR_power_post, RGR_power_pre, LUZ_SUN, LUZ_CL, HERB, etc.
- Seedling gas exchange parameters: SWELTR_seedlings_gasex.csv
  - Time-based measurements; fields include Species, Plot, Treat, Nfix, Photo, Cond, Ci, Trmmol, VpdL, Area, etc.
- Seedling height and herbivory measurements: SWELTR_seedlings.csv
  - Key fields: HEIGHT, LIGHT_CL, LIGHT_SUN, LEAVES, HERBIVORY, PREPOST, etc.
- Seedling leaf chlorophyll data: SWELTR_chlorophyl.csv
  - Plot, Species, CCI, TREAT
- Soil resin nutrients: SWELTR_soilresins.csv
  - Pre/post, Rmonth, Plot, plotpair, Sample, season, treat, Date, P (PO4), NH4 (NH4), NO3 (NO3), TIN (total inorganic N)

## Analytical context and accessibility for monitoring

- Standardised data structure and labeling enable integration with other environmental datasets for monitoring environmental health and policy performance over time.
- Data are organized across multiple clearly named files, with explicit fields for temporal (RMONTH, Date), treatment (PREPOST, TREAT), spatial (Plot, plotpair), and species identifiers.
- Challenges highlighted for analysts monitoring the environment include increasing dataset value through data integration and facilitating access to underlying data for reuse and cross-study comparisons.