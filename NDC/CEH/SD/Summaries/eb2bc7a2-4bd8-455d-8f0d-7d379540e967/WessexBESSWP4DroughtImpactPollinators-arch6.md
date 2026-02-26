# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation.

## Overview
- Experimental study examining how plant functional diversity and drought affect floral resources and pollinator visitation.
- Data collected include floral resources (flower numbers, diversity, nectar presence, nectar quantity and quality) and pollinator visits to plots.
- Fieldwork conducted in Wiltshire, UK, on sown calcareous grassland communities as part of the Winklebury Hill experiments (Wessex BESS WP2).
- Data linked across multiple datasets to enable integrated analyses of plant traits, nectar rewards, and pollinator activity.

## Datasets and files
- NERCPropNectar.csv: nectar production metrics per raceme and treatment.
- NERCNectar.csv: nectar volume and sugar concentration per flower, including handling of missing concentrations.
- NERCFloralSurveys.csv: floral resource surveys by plot, including floral unit counts and pollinator survey metadata.
- NERCPollinatorSurveys.csv: pollinator visitation data by plot and survey, with per-species visit counts where available.
- Linking fields across datasets: PlotID, RacemeID, SubplotID, and SurveyID allow data from the four files to be joined for integrated analyses.

## Field experiment design
- Location: Wiltshire, UK (calcareous grassland on ex-arable soil).
- Plant communities: four communities representing different functional trait combinations; within-plot arrangements combined to create seven distinct functional group mixtures (FG1, FG2, FG3, and their combinations).
- Plot layout: 8 m x 8 m plots with 2 m gaps; replicated across six blocks to control for spatial effects.
- Treatments:
  - Drought (D): six-week rainfall exclusion using shelters, simulating an extreme drought (one in 100-year event).
  - Control (C): ambient rainfall.
  - Roofed control (R): transparent roof with small holes to control for roof effects (temperature/light).
- Timing:
  - Droughts implemented in 2015 and 2016 during late spring/early summer, with shelters in place for six weeks.
  - Soil moisture measured at the end of drought periods to confirm treatment effects.

## Measurements and variables
- Floral resources:
  - Number of flowers and flower diversity per subplot.
  - Proportion of flowers with nectar and nectar quantity/quality.
  - Nectar volume (μl) and sugar concentration (mg/μl) measured on selected racemes and flowers.
  - Calculation of nectar sugar produced per flower over 24 hours.
- Pollinator visitation:
  - 1 m² floral quadrats per subplot for surveys.
  - Pollinator observations: 10-minute sessions per quadrat; recorded visitor identity (to morphotype where possible), plant species visited, and number of floral units visited.
  - Two survey rounds per subplot on different days; weather conditions noted per Pollard & Yates (1993) guidelines.
- Data quality: field protocols followed; data entered in MS Access; identified data gaps and anomalies documented in metadata.

## Data structure and linking
- Each dataset contains IDs that enable linking across files:
  - PlotID: plot-level identifier.
  - SubplotID: treatment subplot within a plot.
  - RacemeID: individual raceme unit for nectar measurements.
  - SurveyID: specific pollinator or floral survey instance.
- Metadata schemas define units and categories (e.g., drought treatment codes D, C, R; FG groups; plant species codes).
- Fields and descriptions align with published methods and previous Fry et al. datasets for cross-study integration.

## Data quality, ethics, and availability
- Data quality assurance:
  - Standardized field protocols; data checked for anomalies; missing data explicitly noted in metadata.
  - Some missing data occurrences:
    - Concentration_Absolute missing for 20% of nectar concentration values due to very small nectar volumes.
    - One subplot in round 1 had observer-related data gaps; all other surveys conducted but may contain zero visits.
- Ethics: study approved by University of Exeter ethics committee (application 2016/1429).
- Access and provenance:
  - Data are part of NERC Environmental Information Data Centre and linked to Fry et al. 2017 and 2018 datasets.
  - Data described with explicit linking fields to facilitate re-use and integration with related ecological datasets.

## Winklebury Hill experiment (context)
- Aim: create diverse plant communities on bare chalk and assess impacts on carbon/nutrient cycling and ecosystem health across functional groups.
- Functional groups (FG) designed to capture different root architectures and leaf traits, predicting variation in soil carbon/nitrogen dynamics and drought responses.
- Experimental grid: large-scale planting in 7 across by 6 down arrangement, replicated across six blocks; included full factorial combinations of FG1, FG2, and FG3.
- Timeline: field setup 2013–2016; drought shelters introduced from 2015 onward to study rainfall exclusion effects on ecosystem processes.

## Data use and practical notes
- Data can support analyses linking plant trait diversity and drought with nectar resources and pollinator visitation patterns.
- Linking to prior work enables broader analyses of ecosystem function, pollination biology, and community-level responses to drought.
- Users should account for missing values in nectar concentration, potential observer gaps in pollinator surveys, and context-specific metadata when combining datasets.

## References (data context)
- Baldock et al. 2015; Corbet 2003; Fry et al. 2017; Fry et al. 2018; Pollard & Yates 1993; Prŷs-Jones & Corbet 1991; Rodwell 1992; Yee 2010.