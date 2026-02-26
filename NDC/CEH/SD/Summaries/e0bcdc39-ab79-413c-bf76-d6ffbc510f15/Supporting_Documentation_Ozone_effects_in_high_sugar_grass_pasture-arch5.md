# Supporting documentation - Ozone effects in high sugar grass pasture

- Purpose: Document the phytometer experiment assessing ozone effects on ozonated high-sugar grass pasture mesocosms, including experimental setup, measurements, and dataset descriptions to enable discovery and reuse.

## Experimental setup and organisms
- Plant species: Lolium perenne cv. AberMagic (grass) and Trifolium repens cv. Crusader (clover).
- Propagation and potting: AberMagic sown directly into 10 L pots; Crusader clover propagated from seed and transplanted into pots after initial growth; soil compost and seed sources specified.
- Inoculation: Pots inoculated with 400 ml soil slurry (5 kg soil from grassland + water) to introduce soil microbe populations.
- Growth environment: Mesocosms grown for 4 weeks in a glasshouse, then moved to six solardomes for ozone exposure.
- Experimental units: 24 pots per solardome, with even distribution of clover and grass; random assignment of treatments within solardomes.
- Monitoring: Ambient temperature, soil moisture, PAR, humidity monitored in one solardome; plants rotated weekly; regular watering to maintain near field capacity.

## Treatments and ozone exposure
- Exposure system: Six hemispherical solardomes (3 m diameter, 2.1 m high) used to apply ozone treatments.
- Ozone profile: Episodic ozone exposure based on a rural monitoring site (Aston Hill, Wales) with weekly repeating treatment profiles.
- Duration: 16-week exposure period (start 11/06/2013, end 01/10/2013).
- Randomization and replication: Treatments applied randomly across solardomes; ozone treatments are not replicated within a single solardome, but prior work supports statistical validity of this design with 6–8 treatments across similar facilities.
- Environmental controls: One solardome included continuous monitoring of temperature, soil moisture, PAR, and humidity.

## Measurements and assays
- Biomass assessments:
  - Above-ground biomass: every 4 weeks; six pots per solardome randomly sampled; maintenance cuts elsewhere.
  - Root biomass: assessed at 16 weeks; Crusader nodules excised from roots.
  - Drying: shoots, roots, and nodules dried to constant mass for analysis.
  - Injury scoring: injured/senesced leaves scored in clover; expressed as percentage to account for biomass differences.
- Nitrogen fixation activity:
  - Acetylene reduction assay (ARA): conducted every 4 weeks (4, 8, 12, 16 weeks) using a 10% acetylene atmosphere and ethylene measurement by gas chromatography.
- Nutritional and forage quality:
  - Near-infrared reflectance (NIR) on mixed shoot biomass to assess nutritive quality characteristics.
  - Relative feed value (RFV) and consumable food value (CFV) calculated from measured parameters.
- Canopy gas exchange and primary production:
  - Whole-canopy CO2 fluxes measured hourly with a bell chamber and infrared gas analyzer.
  - Metrics: Net primary production (NPP), canopy respiration (Rtot), gross primary production (GPP = NPP − Rtot), dark canopy respiration.
  - Measurements conducted under comparable sunny conditions (weeks 8–16) with at least 12 replicates per treatment.
  - Ozone flux estimation using DO3SE model; parameters tailored per cultivar where data allowed (AberMagic default used for L. perenne due to limited gs data).
  - Accumulated stomatal ozone flux used to relate to physiological responses with POD thresholds (POD 6 for AberMagic; POD 1 for Crusader) and “Pasture POD” for seasonal data.
- Leaf area and growth indices:
  - Leaf area index (LAI) derived from biomass samples.
  - Phenology function treated as fixed (fphen = 1) due to repeated cuts.
- Additional environmental/dataset linkage:
  - AOT40 and climate-related data compiled for ozone exposure context and environmental relationships.
  - Measurements of PAR, leaf temperature, soil moisture, VPD, and related climate variables.

## Data processing and analysis
- Data normalization:
  - Biomass and related variables converted to relative values using POD thresholds to enable cross-treatment comparisons.
  - Injury data arcsine transformed prior to analysis.
