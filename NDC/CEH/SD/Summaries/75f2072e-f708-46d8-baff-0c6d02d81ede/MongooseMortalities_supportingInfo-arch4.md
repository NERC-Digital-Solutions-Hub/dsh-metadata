# Supporting information for MongooseMortalities.csv dataset

## Purpose
- Estimate the proportion of mortalities from winning groups versus losing groups in intergroup banded mongoose conflicts.

## Data Structure
- Focal and rival groups are assigned randomly.
- For each observed lethal intergroup encounter, the dataset records:
  - which group won (measured by which group ran from the fight location),
  - which individual died,
  - whether the deceased belonged to the winning or losing group,
  - the date of the encounter.

## Collection / Generation Methods
- Fights observed ad libitum (as they occurred, without a fixed schedule).

## Nature and Units of Recorded Values
- Winning group determination: based on which group fled from the location.
- Deceased individual identification: via unique shaving patterns on the mongoose back; patterns are reapplied when trapped monthly.

## Quality Control
- Field manager Francis performs routine data checks before submission to the University of Exeter to ensure dataset accuracy.

## Location and Dates
- Data collected 19/02/2000 to 11/11/2011.
- Mweya, Uganda (latitude -0.191724, longitude 29.895988).

## Experimental Design / Sampling Regime
- Ad libitum observation; sampling occurs when intergroup encounters are observed.

## Calibration / Instrumentation
- Not applicable.

## Data Column Headers (explanation)
- focal.group: Randomly chosen focal group ID.
- rival.group: Randomly chosen rival group ID.
- winner.group: ID of the winning group (determined by which group ran).
- dead.individual: ID of the deceased individual (based on identifiable markings).
- dead.ind.pack: Which group the deceased individual belonged to.
- dead.ind.in.which.pack: Whether the deceased was from the winning or losing group.
- date: Date of the encounter that led to mortality.