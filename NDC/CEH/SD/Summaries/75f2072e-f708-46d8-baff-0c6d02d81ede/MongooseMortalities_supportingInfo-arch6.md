# Supporting information for MongooseMortalities.csv dataset

- Objective: Estimate the proportion of mortalities that occur in winning groups versus losing groups during intergroup conflicts among banded mongooses.

- Data structure and key variables:
  - Focal and rival groups are assigned randomly for each observation.
  - For each observed lethal intergroup encounter, the dataset records:
    - Which group won (measured by which group ran from the fight location).
    - Which individual died in the battle.
    - Whether the deceased belonged to the winning or losing group.
    - The date of the encounter.

- Death identification and group assignment:
  - Deaths are identified by uniquely identifiable shaving patterns on the mongoose backs (patterns reapplied monthly when mongoose are trapped).

- Collection and data quality:
  - Fights were recorded ad libitum (as they occurred in the field).
  - Data are routinely checked for errors by the field manager prior to submission to the University of Exeter.

- Location and temporal scope:
  - Field site: Mweya, Uganda (latitude -0.191724, longitude 29.895988).
  - Observation period: 19 February 2000 to 11 November 2011.

- Additional notes and non-essential criteria:
  - Experimental design: ad libitum observations; no structured sampling regime described beyond opportunistic encounters.
  - Field/lab instrumentation, calibration steps, and analytical methods are not specified.

- Data column headers (explanation):
  - focal.group: ID of the focal group chosen randomly.
  - rival.group: ID of the rival group chosen randomly.
  - winner.group: ID of the winning group (the group that ran away last or away from the fight location).
  - dead.individual: ID of the deceased individual.
  - dead.ind.pack: Which group the deceased individual belonged to.
  - dead.ind.in.which.pack: Whether the deceased belonged to the winning or losing group.
  - date: Date of the fight leading to the mortality.