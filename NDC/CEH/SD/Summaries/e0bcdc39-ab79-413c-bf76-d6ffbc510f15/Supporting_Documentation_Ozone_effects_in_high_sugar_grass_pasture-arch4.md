# Supporting documentation - Ozone effects in high sugar grass pasture

## Overview
- A phytometer experiment to assess how ozone exposure affects a high-sugar grass pasture, focusing on Lolium perenne cv. AberMagic (grass) and Trifolium repens cv. Crusader (clover).
- Conducted in 2013 at the CEH solardome facility near Bangor, North Wales, using six solardomes with randomized ozone treatments.
- Experimental setup: 24 pots per solardome, equal distribution of clover and grass, inoculated soil microbiome, and staged growth before ozone exposure.
- Ozone exposure followed a weekly repeating episodic profile; measurements spanned 16 weeks (mid-June to early October 2013), including biomass, root and nodules, injury, nitrogenase activity, and canopy gas exchange.

## Experimental Design and Scope
- Plant material: AberMagic grass and Crusader clover, grown in compost-filled pots with a soil microbe inoculum.
- Environment: Solardomes provided controlled ozone exposure, ambient conditions (temperature, moisture, PAR, humidity) monitored within a dome.
- Treatments: Ozone exposures varied by dome with random assignment; a mixture of ambient and elevated ozone levels used to simulate field-like conditions.
- Measurements were conducted at 4-week intervals:
  - Biomass: shoot biomass collected; root biomass and nodules for Crusader; injury assessments for clover.
  - Nitrogenase activity: assessed via acetylene reduction assay (ARA) at 4, 8, 12, and 16 weeks.
  - Forage quality: near-infrared reflectance (NIR) to determine nutritive characteristics; relative forage value (RFV) and consumable food value (CFV) calculated.
  - Canopy gas exchange: whole-canopy CO2 flux measurements to derive net primary production (NPP), gross primary production (GPP), canopy respiration (Rtot), and total dark canopy respiration; fluxes expressed as g C m-2 h-1.
  - Stomatal ozone flux: applied DO3SE model parameterisations (different per cultivar) to estimate accumulated stomatal ozone flux; POD thresholds used for AberMagic (POD6) and Crusader (POD1).
  - Morphometrics: leaf area index (LAI) derived from biomass; injury scoring on clover leaves; harvest-specific adjustments to account for biomass differences.
- Analysis approach: linear regression of biomass, injury, and N-fixation metrics against accumulated POD values; ANOVA for canopy gas exchange with treatment as fixed effect and week as random factor; Tukey HSD for post-hoc differences. All analyses performed in R (v3.1.1).

## Data Collected and Measurements
- Acetylene reduction assays (nitrogenase activity) conducted every 4 weeks (4, 8, 12, 16 weeks) with 15 ml gas samples analyzed for ethylene production.
- Biomass data:
  - Shoot biomass measured at 4, 8, 12, and 16 weeks (combined AberMagic and Crusader for some calculations).
  - Root biomass and nodules measured for Crusader; root nodulation data collected for nitrogen fixation assessments.
  - Injury metrics: percentage injury for Crusader leaves; injury scoring adapted to AberMagic where applicable.
- Gas exchange and productivity:
  - Whole-canopy measurements to derive NPP, GPP, Rtot, and dark canopy respiration; canopy fluxes scaled to mass basis.
  - DO3SE model-based ozone flux estimates used to contextualize ozone exposure.
- Forage quality and composition:
  - NIR-based nutritive parameters; RFV and CFV calculations.
  - Proportions of clover vs. grass in canopy; clover to grass ratios and related metrics.
- Additional environmental data:
  - Portable measurements: mean ozone concentration per dome, PAR, leaf temperature, soil moisture, air temperature, and VPD.
  - All measurements linked to pot, dome, harvest level, and ozone treatment.
