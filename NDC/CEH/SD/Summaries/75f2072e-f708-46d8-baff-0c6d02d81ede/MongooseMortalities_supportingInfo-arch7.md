# Supporting information for MongooseMortalities.csv dataset

## Purpose
- Estimates the proportion of mortalities from winning groups vs losing groups in intergroup conflicts of banded mongooses.

## Data structure and columns
- Focal and rival groups are assigned randomly for each observed encounter.
- For each lethal intergroup conflict, records include:
  - focal.group: ID of the focal group (randomly chosen)
  - rival.group: ID of the rival group (randomly chosen)
  - winner.group: ID of the winning group (the group that ran from the fight location)
  - dead.individual: ID of the deceased individual
  - dead.ind.pack: Which group the deceased individual belonged to
  - dead.ind.in.which.pack: Whether the deceased individual belonged to the winning or losing group
  - date: date of the fight that led to mortality
- A table maps these headers to their descriptions (1 = description) for reference.

## Data collection methods
- Fights were observed ad libitum (as opportunities arose).

## Spatial and temporal details
- Location: Mweya, Uganda
  - Latitude: -0.191724
  - Longitude: 29.895988
- Data collection period: 19 February 2000 to 11 November 2011

## Identification and measurement details
- Winner determination: based on which group ran from the location of the fight.
- Individual mortality identification: via uniquely identifiable shaving patterns on the mongoose backs; patterns are reapplied monthly when mongooses are trapped.

## Quality control
- Field manager Francis routinely checks data for errors before submission to the University of Exeter.

## Additional context
- Field sampling regime: ad libitum (opportunistic encounters)
- Instrumentation/calibration: not specified
- Analytical methods: not specified

## Implications for GIS and data use
- Enables map-based visualization of mortalities by winner/loser status, group, and location over time.
- Useful for spatial-temporal analyses of intergroup conflict outcomes, group dynamics, and mortality distribution.
- Data integration potential with other spatial datasets (e.g., habitat, movement, or group ranges), subject to consistent data standards and alignment of identifiers.