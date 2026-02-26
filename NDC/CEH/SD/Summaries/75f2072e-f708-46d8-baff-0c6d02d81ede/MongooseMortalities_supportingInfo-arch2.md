# Supporting information for MongooseMortalities.csv dataset

## Overview
- Aims to estimate the proportion of mortalities from winning groups versus losing groups in banded mongoose intergroup conflicts.
- Random assignment of focal and rival groups; data collected from observed lethal intergroup encounters.

## Data structure and key variables
- Data capture for each observed fight includes:
  - focal.group: randomly chosen focal group ID
  - rival.group: randomly chosen rival group ID
  - winner.group: ID of the group that won (determined by which group ran away from the fight location)
  - dead.individual: ID of the deceased individual (identified by distinctive shaving patterns)
  - dead.ind.pack: which group the deceased individual belonged to
  - dead.ind.in.which.pack: whether the deceased individual belonged to the winning or losing group
  - date: date of the fight that led to mortality

## Data collection methods
- Observations conducted ad libitum during intergroup encounters.
- Shaving patterns used for individual identification; patterns reapplied when mongooses are trapped (monthly).

## Measurements and units
- Winner determination: based on retreat from the fight location.
- Mortality identification: individual death recorded with unique back-shaving pattern.
- Temporal/spatial data: date of fight; location Mweya, Uganda (lat -0.191724, long 29.895988).

## Quality control
- Field manager Francis performs routine data checks prior to forwarding data to the University of Exeter to ensure accuracy.

## Location and timeframe
- Mweya, Uganda (latitude -0.191724, longitude 29.895988)
- Data collection period: 19 February 2000 to 11 November 2011

## Experimental design and sampling
- Design: ad libitum sampling; encounters recorded whenever observed.
- No additional fieldwork or laboratory instrumentation required for this dataset.

## Data management and accessibility
- Data and quality checks are performed in the field and by the study sponsor before data submission.
- Datasets are intended to be stored and uploaded to appropriate data portals for reuse and verification.

## Analytical potential and outputs
- Primary output: proportion of mortalities arising from winning vs losing groups.
- Data can be combined with other environmental or behavioral datasets to enhance value and enable broader analyses.
- Useful for transparency and policy-like assessment of intergroup conflict outcomes in a monitored wildlife population.

## Limitations and considerations
- Observations are ad libitum and may be influenced by detectability or observer presence.
- Identification relies on monthly pattern reapplication; potential for misclassification if patterns degrade between checks.
- Analytical methods are not specified within the dataset metadata; users may need to apply their own statistical approaches.

## Data columns explained (quick reference)
- focal.group: randomly chosen focal group ID
- rival.group: randomly chosen rival group ID
- winner.group: ID of the winning group
- dead.individual: ID of the deceased individual
- dead.ind.pack: which group the deceased individual belonged to
- dead.ind.in.which.pack: whether the deceased individual belonged to the winning or losing group
- date: date of the fight that led to the mortality