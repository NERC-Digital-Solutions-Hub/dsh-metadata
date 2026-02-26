# WildCrickets02_Behaviour Description of content

- Overview: This dataset contains behavioural data for each adult cricket in the population across its life, recorded from video observations. Each cricket is identified by a plastic tag attached to its pronotum.

- Key variables:
  - Year: The year when the cricket was alive.
  - Tag: Two-character code used to identify the cricket in video recordings.
  - Sex: Male (M) or Female (F).
  - Burrows: Number of different burrows observed for this cricket during its life.
  - Arrivals: Number of times this cricket was observed arriving at a burrow.
  - Fights: Number of times this cricket was observed fighting another cricket.
  - FightsWon: Number of fights this cricket won.
  - Mates: Number of different partners this cricket was observed mating with.
  - Matings: Number of matings observed for this cricket.
  - CallEffort: Proportion of hours of observation during which this cricket was singing.
  - CallSamples: Total hours of observation used to estimate CallEffort.

- Data collection and identification:
  - Data are derived from video recordings.
  - Tagging enables individual identification across observations and, potentially, across years.

- Data structure implications for analysis:
  - Per-cricket records allow tracking life-long behavioural patterns and social interactions (burrow use, arrivals, fights, mating activity, and presence of singing).
  - Variables capture both social interactions (fights, mates, matings) and activity patterns (CallEffort, CallSamples).

- Potential uses and governance considerations for Data Leaders:
  - Use for understanding individual and population-level behaviour, social networks, and mating strategies over time.
  - Ensure clear metadata and definitions for each variable (especially unit implications for CallEffort and CallSamples) to support discovery, reuse, and proper interpretation.
  - Facilitate data quality checks and documentation to enable reliable aggregation across individuals and years.