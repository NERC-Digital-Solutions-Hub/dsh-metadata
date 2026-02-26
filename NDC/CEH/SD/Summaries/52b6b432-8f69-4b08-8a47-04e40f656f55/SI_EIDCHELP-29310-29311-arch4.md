# Supporting Information for data deposit EIDCHELP-29311

## Overview
- Dataset documents an experiment on the combined effects of daily stochastic temperature fluctuations and resource degradation in a host-parasitoid system: Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Objective: characterize individual life-history responses over a single generation using hosts from laboratory stocks and a parthenogenetic parasitoid strain.
- Experimental context: conducted under controlled lab conditions with constant 28°C pre-conditioning, then exposed to designed temperature and diet treatments.

## Experimental design
- Single-generation life-history assay.
- Full factorial design combining two temperature treatments (constant CST and variable VAR) with four levels of host resource degradation (0, 25, 50, 75% replaced by methyl cellulose).
- Temperature treatments: CST maintains mean temperature 26°C; VAR fluctuates daily between 22.3°C and 30.2°C (26°C ± 1.5°C SD; AR(1) = 0.02).
- Resource degradation: diet modified by replacing portions of wheat germ with methyl cellulose (indigestible bulking agent).
- Life-history assay duration: 74 days, starting on day 5 of the temperature time series.
- Sample sizes per treatment: 40 unparasitized host larvae and 25 parasitized host larvae.

## Treatments
- Temperature: constant (Cst) vs. variable (Var).
- Resource degradation: 0, 25, 50, 75% methyl cellulose in diet.
- Parasitism status: unparasitized hosts (Pi) and parasitized hosts (PiVc) included in design.

## Life history assays
- Unparasitized hosts: 40 individuals per temperature-resource combination (in two plates: 25 on plate 1, 15 on plate 2); monitored daily for life-history traits.
- Parasitized hosts: 25 individuals per treatment, parasitism performed over three days (ages 20–22 days) with 8 groups of 100 eggs per treatment; post-parasitism, hosts are monitored daily for life-history outcomes.

## Datasets and key variables
- VariableTemperatureTimeSeries_DQE.csv:
  - DAY, Date, Week, Temp (daily temperature time series)
- LHE-LH-Data_DQE_Pi.csv (unparasitized hosts):
  - Treatment (Species, Temperature, Diet), Individual, Individual code, Diet, Temperature, Starting_Date
  - Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death
  - Sex, Egg_length, Leg_length, Date_leg_photo_taken, leg_measured, comments
- LHE-LH-Data_DQE_PiVc.csv (parasitized hosts):
  - Treatment, Diet, Temperature, Individual, Individual code, Starting_Date
  - Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age
  - Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex
  - Time_at_parasitism, Adult_emergence_date
  - Parasitism_outcome, Date_of_death
  - Date_photo_taken, Leg_length, Leg_measured, Parasitism_observer, comments
- Common notes across datasets:
  - Leg measurements taken from photos using specified equipment/software; leg_measured indicates right or left.
  - All data include metadata that facilitates linking host and parasitoid records and date-based life-history events.
  - Quality control: data entered with error checks; outliers rechecked during initial analysis.

## Quality control
- Systematic checks for data entry errors.
- Outliers re-evaluated in the initial data-analysis stage to ensure data integrity.

## References
- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.
- Harvey, J.A., Harvey, I.F. & Thompson, D.J. (1994) Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology, 75, 1420-1428.