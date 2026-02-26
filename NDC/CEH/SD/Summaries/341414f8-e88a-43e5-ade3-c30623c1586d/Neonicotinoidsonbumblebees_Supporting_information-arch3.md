# Supporting Documentation for the dataset 'The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK'

## Overview
- Documents the design, collection, and structure of data for a study on bumblebees (Bombus terrestris audax) exposed to pesticides.
- Aimed at understanding potential effects of neonicotinoids (and related pesticides) on bee weight and colony condition, using controlled treatment exposures.

## Experimental Design / Sampling Regime
- Bumblebee nests housed in groups within field boxes: 3 nests per box, entrances at both ends and the middle.
- Two Tripols per treatment group, placed ~1 m apart to contain orientation differences within treatments.
- Colonies sited in sheltered, wilderness/enriched grassland habitat in Wester Ross, Highlands, Scotland, an area with substantially reduced pesticide usage compared with intensively farmed regions.
- No neonicotinoids or organophosphates detected on sampled farms in the Highlands and Islands; environmental contamination with these compounds considered unlikely.
- Pesticide exposure delivered via sugar syrup: each colony received 1500 ml of syrup either untreated or spiked with pesticides.
- Order of treatment boxes designed as UT - single treatment - double treatment to minimize local effects.
- Two experimental runs:
  - Experiment 1: untreated, chlorpyrifos (150 nM), chlorpyrifos (150 nM) + imidacloprid (10 nM).
  - Experiment 2: untreated, imidacloprid (10 nM) + chlorpyrifos (150 nM), and imidacloprid (10 nM) alone.
- Field exposure durations: 28–48 days depending on experiment (28 June–9 Aug 2014 or 25 Apr–11 Jun 2014), limited by site access.
- Final day: entrance gates set to permit only bee entry (no exits) for ~5 hours before returning colonies to the laboratory.

## Treatments and Exposure Details
- Pesticides used in treatment arms:
  - Chlorpyrifos at 150 nM
  - Imidacloprid at 10 nM
- Exposure consisted of ad libitum foraging after initial exposure to treated syrup; no pollen was provided, requiring bees to forage.

## Colony Assessment and Fieldwork
- On final day, colonies assessed for:
  - Increase in colony mass
  - Total live bee count
  - Average bee mass
  - Number of healthy brood cells on nest surface
  - Overall nest condition
- Each nest mass recorded at start and end (excluding sugar syrup).
- Post-assessment: bees anesthetized with CO2, then weighed and sacrificed in ice-cold, deters wakefulness.

## Nature and Units of Recorded Values
- Data stored in two CSV files:
  - Neonicotinoidsonbumblebees_Experiment1.csv
  - Neonicotinoidsonbumblebees_Experiment2.csv
- Structure:
  - Columns: Colony number, treatment
  - Rows: Bee mass (mg), ordered by mass

## Data Quality and Verification
- Quality control via dual-recording check:
  - One person read out bee weights to a second person, who entered the values to the database.
  - Recorders were blinded to treatment group to minimize bias.

## Data Structure Details
- Reiterates that the dataset comprises two CSV files with colony-based and treatment information, and bee mass measurements ordered by mass.