# Seedling growth declines in warmed tropical forest soils

## Overview
- Dataset from the Soil Warming Experiment in Lowland Tropical Rainforest (SWELTR) on Barro Colorado Island, Panama.
- Objective: examine seedling growth under soil warming of 4°C across the soil profile.
- Study design: 10 paired control and heated plots; heated plots heated to ~4°C (soil profile to ~1.5 m; surface soils ~3°C) in a 1 ha area.
- Seedling stage: six shade-tolerant species (three N-fixers: Inga laurina, Ormosia macrocalyx, Tachigali versicolor; three non-N-fixers: Lacmellea panamensis, Protium pittieri, Virola surinamensis).
- Size and scope: 360 seedlings total (6 species × 6 replicates per seedling plot × 5 paired sets), arranged as 36 seedlings per seedling plot within each experimental plot.
- Data timeframe: data collected 2016–2022, with seedling census every 3 months and monthly soil resin measurements; leaf chlorophyll measured in Sept 2022.
- Data outputs: five CSV files containing growth, physiology, and soil nutrient data.

## Data contents and structure
- Seedling relative growth rates
  - SWELTR_seedlings_RGRs.csv
  - Variables include SPECIES, PLOT, PLOTPAIR, TREAT, REPLICATE, RMONTH, RGR_POWER and RGR_POWER_post/pre, canopy/leaf light measures (LUZ_SUN, LUZ_CL), HERB (herbivory), etc.
- Seedling gas-exchange parameters
  - SWELTR_seedlings_gasex.csv
  - Variables include Time, Species, Plot, Treat, Nfix, Amax (Light-saturated photosynthesis), stomatal conductance, intercellular CO2, transpiration, leaf/air temperature variables, PPFD, and other gas-exchange metrics.
- Seedling height and herbivory measurements
  - SWELTR_seedlings.csv
  - Variables include HEIGHT, LEAVES, HERBIVORY, PPFD metrics, PREPOST status, sampling dates, plot and species identifiers.
- Seedling leaf chlorophyll data
  - SWELTR_chlorophyl.csv
  - Variables include PLOT, SPECIES, CCI (chlorophyll content index), TREAT.
- Soil resin nutrients
  - SWELTR_soilresins.csv
  - Variables include P (mineralised PO4), NH4, NO3, total inorganic N (TIN), sample metadata (pre/post, RMONTH, Plot, plotpair, season), date, and readings per resin.

## Experimental design and sampling regime
- Plot layout and warming
  - 10 circular paired plots (control vs. heated) across ~1 ha.
  - Heated plots heated to ~4°C across soil profile (up to ~1.5 m); surface soils heated ~3°C.
  - Heating footprint: 16 heating rods per plot with legs extending to 1.2 m depth.
- Seedling plots
  - Seedling plots inside each plot: square 1.5 m × 1.5 m.
  - 6 rows × 6 individuals per row; each seedling plot contains 36 individuals (n = 360 seedlings total).
  - Species composition includes three N-fixers and three non-N-fixers; seeds collected in 2015 nearby and germinated/shaded before transplanting in early wet season 2016 (July–August).
- Measurements and timing
  - Seedling census every 3 months (height, herbivory, etc.).
  - Soil resin measurements monthly (N and P mineralisation) for three years.
  - Leaf chlorophyll measurements taken September 2022 (n = 10 leaves per species/plot, sampled across independent individuals).
- Parameters recorded
  - Seedling growth metrics: height, relative growth rate (RGR) modeled with a first-order power-law approach.
  - Light environment: photosynthetic photon flux density (PPFD) above seedlings; both overcast and sunny-day measurements used to derive representative light conditions.
  - Physiological: gas-exchange parameters (Amax, conductance, CO2, transpiration, leaf temperature, etc.).
  - Nutrient availability: extractable inorganic N (NH4, NO3) and P (PO4) via resin membranes; rate-derived per g resin per day.
  - Biotic interactions: herbivory index (0–3 scale).

## Data processing and analysis
- Growth modeling
  - Relative growth rate (RGR) estimated from a first-order power-law model using the slope of log(height) vs log(time in months).
  - β parameter used to assess warming treatment effects on growth rates.
  - RGR values computed for each individual seedling (n = 30 per species per plot set) and compared pre- and post-warming periods (RGR_power_pre vs RGR_power_post).
- Quality control
  - Data underwent quality control in R to identify outliers and ensure correct seedling identification and proper blank/standard usage.
- Metadata and provenance
  - Detailed file-level descriptions, sampling dates, Pre/Post designation, and relative month (RMONTH) relative to warming onset (RMONTH = 0).

## Data governance, access, and reuse
- Documentation and structure
  - Data are organized into five separate CSV files with explicit column definitions and units, enabling cross-file linkage via common identifiers (PLOT, PLOTPAIR, SPECIES, TREAT, RMONTH, PREPOST, DATE).
- Stewardship considerations
  - Data authorship and contributions: A. T. Nottingham, M. Montero-Sanchez, M. Slot, H. A. Szczygieł, E. Velasquez, P. Meir; affiliations listed.
  - Plans to upload datasets to relevant data portals and catalogue holdings; maintain dataset updates and respect sharing limitations as part of ongoing data governance.
- Potential usage
  - Suitable for analyses of warming effects on seedling growth, photosynthesis, nutrient mineralization, and species- and N-fixer–vs–non-N-fixer–dependent responses.
  - Provides a robust multi-species tropical forest seedling dataset with linked growth, physiology, and soil nutrient data under a controlled warming experiment.

## Author and contact information
- Authors: A. T. Nottingham, M. Montero-Sanchez, M. Slot, H. A. Szczygieł, E. Velasquez, P. Meir
- Institutions: University of Leeds, Smithsonian Tropical Research Institute, University of Edinburgh
- Data provenance: clearly described experimental design, collection methods, and data transformation steps to support reproducibility and reuse.