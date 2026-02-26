# Supporting documentation - Effect of ozone on modern clover cutlivars

## Overview
- Describes a phytometer-style experiment assessing ozone effects on two modern clover cultivars ( Crusader and Merviot ) and the associated data generated.
- Data encompass ozone exposure, physiological responses, biomass production, root-nodule metrics, and nitrogenase activity.

## Experimental locations and timing
- Plants sown in late spring 2012; grown in glass-house plug trays, then transplanted to 5 L pots with sterile topsoil.
- Soil inoculated with a grassland soil slurry from North Wales (Abergwyngregyn, UK).
- Pots moved to seven solardomes (3 m diameter) near Bangor, North Wales for ozone exposure.
- Ozone treatments designed to reflect future scenarios; exposure period lasted 11–12 weeks in summer–autumn 2012.
- Ozone concentration monitored in each dome; occasional dome had continuous weather monitoring (temperature, PAR, VPD).

## Experimental design and treatments
- Cultivars: Crusader (medium-leaved) and Merviot (rapidly growing, autumn finishing).
- 42 pots per cultivar; 6 pots per dome; randomised treatment assignment across 7 domes.
- Treatments implemented with a dedicated ozone delivery system; multiple mitigation/control measures to simulate realistic exposure.

## Ozone generation, monitoring and environmental conditions
- Ozone produced by a G11 generator; air ozonated and delivered to domes via PTFE tubing.
- Concentrations controlled by a computer system (LabVIEW) and verified with two ozone analysers (measured 5 min every 30 min).
- Ozone profiles designed to reflect episodic future scenarios; peak levels reduced relative to background.
- In one dome, ambient climate data (PAR, temperature, VPD) continuously recorded.
- Plants rotated weekly; soil moisture maintained near field capacity.

## Measurements and data collection
- Injury and senescence: percent of leaves injured (>25% leaflet area) in a representative quarter of each pot.
- Stomatal conductance (gs): measured repeatedly over the season on leaves with <10% injury; data filtered for outliers.
- Biomass: shoot and root masses harvested per pot; below-ground biomass quantified in quarters; nodule (size and count) data collected.
- Nitrogenase activity: acetylene reduction assay conducted for Crusader in two treatments (1 and 7) to estimate nitrogen fixation.
- Nodules: counted and weighed; size categories (<0.7 mm; 0.7–1.5 mm) recorded.
- Derived metrics: mass-per-nodule, root:shoot, root:total biomass, nodules per pot, nodules per gram root, etc.
- Ozone exposure metric: AOT40 (accumulated exposure above 40 ppb during daylight at canopy height) used as predictor in analyses.
- Data are organized in multiple CSV files with fields such as date, dome, mean ozone, pot, measurement, biomass, injury, gs, and nitrogenase outputs.

## Data files and variable structure
- Acetylene reduction assay files
  - acetylene reduction: nitrogenasesept.csv, nitrogenaseoct.csv
  - Columns include date, vial, pot, dome, mean.ozone, ethylene metrics, time steps, and production rates.
- Stomatal conductance
  - crusadergs.csv, merviotgs.csv
  - Columns: Species, Cultivar, Time, Date, week, dome, mean.ozone, pot, starting.size, gs
- Above-ground biomass
  - crusaderabovegroundweek11.csv, merviotabovegroundweek7.csv, merviotabovegroundweek11.csv
  - Columns: Date, Cultivar, dome, mean.ozone, pot, starting.size, bag.g, shoot.biomass.g
- Injury and senescence
  - senescence.csv
  - Columns: Date, species, Cultivar, Dome, Pot, Starting.size, Mean ozone, Flower number, Injury, Senescence, Total injury, Leaves, Percent.injured, Percent.senesced, Percent.injury
- Nodule size
  - nodule_size.csv
  - Columns: Date, species, cultivar, dome, mean.ozone, pot, starting.size, size, category, number
- AOT40 ozone data
  - aot40.csv
  - Columns: Date, day, week, Time, Dome1–Dome8, Dome1 >40–Dome8 >40
- Below-ground biomass
  - crusaderbelowground.csv, merviotbelowground.csv
  - Columns include Date, Species, Cultivar, Dome, mean.ozone, AOT40ppm, pot, starting.size, multiple soil-quarter masses (with and without container), representative.quarter, total.soilmass.per.pot, root and nodule metrics, shoot and root masses, and derived ratios
- Data notes
  - Na indicates missing/unobtainable data.
  - Datasets concern a phytometer-style ozone exposure experiment with measurements across injury, biomass, nitrogen fixation, and ozone concentration data.

## Data analysis
- Injury and stomatal conductance modeled with general linear regression using 3-week (injury) or 12-week (AOT40) values as predictors.
- Biomass and acetylene reduction analyses performed via ANOVA with AOT40 as a factor (12-week for biomass; 10–11 weeks for ARA).
- Nodule size analyses performed per category against 12-week AOT40.
- Outlier handling based on PAR quartiles to reduce influence of abnormal light conditions.
- Post hoc Tukey tests used for pairwise comparisons after significant ANOVA results.
- Analyses conducted in R (version 2.15.2).

## GIS relevance and data usability
- Geospatial context: dome locations near Bangor, UK; soil origin in North Wales; ozone monitoring site (Aston Hill) used to design treatments.
- Potential GIS uses:
  - Map ozone exposure (per dome) against physiological responses (injury, gs, biomass, nodulation) to identify spatial patterns of impact.
  - Integrate with climate and air-quality layers (PAR, VPD, ambient ozone) for scenario planning.
  - Link soil provenance and plant response to regional datasets for UK-scale ozone risk assessments.
- Data quality considerations for GIS:
  - Limited replicate design across multiple domes; notes on pseudo-replication caution.
  - Temporal alignment between ozone exposure and physiological measurements; some measurements span different weeks.
  - Uniform reporting of AOT40 and dome-specific ozone data facilitates consistent spatial analyses, but caution required when extrapolating beyond solardome settings.

## Limitations and considerations
- Pseudo-replication acknowledged; experimental design emphasizes breadth of treatments over full replication per treatment.
- Climatic variables not uniformly recorded across all domes; only one dome had continuous climate monitoring.
- Results are specific to two clover cultivars and controlled solardome environments, which may limit direct generalization to field conditions.
- Data offer rich, multi-dimensional attributes suitable for GIS-enabled analyses when integrated with supplementary geospatial layers.