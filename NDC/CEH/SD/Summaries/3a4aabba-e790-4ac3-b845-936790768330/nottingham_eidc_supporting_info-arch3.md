# Seedling growth declines in warmed tropical forest soils

## Overview
- Experiment at the Soil Warming Experiment in Lowland Tropical Rainforest (SWELTR), Barro Colorado Island, Panama (9.1521° N, 79.8465° W).
- Whole soil profile warmed by 4°C; surface soils warmed ~3°C (0–20 cm) on average.
- Seedling community: six shade-tolerant species (Inga laurina, Ormosia macrocalyx, Tachigali versicolor, Lacmellea panamensis, Protium pittieri, Virola surinamensis); three N-fixers and three non-N-fixers.
- Data describe seedling growth, physiology, herbivory, and soil nutrient mineralisation over 2016–2022, with monthly resin-based soil N and P measurements and periodic leaf traits.
- Data are organized into multiple CSV files with detailed metadata fields.

## Experimental design and sampling regime
- Ten paired plots: control (ambient) and heated ( warmed) across ~1 ha.
- Heated plots achieve ~4°C soil warming to ~1.5 m depth; surface soil warmed ~3°C.
- Seedling plots inside each experimental plot: square plots ~1.5 × 1.5 m, containing 36 seedlings (6 species × 6 replicates per plot), arranged in randomized order per row; total of 360 seedlings across all plots.
- Seedling transplantation occurred in early wet season 2016; seeds collected nearby in 2015.
- Seedling measurements conducted over 2016–2019 (growth census every 3 months); monthly soil resin measurements; additional measurements (e.g., chlorophyll) conducted later (2022 for chlorophyll).

## Data collected and structure (files and key variables)
- Seedling growth and physiology data files:
  - SWELTR_seedlings_RGRs.csv: relative growth rates (RGR) by species and plot; includes RGR_power, pre/post values, and related growth metrics.
  - SWELTR_seedlings.csv: seedling height, leaf count, herbivory index, PPFD metrics, treatment, plot, replication, species, and relative month (RMONTH); pre/post indicators.
  - SWELTR_seedlings_gasex.csv: gas-exchange parameters (Amax, stomatal conductance, intercellular CO2, transpiration, leaf/air temperatures, vapor pressure deficit, PAR, etc.) with treatment, plot, species codes, and environmental conditions.
  - SWELTR_chlorophyl.csv: leaf chlorophyll content index (CCI) by plot and species; treatment.
- Soil nutrients data file:
  - SWELTR_soilresins.csv: in situ soil resin measurements for extractable PO4, NH4, NO3, and total inorganic N; includes pre/post indicator, relative month (RMONTH), plot metadata, season, treatment, and sampling date; resin-based mineralisation rates per g resin per day.
- Data fields and organization:
  - Plot, PLOTPAIR (paired warmed vs. control), TREAT (Warmed vs. Control), REPLICATE, SUBPLOT, SPECIES, RMONTH (relative to warming start, 0), MONTH/YEAR, and date-specific measurements.
  - Soil resin measurements include pre/post, date, P, NH4, NO3, TIN (total inorganic N), and resin-specific sampling details.
  - Chlorophyll dataset notes Plot, Species, and TREAT.
  - Missing data represented as NA.

## Analytical methods and approaches
- Relative growth rates (RGR) calculated for each seedling using a first-order power-law model; RGR_power denotes growth rate derived from height changes over time; RMONTH marks the start of warming (0).
- Height measured from soil surface to shoot apex; PPFD measured monthly above each seedling under overcast and clear conditions.
- Light-saturated photosynthesis (Amax) measured with portable photosynthetic system (LI-COR) during gas-exchange campaigns.
- Soil nutrient availability assessed with in situ resin membranes; monthly deployments and chemical analyses (PO4, NH4, NO3) via flow-injection analysis; calculation of mineralised N and P per g resin per day.
- Leaf chlorophyll quantified via chlorophyll content index (CCI) on a subset of leaves.
- Herbivory assessed with a continuous damage scale (0–3).
- Data quality control steps include verification of seedling identities and appropriate use of blanks/standards prior to analyses; data were processed in R.

## Data availability and metadata considerations
- Data are distributed across multiple, clearly named CSV files with explicit column headers and units.
- Metadata include: pre/post treatment status, relative timing (RMONTH), plot and treatment identifiers, seasonal context (dry/wet season), and measurement timing.
- Some fields may be unavailable (NA) due to equipment or analysis constraints; data transparency is supported by explicit field definitions and documentation.
- The data structure supports cross-variable monitoring of warming effects on seedling growth, physiology, herbivory, and soil nutrient dynamics over time.

## Relevance for Monitoring Frameworks
- Provides a comprehensive, time-resolved dataset linking soil warming to seedling performance and soil nutrient availability in a tropical forest context.
- Enables evaluation of environmental health indicators such as growth responses, photosynthetic capacity, nutrient mineralisation, and herbivory under controlled warming.
- Demonstrates practical data governance and data sharing considerations (multiple data files with consistent metadata, pre/post design, time alignment), highlighting challenges such as data silos, metadata completeness, and cross-dataset integration for decision-making.
- Supports pre/post intervention analyses and the assessment of data quality, openness, and reproducibility crucial for monitoring frameworks.