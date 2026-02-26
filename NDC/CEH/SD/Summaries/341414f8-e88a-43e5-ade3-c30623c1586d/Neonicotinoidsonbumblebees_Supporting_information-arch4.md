# Supporting Documentation for the dataset 'The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK'

## Purpose and Scope
- Documentation describing experimental design, sampling, collection methods, fieldwork, and analytical methods for a dataset on bumblebee weights under neonicotinoid exposure.
- Field setting: Wester Ross, Highlands, Scotland; environment characterized by very low baseline pesticide use.
- Treatments delivered via pesticide-spiked sugar syrup; pollen not provided; bees forage independently.

## Experimental Design and Treatment Regime
- Colony setup: 3 nests per box; two Tripols per treatment; approximately 1 m spacing to contain orientation effects within treatments.
- Field placement: sheltered grassland/wilderness habitat; low environmental pesticide load reported.
- Treatments and timing:
  - Experiment 1: untreated; chlorpyrifos (150 nM); chlorpyrifos (150 nM) + imidacloprid (10 nM).
  - Experiment 2: untreated; imidacloprid (10 nM) + chlorpyrifos (150 nM); imidacloprid (10 nM) alone.
- Exposure and duration: colonies exposed for 28–48 days across experiments (dates: late April–June 2014, and June–August 2014).
- Final day protocol: entrance gates set to allow only bee entry for at least 5 hours, then colonies returned to the lab.

## Data Collection and Assessment Methods
- Colony assessments in lab focusing on:
  - Increase in colony mass
  - Total live number of bees
  - Average bee mass
  - Number of healthy brood cells on nest surface
  - Overall nest condition
- Individual nest mass recorded at start and end (excluding syrup).
- Post-assessment processing: bees anesthetized with CO2, weighed, and sacrificed in ice-cold detergent solution.

## Data Structure and Files
- Data files: Neonicotinoidsonbumblebees_Experiment1.csv and Neonicotinoidsonbumblebees_Experiment2.csv
- Columns: Colony number, treatment (per colony)
- Rows: Bee mass (mg) ordered from heaviest to lightest
- Data integrity: two-person weight verification process; recorder blind to treatment to reduce bias.

## Quality Control and Metadata
- Weight data validated by cross-checking spoken weights against entered values.
- Recorders were blind to treatment group to minimize bias.
- Explicit metadata on data structure provided; two separate CSV files correspond to the two experiments.

## Context and Site Information
- Highlands site context: notably reduced arable and insecticide use relative to intensively farmed areas; no detected neonicotinoid or organophosphate use on sampled farms; environmental contamination with these compounds considered unlikely.

## Considerations for Data Management and Reuse
- Data assets include detailed experimental design and concrete measurement protocol, enabling replication or meta-analysis with comparable datasets.
- Key considerations: ecological context, treatment doses, mass-based outcomes, and the absence of pollen provisioning as a factor in interpretation.
- Data governance: clear data lineage (design to data files) and quality checks support reliability and discoverability.