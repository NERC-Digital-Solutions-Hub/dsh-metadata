# WildCrickets02_Behaviour Description of content

## Overview
- A dataset describing behavioural data for each adult cricket in the population, covering multiple traits related to life history, social interactions, and activity.
- Traits include identifiers, life year, sex, movement between burrows, social interactions (arrivals, fights, matings), and acoustic activity (call effort).

## Data Fields and Definitions
- Year: The year when the cricket was alive.
- Tag: The two-character code used to identify the cricket in video recordings; each cricket has a plastic tag on the pronotum readable in video.
- Sex: Male (M) or Female (F).
- Burrows: Number of different burrows where the cricket was observed during its life.
- Arrivals: Number of times this cricket was observed arriving at a burrow.
- Fights: Number of times this cricket was observed fighting another cricket.
- FightsWon: Number of times this individual won a fight among the recorded fights.
- Mates: Number of different partners this cricket was observed mating with.
- Matings: Number of matings observed for this cricket.
- CallEffort: Proportion of hours of observation when this cricket was singing (regardless of sing duration over each observed interval).
- CallSamples: Total number of hours of observation used to estimate CallEffort.

## Data Collection and Structure
- Data are derived from video observations with tags read from the pronotum.
- Observations include counts and durations across life history, enabling calculation of effort-related metrics (e.g., CallEffort).

## Data Quality, Standardisation, and Accessibility
- The dataset is organized for consistency with standard monitoring approaches.
- Data should be verified, quality assured, cleaned, and transformed as needed.
- Outputs (e.g., datasets) should be stored in appropriate data portals and made accessible to stakeholders.

## Relevance for Environmental Monitoring
- The behavioural metrics can serve as indicators of population health, social structure, mating success, and habitat use.
- When integrated with other environmental data, these fields support assessment of ecological conditions and policy-relevant monitoring over time.