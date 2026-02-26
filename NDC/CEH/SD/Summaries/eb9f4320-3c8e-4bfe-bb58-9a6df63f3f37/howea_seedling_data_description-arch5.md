# Experimental location and source site

- Seeds of Howea belmoreana and Howea forsteriana collected from six sites across Lord Howe Island.
  - Howea forsteriana: Bowker Avenue (Ba), Far Flats (Ff), Grey Face (Gf), Middle Beach (Mb), Plantation (P); coordinates provided for each site.
  - Howea belmoreana: Far Flats (Ff) and Golf Course (Gc); coordinates provided for each site.
- Calcareous soil collected from Ned's Beach and volcanic soil from Salmon Beach.
- Experimental work conducted at the Lord Howe Island Nursery (lat -31.525, long 159.067).

# Experimental design

- For each seed set (a single source site and species), 1000 seeds planted.
- Planting setup: boxes 60 cm x 30 cm x 30 cm; soil depth 15 cm; four soil conditions created by combining soil type (calcareous or volcanic) with sterilisation status (sterilised or unsterilised).
  - Four soil conditions: calcareous sterilised, calcareous unsterilised, volcanic sterilised, volcanic unsterilised.
- Replication: five boxes per soil condition with 50 seeds per box.
- Randomization: boxes placed in a random outdoor order under shade.
- Planting date: September 2015.
- Post-germination: November 2016, all surviving seedlings transplanted into individual pots (12 cm x 6 cm x 6 cm) in the same soil type (unsterilised), outdoors under shade, watered every three days.

# Phenotyping and measurements

- Survival assessments at three time points:
  - November 2016 (14 months)
  - March 2018 (30 months, before drought treatment)
  - May 2018 (32 months, after drought treatment)
- Growth measurements:
  - Plant height measured at 14 months and 32 months with a ruler (accuracy 5 mm), from ground to base of tallest leaf.
  - Leaf number counted at 14 months and 32 months, including leaf scars from abscised leaves.
- Drought treatment:
  - March 2018: randomly designated half of plants from each condition to drought (no watering for two weeks); the other half continued regular watering.
  - Drought and non-drought plants maintained in boxes of 40 plants each, with checkerboard arrangement for drought vs non-drought.
- Definitions:
  - Alive status tracked as TRUE/FALSE at each time point.
  - Plants considered dead if the growing shoot was completely desiccated.

# Data fields and coding

- Seed site codes:
  - Ba: Bowker Avenue
  - Ff: Far flats
  - Gc: Golf course
  - Gf: Grey face
  - Mb: Middle beach
  - P: Plantation
- Soil type codes:
  - C: Calcareous
  - V: Volcanic
- Species codes:
  - Hf: Howea forsteriana
  - Hb: Howea belmoreana
- Data columns (examples):
  - Box_code: arbitrary box identifier
  - Seedling_code: arbitrary seedling identifier (survived to November 2016)
  - alive_Nov2016 / alive_Mar2018 / alive_May2018: TRUE/FALSE for survival at the three time points
  - height_Nov2016 / height_May2018: plant height in cm at the two time points
  - N_leaves_Nov2016 / N_leaves_May2018: leaf counts at the two time points
  - drought_treatment: N (non-drought) or D (drought)
  - soil_sterilisation: N (no) or Y (yes)
- Units: Height in centimeters (cm)

# Data governance and stewardship considerations

- Provenance and metadata to capture:
  - Source site, seed species, soil type, sterilisation status, box and seedling identifiers.
  - Planting date, germination status, transplantation details, watering regime, and drought treatment.
  - Measurement protocols (height measurement method and accuracy, leaf counting method) and timepoints.
- Data quality and integrity:
  - Ensure consistent coding for seed sites, soils, and species; validate timepoints and corresponding measurements.
  - Track missing data (NA) and clearly document any non-applicable fields.
  - Verify alignment of soil type with sterilisation flag and drought treatment groupings.
- Data structure and interoperability:
  - Provide a data dictionary and controlled vocabularies for codes (Ba, Ff, Gc, Gf, Mb, P; C, V; Hf, Hb; TRUE/FALSE; N/Y, N/D).
  - Consider versioning and attachment of the experimental protocol to enable reproducibility.
- Data accessibility and reuse:
  - Ensure dataset is discoverable with provenance details (locations, soils, species, treatment) and measurement definitions.
  - If sharing beyond the originating organization, specify data licensing, access controls, and any embargoes.
- Potential challenges for data stewards:
  - Incomplete understanding of user needs for downstream analyses.
  - Timely acquisition of data across multiple timepoints and treatment groups.
  - Harmonizing data from multiple systems or formats if integrated with other datasets.
  - Handling large, multi-factor experimental data and potential legacy database compatibility.