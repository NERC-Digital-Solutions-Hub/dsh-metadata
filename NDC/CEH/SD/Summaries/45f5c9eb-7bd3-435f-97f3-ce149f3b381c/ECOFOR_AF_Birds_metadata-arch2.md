# BirdSpecies.csv

- Overview
  - BirdSpecies.csv contains bird survey data from 441 sampling points in the Atlantic Forest of Brazil.
  - Each point was surveyed four times between December 2015 and February 2017.
  - Part of the ECOFOR project (Biodiversity and Ecosystem Functioning in Degraded and Recovering Tropical Forests) within the NERC Human-Modified Tropical Forest programme.

- Sampling design
  - 441 sampling points across Vale do Paraíba and Serra do Mar, São Paulo, Brazil.
  - Points evenly spread across 49 landscapes using a nine-point regular grid with 75 m spacing (where landscape configuration allowed).
  - 15 landscapes: single predominant land-use type (controls), equally divided among native forest, Eucalyptus plantation, and pasture.
  - 34 landscapes: native forest fragments embedded in other land-use types.
  - Fragmented landscapes: three points in native forest fragment, three at fragment edge, three in surrounding matrix.
  - Matrix types surveyed: pasture (P) and plantation (E); 15 fragments border plantation, 19 border pasture; controls include CF, CP, CE landscape types representing different control configurations.

- Data collection techniques
  - Point counts with 15-minute duration, recording all bird species within a 25 m radius.
  - Four temporal replicates, evenly split between dry and wet seasons (Dec 2015–Feb 2017).

- Data structure and columns
  - Data stored in a single CSV file: BirdSpecies.csv; each row represents one sampling point.
  - Species columns (267 total, columns 1–267) contain counts indicating in how many replicates the species was detected, following BirdLife International taxonomy (BirdLife International 2017).
  - LandscapeID: numeric reference to the landscape containing the sample point.
  - HabitatType: I = native forest interior, E = native forest edge, M = matrix; codes indicate how points in control landscapes were aggregated into transects.
  - MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
  - X and Y: coordinates in SAD 1969 UTM 23S, rounded to the nearest kilometre to protect locations of rare/threatened species.

- Taxonomy and references
  - Species names follow BirdLife International taxonomy (BirdLife International 2017).
  - Reference: BirdLife International 2017 Handbook of the Birds of the World and BirdLife International digital checklist, Version 9.1.

- Context for monitoring and reuse
  - Dataset supports standardized monitoring across habitat types and landscapes to assess environmental health and policy-relevant biodiversity outcomes.
  - Designed for compatibility with broader environmental-monitoring workflows, enabling data QA, standardisation, and potential integration with other ecological data sources.
  - Coordinates and structure facilitate aggregation, spatial analyses, and temporal comparisons across seasons and landscape configurations.