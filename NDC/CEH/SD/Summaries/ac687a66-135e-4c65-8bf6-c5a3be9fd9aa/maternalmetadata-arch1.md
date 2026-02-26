# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

- Overview
  - Dataset of phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
  - Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
  - Aims to capture maternal effects and provide data for analyses of phenotypic variation across populations and environments.

- Sampling design
  - Ten seed trees sampled from each population (21 populations total = 210 mother trees).
  - Sampling around a central tree within a circle ~1 km in diameter, using nine random-direction points.
  - Stratified sampling by distance from the central point in ratio 1:3:5 to cover the area without oversampling near the center.
  - For smaller woodland fragments or few cone-bearing trees, directions maintained to ensure wide coverage; inter-tree distances never closer than 50 m.

- Measurements and traits (mother trees)
  - For each mother tree: height and diameter at breast height (DBH) measured.
  - Ten cones collected and analyzed per mother tree to control for maternal effects in progeny measurements.
  - Mean values for each mother tree across the 10 cones recorded.

- Cone and seed measurements
  - Cone traits (per cone): width (Wi), length (Le), weight (We).
  - Seed metrics per cone: total seeds (SN), percentage viable seeds (SV), weight of all viable seeds (SW).
  - Post-drying cone weight recorded; viability defined as seeds with a wing and an obvious seed.

- Data files and structure
  - Two main files: MotherTraits.txt and ConeSeedTraits.txt.
  - Common columns across files include:
    - PopulationCode: population identifier.
    - Family: ID of the mother tree (corresponds to a unique family code; multiple cones per family).
    - Population: full population name.
    - SeedZone: Scots pine seed zone (e.g., EC: east central; N: north; NC: north central; NE: north east; NW: north west; SC: south central; SW: south west).
    - Latitude/Longitude: geographic coordinates of the population.
  - MotherTraits.txt (per mother tree): PopulationCode, Family, Population, SeedZone, Latitude, Longitude, Aspect, Slope, Altitude, Regeneration, SoilDepth, SoilMoisture, Competition, HA (Height of mother tree), DA (Diameter at breast height).
  - ConeSeedTraits.txt (per cone): PopulationCode, Family, Population, SeedZone, Cone (1–10), Wi (cone width), Le (cone length), We (cone weight), SN (seed count), SV (seed viability percentage), SW (weight of viable seeds).

- Population and environmental context
  - Populations span Scotland’s native range and include three populations from each of seven seed zones.
  - Site coordinates and environmental descriptors (aspect, slope, altitude, soil depth/moisture, regeneration) accompany the phenotype data to support environmental correlation analyses.

- Intended analyses and uses for Analysts
  - Explore correlations between mother-tree traits (e.g., HA, DA) and cone/seed phenotypes (Wi, Le, We, SN, SV, SW).
  - Assess geographic and environmental influences on phenotypic variation across populations (SeedZone, latitude/longitude, altitude, soil characteristics).
  - Develop predictive models linking maternal traits to progeny seed characteristics, and compare across the three garden/site contexts.
  - Unify and transform data for downstream analyses, aggregate cone-level data to mother-tree-level summaries, and track data provenance for reproducibility.

- Practical considerations for use
  - Data captured in 2007 (sampling date March 2007) by the James Hutton Institute, Aberdeen.
  - Data are organized to support cross-population comparisons and maternal-effect disentanglement in a long-term common garden framework.
  - Units and data structure are described in the metadata; attention to PopulationCode/Famil y mappings is essential when merging with spatial or environmental datasets.