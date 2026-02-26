# Experimental location and source site

- Objective and scope
  - Investigates growth and survival of Howea belmoreana (Hb) and Howea forsteriana (Hf) from six source sites on Lord Howe Island.
  - Assesses performance across soil types (calcareous vs. volcanic), soil treatments (sterilised vs. unsterilised), and drought vs. non-drought conditions.
  - Aims to generate comparable data across seed sources, species, and environmental conditions for monitoring and policy-relevant environmental health assessment.

- Experimental design
  - For each seed source site and species, 1000 seeds were planted.
  - Planting medium: boxes (60 cm x 30 cm x 30 cm) with 15 cm soil depth, lined with sealable bags.
  - Four soil conditions: calcareous sterilised, calcareous unsterilised, volcanic sterilised, volcanic unsterilised.
  - Five boxes per soil condition, with 50 seeds per box.
  - Randomized placement outdoors under shade; planting began September 2015.
  - In November 2016, surviving seedlings were potted into individual pots (12 cm x 6 cm x 6 cm) in the same soil type (unsterilised) and kept under shade with irrigation every three days.
  - In March 2018, half of the plants from each condition (by species, seed site, soil type) were assigned to drought treatment (no watering for two weeks); the other half continued with normal watering. Drought and non-drought groups were boxed in groups of 40 plants.

- Sites and soils
  - Seed sites (with abbreviations and locations):
    - Ba Bowker Avenue
    - Ff Far Flats
    - Gc Golf Course
    - Gf Grey Face
    - Mb Middle Beach
    - P Plantation
  - Soil types:
    - C Calcareous
    - V Volcanic
  - Seed sources include both Howea forsteriana (Hf) and Howea belmoreana (Hb).

- Species
  - Howea forsteriana (Hf)
  - Howea belmoreana (Hb)

- Planting, cultivation, and timing
  - 1000 seeds per seed site/species set planted September 2015.
  - Post-germination handling: seedlings moved to pots November 2016; stress treatments applied March 2018.
  - Drought treatment implemented for randomly assigned plants in March 2018.

- Phenotyping and measurements
  - Survival assessments at three time points:
    - November 2016 (14 months)
    - March 2018 (30 months, before drought)
    - May 2018 (32 months, after drought)
  - Growth measurements:
    - Plant height measured at November 2016 and May 2018 (cm; from ground to base of tallest leaf; accuracy 5 mm)
    - Leaf count recorded at November 2016 and May 2018 (including scars from abscised leaves)
  - Criteria for death: desiccated growing shoot

- Data structure and key variables
  - Box_code: Arbitrary box identifier
  - Seedling_code: Arbitrary seedling identifier (survived to November 2016)
  - alive_Nov2016 / alive_Mar2018 / alive_May2018: Survival status at the three time points (TRUE = alive, FALSE = dead)
  - height_Nov2016 / height_May2018: Plant height in cm at November 2016 and May 2018
  - N_leaves_Nov2016 / N_leaves_May2018: Number of leaves at November 2016 and May 2018
  - drought_treatment: N = non-drought, D = drought
  - soil_sterilisation: N = no, Y = yes
  - Seed site and Species: Coded fields for site and species (Ba, Ff, Gc, Gf, Mb, P; Hf; Hb)
  - Units: Plant height (cm)

- Additional notes on data coding
  - Seed site codes: Ba (Bowker Avenue), Ff (Far Flats), Gc (Golf Course), Gf (Grey Face), Mb (Middle Beach), P (Plantation)
  - Soil types: C (Calcareous), V (Volcanic)
  - Species codes: Hf (Howea forsteriana), Hb (Howea belmoreana)

- Relevance for monitoring and data governance
  - Comprehensive, multi-factor experimental design enabling cross-site, cross-species, and cross-environment comparisons.
  - Structured metadata and explicit coding for sites, soils, treatments, and timepoints supports traceability and reproducibility.
  - Randomization, replication (five boxes per condition), and clear measurement protocols align with rigorous data quality standards essential for monitoring frameworks.