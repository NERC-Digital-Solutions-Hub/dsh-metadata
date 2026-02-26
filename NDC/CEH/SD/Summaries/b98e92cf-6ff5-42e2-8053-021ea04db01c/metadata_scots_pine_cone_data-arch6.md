# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

- Location and scope
  - Data from one site of a long-term multisite provenance-progeny trial in the Scottish Borders (lat 55.603625, lon -2.893025).
  - Seeds collected in March 2007 from eight mother trees for each of 21 native Scots pine populations, selected to cover the species’ full Scottish range with three populations per seed zone.
  - Saplings planted in the trial site in 2012 after germination and growth at the James Hutton Institute, Aberdeen.

- Experimental design
  - Trees from the same mother tree are treated as half-siblings (a family).
  - Complete randomized block structure: four blocks of eight rows; 3 m x 3 m spacing; guard row to protect from edge effects.
  - Total: 672 trees from 168 families, with four replicates per family; each block contains one family replicate.

- Data collection timeline and process
  - Cone abundance: counted on the southern-facing half of each tree in February 2024.
  - Cone sampling: five cones per tree from previous-year whorl branches; prioritised from the southern-facing half, but if fewer than five cones were present, cones were sampled from anywhere on the tree. Samples taken from different branches up to 3 m height.
  - Storage: cones stored at 4°C at the UK Centre for Ecology & Hydrology (Penicuik).
  - Trait measurement window: May–July 2024.
  - Cone trait measurements: cone length, cone width, stalk length, scale length, cone ratio, cone angle, colour (via Munsell), and profile (scale flatness: 1–4). Measurements performed with digital calipers; colour assessed with Munsell charts.
  - Seed trait measurements: conducted for seven populations (one from each seed zone) due to time constraints. Traits include seed_number, filled_seed_number, seed_viability (seed_number as total seeds per cone; filled_seed_number as filled seeds per cone; seed_viability = filled/total).

- Data and file structure
  - Single dataset: Scots_pine_cone_data.csv.
  - Columns describe: order, block, tree ID, family code, cone-specific identifiers, cone measurements (length, width, stalk length, scale length/width, scale number, cone_ratio, cone_angle), colour measurements (Hue, Value, Chroma), profile (1–4), openness (1–4 for cone openness after drying), seed measurements (seed_number, filled_seed_number, seed_viability), date of collection, and cone_id; units provided where applicable.
  - Data notes: some fields are NA (e.g., Hue/Value/Chroma), date fields may be NA in places; seed trait measurements limited to seven populations due to time constraints.
  - Reference for the trial and phenotypic trait context: Beaton et al. 2022, Sci Data.

- Location details
  - Site coordinates provided in the description; precise collection and storage locations noted (Penicuik, 4°C).

- Potential uses and context
  - Provides phenotypic data on cone and seed traits across multiple populations and seed zones within a long-term provenance-progeny framework.
  - Enables analyses of variation in cone morphology, colour, scaling, openness, and seed metrics, and their relation to population origin and family structure.
  - Useful for comparative studies within forestry genetics, phenotypic trait variation, and data products for exploring trait distributions across Scots pine populations.

- References
  - Beaton, J., Perry, A., Cottrell, J., Iason, G., Stockan, J., Cavers, S. (2022). Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Sci Data. 9, 671.