- Datasets included:
  - acetylene_reduction_assay_4week.csv, acetylene_reduction_assay_8week.csv, acetylene_reduction_assay_12week.csv, acetylene_reduction_assay_16week.csv
  - week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv
  - week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv
  - week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv
  - Gs file: allmeasurements.csv
  - AOT40 and climate data: AOT40_and_climate_variables.csv

## Data Files and Content
- acetylene_reduction_assay_4week.csv, acetylene_reduction_assay_8week.csv, acetylene_reduction_assay_12week.csv, acetylene_reduction_assay_16week.csv
  - 11 columns: pot, size, harvest.level, ozone, time period, vial, time, ethylene area, ng.ethylene.ml, nL.ethylene.ml, nL.ethylene.cm2
- Shoot biomass files: week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv
  - 27 columns including pot, size, harvest.level, dome, mean.ozone, and multiple biomass components (grass/clover, bag vs. plant, total, ratios)
- Root biomass files: week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv
  - 21 columns including pot, size, harvest.level, dome, mean.ozone, grass and clover root masses, nodules-related metrics, total biomass, and related ratios
- Injury files: week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv
  - 8 columns: pot, size, harvest.level, dome, mean.ozone, injured, total, percent.injury
- Gs file: allmeasurements.csv
  - 12 columns: date, time, pot, size, dome, mean.ozone, gs (stomatal conductance), leaf.temp, soilm, PAR, air.temp, VPD
- AOT40 and climate data: AOT40_and_climate_variables.csv
  - 32 columns: date, time, weekday, week, Dome numbers (1-8), >40ppb values for domes and associated ozone-related plots, PAR, air temp, vpd, etc. Data includes ozone exposure above 40 ppb for several domes and calibration domes; PAR and climate variables captured for context.

## Data Processing, Models, and Analysis Methods
- Ozone flux modeling:
  - DO3SE model used to estimate stomatal ozone flux (accumulated flux) per cultivar with POD thresholds (POD6 for AberMagic; POD1 for Crusader).
  - Accumulated flux calculated for upper-leaf ozone exposure; thresholds chosen to align with literature and intercept-based criteria.
- Data normalization and transformations:
  - Relative biomass and injury values used to account for biomass differences among treatments.
  - Injury data arcsine-transformed prior to analysis.
  - Seasonal analyses for certain biomass variables.
- Statistical analyses:
  - Linear regression of biomass, injury, and N-fixation against POD values (4, 8, 12, or 16 weeks, POD6 for AberMagic and POD1 for Crusader).
  - Seasonal regression for shoot biomass.
  - ANOVA for canopy gas exchange across ozone treatments; random factor included for week.
  - Post-hoc Tukey tests for treatment differences where ANOVA indicated significant effects.
- Software:
  - All analyses performed in R (Version 3.1.1).

## Data Quality, Limitations, and Considerations
- Replication: Ozone treatments within solardomes were not replicated in the experimental design; however, prior studies using the solardome facility support the statistical validity of this approach for multiple treatments.
- Data integration: The dataset provides comprehensive environmental context (AOT40 and climate variables) to enable robust cross-dataset analyses and reproducibility.
- Metadata detail: File naming and column descriptions are provided, with explicit variables for biomass, nitrogen fixation, injury, canopy gas exchange, and environmental conditions to support traceability and reuse.
- Scope: Focused on ozone effects in a high-sugar pasture system, with specific cultivar pairings and controlled mesocosm conditions, which may influence generalizability to field-scale conditions.

## Metadata, Access, and Reuse
- The collection comprises multiple CSV files with clearly labeled variables, enabling data discoverability and modular integration into broader data systems.
- Analyses were conducted in R, facilitating reproducible workflows and potential re-analysis or meta-analysis across similar ozone exposure studies.
- The dataset supports exploring ozone impacts on forage yield and quality, nitrogen fixation via root nodulation, and whole-canopy gas exchange under controlled environmental contexts, with detailed measurements at multiple time points.