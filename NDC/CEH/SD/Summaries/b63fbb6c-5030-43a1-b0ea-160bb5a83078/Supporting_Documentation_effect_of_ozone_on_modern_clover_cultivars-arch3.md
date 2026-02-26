# Supporting documentation - Effect of ozone on modern clover cutlivars

- Purpose of the study
  - Investigates ozone effects on two modern clover cultivars ( Crusader and Merviot ) to understand physiological and growth responses under ozone regimes reflecting future scenarios.

- Experimental design and plant material
  - Clover cultivars: Trifolium repens cv. Crusader and Trifolium pratense cv. Merviot.
  - Propagation: seeds grown in plugs, transplanted to 5 L pots with sterile topsoil; soil inoculated with a microbial slurry from agricultural grassland to introduce soil microbes.
  - Environment: seven solardomes housing six pots per cultivar per dome; randomised ozone treatments.
  - Timeline: exposure from 11/07/2012 to 03/10/2012 (three months).
  - Ozone setup: ozone generated and delivered into charcoal-filtered air; concentration monitored every 30 minutes with paired analyzers.
  - Climate monitoring: one dome tracked ambient temperature, PAR, and vapour pressure deficit; plants rotated weekly; soil moisture maintained near field capacity.
  - Treatment rationale: treatments mirror projected future ozone scenarios with peak levels reduced relative to background; no explicit treatment replication, discussed as a pseudo-replication consideration.

- Measurements and response variables
  - Ozone injury and senescence
    - Injury scored as the percentage of leaves with >25% leaflet injury; recorded per representative quarter of each pot.
    - Additional metrics: injuries and senescence combined; flower numbers recorded.
  - Stomatal conductance (gs)
    - Measured on abaxial leaf surface using porometer; multiple time points during growth; data filtered for ambient PAR influences.
  - Biomass
    - Above-ground shoot biomass (dry weight) harvested after 12 weeks (and a mid-season shoot harvest for Merviot in late August).
    - Below-ground biomass harvested from a representative quarter (with adjustments for sampling practicality).
  - Root nodules
    - Nodules excised, counted, weighed; size categorized into <0.1-0.7 mm and 0.7-1.5 mm.
    - Calculations for nodules per pot, nodule biomass per root, and related root/nodule biomass metrics.
  - Nitrogenase activity
    - Acetylene reduction assay performed on Crusader in treatments 1 and 7 to estimate nitrogen fixation.
    - Ethylene measured via gas chromatography at 0, 4, 8, and 24 hours; a control bottle established baseline ethylene production.
  - Ozone exposure metric
    - AOT40 (accumulated exposure above 40 ppb during daylight at canopy height) used as the primary exposure metric; data summarized per treatment.

- Data collection and formats
  - Data files include:
    - Acetylene reduction assay results (nitrogenase_ files): nitrogenasesep.csv, nitrogenaseoct.csv (13 columns each with sampling date, vial, pot, dome, ozone metrics, ethylene measurements, etc.).
    - Stomatal conductance (gs) data: crusadergs.csv, merviotgs.csv (10 columns: species, cultivar, time, date, week, dome, gs, etc.).
    - Above-ground biomass: crusaderabovegroundweek11.csv, merviotabovegroundweek7.csv, merviotabovegroundweek11.csv (9 columns: date, cultivar, dome, ozone, pot, starting size, biomass values, etc.).
    - Injury and senescence: senescence.csv (15 columns: date, species, cultivar, dome, pot, starting size, mean ozone, flower number, injury, senescence, total injury, leaf counts, and percentages).
    - Nodule size: nodule_size.csv (10 columns: date, species, cultivar, dome, ozone, pot, starting size, nodule size category, count).
    - AOT40 ozone data: aot40.csv (20 columns: date, day, week, time, domes 1–8 ozone, and eight corresponding 40 ppb above-threshold indicators).
    - Below-ground biomass: crusaderbelowground.csv, merviotbelowground.csv (date, species, cultivar, dome, mean ozone, AOT40, pot, starting size, soil mass data, root and nodule metrics, biomass totals, etc.).
  - Missing values: indicated where plant material was absent or undetermined.

- Data analysis approach
  - Injury and gs: analyzed by general linear regression using 3-week injury data or 12-week AOT40 as predictor.
  - Biomass and nitrogenase activity: analyzed by one-way ANOVA with 12-week or 10–11-week AOT40 values as factor.
  - Nodule size: analyzed separately by each size category against 12-week AOT40.
  - PAR-related outliers: gs data filtered using the 25th–75th percentile range to mitigate extreme PAR effects.
  - Post-hoc analysis: Tukey's HSD for pairwise mean differences when ANOVA showed ozone effects.
  - Software: analyses conducted in R (version 2.15.2).
  - Replication caveat: authors acknowledge potential pseudo-replication due to limited treatment replication but argue that increased treatment diversity provides broader dose-response insights, citing Mills et al. 2009 and Hayes et al. 2012.

- Key considerations for interpretation
  - The study provides a comprehensive dataset linking ozone exposure to physiological (gs, injury), growth (shoot and root biomass), nodulation, and nitrogen fixation responses in clover.
  - The experimental design employs controlled ozone dosing and detailed environmental monitoring but notes limitations related to replication that may influence inference about treatment effects.
  - The inclusion of detailed data files and explicit column definitions facilitates reuse, cross-study comparisons, and monitoring-focused analyses for environmental policy and management contexts.