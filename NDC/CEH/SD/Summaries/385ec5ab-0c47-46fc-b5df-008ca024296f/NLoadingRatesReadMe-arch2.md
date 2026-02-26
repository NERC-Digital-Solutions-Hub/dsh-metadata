# NLoadingRates.csv

- Project and provenance: Uplands-N2O, Grant NE/M015351/1. Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick. Data reuse should be fully cited.

- Data scope: Measurements from 2016 urine collection trials with Welsh Mountain ewes. Six replicate sheep housed in urine collection apparatus, fed either semi-improved pasture (spring, summer, autumn) or improved pasture (autumn).

- What the dataset provides:
  - Individual urine event volumes for each sheep
  - Individual urine nitrogen content per event (N in g N per L)
  - Theoretical urine patch area (PatchArea) based on predetermined wetted-area constants
  - Amount of nitrogen deposited in each theoretical urine patch (N_per_patch)
  - Nitrogen loading rate within each theoretical urine patch (N_LoadingRate)

- Key variables and units:
  - Sheep_No: identifier for each replicate sheep
  - Season: season data were collected in
  - Site: diet/pasture type (semi-improved or improved)
  - N: urine N content (g N L-1)
  - Vol: urine volume (L)
  - PatchArea: hypothetical urine patch area (ha)
  - N_per_patch: nitrogen deposited per patch (kg)
  - N_LoadingRate: nitrogen loading rate per patch (kg N ha-1)

- How PatchArea is derived:
  - Based on site-specific wetted-area assumptions: 17.5 L urine m-2 for semi-improved pasture and 8.9 L urine m-2 for improved pasture.

- Purpose and use for environmental monitoring:
  - Enables estimation of nitrogen loading from ruminant urine patches under different pasture systems
  - Supports standardized assessment of environmental nitrogen deposition and potential impact on upland ecosystems
  - Outputs (N_per_patch and N_LoadingRate) facilitate comparison across seasons and pasture types

- Data handling and reuse notes:
  - Data should be cited fully when reused
  - Datasets can be stored/uploaded to appropriate data portals as part of environmental monitoring outputs

- Contextual notes:
  - Study focus: upland pasture systems and nitrogen loading related to sheep urine
  - Timeframe: trials conducted in 2016
  - Audience: analysts monitoring environmental health and policy performance, with emphasis on consistent data formats and transparent provenance