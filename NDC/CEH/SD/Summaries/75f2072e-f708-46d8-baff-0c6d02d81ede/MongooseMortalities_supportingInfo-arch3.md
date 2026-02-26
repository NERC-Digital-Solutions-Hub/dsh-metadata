# Supporting information for MongooseMortalities.csv dataset

## Purpose and scope
- The dataset aims to estimate the proportion of mortalities among two banded mongoose groups that occur in intergroup conflicts, distinguishing deaths in winning versus losing groups.

## Data structure and variables
- Focal and rival groups are assigned randomly for each observed intergroup encounter.
- Records pertain to each lethal intergroup fight observed at the field site.
- Key variables include:
  - winner.group: ID of the group that won the encounter (determined by which group fled from the fight location).
  - dead.individual: ID of the deceased individual (identified by unique shaving patterns on the mongoose back).
  - dead.ind.pack: which group the deceased individual belonged to.
  - dead.ind.in.which.pack: whether the deceased individual belonged to the winning or losing group.
  - date: date of the fight that led to the mortality.

## Data collection methods
- Fights were observed ad libitum (opportunistic observations by field team).
- Individual identification via shaved back patterns; patterns are reapplied monthly when mongooses are trapped.

## Data quality and provenance
- Data quality checks are performed by the field manager (Francis) before submission to the University of Exeter.
- The dataset includes an explicit data-quality control process to minimize errors prior to data sharing.

## Location, timeframe, and sampling frame
- Location: Mweya, Uganda (latitude -0.191724, longitude 29.895988).
- Data collection period: 19 February 2000 to 11 November 2011.
- Sampling frame: Intergroup encounters observed during fieldwork, with random selection of focal and rival groups for each observed fight.

## Data processing and metadata
- No calibration steps or laboratory instrumentation reported.
- Analytical methods are not specified within this dataset description.
- A table is provided describing data column headers and their meanings.

## Data column headers description
- focal.group: ID of the randomly chosen focal group.
- rival.group: ID of the randomly chosen rival group.
- winner.group: ID of the winning group (determined by which group fled).
- dead.individual: ID of the deceased individual.
- dead.ind.pack: which group the deceased individual belonged to.
- dead.ind.in.which.pack: whether the deceased individual belonged to the winning or losing group.
- date: date of the fight leading to mortality.

## Non-essential criteria and notes
- Fieldwork design: ad libitum, based on when intergroup encounters are observed.
- Fieldwork and laboratory instrumentation: not applicable (NA).
- Calibration steps and values: NA.
- Experimental design considerations: described as ad hoc observational encounters rather than a predefined experimental design.

## Relevance for monitoring and governance
- Illustrates essential data governance considerations for monitoring frameworks:
  - Clear data provenance and metadata (who collected, when, where, and how).
  - Transparency in data collection methods and identification procedures.
  - Data quality checks and accountability (field manager review).
  - Explicit data structure detailing the variables needed to estimate the proportion of mortalities by group outcome.
  - Timeliness and location-specific context important for scalable monitoring in environmental health or ecological policy evaluations.
  - Demonstrates challenges common to monitoring datasets (ad libitum data collection, need for robust identification markers, and potential data-sharing considerations).