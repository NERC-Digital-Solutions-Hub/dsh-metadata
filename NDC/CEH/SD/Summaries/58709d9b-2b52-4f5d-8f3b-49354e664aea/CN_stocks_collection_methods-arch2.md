# Soil_C_budgets_to_depth.csv

## Purpose and scope
- Provides per-depth soil carbon and nitrogen stocks (tonnes per hectare) by site and land-use type.
- Supports standardized environmental monitoring and policy performance assessment over time.
- Uses a defined sampling, analysis, and data-definition workflow to enable cross-site comparisons and data reuse.

## Sampling procedure
- Two soil samples per site collected with a 4 cm width auger, taken as deep as possible.
- Samples passed through a 2 mm sieve to remove stones and roots.
- Stones weighed to determine the proportion of gravel and chalk flints.
- Soil cores divided into 5 cm depth increments, dried at 80 °C for 48 hours after sieving.
- Cores stored at 25 °C until processing.

## Bulk density (BD)
- BD calculated as mass/volume from the weighed soil sample.
- BD adjusted for gravel using: Adjusted BD = unadjusted BD × (100 − % gravel) / 100.

## Carbon and nitrogen analysis
- Each depth fraction ground in a ball mill (25 s^-1, 2 minutes).
- Carbonates dissolved with 10% HCl (dropwise until effervescence ceases) to remove chalk carbonates.
- Samples redried; 10 ± 0.5 mg weighed for combustion analysis.
- Measured with an Elementar vario EL combustion analyser, calibrated with acetanilide standard (10.45% N, 71.4% C).
- Stocks calculated per depth using the depth, corrected BD, and measured carbon and nitrogen percentages.

## Stock calculations
- Carbon and nitrogen stocks per depth are derived from core depth, corrected bulk density, and %C/%N post-acid treatment.
- Stocks expressed as tonnes per hectare.

## Quality control
- Standards and blanks run every 20 samples on the combustion analyser.
- 5% analytical replicates included to assess precision.

## Data schema: Soil_C_budgets_to_depth.csv
- Land Use: Land use type.
- Site: Site identifier.
- Replicate: Replicate (1 or 2).
- Soil level: Top, middle, or bottom of the soil column.
- Soil Depth from surface: Depth from surface where soil was sampled (in 5 cm increments where possible).
- Core depth: Length of the core (depth actually sampled).
- Core diameter: Diameter of the auger used.
- Core volume: Overall core volume (pi r^2 h).
- Dry wt: Soil weight for this increment.
- Gravel wt: Weight of stones >2 cm diameter.
- %gravel: Percentage of core occupied by gravel.
- Bulk density with gravel: Mass/volume including gravel.
- BD corrected for gravel: Mass/volume of soil excluding gravel.
- N post acid: Total nitrogen after acid treatment.
- C post acid: Total carbon after acid treatment.
- C t ha: Carbon in tonnes per hectare.
- N t ha: Nitrogen in tonnes per hectare.
- CN post acid: Carbon-to-nitrogen ratio after carbonate removal.

## Data management and reuse
- Data documented with explicit definitions to ensure consistency and interoperability.
- Outputs are stored and uploaded to appropriate data portals to facilitate access for monitoring, analysis, and evidence-based decision-making.