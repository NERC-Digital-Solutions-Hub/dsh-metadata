# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

## Overview
- A glasshouse experiment assessing how self-fertilisation versus outcrossing affects plant fitness.
- 40 plants were used; on each plant two flowers were treated differently (one selfed, one outcrossed).
- Seeds from each treatment were grown and analyzed for several fitness traits.

## Experimental design
- For each plant:
  - Two flowers were emasculated; one received outcrossed pollen, the other self-pollen.
  - Pollen transfer involved wiping anthers onto stigmas, then covering with fine muslin.
  - From each supplemented flower, one seed from the outcrossed fruit and one from the selfed fruit were sown in 1 L pots (selfed fruits typically produced one seed).
- Growth conditions: glasshouse with day/night temperatures of 20°C/15°C and a 12:12 hour light:dark cycle.
- Traits recorded:
  - Germination (binary: 1 = germinated, 0 = did not germinate)
  - Duration from germination to reproductive maturity (days to first flower)
  - Height at reproductive maturity (cm)
  - Number of flowers at reproductive maturity
  - Number of buds at reproductive maturity
  - Total biomass at reproductive maturity (flowers + buds)

## Data structure and units
- Data file: Fitness_traits_of_outcrossed_and_selfed_plants.csv
- Key columns:
  - Plant: identifier for the artificially supplemented plant
  - Parentage: indicates outcrossed vs selfed seed
  - Germination: binary germination indicator (1 = yes, 0 = no)
  - Duration_from_germination_to_reproductive_maturity: days
  - Height_at_reproductive_maturity: cm
  - Number_of_flowers_at_reproductive_maturity: count
  - Number_of_buds_at_reproductive_maturity: count
  - Total_biomass_at_reproductive_maturity: count (sum of flowers and buds)
- Missing data: NA used where measures could not be taken because seeds did not germinate

## Context and scope
- Part of a larger study on the effect of floral resources on pollination services to isolated plants.
- The dataset is described as complete and was collected and interpreted by Evans, T.M.

## Relevance and potential uses for GIS-oriented data work
- While the experiment is glasshouse-based, the data structure supports spatial mapping of results if integrated with experimental metadata (e.g., plant provenance, treatment blocks, or greenhouse zones).
- Useful for developing map-based data products that compare selfed vs outcrossed fitness traits across individuals or experimental conditions.
- Data quality and provenance details support reproducibility and integration with other datasets, including metadata on experimental design and growth conditions.