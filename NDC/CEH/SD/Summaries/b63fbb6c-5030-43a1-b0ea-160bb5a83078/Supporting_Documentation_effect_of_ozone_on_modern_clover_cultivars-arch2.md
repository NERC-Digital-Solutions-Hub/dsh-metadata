# Supporting documentation - Effect of ozone on modern clover cutlivars

## Purpose and scope
- Investigates the impact of ozone on two modern clover cultivars ( Crusader and Merviot ) under controlled ozone treatments.
- Data collected includes injury, physiological responses, biomass, nodulation, and nitrogenase activity to support understanding of ozone effects on clover in a UK context.

## Experimental design and setup
- Species and cultivars: Trifolium repens cv. Crusader (medium-leaved) and T. pratense cv. Merviot (used for cutting finishing stock).
- Propagation: seeds sown in John Innes No. 2 compost, grown in a glass-house, transplanted to 5 L pots with sterile topsoil, inoculated with a soil slurry to introduce a microbial population.
- Environments: 7 solardomes (hemispherical glasshouses) at CEH solardome facility; randomised ozone treatments with 6 pots per cultivar per dome.
- Ozone treatments: based on episodic profile from a rural monitoring site (Aston Hill, Wales); peak concentrations capped relative to background; designed to reflect future ozone scenarios.
- Experimental duration: 3-month exposure from July 11, 2012 to October 3, 2012.
- Monitoring and maintenance: ozone delivered via generators, concentration measured every 30 minutes; temperature, PAR, VPD monitored in at least one dome; weekly plant rotations; soil moisture maintained near field capacity; measurements performed under ozone present.

## Measurements and methods
- Injury and senescence: scored after 3 weeks; injury defined as >25% leaflet area damaged; expressed as percent of leaves affected.
- Stomatal conductance (gs): measured on abaxial leaf surface with a porometer at 10:00–16:00 h across treatments and times.
- Biomass: shoot, root, and nodule biomass harvested after 12 weeks; additional mid-season shoot biomass measurements for Merviot (week 7); below-ground biomass measured from representative soil quarters.
- Nodulation: nodules excised, counted, weighed; categorized by size (<0.1–0.7 mm; 0.7–1.5 mm).
- Nitrogenase activity: acetylene reduction assay performed on Crusader in treatments 1 and 7; ethylene production measured via GC with sampling at 0, 4, 8, and 24 hours.
- Soil and tissue metrics: drought and soil moisture monitored; mass of soil per pot, root-to-shoot ratios, and total biomass calculated with specified formulas; AOT40 used as the exposure metric (ppm·h) based on daylight hours and canopy height measurements.

## Data collection, processing, and analysis
- AOT40 and related biomass metrics: calculated to allow UK-scale comparison and literature consistency.
- Statistical approaches:
  - Injury and stomatal conductance: analyzed with general linear regression using the corresponding week’s AOT40 as predictor.
  - Biomass and related outputs: analyzed by one-way ANOVA with AOT40 values as factors (12-week for some measures; 10–11-week values for others).
  - Nodule size data: analyzed separately per size category against 12-week AOT40.
  - Outlier handling: gs data filtered using 25th–75th percentile PAR ranges to reduce PAR-related outliers.
  - Post hoc: Tukey’s HSD for pairwise comparisons when ANOVA showed ozone effects.
- Replication caveat: noted potential pseudo-replication due to limited true treatment replication; airflow and climatic conditions were controlled to mitigate differences.

## Datasets and data files
- Acetylene reduction assay files: nitrogenaseepst.csv, nitrogenaseoct.csv (13 columns each; includes sampling date, dome, mean ozone, ethylene metrics, etc.).
- Stomatal conductance: crusadergs.csv, merviotgs.csv (10 columns; species, cultivar, time, ozone, etc.).
- Above-ground biomass: crusaderabovegroundweek11.csv, merviotabovegroundweek7.csv, merviotabovegroundweek11.csv (9 columns; date, cultivar, dome, ozone, biomass data).
- Injury and senescence: senescence.csv (15 columns; injury, senescence, percent injury, etc.).
- Nodule size: nodule_size.csv (10 columns; nodule size categories and counts).
- AOT40 data: aot40.csv (20 columns; dome-specific ozone and >40 ppb indicators).
- Below-ground biomass: crusaderbelowground.csv, merviotbelowground.csv (soil quarter masses, AOT40, root and soil measurements, nodules, etc.).
- Data scope: pertains to a phytometer-type experiment examining ozone impacts on clover cultivars, including ozone concentrations, injury, photosynthesis-related metrics, biomass, root/nodule data, and nitrogenase activity.

## Data quality and usage notes
- “FALSE” in AOT40 table indicates ozone concentration < 40 ppb for a given dome.
- Data are structured to support cross-study UK-scale comparisons and ozone-health assessments in pasture systems.
- Datasets offer standardized formats (CSV) and clearly defined variable names to facilitate re-use in monitoring and policy-performance analyses.