# Supporting documentation - Effect of ozone on modern clover cutlivars

- Two clover cultivars studied: Crusader (Trifolium repens cv. Crusader) and Merviot (T. pratense cv. Merviot), grown in pots under ozone treatments.
- Purpose: assess ozone effects on modern clover cultivars across physiological, biochemical, and morphological traits; data intended to support understanding of ozone tolerance and potential productivity impacts.

## Experimental design and setup

- Seed origins and propagation:
  - Crusader and Merviot sown in spring 2012, propagated in plug trays, transplanted to 5 L pots with sterile topsoil; 4 seedlings per pot.
  - Soil inoculated with a slurry derived from agricultural grassland soil to establish a soil microbial community.
- Growth environment:
  - 42 pots per cultivar (84 pots total), distributed into 7 solardomes (3 m diameter, 2.1 m high) with randomization of treatments across domes.
  - Plants rotated weekly; watered to maintain soil moisture near field capacity.
- Ozone treatment system:
  - Treatments reflect future ozone scenarios; peak concentrations reduced relative to ambient.
  - Ozone supplied via G11 generator and 8-oxygen generator; delivered in charcoal-filtered air.
  - Concentrations in domes continuously monitored; 5-minute measurements every 30 minutes using two calibrated ozone analyzers.
  - In one dome, continuous monitoring of ambient temperature, PAR, and VPD.
- Harvest and sampling:
  - After 12 weeks, shoot, root, and nodule biomass measured; nodules excised, counted, weighed; nodules sized into two categories.
  - For Merviot, a mid-season (week 7) harvest of shoot biomass performed (cut to 7 cm).
  - Acetylene reduction assay (nitrogenase activity) performed on Crusader in treatments 1 and 7 two weeks prior to assay; ethylene measured via GC at 0, 4, 8, and 24 hours.
- Measurements under ozone exposure:
  - Injury and senescence scored after 3 weeks (leaves with >25% injury considered injured).
  - Stomatal conductance (gs) measured throughout the season across all treatments using a porometer; measurements during daylight with leaves showing ≤10% ozone injury.
  - Soil moisture logged after each measurement.
- Data considerations:
  - An explicit note on potential pseudo-replication: no true replicates per treatment across domes; authors justify by referencing prior work and stating broad treatment-level insights.
  - Air flow and climatic conditions between domes were matched or did not significantly differ where recorded.

## Treatments and ozone data

- Ozone profile:
  - Treatments based on episodic ozone profiles, with randomised assignment across solardomes.
  - Treatments designed to simulate dose-response scenarios; ozone concentration monitored and recorded for each dome.
- Dose metrics:
  - AOT40 (Accumulated Exposure Over a Threshold of 40 ppb, in ppm·h) used to quantify ozone exposure for comparisons across treatments and time points.
  - 12-week AOT40 used for most biomass analyses; 10–11 week AOT40 used for some gs and specific analyses; 3-week injury analyses also linked to exposure values.

## Measurements and variables recorded

- Acetylene reduction assay (nitrogenase activity):
  - Ethylene production measurements (via GC) at multiple time points; data stored with date, vial, pot, dome, mean ozone, time step, etc.
- Stomatal conductance (gs):
  - Species, cultivar, time, date, week, dome, starting size, and gs readings recorded.
- Above-ground biomass:
  - For Crusader and Merviot, shoot biomass per pot (grams) at specified weeks; includes bag tare and corrected shoot biomass.
- Injury and senescence:
  - Injury counts, senescence counts, total injury, leaves counted, percent injured, percent senesced, and overall injury percentage per pot.
- Nodules and root data:
  - Nodule size distribution (two categories), nodule count, and weights; root and shoot masses; below-ground biomass per quarter and total soil mass per pot; root-to-shoot and root-to-total biomass ratios; nodules per pot and nodule mass per pot.
  - Detailed soil quarter measurements including soil mass, corrected masses, container masses, and derived metrics (mass per nodule, nodules per gram root, etc.).
- AOT40 and ozone concentration data:
  - Ozone measurements per dome, with indicators for measurements above 40 ppb (TRUE/FALSE represented in datasets; detailed per dome).
