# Seedling growth declines in warmed tropical forest soils

- The study documents data from an experimental soil warming experiment (SWELTR) in a lowland tropical rainforest on Barro Colorado Island, Panama.
- Objective: quantify seedling growth and related physiological and soil parameters under soil warming (+4°C across the soil profile; surface warming ~3°C) over multiple years and species.
- Focus species: six shade-tolerant tree species (Inga laurina, Ormosia macrocalyx, Tachigali versicolor – N-fixers; Lacmellea panamensis, Protium pittieri, Virola surinamensis – non N-fixers).

## Experimental design and sampling

- Location and setup:
  - 10 paired control and heated plots within 1-hectare area.
  - Heated plots warm the soil profile to about 4°C (to ~1.5 m depth); surface soils warmed ~3°C.
  - Heating footprint around the inside of circular plots; 16 heating rods extend to 1.2 m depth.
- Seedling plots:
  - Each main plot contains a seedling plot (1.5 x 1.5 m) with 36 seedlings (6 rows x 6 species; randomised order per row).
  - 5 paired sets of experimental plots (A–E), yielding a total of 360 seedlings (6 species x 60 seedlings per set).
- Species and origin:
  - Seeds collected in 2015 nearby on Barro Colorado Island; germinated in shade house; transplanted during early wet season 2016.
- Sampling regime:
  - Seedling census every 3 months (height, leaf count, herbivory, etc.).
  - Monthly soil resin measurements for N and P mineralisation over three years.
  - Chlorophyll measurements in September 2022 (n = 10 leaves per population, sampled across individuals per species/plot).
  - Herbivory scored on a 0–3 scale (0 = none to 3 = >40% leaf area damaged).

## Measurements and data collection methods

- Seedling growth and physiology:
  - Height: measured from soil surface to shoot apex.
  - Relative growth rates (RGR): derived from height over time using a first-order power-law model; RGR calculated per individual seedling and summarized by species and treatment.
  - Light environment: PPFD measured monthly above each seedling for overcast and clear days; photosynthesis at light-saturated conditions (Asat) measured with LI-COR equipment.
- Gas exchange and leaf physiology:
  - Gas-exchange parameters collected (light intensity, Amax, stomatal conductance, internal CO2, transpiration, leaf temperature, vapor pressure deficit, etc.).
  - N-fixer status (Nfix) recorded for each species.
- Soil nutrients:
  - In situ resin membranes used to estimate mineralised N (NH4+, NO3−) and P (PO4^3−) monthly; results expressed as extractable nutrients per g resin per day.
- Leaf chlorophyll:
  - Chlorophyll content index (CCI) measured on a subset of leaves using a chlorophyll meter.
- Herbivory:
  - Continuous 0–3 scale indicating level of leaf damage.
- Quality control:
  - Data quality checks in R to confirm seedling identification and proper use of blanks/standards.

## Data structure and files

- Seedling relative growth rates
  - SWELTR_seedlings_RGRs.csv
  - Includes: SPECIES, PLOT, PLOTPAIR, TREAT, REPLICATE, RMONTH, RGR_power, RGR_power_post/pre, LUZ_SUN, LUZ_CL, HERB, etc.
- Seedling gas-exchange parameters
  - SWELTR_seedlings_gasex.csv
  - Includes: Time, Species, Light_Cl_Nov19, Tset, Plot, Treat, Nfix, Amax (Photo), Cond, Ci, Trmmol, VpdL, Area, PARi, etc.
- Seedling height and herbivory measurements
  - SWELTR_seedlings.csv
  - Includes: HEIGHT, LEAVES, HERBIVORY, PREPOST, PLOT, REPLICATE, SUBPLOT, SPECIES, RMONTH, MONTH, YEAR, etc.
- Seedling leaf chlorophyll data
  - SWELTR_chlorophyl.csv
  - Includes: Plot, Species, CCI, TREAT
- Soil resin nutrients
  - SWELTR_soilresins.csv
  - Includes: prepost, Rmonth, Plot, plotpair, Sample, season, treat, Date, P, NH4, NO3, TIN, etc.
- Data fields and units are described within each file and include metadata such as pre/post warming status, relative month (RMONTH), plot identifiers, season (dry/wet), and measurement dates.

## Temporal and spatial scope

- Temporal coverage:
  - Field data collected 2016–2019 (seedling census every 3 months; monthly resin measurements for three years).
  - Leaf chlorophyll measurements captured in September 2022.
  - Relative timing defined as RMONTH with warming initiated at month 0.
- Spatial coverage:
  - 10 paired plots within a 1-hectare SWELTR area on Barro Colorado Island, Panama.

## Data usage and potential analyses

- The dataset enables comparisons of warmed versus control seedling performance across six species, with a mix of N-fixer and non–N-fixer taxa.
- Potential analyses include:
  - Assessing warming effects on relative growth rates (RGR) and height trajectories.
  - Linking growth outcomes to physiological measures (Amax, PPFD, stomatal conductance, chlorophyll) and leaf traits (CCI).
  - Exploring relationships between soil mineralisation (N and P) and seedling growth responses.
  - Evaluating species-specific responses and potential differences between N-fixer and non–N-fixer species.
  - Investigating seasonal (dry vs wet) influences on growth and nutrient dynamics.