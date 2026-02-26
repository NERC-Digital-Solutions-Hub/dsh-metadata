# Fitness traits of experimentalIy selfed and outcrossed Eschscholzia californica plants

- Overview
  -Dataset measuring fitness traits to determine the effects of self-fertilisation on Eschscholzia californica, a plant with low propensity to self.
  -Glasshouse experiment with 40 plants, comparing selfed vs outcrossed pollen on two flowers per plant.
  -For each plant, seeds from both treatments were sown and monitored for germination and growth traits.

- Experimental design
  -On each of 40 plants, two flowers were emasculated.
  -First flower received outcrossed pollen; second received self-pollen.
  -Pollination performed by transferring pollen with tweezers and shielding with muslin.
  -Seeds from the outcrossed and selfed fruits were sown separately into 1 L pots.
  -Growing conditions: glasshouse with day/night 20°C/15°C and 12:12 light:dark cycle.
  -Traits recorded: germination, time from germination to reproductive maturity (first flower), height at reproductive maturity, and biomass at reproductive maturity (flowers and buds).

- Data structure and variables
  - Data stored in a single CSV: Fitness_traits_of_outcrossed_and_selfed_plants.csv.
  - Key columns:
    - Plant: identifier for the supplemented plant.
    - Parentage: indicates whether the seed came from outcrossed or selfed pollen.
    - Germination: 1 = yes, 0 = no.
    - Duration_from_germination_to_reproductive_maturity: days to first flower.
    - Height_at_reproductive_maturity: height in cm.
    - Number_of_flowers_at_reproductive_maturity: count.
    - Number_of_buds_at_reproductive_maturity: count.
    - Total_biomass_at_reproductive_maturity: total number of flowers and buds.
  - NA entries indicate traits not measured due to lack of germination.

- Provenance and documentation
  - Part of a larger experiment examining the effect of floral resources on pollination services to isolated plants.
  - Data collected and interpreted by Evans, T.M.
  - Supporting documentation titled: Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants.

- Relevance for environmental monitoring
  - Demonstrates standardized, replicable measurement of plant reproductive fitness under different pollen treatments.
  - Produces outputs (germination, development timing, growth metrics) suitable for time-series or cross-study comparisons when monitoring environmental effects on plant-pollinator dynamics.
  - Data quality and structure support integration with other environmental datasets and broader monitoring portals.