# Supporting Information for data deposit EIDCHELP-29311

## Overview
- Investigates combined effects of daily stochastic temperature fluctuations and host resource degradation on a Plodia interpunctella (host) and Venturia canescens (parasitoid) interaction.
- Life history assay conducted over a single generation to characterize individual responses.
- Organisms sourced from laboratory stocks; hosts maintained at constant 28°C prior to experiments; experimental phase uses mean 26°C with two temperature treatments (constant and variable) and four levels of resource degradation.
- Aims to enable analysis of how environmental variation and diet quality affect life-history traits and parasitism outcomes.

## Experimental Setup
- Design: full factorial with two temperature treatments (Constant [Cst] and Variable [Var]) and four resource degradation levels (0, 25, 50, 75% methyl cellulose replacing wheat germ).
- Temperature treatments:
  - Constant (Cst): mean 26°C with no fluctuation.
  - Variable (Var): mean 26°C with daily fluctuations between ~22.3°C and 30.2°C (SD ~1.5°C; AR(1) = 0.02).
- Resource degradation: methyl cellulose used as indigestible bulking agent to create dietary stress.
- Duration: life history assay started on day 5 of the temperature time series and lasted 74 days.
- Sample sizes per temperature-resource treatment:
  - Unparasitized hosts: 40 individuals per treatment.
  - Parasitized hosts: 25 individuals per treatment (groups parasitized across days to achieve 8 treatment combinations).
- Parasitism: Venturia canescens parasitized hosts in groups; parasitism occurred over three days (ages 20–22 days) with 8–9 larvae per treatment parasitized per day.

## Datasets and Key Variables
- VariableTemperatureTimeSeries_DQE.csv
  - DAY, Date, Week, Temp
- LHE-LH-Data_DQE_Pi.csv (unparasitized hosts)
  - Treatment (species, temperature, diet)
  - Individual, Individual code, Diet, Temperature, Starting_Date
  - Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death
  - Sex, Egg_length, Leg_length, Date_leg_photo_taken, leg_measured, comments
- LHE-LH-Data_DQE_PiVc.csv (parasitized hosts)
  - Treatment, Diet, Temperature, Individual, Individual code, Starting_Date
  - Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age
  - Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex
  - Time_at_parasitism, Adult_emergence_date
  - Parasitism_outcome, Date_of_death
  - Date_photo_taken, Leg_length, Leg_measured, Parasitism_observer
  - comments
- Notes:
  - Leg measurements (mm) for hosts and parasitoids used as proxies for body size; measurements taken from Nikon high-precision imaging equipment with standardized software.
  - Data include both daily life-history outcomes and parasitism-specific metrics.

## Data Collection and Measurements
- Life-history traits recorded for unparasitized hosts include viability, hatching success, development timing, adult emergence, survival, sex, and body size proxies (egg length, leg length with photo date).
- For parasitized hosts, additional metrics include parasitoid-related data such as larval stage and mass at parasitism, parasitoid sex when determined, parasitism timing, emergence data for host or parasitoid, and parasitism outcome categories.
- Imaging and measurement details:
  - Leg measurements captured via Nikon DS-5M camera and NIS-element software; leg_side recorded (R/L) with date recorded for measurement.
- Quality control: data entry checks performed and outliers rechecked during initial analysis.

## Data Quality, Provenance, and References
- Quality control: all data checked for entry errors; outliers rechecked in initial analyses.
- References cited for experimental design context:
  - Boots, M. 2011. The evolution of resistance to a parasite is determined by resources.
  - Cameron, T.C. et al. 2007. Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions.
  - Harvey, J.A. et al. 1994. Flexible larval growth allows use of a range of host sizes by a parasitoid wasp.