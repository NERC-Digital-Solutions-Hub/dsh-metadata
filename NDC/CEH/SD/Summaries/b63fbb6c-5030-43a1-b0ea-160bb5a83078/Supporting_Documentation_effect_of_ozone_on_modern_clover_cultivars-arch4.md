# Supporting documentation - Effect of ozone on modern clover cutlivars

- Purpose and scope
  - Phytometer-style study assessing how ozone affects two modern clover cultivars, Crusader and Merviot, over a three-month period in controlled solardomes.
  - Aimed at understanding ozone injury, physiological responses (stomatal conductance), biomass allocation (shoot/root/nodule), and nitrogenase activity under ozone exposure.

- Experimental design and environment
  - Plants: Crusader (medium-leaved) and Merviot (finisher) grown from UK-sourced seeds in John Innes No. 2 compost, then transplanted into 5 L pots with sterile topsoil and soil microbial inoculum from agricultural grassland.
  - Setup: 7 solardomes (3 m diameter, 2.1 m high) at CEH solardome facility; 6 pots per cultivar per solardome; randomised ozone treatments reflecting future scenarios.
  - Ozone treatment: Computer-controlled generation and delivery system with fluorinated air, delivering episodic profile treatments based on a rural monitoring site; 11/07/2012–03/10/2012 exposure.
  - Measurements and monitoring: ozone concentration in domes (two analyzers), temperature, PAR, and vapour pressure deficit; soil moisture monitored; weekly plant rotation; irrigation to field capacity.

- Measurements and data collected
  - Injury and senescence: percent injured leaves and total injury (leaf area >25% injured), collected per representative quarter of each pot.
  - Stomatal conductance (gs): measured on abaxial leaf surface with porometer across seasons; data filtered to exclude PAR extremes.
  - Biomass: shoot and root biomass for each pot; above-ground measurements at 11 weeks; mid-season shoot harvest for Merviot; below-ground biomass quantified for select treatments due to handling time.
  - Nodules: number and biomass; organ-size categorised into two size classes (<0.1-0.7 mm; 0.7–1.5 mm).
  - Nitrogenase activity: acetylene reduction assay (ARA) on Crusader in treatments 1 and 7; ethylene production measured over 0, 4, 8, and 24 hours.
  - Soil/plant metrics: AOT40 (accumulated ozone exposure above 40 ppb during daylight at canopy height), soil mass by quarter, total soil mass per pot, and representative quarter mass used for normalization.
  - Data organization: a comprehensive set of CSV files capturing ozone data, gs, biomass, injury/senescence, nodules, AOT40, and below-ground biomass.

- Data files and structures (summary)
  - Acetylene reduction data: nitrogenasesept.csv and nitrogenaseoct.csv (13 columns; date, vial, pot, dome, mean.ozone, ethylene metrics, time steps).
  - Stomatal conductance: crusadergs.csv, merviotgs.csv (10 columns; species, cultivar, week, dome, mean ozone, gs, starting size).
  - Above-ground biomass: crusaderabovegroundweek11.csv, merviotabovegroundweek7.csv, merviotabovegroundweek11.csv (9 columns; date, cultivar, dome, mean ozone, biomass measures).
  - Injury and senescence: senescence.csv (15 columns; injury, senescence, percent injured, leaves counted, etc.).
  - Nodule size: nodule_size.csv (10 columns; mean ozone, nodule size category, counts).
  - AOT40 ozone data: aot40.csv (20 columns; dome-wise ozone measurements and >40 ppb indicators).
  - Below-ground biomass: crusaderbelowground.csv, merviotbelowground.csv (extensive set of columns detailing soil quarters, masses, nodules, root metrics, total biomass).
  - Missing data indicator: Na used for unavailable/missing plant material data.

- Data quality, limitations, and analyses
  - Acknowledged potential pseudo-replication due to limited treatment replication; authors justify more treatments for broader dose-response insights (cited Mills et al., 2009; Hayes et al., 2012).
  - Controls and replication across domes ensured via randomization and matched airflow; climatic conditions reported as not significantly different between domes.
  - Statistical approaches: general linear regression for injury and gs using 3-week or 12-week AOT40 values; ANOVA for biomass and ARA using 12-week and 10–11 week AOT40 as factors; outliers filtered for gs based on PAR quartiles; post hoc Tukey tests for significant ANOVA results.
  - Software: analyses performed in R (version 2.15.2).

- Data use and relevance for data leadership
  - Demonstrates end-to-end data handling: from complex experimental design and data collection to multi-faceted data files with explicit metadata.
  - Provides a model for building programs around data discoverability, metadata consistency, and cross-study comparability (AOT40-based exposure metrics, standardized biomass and physiological measurements).
  - Highlights practical data governance considerations: explicit variable definitions, units, data provenance, handling of missing data, and explicit caveats about replication and interpretation.
  - Useful for cross-institution data sharing, dose-response modelling, and informing data standards for environmental exposure studies involving plants and ozone.