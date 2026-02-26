# Supporting information for MongooseMortalities.csv dataset

## Purpose and scope
- The dataset estimates the proportion of mortalities from winning groups versus losing groups in intergroup lethal conflicts among banded mongoose groups.
- Focal and rival groups are assigned randomly to ensure unbiased comparison.

## Data structure
- For each observed lethal intergroup encounter, the dataset records:
  - Which group won the contest (determined by which group ran from the fight location).
  - Which individual died in the battle (identified by uniquely observable shaving patterns on the mongoose back, patterns reapplied monthly during trapping).
  - Which group the deceased individual belonged to (winning or losing group).
  - The date of the fatal encounter.

## Collection methods
- Fights were observed ad libitum by field researchers at the Mweya field site, Uganda.

## Units, definitions, and measurements
- Winner group: determined by the group that ran from the fight location.
- Dead individual: identified by shaving pattern on the back; patterns are refreshed monthly during trapping.
- Group membership of the deceased: indicated by the deceased individual’s pack.

## Quality assurance and provenance
- Field manager Francis performs routine quality checks before data are sent to the University of Exeter to ensure there are no errors.

## Location and time span
- Location: Mweya, Uganda (lat -0.191724, long 29.895988).
- Data collection period: 19 February 2000 to 11 November 2011.

## Non-essential criteria and additional context
- Experimental design/sampling regime: ad libitum, opportunistic observations of intergroup encounters.
- Fieldwork and laboratory instrumentation: not applicable (NA).
- Calibration steps and values: NA.
- Analytical methods: NA.

## Data column headers (description table)
- focal.group: Randomly chosen focal group ID.
- rival.group: Randomly chosen rival group ID.
- winner.group: ID of the winning group; the loser is determined by which group ran from the fight location.
- dead.individual: ID of the deceased individual.
- dead.ind.pack: Which group the deceased individual belonged to.
- dead.ind.in.which.pack: Whether the deceased belonged to the winning or losing group.
- date: Date of the fight leading to mortality.