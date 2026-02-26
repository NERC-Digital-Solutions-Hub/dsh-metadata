# WildCrickets02_Behaviour

## Overview
- A dataset of behavioral data for each adult cricket in the population, captured by year.
- Each cricket is identified by a two-character Tag (read from video recordings) and sex (Male or Female).

## Data fields and meanings
- Year: The year the cricket was alive (observation year).
- Tag: Two-character identifier from video tagging.
- Sex: M or F.
- Burrows: Number of different burrows where the cricket was observed during its life.
- Arrivals: Number of times the cricket was observed arriving at a burrow.
- Fights: Number of observed fights with other crickets.
- FightsWon: Number of fights won.
- Mates: Number of different mating partners observed.
- Matings: Total number of matings observed.
- CallEffort: Proportion of observation hours during which the cricket was singing.
- CallSamples: Total hours of observation used to estimate CallEffort.

## GIS relevance and potential visualisations
- Link to spatial data by joining to burrow locations or observation sites to map activity.
- Visualise:
  - Distribution of individuals by sex across space and over time.
  - Burrow usage and site visitation patterns (burrow-level maps).
  - Movement proxies through Arrivals and Burrows metrics.
  - Social/interactions mapping via Mates, Matings, Fights (where location data exists).
  - Acoustic activity intensity using CallEffort across locations or habitats.
- Create time-series maps by Year to show changes in behavior and site usage.

## Data integration and workflow considerations
- Data originates from video-based tagging; ensure Tag-to-identity consistency across datasets.
- Potential to combine with spatial layers (burrow coordinates, habitat types, environmental covariates).
- Suitable for joining with other observational datasets (e.g., site surveys, weather data) to enrich analyses.

## Data quality and management challenges
- Data may be dispersed across sources; require standardization and harmonisation.
- Variable data resolution and observation effort (CallEffort depending on hours observed).
- Gaps or missing observations for certain years or individuals.
- Needs careful handling of multi-year data for longitudinal spatial analyses.

## Practical guidance for GIS analysts
- Establish a consistent schema for Year-based records per Tag, with clear handling of missing values.
- Ensure spatial references are aligned when linking to burrow or site coordinates.
- Normalize CallEffort by observation hours (CallSamples) where possible to compare across individuals or sites.
- Document data provenance and any transformations to maintain traceability.
- Consider creating derived GIS layers (e.g., per-burrow activity, per-year social interaction maps) to facilitate exploration for policy colleagues, clients, or the public.