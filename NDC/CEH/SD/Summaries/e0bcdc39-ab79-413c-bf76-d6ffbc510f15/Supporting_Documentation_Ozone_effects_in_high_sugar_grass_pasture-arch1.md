# Supporting documentation - Ozone effects in high sugar grass pasture

- Objective: Investigate how ozone exposure affects high-sugar pasture using a mesocosm system, measuring biomass production, injury, nitrogen fixation, and forage quality.

- Plant materials and setup:
  - Grass: Lolium perenne cv AberMagic; seed sown directly into 10 L pots.
  - Clover: Trifolium repens cv Crusader; propagated and grown in identical conditions, then transplanted into pots.
  - Pots: 27.5 cm diameter, 22 cm height, filled with John Innes No. 2 compost.
  - Soil microbial inoculation: 400 ml soil slurry from field grassland mixed with water.
  - Growth: 4 weeks before transfer to solardomes; 24 pots per solardome, with equal grass/clover distribution.

- Experimental environment and ozone exposure:
  - Facility: CEH solardome facility near Bangor, UK (six hemispherical domes, 3 m diameter, 2.1 m high).
  - Treatments: Randomly assigned ozone treatments; one dome monitored for ambient conditions. Treatments not replicated within domes, but design supported by prior studies for statistical validity.
  - Exposure duration: 16 weeks (mid-June to early October 2013).
  - Ozone profile: Episodic, based on rural monitoring (Aston Hill, Wales) with weekly repeating patterns; ozone concentrations approximately recorded as mean in each dome.
  - Environmental monitoring: In one dome, continuous monitoring of ambient temperature, soil moisture, PAR, and relative humidity.
  - Watering: Maintained near field capacity; plants rotated weekly.

- Measurements and assessments:
  - Biomass: Above-ground shoot biomass measured every 4 weeks; pots with six random shoots per dome harvested for biomass, with maintenance cuts on remaining pots.
  - Root and nodule data: At harvest (week 16), root biomass measured for both cultivars; Crusader nodules excised and analyzed.
  - Injury assessment: Leaf injury and senescence scored for clover leaves; expressed as percentage injury relative to total leaves.
  - Nitrogen fixation: Nitrogenase activity assessed every 4 weeks via acetylene reduction assay (ARA) using a sealable bottle in the soil collar; ethylene production measured by GC; ARA performed before 4-week maintenance cuts (weeks 4, 8, 12, 16).
  - Forage quality: Near-infrared reflectance (NIR) used to determine nutritive characteristics; relative feed value (RFV) and consumable food value (CFV) calculated.
  - Canopy gas exchange: Whole-canopy hourly CO2 fluxes measured with a bell chamber and infrared gas analyser; measurements yield Net Primary Production (NPP), total canopy respiration (Rtot), and, with an opaque cover, dark canopy respiration; gross primary production (GPP) derived from NPP and Rtot.
  - Ozone flux modelling: DO3SE model used to estimate stomatal ozone flux; parameterised differently for AberMagic and Crusader where data allowed; accumulated flux calculated at 4, 8, 12, and 16 weeks with POD thresholds (POD 6 for AberMagic; POD 1 for Crusader).
  - Leaf area index: Derived from biomass, with cultivar-specific ranges reported.
  - Data handling: All biomass, injury, and N-fixation data transformed to relative or percentage metrics as appropriate; season-long analyses also performed for shoot biomass.
  - Data analysis: Linear regression of biomass, injury, and N-fixation against accumulated POD values; ANOVA on canopy gas exchange against ozone treatment with week as a random factor; Tukey HSD tests for post-hoc differences; all analyses performed in R (v3.1.1).

- Modelling and data interpretation notes:
  - Phenology function fixed at 1 throughout the season due to frequent cuts.
  - For forage quality parameters, analyses attributed to seasonal data against total stomatal flux to the whole mesocosm (Pasture POD) weighted by cultivar proportions.
  - Injury data arcsine-transformed prior to analysis.

- Datasets and files available:
  - Acetylene reduction assays (4, 8, 12, 16 weeks): acetylene_reduction_assay4week.csv, acetylene_reduction_assay8week.csv, acetylene_reduction_assay12week.csv, acetylene_reduction_assay16week.csv (11 columns each; includes pot, size, harvest level, dome, mean ozone, time, vial, ethylene measurement, and related metrics).
  - Shoot biomass (week 4, 8, 12, 16): week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv (27 columns; includes pot, size, harvest level, dome, mean ozone, and detailed biomass components for grass and clover).
  - Root biomass (week 4, 8, 12, 16): week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv (21 columns; includes root biomass for grass and clover, nodules, and related metrics).
  - Injury data (week 4, 8, 12, 16): week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv (8 columns; includes injury counts and percentages for T. repens).
  - All measurements (Gs file): allmeasurements.csv (12 columns; includes date, time, pot, size, dome, mean.ozone, gs, leaf.temp, soil moisture, PAR, air.temp, VPD).
  - AOT40 and climate data: AOT40_and_climate_variables.csv (32 columns; includes date, time, weekday, week, dome data, >40ppb counts for domes and plots, PAR, temperatures, VPD, and PAR>200 metrics).

- Data context and scope:
  - The datasets concern a phytometer-type experiment examining ozone impacts on ozonated high-sugar grass pasture mesocosms, including both shoot and root biomass, N-fixation activity, injury, forage quality, and canopy gas exchange under varying ozone exposures and environmental conditions.
  - Comprehensive metadata and columns are provided to enable reanalysis, trend detection, and correlation assessments between ozone exposure (POD-based flux) and plant responses across time and cultivars.