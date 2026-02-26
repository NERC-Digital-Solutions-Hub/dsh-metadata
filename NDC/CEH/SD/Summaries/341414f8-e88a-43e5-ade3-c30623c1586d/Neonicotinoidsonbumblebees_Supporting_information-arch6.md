# Supporting Documentation for the dataset 'The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK'

## Overview
- Study of the number and individual weight of buff-tailed bumblebees (Bombus terrestris audax) from nests exposed to neonicotinoids.
- Conducted in Wester Ross, Highlands, Scotland, with field exposure to pesticides and subsequent laboratory assessment.

## Experimental design and site
- Bumblebee colonies housed as 3 nests per box with dual end entrances and one middle entrance.
- Two Tripols per treatment group placed in the field, spaced about 1 m apart to contain orientation effects within treatment.
- Field site chosen in sheltered wilderness/enriched grassland; Highlands region with markedly lower background pesticide and insecticide use compared with intensively farmed areas.
- Field exposure duration: two separate experiments.
  - Experiment 1: 48 days (April 25 – June 11, 2014), treatments include untreated, chlorpyrifos (150 nM), and chlorpyrifos (150 nM) with imidacloprid (10 nM).
  - Experiment 2: 43 days (June 28 – August 9, 2014), treatments include untreated, imidacloprid (10 nM) with chlorpyrifos (150 nM), and imidacloprid (10 nM) alone.
- Post-exposure: entrances opened briefly for foraging, then gates closed; bees returned to laboratory for assessment after at least 5 hours of foraging.

## Treatments and administration
- Pesticide exposure via sugar syrup: each colony received 1500 ml of sugar syrup containing the designated pesticide or left untreated.
- Bees were not forced to consume treated syrup; they could forage post-exposure.
- Pesticide types used: chlorpyrifos and imidacloprid, in specified concentrations.

## Data collection and measured variables
- Colony-level and individual-level measurements taken on final day:
  - Increase in colony mass
  - Total live number of bees remaining
  - Average bee mass
  - Number of healthy brood cells on nest surface
  - Overall nest condition
  - Individual bee masses recorded at the start and end of the experiment (excluding the sugar syrup feed)
- Individual bees were anesthetized with CO2, weighed, and sacrificed in ice-cold detergent solution to prevent awakening.
- Final dataset captures bee masses (in mg) for individuals, ordered by mass.

## Data structure and files
- Two CSV data files:
  - Neonicotinoidsonbumblebees_Experiment1.csv
  - Neonicotinoidsonbumblebees_Experiment2.csv
- Data schema:
  - Columns: Colony number and treatment
  - Rows: Bee mass (mg), ordered from heaviest to lightest
- Additional notes indicate the dataset comprises two CSV files with the same structure for the respective experiments.

## Quality control and data integrity
- Dual-entry verification: one person read each bee’s weight aloud to a second person, who re-entered the weight to ensure accuracy.
- Recorders were blind to the treatment group to minimize bias.

## Data handling, provenance, and access
- Data collected through a combination of field exposures and laboratory assessments, with explicit treatment order design to minimize local effects.
- The documentation provides details on experimental procedures, measurement timing, and data structure to support reproducibility and re-use.
- The dataset is structured to enable inspection of individual bee weights by colony and treatment, supporting downstream analysis and comparison across treatment conditions.

## Notes and considerations
- No neonicotinoid or organophosphate use was encountered on farms in the Highlands and Islands, suggesting low background environmental contamination for these compounds in the study area.
- For data users: the two CSV files contain mass measurements suitable for analysis of treatment effects on individual bee weights, with careful blinding during data entry to reduce bias.