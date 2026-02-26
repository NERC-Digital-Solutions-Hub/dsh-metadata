# Experimental location and source site

- Seeds collected from six sites on Lord Howe Island for two species:
  - Howea forsteriana (Hf): Bowker Avenue (Ba), Far Flats (Ff), Grey Face (Gf), Middle Beach (Mb), Plantation (P)
  - Howea belmoreana (Hb): Far Flats (Ff), Golf Course (Gc)
- Soil types used: calcareous (C) and volcanic (V)
  - Calcareous soil collected from Ned's Beach
  - Volcanic soil collected from Salmon Beach
- Experimental location: Lord Howe Island Nursery (coordinates provided in the text)

## Experimental design

- For each seed source site and species, 1000 seeds were planted
- Four soil conditions per seed set:
  - Calcareous sterilised
  - Calcareous unsterilised
  - Volcanic sterilised
  - Volcanic unsterilised
- For each soil condition: 5 boxes, each with 50 seeds
- Boxes placed in random order outdoors under shade
- Planting date: September 2015
- Post-germination: November 2016, surviving seedlings potted individually (12 cm × 6 cm × 6 cm) in the same soil type (all unsterilised), then kept outside under shade and watered every three days
- Drought treatment (March 2018):
  - Randomly designated half of plants from each condition to drought; two weeks without watering for the drought group
  - Drought and non-drought plants were organized into boxes with 40 plants each, arranged in a checkerboard pattern

## Phenotyping and measurements

- Survival recorded at three time points:
  - November 2016 (14 months after planting)
  - March 2018 (30 months, before drought)
  - May 2018 (32 months, after drought)
- Morphometrics:
  - Plant height: measured at November 2016 and May 2018 (from ground to base of tallest leaf), accuracy 5 mm
  - Leaf number: counted at November 2016 and May 2018 (including leaf scars)
- Death criteria: plant considered dead if the growing shoot was completely desiccated

## Data and variable details

- Seed sites (codes and full names):
  - Ba: Bowker Avenue
  - Ff: Far Flats
  - Gc: Golf Course
  - Gf: Grey Face
  - Mb: Middle Beach
  - P: Plantation
- Soil types:
  - C: Calcareous
  - V: Volcanic
- Species:
  - Hf: Howea forsteriana
  - Hb: Howea belmoreana
- Data columns and codes:
  - Box_code: arbitrary box identifier
  - Seedling code: arbitrary seedling identifier (survived to November 2016)
  - alive_Nov2016/Mar2018/May2018: whether the seedling was alive at the respective time points (TRUE = alive, FALSE = dead)
  - height_Nov2016/May2018: height in cm at the respective time points
  - N_leaves_Nov2016/May2018: number of leaves at the respective time points
  - drought_treatment: N = non-drought, D = drought
  - soil_sterilisation: N = unsterilised, Y = sterilised

- Units: height in centimeters
- Additional notes:
  - NA indicates not applicable or missing data
  - The dataset includes a structured linkage between seed source, species, soil condition, drought treatment, and longitudinal survival and growth metrics