- Statistical analyses:
  - Regression of biomass, injury, and N-fixation against accumulated POD values (4, 8, 12, 16 weeks; POD 6 for AberMagic, POD 1 for Crusader).
  - Seasonal regression for shoot biomass; seasonal analysis for forage quality parameters against total stomatal flux (Pasture POD).
  - Canopy gas-exchange data analyzed by analysis of variance (ANOVA) against ozone treatment, with week as a random factor.
  - Post-hoc comparisons: Tukey’s HSD when ANOVA shows significant ozone effects.
- Software: All analyses performed in R (Version 3.1.1).

## Datasets and file structure
- Data files included (CSV format), organized as seven primary data groups:
  - Acetylene reduction assays:
    - acetylene_reduction_assay_4week.csv
    - acetylene_reduction_assay_8week.csv
    - acetylene_reduction_assay_12week.csv
    - acetylene_reduction_assay_16week.csv
    - Columns: pot, size, harvest.level, ozone, time period, vial, time, ethylene area, ng.ethylene.ml, nL.ethylene.ml, nL.ethylene.cm2
  - Shoot biomass:
    - week4shootbiomass.csv
    - week8shootbiomass.csv
    - week12shootbiomass.csv
    - week16shootbiomass.csv
    - Columns include pot, size, harvest.level, dome, mean.ozone, various biomass metrics for grass and clover, and ratios.
  - Root biomass:
    - week4rootbiomass.csv
    - week8rootbiomass.csv
    - week12rootbiomass.csv
    - week16rootbiomass.csv
    - Columns include pot, size, harvest.level, dome, mean.ozone, mass and biomass metrics for Lolium perenne and Trifolium repens, nodules, and related ratios.
  - Injury:
    - week4injury.csv
    - week8injury.csv
    - week12injury.csv
    - week16injury.csv
    - Columns include pot, size, harvest.level, dome, mean.ozone, injured leaves, total leaves, percent injury for clover.
  - Gs and related measurements:
    - allmeasurements.csv
    - Consists of date, time, pot, size, dome, mean.ozone, gs, leaf.temp, soil moisture, PAR, air.temp, VPD
  - AOT40 and climate data:
    - AOT40_and_climate_variables.csv
    - 32 columns including date, time, weekday, week, dome-related >40ppb metrics, PAR, air temp, vpd, PAR>200, etc.
- Overall dataset scope: Phytometer data capturing ozone responses in a high-sugar pasture mesocosm system, including experimental results (acetylene reduction, injury, biomass) and environmental context (AOT40, climate variables).

## Data quality, provenance, and governance notes
- Provenance: Detailed experimental methods and data definitions are provided to enable traceability from treatment to measured outcomes (biomass, injury, N-fixation, gas exchange).
- Metadata richness: File-level and column-level descriptions capture specimen identity (pot, size, dome), treatment (harvest level, ozone), time points, and instrument outputs (gas chromatography, infrared gas analyzer, NIR).
- Interoperability considerations: CSV format with explicit column naming; consistent units across files (e.g., biomass in grams, ozone in ppb, gas concentrations in ng/nL, etc.), facilitating reuse and integration.
- Potential caveats for reuse:
  - Non-replicated ozone treatments within a single solardome; cross-dome replication provides overall design validity but users should account for dome-level effects.
  - Model parameters for ozone flux (DO3SE) used with some default values due to limited cultivar-specific data; consider this when performing flux-related analyses.
  - Season and protocol specifics (2013 study) should be considered when comparing to other experiments or when extending analyses to different years or conditions.
- Target applications for Data Stewards and users:
  - Meta-analyses of ozone effects on forage quantity and quality.
  - Investigations of nitrogen fixation responses under ozone stress.
  - Linking physiological responses (NPP, GPP, canopy fluxes) to environmental drivers (AOT40, PAR, VPD).
  - Integration with other datasets requiring consistent metadata for cross-study comparability.

## Usage and sharing considerations for data stewards
- Ensure dataset is discoverable with clear, persistent metadata and DOI where possible.
- Maintain data provenance notes, including experimental design decisions (randomization, non-replicated ozone treatments within domes) and analysis approaches (POD thresholds, regression frameworks, ANOVA).
- Provide data dictionaries and codebooks for all columns and units; offer example analysis scripts in R to facilitate reuse.
- Consider adding a data release note clarifying limitations and assumptions (e.g., flux parameterization, seasonal scope, and potential dome-level effects) to guide downstream analyses.