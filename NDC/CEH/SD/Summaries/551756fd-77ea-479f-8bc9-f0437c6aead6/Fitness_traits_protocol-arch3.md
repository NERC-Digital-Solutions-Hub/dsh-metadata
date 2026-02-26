# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

## Overview
- Dataset measures fitness traits of Eschscholzia californica progeny subjected to selfed versus outcrossed pollen to assess effects of self-fertilisation on a species with low selfing propensity.
- Glasshouse experiment with 40 plants; two flowers per plant were emasculated and pollinated with outcrossed pollen on one flower and self-pollen on the other.
- For each supplemented plant, seeds from both cross types were cultivated and evaluated.
- Recorded traits include germination rate, time from germination to first flower, plant height at maturity, and biomass proxies (flowers and buds at maturity).
- Context: part of a larger study on how floral resources influence pollination services to isolated plants.
- Data collected and interpreted by Evans, T.M.; supports a supporting dataset and documentation.

## Experimental design
- 40 plants in a glasshouse environment.
- On each plant:
  - Two flowers emasculated.
  - One flower pollinated with outcrossed pollen; the other with self-pollen.
- Seeds from outcrossed and selfed fruits germinated and grown in 1 L pots under controlled conditions (day/night 20°C/15°C; 12:12 h photoperiod).
- From each supplemented plant, a seed from the outcrossed fruit and a seed from the selfed fruit were sown.
- Measurements taken at reproductive maturity include height, number of flowers, and number of buds.
- Selfed fruits predominantly produced a single seed; germination and subsequent growth tracked to maturity.

## Data structure and variables
- Data file: Fitness_traits_of_outcrossed_and_selfed_plants.csv
- Plant: identifier for the artificially supplemented plant
- Parentage: whether the seed came from outcrossed or selfed pollen
- Germination: binary indicator (1 = germinated, 0 = did not germinate)
- Duration_from_germination_to_reproductive_maturity: days from germination to first flower
- Height_at_reproductive_maturity: height in cm at first flowering
- Number_of_flowers_at_reproductive_maturity: count of flowers at maturity
- Number_of_buds_at_reproductive_maturity: count of buds at maturity
- Total_biomass_at_reproductive_maturity: combined measure of flowers and buds
- NA entries indicate measures skipped due to non-germination

## Supporting documentation and context
- Supporting documentation titled: Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants
- The dataset is part of a broader investigation into how floral resources affect pollination services to isolated plants.

## Data quality, governance and sharing considerations (relevant to monitoring frameworks)
- Completeness: dataset described as complete; explicit handling of NA for non-germinated seeds.
- Metadata clarity: explicit column names and units; clearly defines treatments (outcrossed vs selfed) and maturity measurements.
- Data structure: stored in a single CSV with plant- and treatment-level identifiers enabling traceability.
- Reproducibility: controlled glasshouse conditions documented; cross-type treatment clearly delineated, aiding auditability.
- Governance and sharing: results are presented with underlying data; potential barriers for broader sharing (depending on metadata richness and data provenance) are mitigated by explicit data definitions and provenance.
- Practical implications for monitoring: enables assessment of how selfing versus outcrossing influences early-life fitness traits, informing measures of reproductive success and potential pollination service impacts in managed plant populations.