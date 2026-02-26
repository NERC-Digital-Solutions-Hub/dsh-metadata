# Individual life history data from a resource degradation and temperature variation life history experiment in the Plodia -Venturia host-parasitoid interaction

## Overview
- Experimental aim: investigate combined effects of daily stochastic temperature fluctuations and host resource degradation on a Plodia interpunctella (host) and Venturia canescens (parasitoid) life-history model.
- System: laboratory populations of Plodia hosts and Venturia wasps (parthenogenetic thelytokous strain); hosts reared on non-degraded diet under constant 28°C prior to treatments.
- Study scope: single-generation life-history assay to characterize individual responses across treatments.
- Duration: life-history assay lasted 74 days, starting on day 5 of the temperature time series.

## Experimental design and treatments
- Factorial design: two temperature treatments × four resource degradation levels.
  - Temperature treatments:
    - CST (constant): mean 26°C
    - VAR (variable): 26°C ± 1.5°C SD, daily random variation; range 22.3–30.2°C; AR(1) = 0.02
  - Resource degradation treatments (diet replacement by methyl cellulose):
    - 0%, 25%, 50%, 75%
- Treatments seeded by daily temperature time series data; each combination tested with both unparasitized and parasitized hosts.
- Life-history assay setup:
  - Unparasitized hosts: 40 individuals per temperature × diet treatment (per treatment), monitored individually.
  - Parasitized hosts: 25 hosts per temperature × diet treatment, parasitized during a 3-day window (days 20–22).

## Datasets and key variables
- Dataset: VariableTemperatureTimeSeries_DQE.csv
  - Variables include: DAY, Date, Week, Temp (daily temperature data)
- Dataset: LHE-LH-Data_DQE_Pi.csv (unparasitized hosts)
  - Key fields: Treatment, Individual, Diet, Temperature, Starting_Date, Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death, Sex, Egg_length, Leg_length, Date_leg_photo_taken, leg_measured, comments, and other daily monitoring data
- Dataset: LHE-LH-Data_DQE_PiVc.csv (parasitized hosts)
  - Key fields: Treatment, Diet, Temperature, Individual, Starting_Date, Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age, Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex, Time_at_parasitism, Adult_emergence_date, Parasitism_outcome, Date_of_death, Date_photo_taken, Leg_length, Leg_measured, Parasitism_observer, comments
- Measurements and proxies:
  - Host metrics: egg viability, hatching status, hatching date, adult emergence date, host death date, sex, egg length, leg length (proxy for body size)
  - Parasitoid metrics (in PiVc data): parasitoid maternal info, larval stage at parasitism, mass at parasitism, parasitoid and host emergence outcomes, leg length for parasitoid body size
- Measurement methods: leg measurements taken from images with Nikon DS-5M camera and NIS-element software; leg measurements recorded as right/left; date of photography logged.

## Quality control and data provenance
- Quality control: data entry checks and rechecking of outliers during initial analysis stage.
- Documentation: explicit definitions of variables, treatment codes, and measurement protocols; references for diet and host-parasitoid context provided.

## References
- Boots, M. 2011. The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C. et al. 2007. Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.
- Harvey, J.A. et al. 1994. Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology, 75, 1420-1428.

## Relevance for environmental monitoring and data use
- Purpose aligned with environmental monitoring: provides standardized, traceable life-history data under controlled environmental stressors (temperature variability and resource degradation).
- Potential uses:
  - Cross-study comparisons of how temperature variability and resource quality affect host and parasitoid life-history traits.
  - Integration with other monitoring datasets to assess broader ecological responses to environmental stressors.
  - Data sharing and transparency: deposit contains detailed metadata and clear variable definitions to enable reuse and reproducibility.
- Key considerations for analysts:
  - Understand the full factorial design and treatment coding to correctly interpret interactions between temperature and diet.
  - Leverage both host-only (Pi) and host–parasitoid (PiVc) datasets to assess direct and indirect effects on life-history traits.
  - Consider data integration opportunities to enrich monitoring datasets with environmental stressor metrics and derived indicators.