- Data files (described):
  - Acetylene reduction assay files: nitrogenasesept.csv, nitrogenaseoct.csv (13 columns: date, vial, pot, dome, mean.ozone, peak area, time.step, ethylene metrics, etc.).
  - Stomatal conductance: crusadergs.csv, merviotgs.csv (10 columns: species, cultivar, time, date, week, dome, mean ozone, pot, starting size, gs).
  - Above-ground biomass: crusaderabovegroundweek11.csv, merviotabovegroundweek7.csv, merviotabovegroundweek11.csv (9 columns: date, cultivar, dome, mean.ozone, pot, starting size, bag.g, shoot.biomass.bag.g, shoot.biomass.g).
  - Injury and senescence: senescence.csv (15 columns: date, species, cultivar, dome, pot, starting size, mean.ozone, flower number, injury metrics, percent injury, etc.).
  - Nodule size: nodule_size.csv (10 columns: date, species, cultivar, dome, mean.ozone, pot, starting size, size, category, number).
  - AOT40 ozone data: aot40.csv (20 columns: date, day, week, time, eight domes, mean ozone in each dome, and dome-specific >40 ppb indicators).
  - Below-ground biomass: crusaderbelowground.csv, merviotbelowground.csv (dates, species, cultivar, dome, mean.ozone, AOT40, pot, starting size, soil masses across quarters, corrected masses, total soil mass, root/shoot metrics, root masses, nodules, bag, biomass totals, ratios).
- Data usage context:
  - Data sets comprise a phytometer experiment focusing on ozone impacts on two clover cultivars, including physiological responses, biomass, nodulation, and nitrogenase activity, alongside ozone concentration data.

## Statistical analysis and data processing

- Analytical approaches:
  - Injury data: general linear regression with 3-week injury data or 12-week AOT40 as predictor.
  - Stomatal conductance: GLM with 12-week AOT40 as predictor; gc data filtered using PAR-based quartiles to remove outliers.
  - Biomass and acetylene reduction data: one-way ANOVA with 12-week (biomass) or 10–11 week (ARA) AOT40 as a factor.
  - Nodule size: analyzed separately by size category against 12-week AOT40.
- Data handling and tools:
  - Analyses conducted in R (version 2.15.2).
  - Post hoc tests: Tukey’s HSD to assess pairwise differences after significant ANOVA.
  - Some data exclusion decisions due to outliers or insufficient measurements (e.g., insufficient gs data for modeling ozone flux-effect relationships).
- Replication caveat:
  - Acknowledgement of potential pseudo-replication due to lack of true replication for ozone treatment across domes; authors justify with prior studies and improved treatment coverage.

## Data quality, limitations, and considerations for use

- Limitations:
  - Pseudo-replication risk due to single-dome representation per treatment.
  - Some datasets have limited replication for certain measurements (e.g., gs data, nitrogenase assays limited to Crusader treatments in specific domes).
  - Outlier handling and PAR-based filtering may influence gs analyses.
- Data structure considerations:
  - Data are organized per pot, dome, and treatment, enabling dose-response exploration but requiring careful handling of the non-independent dome-level design.
  - Ozone exposure is quantified via AOT40 and mean dome ozone values; domain-specific interpretations should consider the dome-level design.
- Data accessibility and transparency:
  - Comprehensive metadata for each dataset provided; explicit column definitions and units included for reproducibility.
  - Clear documentation of experimental conditions, measurement protocols, and statistical approaches.

## How to use this data

- Potential analyses:
  - Dose–response modelling of ozone exposure (AOT40 and dome mean ozone) against injury, gs, biomass components (shoot, root), nodulation metrics, and nitrogenase activity.
  - Comparative analysis between Crusader and Merviot to identify cultivar-specific ozone sensitivity.
  - Evaluation of relationships between ozone exposure and below-ground vs above-ground biomass allocations, root:shoot ratios, and nodule dynamics.
- Data considerations:
  - Account for pseudo-replication in the design when fitting models; consider dome-level random effects if reanalyzing.
  - Use AOT40 as a primary exposure metric, with supplementary analyses using mean dome ozone concentration where appropriate.
  - When combining datasets (above- and below-ground metrics, ARA data), ensure consistent time points (11–12 weeks and corresponding AOT40) for comparability.
- Expected outputs:
  - Dose-response curves for injury, gs, and various biomass components; statistical comparisons between cultivars and treatment levels; insights into ozone effects on nitrogen fixation via ARA.