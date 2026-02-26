# Supporting documentation - Ozone effects in high sugar grass pasture

- A controlled mesocosm study to quantify the effects of ozone on a high-sugar grass pasture comprising Lolium perenne (AberMagic) and Trifolium repens (Crusader), exposed in six solardomes with a repeating episodic ozone profile based on rural monitoring data.

## Experimental design and setting

- Plant setup:
  - Lolium perenne cv. AberMagic sown directly in pots; density 0.28 g seed per pot.
  - Trifolium repens cv. Crusader grown similarly and established with 3 clover plants per pot.
  - Soil inoculated with a slurry from agricultural grassland to introduce microbial populations.
- Environment and ozone exposure:
  - 24 pots per solardome, with 6 solardomes total.
  - Ozone exposure uses an episodic profile with randomised treatments across solardomes.
  - One solardome included continuous ambient monitoring of temperature, soil moisture, PAR, and humidity.
  - Exposure duration: 16 weeks (mid-June to early October 2013).
- Sampling and maintenance:
  - Plants rotated weekly; soil moisture maintained near field capacity; regular watering.
  - 4-weekly assessments of above-ground biomass; maintenance cut backs to 4 cm for remaining plants.
  - Root biomass measured after 16 weeks; Crusader nodules excised for analysis.
  - Injury scoring on leaves for both species (injury or senescence >25% surface considered injured/senesced).
  - Nitrogenase activity measured bi-monthly via acetylene reduction assay (ARA).

## Measurements and analyses

- Biophysical and biochemical outputs:
  - Above-ground biomass by species; shoots and roots dried and weighed.
  - Nodulation metrics for Crusader (nodule mass and numbers).
  - Injury metrics expressed as a percentage (adjusted for biomass differences).
  - Nitrogen fixation activity tracked via ARA at 4-week intervals.
  - Forage quality: near-infrared reflectance (NIR); relative feed value (RFV) and consumable feed value (CFV) calculated.
- Canopy gas exchange:
  - Whole-canopy CO2 fluxes measured with a bell chamber and IR gas analyzer.
  - Calculations include net primary production (NPP), canopy respiration (Rtot), and gross primary production (GPP = NPP - Rtot).
  - Measurements performed across 8–16 weeks on sunny days; data expressed as g C m^-2 h^-1.
- Ozone flux and exposure metrics:
  - Ozone flux estimated using the DO3SE model (Deposition of Ozone for stomatal exchange) with parameters:
    - Crusader parameterised from observed environmental variables (n=607 data points for gs).
    - AberMagic parameterised with a default (no gs data).
  - Accumulated stomatal ozone flux values (POD 6 for AberMagic; POD 1 for Crusader) used to relate ozone exposure to biological responses.
  - Leaf area index derived from biomass, phenology function assumed constant (1) due to frequent defoliation.
- Data analysis:
  - Biomass, injury, and nodulation variables regressed against accumulated POD values.
  - Shoot biomass also analysed seasonally.
  - For forage quality, regression against Pasture POD (whole-mesocosm stomatal flux) weighted by cultivar proportions.
  - Canopy gas exchange data analysed by ANOVA against ozone treatment; week included as random factor.
  - Post-hoc comparisons using Tukey’s HSD where significant ozone effects detected.
  - Analyses conducted in R (Version 3.1.1).

## Data products and structure

- Dataset comprises seven data file groups:
  - Acetylene reduction assays (4-week, 8-week, 12-week, 16-week)
  - Shoot biomass (week4, week8, week12, week16)
  - Root biomass (week4, week8, week12, week16)
  - Injury (week4, week8, week12, week16)
  - All measurements (Gs file)
  - AOT40 and climate variables
- File-level descriptions:
  - acetylene_reduction_assay_4week.csv, acetylene_reduction_assay8week.csv, acetylene_reduction_assay12week.csv, acetylene_reduction_assay16week.csv
    - 11 columns including pot, size, harvest level, ozone, time period, vial, time, ethylene metrics.
  - week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv
    - 27 columns including pot, size, harvest level, dome, mean.ozone, various biomass components (grass, clover), ratios (e.g., clover:grass), total biomass.
  - week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv
    - 21 columns including pot, size, harvest level, dome, mean.ozone, gram masses for grass/clover, nodules, total biomass, nodules per gram, etc.
  - week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv
    - 8 columns including pot, size, harvest level, dome, mean.ozone, injured T.repens leaves, total leaves, percent injury.
  - allmeasurements.csv
    - 12 columns covering date, time, pot, size, dome, mean.ozone, gs, leaf.temp, soil moisture, PAR, air temp, VPD.
  - AOT40_and_climate_variables.csv
    - 32 columns including date, time, weekday, week, dome-specific >40ppb values, PAR, air temp, VPD, etc.
- Ozone exposure labeling:
  - Datasets include a boolean-like indicator Cells labelled 'FALSE' indicating ozone concentrations <40 ppb for respective solardomes or PAR < 200 for a given measurement.

## Data handling, accessibility, and purpose

- Data are designed to support standardized assessment of ozone effects on mixed pasture mesocosms, enabling cross-comparison with standardized environmental monitoring outputs (e.g., AOT40, PAR, VPD).
- Outputs intended for integration with environmental monitoring portals and data repositories; datasets are organized for straightforward QA, cleaning, and transformation to outputs such as biomass, nutrient status, injury, nitrogen fixation, and canopy gas exchange metrics.
- The study provides rich linked datasets combining biological responses (biomass, nodulation, injury, ARA) with environmental drivers (ozone flux, PAR, temperature, soil moisture, VPD), suitable for data-driven assessments of ozone-health/policy implications in grassland systems.

## Relevance to the Analysts Monitoring the Environment

- Demonstrates a standardized workflow to verify, clean, and transform multi-omics and ecological data into comparable environmental health indicators.
- Produces clear outputs (biomass, injury, N-fixation, forage quality, canopy gas exchange) aligned with policy-relevant environmental performance metrics under ozone exposure.
- Includes detailed metadata on experimental conditions and environmental drivers (AOT40, climate variables) to support reproducibility and cross-study synthesis.
- The dataset design supports increasing the value of data through combination with other datasets (e.g., broader ozone datasets, climate data) and enables access to underlying data for secondary analysis and policy evaluation.