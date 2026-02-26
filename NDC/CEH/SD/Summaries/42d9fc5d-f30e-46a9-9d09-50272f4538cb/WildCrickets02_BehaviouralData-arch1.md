# WildCrickets02_Behaviour Description of content

## Overview
- A dataset of behavioural data for each adult cricket in the population for the year of the cricket’s life.
- Each row represents an individual cricket, identified by a unique tag read from video recordings.
- Records cover basic demographics, social/behavioural events, and measured activity like singing.

## Fields and definitions
- Year: The year when the cricket was alive.
- Tag: Two-character code identifying the cricket in video recordings (attached to the cricket’s pronotum).
- Sex: Male (M) or Female (F).
- Burrows: Number of different burrows observed for this cricket during its life.
- Arrivals: Number of times the cricket was observed arriving to a burrow.
- Fights: Number of times the cricket was observed fighting another cricket.
- FightsWon: Number of fights won by the cricket.
- Mates: Number of different partners this cricket was observed mating with.
- Matings: Total number of matings observed for this cricket.
- CallEffort: Proportion of hours of observation during which the cricket was singing.
- CallSamples: Total hours of observation used to estimate CallEffort.

## How this data could be analyzed
- Explore correlations between CallEffort and Matings or Fights to assess mating benefits of singing.
- Model life-history traits (Burrows, Arrivals, Fights, Mates, Matings) against Year and Sex.
- Investigate whether social activity (Arrivals, Burrows, Fights) predicts mating outcomes (Mates, Matings).
- Use CallSamples as a measure of sampling effort to weight CallEffort estimates or adjust analyses.
- Develop predictive models for reproductive success or survival based on observed behaviours.

## Considerations for analysts
- Data are per individual cricket across the observed year, enabling longitudinal or life-history type analyses if multiple years exist.
- CallEffort is a derived proportion requiring explicit observation hours (CallSamples) for interpretation.
- Potential issues to address: incomplete observation, variation in sampling effort across individuals, and potential measurement error in behavioural counts.