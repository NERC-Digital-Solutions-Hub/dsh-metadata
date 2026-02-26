# Seedling growth declines in warmed tropical forest soils

## Overview
- Study of seedling growth parameters for six tropical tree species in a lowland rainforest in Panama, under experimental soil warming.
- Location: Soil Warming Experiment in Lowland Tropical Rainforest (SWELTR), Barro Colorado Island, Panama.
- Warming treatment: entire soil profile warmed by 4°C (surface soils heated ~3°C; depth to ~1.5 m).
- Species: Inga laurina, Ormosia macrocalyx, Tachigali versicolor (N-fixers), Lacmellea panamensis, Protium pittieri, Virola surinamensis.
- Data span: seedling data collected 2016–2019; additional measurements (chlorophyll) 2022; soil resin nutrients measured monthly over the experimental period.
- Data organization: spread across multiple CSV files with rich metadata for each dataset.

## Experimental design
- Plot layout: 10 paired control and heated plots over ~1 ha; heated plots have a heating footprint of ~5 m diameter with 16 heating rods extending to 1.2 m depth.
- Seedling plots inside each experimental plot: square 1.5 x 1.5 m, containing 36 seedlings (6 species x 6 replicates per seedling plot), total of 360 seedlings across all plots.
- Seedling establishment: seeds collected in 2015 from Barro Colorado Island, germinated in shade house, transplanted during early wet season 2016.
- Species composition: 6 species with randomised intra-row order; 5 paired sets (A–E) of control vs heated plots.

## Data collected and key variables
- Seedling growth parameters
  - Relative growth rates (RGR) calculated using a first-order power-law model; RGR determined per seedling (based on height over time) and summarized by species and treatment.
  - Height measurements (cm) and herbivory index (0–3 scale) recorded per seedling.
- Light environment
  - Photosynthetic photon flux density (PPFD) measured monthly for each seedling; two metrics captured: above-seedling measurements on overcast and clear days.
  - Light-saturated photosynthesis (Asat) obtained via LI-COR gas-exchange system.
- Gas exchange and leaf physiology
  - Gas-exchange parameters: Amax (light-saturated photosynthesis), stomatal conductance, intercellular CO2, transpiration, leaf-to-air vapor pressure deficit, leaf area, stomatal ratio, leaf temperatures, and related chamber/ambient conditions.
  - Measurement period highlighted by a Nov 2019 campaign for gas-exchange data.
- Leaf chlorophyll
  - Chlorophyll content index (CCI) measured on 10 leaves per species per plot (Sept 2022), using a chlorophyll meter.
- Soil nutrient availability
  - In situ resin membrane approach to quantify mineralised soil N and P: PO4-P, NH4-N, NO3-N and total inorganic N (TIN) per g resin per day.
  - Monthly deployments at 5 cm depth across plots; pre/post warming status recorded.
- Metadata and structure
  - Pre/post warming indicator, relative month (Rmonth) since warming onset, plot and plot-pair IDs, season (dry/wet), sampling date, and treatment (control vs warmed).
  - Data are provided as separate CSV files with defined column schemas.

## Data collection and processing methods
- Collection timeline
  - Seedling census every 3 months; soil parameters collected monthly; measurements span 2016–2019 for seedling growth and gas exchange, with chlorophyll data in 2022.
- Measurements and instruments
  - Height: measured from soil surface to shoot apex with a tape measure.
  - PPFD: measured with LI-250A light meter; monthly readings for overcast and clear day conditions.
  - Asat: measured with LI-6400 portable photosynthesis system using standard leaf cuvettes.
  - Soil nutrients: resin membranes extracted with 0.5 M HCl and analyzed for PO4, NH4, and NO3 using Lachat Quickchem 8500.
  - Chlorophyll: CCI calculated from 931 nm and 653 nm transmissions.
- Data quality
  - Quality control performed on all data prior to analysis to ensure seedling identification, correct blanks/standards, and data integrity.
  - NA values indicate unavailable data due to equipment or analyses.

## Data files and structure
- Seedling relative growth rates: SWELTR_seedlings_RGRs.csv
  - Key fields: SPECIES, PLOT, PLOTPAIR, TREAT, REPLICATE, RMONTH, RGR_power, RGR_power_post, RGR_power_pre, additional leaf- and light-related averages.
- Seedling gas-exchange parameters: SWELTR_seedlings_gasex.csv
  - Key fields: Time, Species, Plot, Treat, Nfix, Amax (Light_Cl_Nov19), Ci, Gs (stomatal conductance), Transpiration, VPD, PARi, etc.
- Seedling height and herbivory measurements: SWELTR_seedlings.csv
  - Key fields: HEIGHT, LEAVES, HERBIVORY, PREPOST, etc.
- Seedling leaf chlorophyll data: SWELTR_chlorophyl.csv
  - Key fields: Plot, Species, CCI, TREAT.
- Soil resin nutrients: SWELTR_soilresins.csv
  - Key fields: P (PO4), NH4, NO3, TIN, pre/post, Rmonth, Plot, plotpair, season, Date, treat, etc.
- Data descriptions confirm the presence of pre/post indicators, relative timing (Rmonth), plot identifiers, species codes, and measurement metadata.

## How data can be used (for Data Leaders perspective)
- Evaluate how soil warming influences seedling growth trajectories across multiple species, including N-fixers vs non N-fixers.
- Compare above- and below-ground proxies of plant response: height growth, RGR, leaf chlorophyll, photosynthetic capacity, and water use indicators.
- Investigate links between soil nutrient mineralisation (N and P) and seedling performance under warming.
- Explore spatiotemporal patterns by plot, season, and relative warming month to identify potential lag effects or transient responses.
- Support data governance and collaboration efforts by providing a well-documented, multi-file dataset with clear metadata and standardized measurements suitable for cross-study synthesis and broader data sharing.