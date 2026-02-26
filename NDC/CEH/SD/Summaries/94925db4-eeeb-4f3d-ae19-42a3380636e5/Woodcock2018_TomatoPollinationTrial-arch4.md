# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

- Authors and context
  - Woodcock, B.A. & Pywell, R.F. (NERC Centre for Ecology & Hydrology, UK)
  - Year: 2017; funded by CEH Commercial Innovation Fund (National Capability), Project NEC06344

- Dataset purpose and scope
  - Experimental test of potential over-yielding effects on fruit set and average fruit size in tomato plants
  - Three pollinator treatment combinations:
    - Bombus terrestris (B. terrestris) alone
    - Lasioglossum spp. alone
    - Additive combination of B. terrestris and Lasioglossum spp.
  - Field experiments conducted under controlled conditions to compare pollination effectiveness

- Experimental design and setting
  - Location: Earth Trust, Little Whittenham, UK (Latitude 51.633329, Longitude -1.1956796)
  - Setup: three 2 × 3 m net cages to hold free-flying bees
  - Pollinator sources:
    - B. terrestris: single 30–40 worker colony (commercial stock from Biobest Ltd)
    - Lasioglossum spp.: resident populations (L. malachurum and L. pauxillum) identified in the field
    - Treatment 3 included B. terrestris colony in cage with Lasioglossum nests
  - Density: approximate 4.2 nests m^-2 in Lasioglossum cages
  - Nectar provisioning: Asteraceae plants provided as a nectar source since tomato provides no nectar
  - Plant material: tomato cultivar ‘Moneymaker’; initial greenhouse-grown, pollinators excluded, then moved to field cages
  - Experimental exposure: 4 days per batch, with batches repeated four times
  - Replication: batches contained five plants per treatment, with two flowering stems per plant; one stem exposed to pollinators, the other kept as a non-pollinated control

- Measurements and outcomes
  - Primary outcomes: fruit set and fruit size
  - Assessment timing: when tomatoes reached deep red maturation
  - Per stem: up to five flowers assessed for fruit set; subsequent flowers were pinched off
  - Metrics recorded:
    - Number of fruits per stem (up to 5)
    - Individual fruit mass
    - Mass statistics and proportions for control (no bees) and exposed stems

- Data structure and metadata
  - Dataset: Woodcock2018_tomatoes.csv
  - Plant-level data describing fruit set and fruit size across pollinator treatments
  - Key fields (examples):
    - Unique_ID: individual tomato plant code
    - Treatment: Lasioglossum, Bombus, or Bombus_Lasiog (additive)
    - C_Flow_N, C_Flow_set, C_Prop_set, C_Mass_ave: control (no bees) flower counts, fruit set, and masses
    - T_Flow_N, T_Flow_set, T_Prop_set, T_Mass_ave: corresponding measures under bee exposure
    - C1_mass … C5_mass and T1_mass_mass … T5_mass_mass: masses of individual fruits (up to five per stem) under control and exposed conditions
  - Data types and units are defined (Discrete/Numerical, grams, proportions, etc.)
  - Temporal replication: four batches per treatment

- Time frame and references
  - Experimental period: April–June 2017
  - References supporting methods:
    - Dag A. (2008) Bee pollination in enclosures
    - Greenleaf S.S. & Kremen C. (2006) Wild bee species and tomato production

- Implications for data governance and reuse (Data Leaders perspective)
  - Rich, well-documented metadata and a detailed data dictionary facilitate discoverability, interpretability, and reuse
  - Clear description of experimental design, treatments, and replication supports comparability and meta-analyses
  - Explicit treatment definitions and measurement protocols aid data quality assessment and integration with other datasets
  - Provenance includes authors, funding, site coordinates, and dates, aiding data lineage and trust
  - Potential usability considerations:
    - Use of wild Lasioglossum populations introduces variability in species composition
    - Field cage constraints and specific crop and pollinator management practices may influence generalizability
    - Data model distinguishes control vs. pollinator-exposed outcomes, enabling contrasting analyses across treatments