# WildCrickets02_Behaviour Description of content

## Overview
- A dataset of behavioural observations for each adult cricket in the population.
- Records for key life and behavioural attributes across the year(s) the cricket was alive.

## Key variables (per cricket)
- Year: The year during which the cricket was alive.
- Tag: A two-character code read from a plastic tag attached to the cricket’s pronotum, used to identify individuals in video recordings.
- Sex: Male (M) or Female (F).
- Burrows: Number of different burrows where the cricket was observed during its life.
- Arrivals: Number of times the cricket was observed arriving at a burrow.
- Fights: Number of times the cricket was observed fighting another cricket.
- FightsWon: Number of fights the cricket won (within the fights observed above).
- Mates: Number of different partners the cricket was observed mating with.
- Matings: Total number of matings observed for the cricket.
- CallEffort: Proportion of hours of observation during which the cricket was singing (regardless of duration in each hour).
- CallSamples: Total hours of observation used to estimate CallEffort.

## Data structure and collection
- Each record corresponds to an individual adult cricket, identified by Tag.
- Observations are derived from video recordings; the Tag is readable from the video.
- CallEffort is an activity measure derived from observation hours, with CallSamples indicating the basis (hours) used to estimate CallEffort.

## Potential uses for monitoring and evaluation
- Assessing activity budgets and social/sexual behaviour within the population (e.g., burrow use, arrival dynamics, fights, mating opportunities).
- Monitoring reproductive and social interaction indicators over time (mates and matings).
- Evaluating communication or signalling activity through CallEffort as an index of vocalisation patterns.

## Data quality, metadata and governance considerations
- Identification relies on readable tags; data integrity depends on accurate tag reading and consistent video coding.
- CallEffort depends on the amount and distribution of observation hours; transparency about observation effort (CallSamples) is essential for comparability.
- Metadata completeness is important to verify life stage, observation periods, and potential gaps in observations (e.g., missing fights or matings).
- Data standardisation and provenance are needed to support data sharing, reuse, and integration with other monitoring datasets.