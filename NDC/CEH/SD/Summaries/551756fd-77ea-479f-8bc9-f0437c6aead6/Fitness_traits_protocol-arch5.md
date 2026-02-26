# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

## Aim and context
- Dataset measures fitness traits from Eschscholzia californica progeny to assess the effects of self-fertilisation on a species with low propensity to selfing.
- Part of a larger glasshouse experiment examining the effect of floral resources on pollination services to isolated plants.
- Experimental work conducted with 40 plants, data interpreted by Evans, T.M.

## Experimental design
- Glasshouse experiment with 40 artificially crossed plants.
- On each plant, two flowers were emasculated: one pollinated with outcrossed pollen, the other with self-pollen.
- From each supplemented plant, seeds from the outcrossed and selfed fruits were sown into 1 L pots.
- Environmental conditions: day/night 20°C/15°C with a 12:12 h light/dark cycle.

## Data content and structure
- Data file: Fitness_traits_of_outcrossed_and_selfed_plants.csv (one CSV file).
- Columns:
  - Plant: identifier for the artificially supplemented plant.
  - Parentage: whether the seed came from an outcrossed or selfed fruit.
  - Germination: binary (1 = germinated, 0 = did not germinate).
  - Duration_from_germination_to_reproductive_maturity: days from germination to first flower.
  - Height_at_reproductive_maturity: height in cm at first flowering.
  - Number_of_flowers_at_reproductive_maturity: count of flowers at maturity.
  - Number_of_buds_at_reproductive_maturity: count of buds at maturity.
  - Total_biomass_at_reproductive_maturity: total biomass at maturity (described as number of flowers and buds).
- Data conventions:
  - NA is recorded where measures could not be obtained because seeds did not germinate.

## Data semantics and units
- Germination: binary indicator (yes/no).
- Duration: days.
- Height: centimeters.
- Counts: number of flowers, buds, and associated biomass at reproductive maturity.

## Provenance and supporting documentation
- The dataset was created as part of a broader investigation into pollination services and floral resources.
- Supporting document: Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants.
- All data were collected and interpreted by Evans, T.M.

## Data quality and governance considerations
- Completeness: dataset described as complete; includes explicit NA entries for seeds that did not germinate.
- Metadata clarity: explicit column definitions align with common plant fitness metrics, enabling reuse and integration with related datasets.
- Scope: limited to a controlled glasshouse experiment on a single species, which should be considered when generalizing findings.

## Data stewardship implications
- Storage and discoverability: single CSV file with clear, field-level metadata; easy to upload to data portals and catalogue with dataset holdings.
- Standards and interoperability: consistent naming and units across fields; consider aligning with broader metadata schemas (e.g., including collection date, location, and accession details if expanding the dataset).
- Update and governance: dataset appears complete; if expanded, maintain versioning and document any additional cross-referenced experiments (e.g., linkage to the larger study on pollination services).
- Data use guidance for users: the dataset provides readiness for analysis of germination outcomes, time-to-mertilization, and growth metrics by pollen parentage, enabling comparisons between selfed and outcrossed progeny.