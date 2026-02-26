# WildCrickets06A_EarlyLatencyVsSenescence Description of content

## Overview
- Dataset describes singing activity per sample and per individual male crickets.
- Focus is on mating latency and classification of individuals by mating speed relative to the population median (EarlyLatency).
- Variables capture both per-sample measurements and individual identifiers, enabling both cross-sectional and longitudinal analyses.

## Variables
- EarlyLatency: whether mating latency is above or below the population median (high vs low speed in mating).
- Latency: actual latency category (high, H; low, L).
- Year: year when the cricket was alive.
- ID: unique individual identifier.
- Temp: ambient temperature at sampling (in °C).
- Age: age at sampling (in days).
- Sings: whether the cricket was singing at the time of sampling (1 = yes, 0 = no).

## Analyses and questions (analyst perspective)
- Examine associations between EarlyLatency and Sings to identify if mating speed relates to vocal activity.
- Model Sings as a function of Latency, EarlyLatency, Age, Temp, and Year; consider mixed-effects models with ID as a random effect to account for repeated measures.
- Investigate age-related patterns (senescence) in latency categories and singing behavior.
- Assess temperature effects on latency classification and singing likelihood.
- Explore cohort or year effects to detect temporal trends across generations.

## Data considerations
- Data includes both per-sample and per-individual observations, enabling within- and between-individual analyses.
- Variables are mostly categorical (EarlyLatency, Latency) and binary (Sings), with continuous covariates Age, Temp, and Year-related factors.