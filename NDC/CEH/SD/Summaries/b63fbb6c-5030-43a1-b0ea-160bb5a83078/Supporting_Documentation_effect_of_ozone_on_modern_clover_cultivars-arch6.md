# Supporting documentation - Effect of ozone on modern clover cultivars

## Overview
- Study on ozone effects using two clover cultivars: Crusader (Trifolium repens) and Merviot (T. pratense).
- Plants grown in pots with soil inoculation to introduce a soil microbe population; exposed to a range of ozone treatments reflecting future scenarios.
- Objectives: assess ozone-induced injury, physiological responses (stomatal conductance), biomass development (shoot, root, nodules), nodulation metrics, and nitrogenase activity (via acetylene reduction assay).
- Data produced are intended to support exploration of ozone-health and productivity relationships and to enable cross-cultivar comparisons.

## Experimental design highlights
- Cultivars and origin:
  - Crusader and Merviot seeds sourced in the UK; grown in seedling trays, transplanted into 5 L pots with sterile topsoil.
- Soil and cultivation:
  - Pots inoculated with 200 ml soil slurry from agricultural grassland; plants grown for 4 weeks before ozone exposure.
- Ozone exposure:
  - 7 solardomes (3 m diameter, 2.1 m high) with randomised ozone treatments; 6 pots per cultivar per dome.
  - Treatments based on episodic profiles from Aston Hill, Wales; designed to reflect future ozone scenarios; peak concentrations reduced relative to background.
  - Exposure period: 11 July 2012 to 3 October 2012 (approximately 3 months).
  - Ozone delivery via G11 and oxygen generators; monitored with two analyzers every 30 minutes.
  - Continuous environmental monitoring in at least one dome (temperature, PAR, VPD); weekly rotation of plants; irrigation to near field capacity.
- Measurements and sampling:
  - Injury assessment after 3 weeks: number of injured leaves (>25% leaflet area) expressed as percent of total leaves.
  - Stomatal conductance (gs) measured throughout the season under fluctuating conditions on leaves with <10% injury.
  - Harvest after 12 weeks for shoot, root, and nodules; mid-season shoot harvest for Merviot at 7 weeks.
  - Below-ground biomass sampled in a subset (treatments 1, 4, 7) due to labor intensity.
  - Nodules counted, weighed, and categorized by size.
  - Biomass variables normalized and expressed relative to accumulated ozone exposure (AOT40; ppm·h) above 40 ppb during daylight at canopy height.
  - Nitrogenase activity assessed with acetylene reduction assay ( Crusader in treatments 1 and 7).
- Data handling and limitations:
  - Acknowledgement of potential pseudo-replication due to lack of true treatment replication; authors justify design with precedent in literature.
  - Consistent airflow across domes and comparable climatic conditions reported.
- Analysis approach:
  - Injury and gs: general linear regression using 3-week (injury) or 12-week AOT40 as predictor.
  - Biomass and nitrogenase-related measures: one-way ANOVA with 12-week AOT40 (or 10–11 week AOT40 for some analyses) as a factor.
  - Nodule size categories analyzed against 12-week AOT40.
  - Outlier handling for PAR: gs data filtered by 25th–75th percentile range.
  - Software: R version 2.15.2.

## Datasets and structure
- Acetylene reduction assay files
  - nitrogenasesept.csv
  - nitrogenaseoct.csv
  - Columns include: Date, Vial, Pot, Dome, mean.ozone (ppb), peak area (ethylene), Time.step, ethylene-related metrics, and ethylene production.
- Stomatal conductance
  - crusadergs.csv
  - merviotgs.csv
  - Columns include: Species, Cultivar, Time, Date, week, Dome, mean.ozone, Pot, starting.size, gs.
- Above-ground biomass
  - crusaderabovegroundweek11.csv
  - merviotabovegroundweek7.csv
  - merviotabovegroundweek11.csv
  - Columns include: Date, Cultivar, Dome, mean.ozone, Pot, starting.size, bag.g, shoot.biomass.bag.g, shoot.biomass.g.
- Injury and senescence
  - senescence.csv
  - Columns include: Date, species, Cultivar, Dome, Pot, Starting.size, Mean ozone, Flower number, Injury, Senescence, Total injury, Number of leaves, Percent.injured, Percent.senesced, Percent.injury.
- Nodule size
  - nodule_size.csv
  - Columns include: Date, species, cultivar, Dome, mean.ozone, Pot, starting.size, size, category, number.
- AOT40 data
  - aot40.csv
  - Columns include: Date, day, week, Time, Dome1–Dome8 ozone values, and Dome1–Dome8 >40 indicators.
- Below-ground biomass
  - crusaderbelowground.csv
  - merviotbelowground.csv
  - Extensive set of columns for soil quarters, corrected masses, total soil masses, representative quarters, root and shoot masses, nodules, and derived metrics (e.g., root:shoot, root:total, total biomass, nodules per pot, mass per nodule).
- Additional notes:
  - Na indicates missing values where plant material is unavailable or not determined.
  - All data pertain to a phytometer-style experiment examining ozone impacts on ozonated clover cultivars, including physiological, morphological, nodulation, and nitrogen-fixation outcomes.

## Data usage and integration suggestions
- Potential data products:
  - Dose–response curves for injury, gs, biomass components, and nitrogenase activity as a function of AOT40.
  - Time-aligned dashboards comparing ozone exposure (AOT40 and PPB) with physiological responses across cultivars.
  - Cross-dataset summaries by dome, pot, and cultivar to explore replicate-like patterns and variability.
- Data integration considerations:
  - Align time scales across gs measurements, injury assessments, and biomass harvests.
  - Use AOT40 (12-week or 10–11-week values as appropriate) to normalize ozone exposure across measurements.
  - Join datasets via common keys: Dome, Pot, Cultivar, Date/Week for consistent analyses.
- Quality assurance tips:
  - Be mindful of the pseudo-replication limitation when interpreting treatment-level effects; consider dome-level effects as a potential random factor if reusing dataset for broader analyses.
  - Validate PAR exclusion and outlier handling steps when reproducing gs analyses.
  - Ensure handling of missing values (Na) in below-ground and nitrogenase datasets during modeling.

## Practical takeaways for data support
- Rich, multi-dimensional dataset linking ozone exposure to plant injury, physiology, growth, nodulation, and nitrogen fixation in two clover cultivars.
- Comprehensive ozone metrics (PPB and AOT40) with detailed time windows for different response variables.
- Data files are well-documented with explicit column descriptions, enabling straightforward data cleaning, joining, and exploratory analyses.
- Suitable for developing data products that illustrate ozone dose–response patterns and cultivar-specific susceptibilities, as well as for validating or extending dose–response models in future studies.