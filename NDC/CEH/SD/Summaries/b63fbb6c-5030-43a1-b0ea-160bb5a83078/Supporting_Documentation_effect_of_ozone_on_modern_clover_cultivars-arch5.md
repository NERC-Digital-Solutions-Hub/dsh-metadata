# Supporting documentation - Effect of ozone on modern clover cutlivars

## Overview
- Phytometer-style experiment examining the impact of ozone on two modern clover cultivars: Crusader (Trefolium repens cv. Crusader) and Merviot (T. pratense cv. Merviot), subjected to a range of ozone treatments in solardomes.
- Data collected include injury and senescence, stomatal conductance (gs), above- and below-ground biomass, nodule metrics, shoot/root/nodule masses, and nitrogenase activity (acetylene reduction assay).
- Aimed to enable analysis of ozone effects and to facilitate UK-scale comparisons via AOT40 metrics.

## Experimental setup and data collection
- Seedlings sown in late spring 2012, transplanted to 5 L pots with sterile topsoil; soil inoculated with a soil slurry to introduce microbes.
- Plants placed in eight solardomes (3 m diameter) with 6 pots per cultivar per dome; randomised treatments across domes.
- Ozone treatments designed to reflect future scenarios, with peak concentrations reduced relative to background; ozone delivered via generators and monitored continually.
- Measurements and sampling schedule:
  - Injury and senescence scored after 3 weeks of exposure (injured leaves >25% leaflet area).
  - Stomatal conductance (gs) measured at intervals during the 12-week growth period in natural climate conditions.
  - Soil moisture monitored; plants rotated weekly; watering as needed.
  - Harvest at 12 weeks: shoot, root, and nodule biomass; mid-season shoot harvest for Merviot after 7 weeks.
  - Nodules excised, counted, and weighed; nodules classified into size categories.
  - Below-ground biomass determined from representative soil quarters; extensive root systems limited sampling to select treatments.
  - Nitrogenase activity assessed (Crusader) two weeks prior to assay using acetylene reduction (ARA) with ethylene production quantified over 0, 4, 8, 24 h.
  - Measurements expressed relative to AOT40 (accumulated O3 exposure above 40 ppb during daylight at canopy height).
- Data handling notes:
  - Treatment replication is not explicit; authors acknowledge potential pseudo-replication but justify the approach for evaluating multiple treatments.
  - Climatic variables were monitored in one dome where available; air flow rates matched across domes; treatment randomisation maintained.

## Data files and structure
- Acetylene reduction assay files
  - nitrogenasesept.csv
  - nitrogenaseoct.csv
  - Contain: date, vial, pot, dome, mean.ozone (ppb), peak area (ethylene), time step, ethylene metrics, and calculated ethylene production.
- Stomatal conductance
  - crusadergs.csv
  - merviotgs.csv
  - Contain: species, cultivar, time, date, week, dome, mean ozone, pot, starting size, gs (abaxial conductance) and related identifiers.
- Above-ground biomass
  - crusaderabovegroundweek11.csv
  - merviotabovegroundweek7.csv
  - merviotabovegroundweek11.csv
  - Contain: date, cultivar, dome, mean.ozone, pot, starting size, bag mass, shoot biomass (dry).
- Injury and senescence
  - senescence.csv
  - Contain: date, species, cultivar, dome, pot, starting size, mean ozone, flower number, injury, senescence, total injury, leaf counts, percent injury/senescence, and related injury metrics.
- Nodule size
  - nodule_size.csv
  - Contain: date, species, cultivar, dome, mean.ozone, pot, starting size, nodules size category, and counts.
- AOT40 data
  - aot40.csv
  - Contain: date, day of week, week, time, eight domes, ozone above 40 ppb per dome.
- Below-ground biomass
  - crusaderbelowground.csv
  - merviotbelowground.csv
  - Contain: date, species, cultivar, dome, mean.ozone, AOT40 metrics, pot, starting size, soil quarter masses (corrected and uncorrected), total soil mass, representative quarter metrics, nodules per quarter, root and nodule masses, and derived biomass sums per pot.
- Additional context file
  - Data described as part of a phytometer experiment assessing ozone impacts on clover cultivars, including raw measurements and ozone concentration data.
- Data characteristics:
  - Na = missing values where material not present or undetermined.
  - Units include ppb (ozone), g or kg (biomass), mmol H2O m-2 s-1 (gs), and various derived metrics (e.g., AOT40, all expressed as specified).

## Data processing and analysis
- Analyses conducted to relate ozone exposure to responses:
  - Injury and gs: general linear regression using the 3-week injury data or 12-week AOT40 as predictor.
  - Biomass and ARA: one-way ANOVA with 12-week or 10–11 week AOT40 as the predictor, depending on biomass or assay.
  - Nodule size: analyzed separately for each size category against 12-week AOT40.
  - Data trimmed to exclude extreme PAR values using 25th–75th percentile range for each cultivar.
  - Post hoc Tukey's HSD used to compare means after significant ANOVA results.
- Limitations:
  - Insufficient gs data to model ozone flux–effect relationships.
  - Potential pseudo-replication due to non-explicit treatment replication; authors note the trade-off with multiple treatments, citing prior work.

## Data quality, limitations, and governance considerations
- Data provenance: collected at CEH solardome facility, Bangor, UK, during 2012 with a detailed ozone delivery and monitoring setup.
- Metadata needs for stewardship:
  - Experimental design details (treatment mapping to domes, replication scheme, randomization strategy).
  - Instrumentation and calibration notes for ozone analysers and stomatal conductance devices.
  - Exact unit definitions and any data normalization steps (AOT40 calculations, canopy height definitions, etc.).
  - Data provenance traceability (who collected, who processed, versioning of data files).
- Quality considerations for reuse:
  - The lack of explicit treatment replication requires careful statistical interpretation and may affect generalizability.
  - AOT40-based metrics enable UK-scale comparisons but require careful alignment with other datasets.
  - Missing values are present (Na) in fields; handling strategies should be defined in downstream analyses.

## Provenance and accessibility
- Origin: phytometer experiment on ozone effects in modern clover cultivars Crusader and Merviot; integrated measurements of injury, gs, biomass, nodulation, and nitrogenase activity.
- Temporal scope: growth period from mid-2012 with ozone exposure from July to October; data files reflect measurements across multiple time points and dome treatments.
- Accessibility: data are organized into clearly described CSV files with explicit column names and units, intended for reuse in ozone impact analyses and cross-dataset comparisons.

## Usage guidance for Data Stewards
- Ensure complete metadata capture for future reuse, including treatment-to-dome mapping, replication details, and calibration records.
- Validate units and scaling for AOT40 and ozone concentrations to ensure consistency with other datasets.
- Document handling of missing values and decisions regarding pseudo-replication in any downstream analyses.
- Consider creating a data dictionary that maps each file to its corresponding biological response variable (injury, gs, biomass, nodules, ARA) and the associated predictor (AOT40 or 12-week exposure).
- Provide clear notes on the experimental limitations to guide appropriate interpretation and integration with broader datasets.