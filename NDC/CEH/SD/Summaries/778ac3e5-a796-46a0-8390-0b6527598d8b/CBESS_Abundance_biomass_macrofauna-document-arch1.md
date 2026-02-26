# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) mobile macrofaunal abundance, biomass and species richness from Fyke netting in mudflat habitats.

- Overview
  - Dataset capturing abundance, biomass, and species richness of larger mobile macrofauna using fyke netting on mudflat habitats.
  - Focuses on Essex and Morecambe Bay sites, with field campaigns conducted in Winter and Summer 2013.
  - Staff: Mark Emmerson.

- Locations and habitat context
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Geographic coordinates provided for each site.
  - Habitat descriptions: Essex mudflats are cohesive clays/mud/silt within protected estuarine sites; Morecambe mudflats dominated by coarse, mobile sediments with greater tidal ranges and exposure.

- Sampling and field methods
  - Target taxa: larger mobile macrofauna.
  - Equipment: five double hoop fyke nets (mesh 22 mm, 8 m leader, 0.5 m hoop).
  - Deployment: nets positioned at the outer edge of each quadrat; deployed over two executive tidal cycles; catches processed the following day.
  - Measurements per deployment: abundance (count), biomass (wet weight in g) by species, and species richness (number of species caught).
  - Sampling timeframe: Winter and Summer 2013 as part of a general field campaign.

- Data structure and variables
  - Data format: Excel workbook; NA cells indicate no data.
  - Core fields (examples):
    - Row Number: sortable index.
    - Season: Winter (W) or Summer (S).
    - Location: Morecambe (M) or Essex (E).
    - Site: Morecambe (CS, WS, WP) or Essex (AH, FW, TM).
    - Habitat: Mudflat (MF).
    - Quadrat Number: 1 to 22.
    - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - Taxa and metrics (per fyke net deployment):
    - Abundance for specific species (e.g., Carcinus maenas_A, Clupea harengus_A, Crangon crangon_A, Anguilla anguilla_A, Pollachius virens_A, Dicentrarchus labrax_A, Pomatoschistus sp_A, Asterias rubens_A, etc.).
    - Biomass for corresponding species (e.g., Platichthys flesus_B, Carcinus maenas_B, Clupea harengus_B, Crangon crangon_B, Anguilla anguilla_B, Pollachius virens_B, Dicentrarchus labrax_B, Pomatoschistus sp_B, etc.) measured as total wet weight in grams.
    - Species richness: number of species caught per deployment.
  - Notes: Some fields reflect species-specific abundance and biomass entries; data include a mix of fish, crustaceans, and echinoderms.

- Data quality, provenance, and handling
  - Observations and measurements were cross-checked against field/lab notebooks after digitization.
  - Data are organized to track season, location, site, quadrat, and scale to support analyses across space and time.
  - The dataset provides granular, deployment-level observations suitable for calculating per-net metrics and aggregating by site, season, or habitat.