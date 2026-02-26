# Experimental location and source site

- Purpose and scope
  - A controlled study to assess Howea seedling survival and growth under different soil conditions (calcareous vs volcanic), soil sterilisation status, and drought treatment, using seeds from multiple field sites on Lord Howe Island.
  - Aimed at generating standardized, comparable data across species, sites, and environmental treatments suitable for long-term environmental monitoring.

- Experimental location and seed sources
  - Seeds of Howea belmoreana (Hb) and Howea forsteriana (Hf) collected from six Lord Howe Island sites:
    - Hf: Bowker Avenue (Ba), Far Flats (Ff), Grey Face (Gc), Middle Beach (Mb), Plantation (P)
    - Hb: Far Flats (Ff) and Golf Course (Gc)
  - Calcareous soil from Ned's Beach; volcanic soil from Salmon Beach.
  - Experiment conducted at the Lord Howe Island Nursery.

- Experimental design
  - For each species-source combination, 1000 seeds planted.
  - Boxes: 60 cm x 30 cm x 30 cm, lined with sealable bags filled to 15 cm depth.
  - Soil conditions: calcareous and volcanic soils, each in sterilised and unsterilised forms, yielding four conditions:
    - Calcareous sterilised
    - Calcareous unsterilised
    - Volcanic sterilised
    - Volcanic unsterilised
  - Replication: five boxes per soil condition, 50 seeds per box.
  - Setup: boxes placed outdoors in random order under shade; planting date September 2015.
  - 2016 transfers: November 2016, surviving seedlings potted into individual pots (12 cm x 6 cm x 6 cm) in the same soil type (unsterilised); maintained under shade, watered every three days.
  - Drought treatment: March 2018, randomly assigned half of the plants in each condition to drought (no watering for two weeks) and the other half to normal watering; plants organized into drought and non-drought boxes of 40 with checkerboard randomization.

- Phenotyping and timepoints
  - Survival measurements at three timepoints:
    - November 2016 (14 months)
    - March 2018 (30 months, before drought)
    - May 2018 (32 months, after drought)
  - Growth measurements:
    - Plant height and leaf number at 14 months and 32 months
    - Height measured in cm to 5 mm accuracy; leaves counted including scars from abscised leaves
  - Death criteria: plant dead when the growing shoot is completely desiccated.

- Data structure and metadata
  - Key fields:
    - Box_code (arbitrary box name)
    - Seedling code (arbitrary seedling identifier for survivors as of Nov 2016)
    - alive_Nov2016 / alive_Mar2018 / alive_May2018 (TRUE = alive, FALSE = dead)
    - height_Nov2016 / height_May2018 (cm)
    - N_leaves_Nov2016 / N_leaves_May2018
    - drought_treatment (N = non-drought, D = drought)
    - soil_sterilisation (N = no, Y = yes)
  - Seed site codes:
    - Ba Bowker Avenue
    - Ff Far Flats
    - Gc Golf Course
    - Gf Grey Face
    - Mb Middle Beach
    - P Plantation
  - Soil type codes:
    - C Calcareous
    - V Volcanic
  - Species codes:
    - Hf Howea forsteriana
    - Hb Howea belmoreana
  - Units:
    - Plant height (cm)

- Additional notes
  - Data interpretation relies on longitudinal tracking across timepoints and conditions to assess resilience to drought and the influence of soil type and sterilisation on survival and growth for each species-site combination.  
  - The dataset is organized to support cross-factor analyses and can be integrated with broader environmental monitoring datasets for island plant health and adaptation studies.