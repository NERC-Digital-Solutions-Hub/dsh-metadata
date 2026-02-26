# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

## Overview
- Datasets measure fitness traits from Eschscholzia californica progeny subjected to self-pollination versus outcrossing.
- Purpose: determine effects of self-fertilisation on a plant with low propensity to selfing.
- Context: part of a larger glasshouse experiment examining how floral resources influence pollination services to isolated plants.
- Data were collected and interpreted by Evans, T.M. and are accompanied by supporting documentation.

## Experimental design
- 40 plants grown in a glasshouse.
- On each plant, two flowers were emasculated: one received outcrossed pollen, the other self-pollen.
- From each supplemented flower, seeds were sown into 1 L pots (outcrossed seeds from the outcrossed fruit; selfed seeds from the selfed fruit; selfed fruits typically produced one seed).
- Growing conditions: day/night 20°C/15°C with a 12:12 h light/dark photoperiod.
- Fitness traits recorded: germination rate, time from germination to reproductive maturity (first flower), height at reproductive maturity, and biomass (number of flowers and buds) at reproductive maturity.

## Data structure and units
- Data stored in a single CSV file: Fitness_traits_of_outcrossed_and_selfed_plants.csv.
- Key columns:
  - Plant: identifier for the supplemented plant.
  - Parentage: indicates whether the seed came from an outcrossed or selfed flower.
  - Germination: binary indicator (1 = germinated, 0 = did not germinate).
  - Duration_from_germination_to_reproductive_maturity: duration in days to first flower.
  - Height_at_reproductive_maturity: height in centimeters at first flowering.
  - Number_of_flowers_at_reproductive_maturity: count of flowers at reproductive maturity.
  - Number_of_buds_at_reproductive_maturity: count of buds at reproductive maturity.
  - Total_biomass_at_reproductive_maturity: total biomass expressed as the number of flowers and buds at reproductive maturity.
- Missing values: NA used when germination did not occur, precluding other measurements.

## Data provenance and scope
- Dataset is complete for the recorded measures, with the scope focused on comparing selfed vs outcrossed progeny within 40 plants.
- Collected and interpreted by Evans, T.M.
- Related documentation: Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants.

## Potential uses and considerations
- Compare germination rates between selfed and outcrossed progeny.
- Assess effects of parentage on time to reproductive maturity, plant height, and reproductive biomass.
- Explore relationships among early germination, growth, and final fitness traits within a controlled cross-type framework.
- Useful as a component of broader analyses on pollination biology and the influence of floral resources on pollination services.
- Limitations to consider: modest sample size (40 plants), controlled glasshouse conditions, and NA values for non-germinated seeds.