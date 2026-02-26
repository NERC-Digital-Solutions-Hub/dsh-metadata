# Experimental location and source site

- Scope: Study of Howea belmoreana (Hb) and Howea forsteriana (Hf) seeds collected from six Lord Howe Island sites, with experiments on growth, survival, and morphology under different soil types and moisture regimes.
- Seed sources:
  - Hf: Bowker Avenue (Ba), Far Flats (Ff), Grey Face (Gc), Middle Beach (Mb), Plantation (P)
  - Hb: Far Flats (Ff), Golf Course (Gc)
- Soil types and collection sites:
  - Calcareous (C): Ned's Beach
  - Volcanic (V): Salmon Beach
- Experimental location: Lord Howe Island Nursery (LHIN)

- Research design overview:
  - For each combination of species and seed site, 1000 seeds were planted.
  - Four soil conditions: calcareous sterilised (CY), calcareous unsterilised (CN), volcanic sterilised (VY), volcanic unsterilised (VN).
  - Each seed-set and soil condition had five boxes with 50 seeds per box (total replication per condition).
  - Planting date: September 2015.
  - Boxes were randomly ordered outdoors under shade.

- Plant propagation and maintenance:
  - November 2016: germinated seedlings surviving to date potted individually (12 cm x 6 cm x 6 cm) in the same soil type, unsterilised; grown outdoors under shade with watering every three days.
  - March 2018: a randomly designated half of the plants from each condition (species x seed site x soil condition) subjected to drought (no watering for two weeks); the other half remained well-watered.
  - Drought and non-drought plants were kept in boxes; each box contained 40 plants and boxes were arranged in a checkerboard pattern.

- Phenotyping and data collection:
  - Survival assessments at three time points:
    - November 2016 (14 months)
    - March 2018 (30 months, before drought treatment)
    - May 2018 (32 months, after drought treatment)
  - Morphometrics:
    - Height measured at 14 and 32 months (distance from ground to base of tallest leaf; precision to 5 mm)
    - Leaf number counted at 14 and 32 months (including leaf scars from abscised leaves)
  - Criteria: plants considered dead if the growing shoot was completely desiccated.

- Data and variable schema (as described in the dataset):
  - Seed site codes: Ba (Bowker Avenue), Ff (Far Flats), Gc (Golf Course), Gf (Grey Face), Mb (Middle Beach), P (Plantation)
  - Soil types: C (Calcareous), V (Volcanic)
  - Species: Hf (Howea forsteriana), Hb (Howea belmoreana)
  - Key data fields:
    - Box_code (arbitrary box identifier)
    - Seedling_code (identifier for each surviving seedling as of Nov 2016)
    - alive_Nov2016 / alive_Mar2018 / alive_May2018 (TRUE = alive, FALSE = dead)
    - height_Nov2016 / height_May2018 (cm, measured height)
    - N_leaves_Nov2016 / N_leaves_May2018 (number of leaves)
    - drought_treatment (N = non-drought, D = drought)
    - soil_sterilisation (N = no, Y = yes)
  - Additional notes on data: There is an explicit data dictionary and abbreviations explanation to support data discoverability and reuse.