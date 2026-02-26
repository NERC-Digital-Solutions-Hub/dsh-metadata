# Supporting Documentation for the dataset 'The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK'

## Overview
- Study on the effect of neonicotinoids (and related pesticides) on Bombus terrestris audax nests.
- Two field-experiment trials at Wester Ross, Highlands, Scotland, measuring individual bee mass and colony health indicators.
- Bees were exposed to pesticides via sugar syrup and then assessed in the lab.

## Experimental design and treatments
- Colony setup:
  - 3 nests per box, with two Tripols per treatment group and 1 m spacing between Tripols.
  - Entrances at two ends and one in the middle to contain orientation effects within a treatment.
- Site arrangement:
  - Colonies placed in sheltered wilderness/enriched grassland habitat.
  - Order of treatments at site: UT (untreated) - single treatment - double treatment to minimize local effects.
- Treatments and timing:
  - Experiment 1: untreated, chlorpyrifos (150 nM), and chlorpyrifos (150 nM) + imidacloprid (10 nM).
  - Experiment 2: untreated, imidacloprid (10 nM) / chlorpyrifos (150 nM), and imidacloprid (10 nM).
  - Pesticide exposure via 1500 ml of sugar syrup containing the appropriate pesticide, provided to colonies; no pollen was supplied (foraging required).
- Duration:
  - Experiment 1: 48 days (25 April – 11 June 2014).
  - Experiment 2: 43 days (28 June – 9 August 2014).
- End-of-experiment procedures:
  - On final day, entrance gates adjusted to allow only bee entries for at least 5 hours; colonies returned to the laboratory for assessment.
  - Colony assessment included mass increase, live bee count, average bee mass, healthy brood cells on the nest surface, and overall nest condition.
  - Individual bees were weighed and then sacrificed for weighing confirmation.

## Site and environmental context
- Location: Wester Ross, The Highlands, Scotland.
- Environmental context: low baseline pesticide use in the area (pesticide load ~130-fold lower; insecticide use ~5000-fold lower) compared with intensively farmed arable regions (e.g., East Fife).
- Prior observations: no neonicotinoid or organophosphate use encountered on sampled farms, reducing likelihood of environmental contamination from these compounds.

## Sampling, data collection, and processing
- Data collection:
  - Beginning and end nest masses recorded for each colony (excluding the sugar syrup feed).
  - On final day, bees weighed in the lab after CO2 anesthesia and quick sacrifice in ice-cold detergent-containing water to prevent awakening.
- Data integrity:
  - Weights recorded via a two-person cross-check: one person reads the weight aloud and a second person confirms and records it.
  - Recorders were blinded to treatment group to reduce bias in data entry.
- Foraging context:
  - After exposure, bees were free-flying; they could forage for resources since no pollen was supplied.

## Data structure and files
- Two CSV files:
  - Neonicotinoidsonbumblebees_Experiment1.csv
  - Neonicotinoidsonbumblebees_Experiment2.csv
- Columns:
  - Colony number
  - Treatment
  - Bee mass (mg) values
- Notes on structure:
  - Columns represent colony number and treatment.
  - Rows represent individual bee masses (mg), ordered by mass.

## Quality control and limitations
- Quality control:
  - Duplicate weight verification during data entry; weight recorders were unaware of treatment groups.
- Limitations and considerations for analysis:
  - Environmental background pesticide exposure is minimized but not zero; interpretation should consider real-world variability.
  - Two separate experiments with different treatment sets and durations; cross-experiment comparability may require careful normalization.
  - Data capture focuses on mass and colony health proxies; other potentially important endpoints (e.g., behavioral or sublethal effects) are not reported here.
  - Pesticide exposure via sugar syrup without pollen intake may influence foraging behavior and colony dynamics differently than chronic field exposure.

## Practical implications for analysis
- Suitable for examining correlations between pesticide exposure (chlorpyrifos and/or imidacloprid) and:
  - Individual bee mass distributions
  - Colony-level health indicators (mass change, bee counts, brood health, nest condition)
- The dataset enables comparing treatment impacts within each experiment and, with appropriate caveats, across experiments.
- Data structure supports analysis of mass as the primary response variable, with colony and treatment as predictors, while accounting for paired experimental design and field conditions.