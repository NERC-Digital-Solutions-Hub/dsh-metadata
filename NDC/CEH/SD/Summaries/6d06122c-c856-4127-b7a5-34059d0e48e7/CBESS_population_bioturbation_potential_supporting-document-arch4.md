# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) population bioturbation potential in mudflat and saltmarsh habitats..

- Overview
  - A dataset measuring population bioturbation potential (BPp) in mudflat and saltmarsh habitats, using CBESS field data.
  - Collected from 6 sites across 2 locations (Essex and Morecambe Bay) during winter and summer 2013.
  - Sampling design: 3 replicate cores per quadrat across 22 quadrats, at 4 spatial scales.
  - Staff: Christina Wood and Martin Solan.

- Data Scope and Content
  - Location/Habitat
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing cohesive clays/mud/silt in mudflats; saltmarsh with clay soils.
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) representing coarser sediments in mudflats; saltmarsh with sandy soils.
    - Saltmarsh regions differ in inundation, creek structure, and vegetation; mudflats differ in sediment type.
  - Sampling and Scale
    - General CBESS field campaign conducted in winter and summer 2013; no planned repeats.
    - 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter); fixed in 4% buffered formalin; organisms identified to species or appropriate taxon.
    - Abundance and biomass data collected; BPp calculated for each species and site.
    - 4 spatial scales (A–D) and 3 replicates per quadrat; 22 quadrats total.
  - Variables and Measurements
    - Primary variable: Population bioturbation potential BPp (per sample population).
    - Species-level BPp data for a wide list of macrofauna (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Mytilus edulis juvenile, Crangon crangon, etc.), plus major debris where applicable.
    - Additional fields describe location, site, season (Winter/W, Summer/S), scale, replicate, and measurement type.
  - Data Processing
    - BPp calculation: BPp = BPi × Ai
      - Ai = individual species abundance per m²
      - BPi = (√Bi) × Mi × Ri
        - Bi = biomass per m² for the species
        - Mi = mobility of the species
        - Ri = reworking ability of the species
    - Biomass and abundance derived from:
      - 3 cores per quadrat were processed; individuals counted and weighed (0.0001 g precision or 0.0001 g if too light).
      - Abundance to nearest whole individual; biomass to 0.0001 g.
      - A conversion factor of 127.323955 used to express results per m².
  - Data Quality and Validation
    - Raw data input by 2 people and double-checked at input.
    - Biomass data cross-validated against the abundance data (CBESS_macrofauna_abundance.csv).
    - BPp calculations double-checked.
  - File Formats and Access
    - Primary format: .csv
    - Indicator of data completeness via "NA" entries where data are not available.
    - Dataset Field Descriptions provided (extensive species- and field-level metadata).

- Data Structure and Metadata
  - Core fields include: Row Number, Season (Winter/Summer), Location (Morecambe/Essex), Site (CS, WS, AH, FW, TM), Quadrat Number, Scale (A–D), Replicate (1–3), Measurement Type (BPp).
  - Species-specific BPp columns are provided for a long list of taxa (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Mya arenaria, Crangon crangon, Ampharete spp., etc.).
  - Additional fields capture presence/absence data and per-species BPp values as applicable.

- Relevance for Data Leaders
  - Demonstrates end-to-end data stewardship: clearly defined sampling design, detailed laboratory methods, explicit BPp calculation, robust quality assurance, and comprehensive metadata.
  - Supports a whole-data-system view: cross-site, cross-habitat ecosystem function measure (BPp) that can inform data strategy, standards, and governance for ecosystem-service-related datasets.
  - Useful for governance of data assets: explicit unit conventions, species-level taxonomic resolution, data lineage (collection to BPp calculation), and cross-validation procedures.
  - Provides a baseline cross-site dataset with a clearly defined scope (2013, two locations, two habitats, winter/summer) suitable for benchmarking, integration with broader data networks, and future longitudinal extensions.

- Considerations and Notes
  - Snapshot dataset: no planned sampling repeats beyond 2013 within this description.
  - Data gaps are indicated by NA entries in the field descriptions.
  - Metadata enriches discoverability through explicit field definitions (season, location, site, scale, replicate, measurement type) and a detailed species list for BPp calculations.