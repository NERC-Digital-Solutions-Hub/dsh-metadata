# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

- Overview
  - Dataset records macrofaunal abundance (individuals per m²) across mudflat and saltmarsh habitats.
  - 6 sites across 2 locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
  - Sampling conducted in winter and summer 2013 as part of the CBESS field campaign; no planned repeats.
  - Each site includes both habitats; 3 replicates across 22 quadrats at 4 spatial scales.
  - Staff responsible: Christina Wood and Martin Solan.

- Location and habitat detail
  - Essex sites represent saltmarsh and mudflat with cohesive clays and sandy sediments, differing inundation, creek structure, and vegetation.
  - Morecambe Bay sites represented by sandy soils (saltmarsh) and mudflat conditions dominated by coarse, mobile sediments.
  - Precise site coordinates provided for each location.

- Sampling design and temporal coverage
  - Winter and summer 2013 sampling under the CBESS field campaign.
  - 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter) for sediment sampling.
  - 22 quadrats across 6 sites, across 4 spatial scales (A, B, Replicate categories) to capture multi-scale variability.

- Observed variables and data processing
  - Primary variable: Species abundance (number of individuals per m²) for macrofauna.
  - Taxa observed include numerous invertebrates (e.g., Arenicola marina, Capitella sp., Hediste diversicolor, Macoma balthica, Crangon crangon, Mytilus edulis juvenile, and many others) plus debris categories (annelid, mollusc, crustacea, etc.).
  - Observational procedure: 3 cores per quadrat, fixed in formalin, sieved, preserved, and organisms identified to species level (or appropriate taxon) and counted.
  - Abundances converted to per m² using a multiplier (127.323955) and rounded to the nearest whole individual.
  - Data checked against biomass data file (CBESS_macrofauna_biomass.csv) to ensure consistency; species names validated against the World Register of Marine Species (WoRMS).

- Data structure and formats
  - File format: CSV.
  - Dataset Field descriptions cover: season (Winter/Summer), location (Essex/Morecambe), site codes (AH, FW, TM, CS, WS, etc.), habitat (Mudflat, Saltmarsh), quadrat and scale identifiers, replicate designations, measurement type (macrofauna abundance), and per-species abundance values.
  - Includes presence/absence markers for debris and a wide range of taxa (both major groups and specific species) alongside detailed metadata fields to sort and interpret data.

- Quality control and governance
  - Data entry performed by two people with double checking at input.
  - Abundance data cross-validated against biomass dataset to ensure integrity.
  - Species nomenclature aligned with WoRMS to maintain taxonomic consistency.
  - Metadata captures site characteristics, habitat contrasts, and sampling methodology to support reproducibility and reuse.

- Practical considerations for data leaders
  - Useful for multi-site, multi-habitat comparisons of macrofaunal community structure and density within coastal ecosystems.
  - Rich taxonomic detail enables diversity and community composition analyses across spatial scales and seasons.
  - The explicit conversion and quality checks support reliable aggregation to per-square-meter metrics and cross-dataset integration.
  - Metadata provides clear context on habitat differences, sediment types, and inundation regimes, aiding transferability to other coastal systems.

- Contact and provenance
  - Staff responsible: Christina Wood and Martin Solan.
  - Data aligned with CBESS project standards and integrated with supplementary biomass data for quality assurance.