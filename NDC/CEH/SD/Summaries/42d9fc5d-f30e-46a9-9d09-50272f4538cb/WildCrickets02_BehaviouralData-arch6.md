# WildCrickets02_Behaviour Description of content

## Overview
- A dataset of behavioral data for each adult cricket in the population.
- Captures a set of life-long traits and observed behaviors across observations, including identity, sex, social/territorial activity, and vocalization effort.

## Data fields (traits and definitions)
- Year: Year the cricket was alive.
- Tag: Two-character code identifying the cricket in video recordings; read from a plastic tag on the pronotum.
- Sex: Male (M) or Female (F).
- Burrows: Number of different burrows where the cricket was observed during its life.
- Arrivals: Number of times the cricket was observed arriving at a burrow.
- Fights: Number of times the cricket was observed fighting another cricket.
- FightsWon: Number of fights won by the cricket.
- Mates: Number of different mating partners observed.
- Matings: Total number of matings observed for the cricket.
- CallEffort: Proportion of hours of observation when the cricket was singing.
- CallSamples: Total hours of observation used to estimate CallEffort.

## How this data supports analysis and data products
- Enables life-history and behavioral analyses at the individual level (e.g., linking social interactions, territorial behavior, and reproduction).
- Supports creation of self-serve analytics (dashboards, pivot tables) by cricket, year, sex, or life stage.
- Facilitates cross-field analyses (e.g., relationships between CallEffort and mating success, or between burrow use and fights).
- Can be combined with video metadata or other datasets to enrich insights.

## Data quality and preparation considerations
- Observational effort varies (CallEffort relies on CallSamples); normalization may be needed for fair comparisons.
- Data includes counts and rates; ensure consistent units and definitions across records.
- Tag-based identity should be validated to ensure continuity of a cricket’s life record across observations.
- Potential for patchy data or incomplete life histories; document gaps and apply appropriate missing-data handling.

## Practical next steps for Data Support
- Validate field definitions with domain experts (e.g., what constitutes a “fight” or a “mate”).
- Clean and standardize the dataset; compute derived metrics (e.g., fights per year, matings per mate, call effort per observation hour).
- Develop self-serve dashboards (by Year, Sex, Tag) and per-cricket life-history views.
- Create a data dictionary and usage guide to support reuse and promote broader sharing and re-use.