# Soil sampling

## Purpose and scope
- Document describes methods for collecting and processing soil samples to analyze bulk density, carbon, and nitrogen, with outputs suitable for data analysis and reporting.

## Sampling and preparation
- Two soil samples taken per site using a 4 cm width auger, as deep as possible.
- Soil passed through a 2 mm sieve to remove stones and roots.
- Stones retained weighed to determine gravel and chalk flint content.
- Soil cores divided into 5 cm depth increments; dried at 80°C for 48 hours after sieving.
- Samples stored at 25°C until processing.

## Bulk density
- Bulk density (BD) calculated as mass/volume.
- BD adjusted for gravel content using: Adjusted BD = (unadjusted BD) × (100 − % gravel) / 100.

## Carbon and nitrogen analysis
- Each depth fraction ground in a ball mill (25 s⁻¹ for 2 minutes).
- Carbonates removed with 10% HCl until effervescence ceases; samples redried.
- About 10 ± 0.5 mg used for combustion analysis with an Elementar Vario EL instrument; calibrated with acetanilide standard (10.45% N, 71.4% C).
- Carbon and nitrogen stocks calculated per depth from core depth, corrected BD, and measured C and N percentages after acid treatment.

## Quality control
- Standards and blanks run every 20 samples on the combustion analyser.
- 5% analytical replicates included to ensure data reliability.

## Data products and data dictionary
- Primary data file: Soil_C_budgets_to_depth.csv
- Data fields and definitions:
  - Land Use: Land use type
  - Site: Site identifier
  - Replicate: Replicate (1 or 2)
  - Soil level: Where the soil was taken from (top, middle, bottom)
  - Soil Depth from surface: Depth from surface (5 cm increments where possible)
  - Core depth: Length of the core
  - Core diameter: Diameter of the auger
  - Core volume: Overall volume (pi r^2 x h)
  - Dry wt: Soil weight of this increment
  - Gravel wt: Weight of stones >2 cm
  - %gravel: Proportion of core occupied by gravel
  - Bulk density with gravel: mass/volume including gravel
  - BD corrected for gravel: BD with gravel subtracted from the calculation
  - N post acid: Total nitrogen after acid treatment
  - C post acid: Total carbon after acid treatment
  - C t ha: Carbon stock in tonnes per hectare
  - N t ha: Nitrogen stock in tonnes per hectare
  - CN post acid: Carbon-to-nitrogen ratio after acid treatment

## Notes for data use
- The dataset enables depth-resolved carbon and nitrogen stock estimations and supports self-serve analysis through calculated stocks and related metadata.
- Data definitions emphasize units and measurement context to support consistent aggregation and comparison across sites.