# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

## Overview
- Dataset of fitness traits for Eschscholzia californica progeny to assess effects of self-fertilisation on a plant with low selfing propensity.
- Glasshouse experiment with 40 plants examining selfed vs outcrossed pollen supplementation.
- Traits recorded: germination rate, time from germination to first flower (reproductive maturity), height at reproductive maturity, and biomass (flowers and buds) at reproductive maturity.
- Part of a larger study on how floral resources influence pollination services to isolated plants.
- Collected and interpreted by Evans, T.M.; supporting documentation titled “Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants.”

## Experimental design
- 40 artificially crossed plants; on each plant, two flowers were emasculated.
- One flower received outcrossed pollen; the other received self-pollen.
- From each supplemented flower, seeds were sown: outcrossed-fruit seeds and selfed-fruit seeds (selfed fruits typically yield one seed).
- Seeds sowed into 1-liter pots; glasshouse conditions: day 20°C / night 15°C, 12:12 h light:dark.
- Recorded metrics: germination, duration to first flower, height at first flowering, and biomass characteristics at reproductive maturity.

## Data structure and units
- All data in one CSV: Fitness_traits_of_outcrossed_and_selfed_plants.csv
- Key columns:
  - Plant: identifier of the supplemented plant
  - Parentage: whether the seed came from outcrossed or selfed pollen
  - Germination: 1 = germinated, 0 = did not germinate
  - Duration_from_germination_to_reproductive_maturity: days from germination to first flower
  - Height_at_reproductive_maturity: height in cm at first flowering
  - Number_of_flowers_at_reproductive_maturity
  - Number_of_buds_at_reproductive_maturity
  - Total_biomass_at_reproductive_maturity: sum of flowers and buds
- NA present where measures were not recorded due to seed non-germination
- Data provenance: complete dataset; collected and interpreted by Evans, T.M.
- Supporting documentation: “Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants”