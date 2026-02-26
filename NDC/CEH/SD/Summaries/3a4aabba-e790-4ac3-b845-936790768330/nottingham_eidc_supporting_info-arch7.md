# Seedling growth declines in warmed tropical forest soils

## Overview
- Long-term experiment on soil warming in a lowland tropical rainforest on Barro Colorado Island, Panama (SWELTR).
- Whole soil profile heated by ~4°C; surface soil warmed ~3°C.
- Six shade-tolerant seedling species (three N-fixers: Inga laurina, Ormosia macrocalyx, Tachigali versicolor; three non-N-fixers: Lacmellea panamensis, Protium pittieri, Virola surinamensis).
- 10 paired plots (control vs heated) across ~1 hectare; seedling plots within each plot contain 36 individuals (6 species x 6 replicates), totaling 360 seedlings.
- Data span 2016–2022, with seedling census every ~3 months and monthly soil resin nutrient measurements.

## Study site and spatial design
- Location: SWELTR site, Barro Colorado Island, Panama (approximate coordinates 9.1521° N, 79.8465° W).
- Plot structure: circular main plots (~3.5 m internal diameter; heated footprint to ~5 m external diameter) with heating rods around the inner circumference and 16 legs extending to 1.2 m depth.
- Seedling plots: square subplots ~1.5 × 1.5 m inside each circular plot, containing 6 rows of 6 individuals (all six species randomized within each row).

## Data collection and parameters
- Seedling growth and condition:
  - Relative growth rates (RGR) and height changes
  - Herbivory index (0 = none to 3 = heavy damage)
  - Leaf chlorophyll content (CCI)
  - Light-limited and light-saturated photosynthesis (Asat) and PPFD
- Soil and nutrient measurements:
  - In situ resin-based mineralisation measurements for N and P (monthly over three years)
  - Extractable PO4-P, NH4-N, NO3-N per g resin per day
- Sampling regime:
  - Seedling census every ~3 months (2016–2019 data collection period)
  - Resin measurements monthly (during the same period)
  - Chlorophyll measured in Sept 2022 on a subset of leaves
- Data transformation and analysis:
  - RGR estimated via a first-order power-law model; growth rate parameter (β) used to assess warming effects
  - Quality control in R (outlier checks, correct seedling identification, blanks/standards)

## Data files and key fields
- SWELTR_seedlings_RGRs.csv
  - Core fields: SPECIES, PLOT, PLOTPAIR, TREAT, REPLICATE, RGR_power, RGR_power_post, RGR_power_pre, LUZ_SUN, LUZ_CL, HERB, Nfix
- SWELTR_seedlings_gasex.csv
  - Core fields: Time, Species, Plot, Treat, Nfix, Light_Cl_Nov19, Tset, Photo, Cond, Ci, Trmmol, VpdL, Area, StmRat, Tair, Tleaf, TBlk, CO2R, CO2S, H2OR, H2OS, RH_R, RH_S, Flow, PARi, Press
- SWELTR_seedlings.csv
  - Core fields: PLOT, REPLICATE, SUBPLOT, PLOT_CODE, SP_CODE, SPECIES, RMONTH, MONTH, YEAR, HEIGHT, LIGHT_CL, LIGHT_SUN, LEAVES, HERBIVORY, PREPOST
- SWELTR_chlorophyl.csv
  - Core fields: Plot, Species, CCI, TREAT
- SWELTR_soilresins.csv
  - Core fields: prepost, Rmonth, Plot, plotpair, Sample, season, treat, Date, P (PO4), NH4, NO3, TIN, NA notes

## Measurements and methods
- Instruments:
  - PPFD: LI-250A light meter; PPFD measured monthly on overcast and clear days
  - Asat: LI-6400 portable photosynthetic system with standard leaf cuvette and CO2 mixer
  - Chlorophyll: MC-100 chlorophyll meter (CCI computation from transmittance at 931 nm and 653 nm)
  - Soil nutrients: in situ resin membranes (Dowex Marathon Mr-3) with extraction via 0.5 M HCl; nutrient analysis via Lachat Quickchem 8500
- Experimental design details:
  - 10 paired plots; heated plots heated to ~4°C soil profile (≈1.5 m depth)
  - Seedling plots established in early wet season 2016; 360 seedlings across plots
- Data processing:
  - Outlier checks and verification of seedling identification and blanks/standards
  - Data are provided in separate CSV files for growth, gas exchange, chlorophyll, leaf data, and soil resins

## Temporal scope
- Overall data collection: 2016–2022
- Seedling census: 2016–2019
- Soil resin measurements: monthly over three years within the study period
- Chlorophyll measurement: September 2022

## Data management and integration considerations for GIS
- Data are distributed across five CSV files, requiring join via key fields (plot ID, plot pair, treatment, and species) to build spatially integrated datasets.
- Spatially explicit elements include plot-level heating treatment, paired-control design, and the seedling subplot arrangement within each plot.
- Temporal metadata (RMONTH, DATE) enables time-series analyses and aligning growth, photosynthesis, and soil nutrient data with warming duration.
- Data are robust for GIS analyses linking spatial variation in growth responses to micro-environmental and soil nutrient gradients, though precise geographic coordinates for each plot are not included in the file metadata and may need to be sourced from project/site metadata.

## Summary for GIS use
- Suitable for creating map-based visualisations of warming effects on seedling growth across the 10 plots.
- Can be combined with soil resin nutrient data to explore spatial correlations between nutrient availability and growth/physiological responses.
- Temporal aspects allow exploration of treatment onset effects (pre- vs post-warming) and seasonal dynamics.
- Requires data integration steps to merge multiple CSVs using common identifiers (plot, plotpair, species, replicate) for cohesive GIS analyses.