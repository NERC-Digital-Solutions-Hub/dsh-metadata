# Influence of jasmonic acid on the effect of ozone on pasture

- Objective: Examine interactive effects of ozone and methyl jasmonate (MeJa) on white clover (Trifolium repens cv. Crusader) using a phytometer approach, with standardized data collection to support environmental health assessments over time.

- Experimental design
  - Plant material and inoculation: Seedlings grown, transplanted into 7.5 L pots (three seedlings per pot), inoculated with a soil slurry to introduce soil microbes.
  - Treatments: 
    - Uncut controls
    - Cut+ (single cut to 4 cm height immediately before ozone exposure)
    - MeJa+ (uncut with weekly application of 500 µM MeJa solution; control sprays with 0.1% ethanol to match solvent effects)
  - Growth and environment: Plants moved to six solardomes (3 m diameter, 2.1 m high) with five replicate pots per treatment; random ozone profiles applied; one dome equipped with automatic weather monitoring (temperature, soil moisture, PAR, RH) and soil moisture probes.
  - Ozone exposure: 4 weeks (May 28 to June 24, 2014); ozone profiles categorized as low or high background; standard solardome facilities used with established validity for multiple treatments.
  - Sampling and rotation: Plants rotated weekly; watered twice weekly (more as needed); leaves sampled in weeks 2–4 for injury and senescence.

- Measurements and outcomes
  - Injury and senescence: Leaves scored as injured or senesced if >25% of leaf area affected; results expressed as injury/senescence percentages per pot.
  - Biomass and plant metrics: Harvest after 4 weeks; shoot and root biomass measured (including bag corrections); root nodules collected, dried, weighed; LAI calculated from dried forage; root-to-shoot ratio computed.
  - Data handling: Ozone exposure grouped into low and high background; injury and senescence data arcsine-transformed for ANOVA; key correlations explored (e.g., root nodule biomass vs total biomass and injury parameters).
  - Analysis: ANOVA with factors ozone background and treatment; posthoc Tukey tests; Pearson correlations; all analyses in R (v3.1.2).

- Data files and content
  - "Influence of jasmonic acid on the effect of ozone on pasture biomass1worksheet.csv" (23 columns; includes pot ID, treatment code, MeJa presence, cutting status, dome, mean ozone, ozone category, various biomass measures, nodules, total biomass, and mass per nodule).
  - Injury assessments: "injury_first_assessment.csv", "injury_second_assessment.csv", "injury_third_assessment.csv" (each 11 columns; includes pot, treatment, MeJa, cutting, dome, mean ozone, total injury, total senescence, total leaves, percent injured, percent senesced).

- Key considerations for data use and interpretation
  - The design uses a controlled, repeatable environment (solardomes) with standardized treatments and measurements to monitor environmental health indicators over time.
  - While individual ozone treatments were not replicated within a dome, prior studies support the statistical validity of such solardome experiments with multiple ozone profiles.
  - The dataset enables assessment of how external chemical signaling (MeJa) interacts with ozone stress on pasture species, with comprehensive biomass, nutrient-related (nodules), and injury metrics.
  - Emphasizes data quality through controlled spraying procedures, solvent controls, systematic sampling, and detailed data documentation to facilitate reuse and integration with other environmental datasets.