# Soil sampling

- Two soil samples were taken per site using a 4 cm width auger, as deep as possible.
- Soil was passed through a sieve with 2 mm aperture to remove stones and roots.
- Stones retained were weighed to determine the proportion of gravel and chalk flints in the sample.
- Soil cores were split into 5 cm depth increments, dried at 80 °C for 48 hours after sieving.
- Samples were stored at 25 °C until processing.

## Bulk density

- Soil was weighed and bulk density (BD) calculated as mass/volume.
- BD adjusted for gravel incursions using:
  Adjusted BD = (unadjusted BD) / 100 × (100 − % gravel)

## Carbon and nitrogen analysis

- Each depth fraction was ground with a ball mill at 25 s−1 for two minutes.
- Samples treated with 10% HCl to dissolve carbonates from chalk via dropwise addition until effervescence ceased.
- Samples redried and ~10 ± 0.5 mg used for combustion analysis.
- Analysis performed with an Elementar Vario EL combustion analyser, calibrated with an acetanilide standard (10.45% N, 71.4% C).
- Carbon and nitrogen stocks calculated for each soil depth using:
  C_t ha = 100 × (core depth / 100) × corrected BD × raw C%
  N_t ha = 100 × (core depth / 100) × corrected BD × raw N%
  (where stock represents carbon or nitrogen in tonnes per hectare).

## Quality control

- Standards and blanks run every 20 samples on the combustion analyser.
- 5% analytical replicates included.

## Soil_C_budgets_to_depth.csv (data structure and definitions)

- Land Use: Land use type.
- Site: Site identifier.
- Replicate: Replicate (1 or 2).
- Soil level: Where the soil was taken from (top, middle, or bottom of the column).
- Soil Depth from surface: Depth from the surface at which the soil was collected (in 5 cm increments where possible).
- Core depth: Length of the core (not always possible to cut into 5 cm sections).
- Core diameter: Diameter of the auger used to dig the soil.
- Core volume: Overall volume (π r^2 h).
- Dry wt: Soil weight of this increment.
- Gravel wt: Weight of stones in soil > 2 cm diameter.
- %gravel: Percentage of the core comprised of gravel.
- Bulk density with gravel: Mass/volume including gravel.
- BD corrected for gravel: Mass/volume of soil excluding gravel (BD adjusted by subtracting gravel fraction).
- N post acid: Total nitrogen after acid treatment to remove carbonates.
- C post acid: Total carbon after acid treatment to remove carbonates.
- C t ha: Carbon in tonnes per hectare.
- N t ha: Nitrogen in tonnes per hectare.
- CN post acid: Carbon-to-nitrogen ratio after carbonate removal.