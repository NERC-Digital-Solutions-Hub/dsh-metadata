# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) mobile macrofaunal abundance, biomass and species richness from Fyke netting in mudflat habitats..

- Overview
  - Dataset measuring abundance, biomass, and species richness of larger mobile macrofauna captured with fyke nets on mudflat habitats.
  - Location: Essex and Morecambe Bay mudflats; Winter and Summer 2013 sampling.
  - Lead staff: Mark Emmerson.

- What is included
  - Basic dataset description and scope: abundance (per fyke net deployment), biomass (wet weight in g, per deployment), and species richness (number of species per fyke net).
  - Observations and sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain); coordinates provided for each site.
  - Habitat context: Essex mudflats (cohesive clays, mud, silt; protected estuarine sites) vs. Morecambe mudflats (coarser, more exposed sediments; greater tidal ranges).
  - Sampling period: general field campaigns during Winter and Summer 2013.
  - Data structure: species-level observations with both abundance and biomass fields for selected taxa; per-quadrat data across multiple sites.

- Data collection and location details
  - Sites and coordinates
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
  - Habitat descriptions and site characteristics provided (mudflat type, sediment differences, tidal exposure)
  - Equipment and deployment
    - Five double hoop fyke nets (mesh 22 mm, 8 m leader, 0.5 m hoop)
    - Deployed perpendicular to shore at outer edge of each quadrat
    - Deployed over two tidal cycles; catches processed the following day
  - Measurements
    - Abundance: total number of individuals per fyke net deployment
    - Biomass: total catch wet weight (in grams) per species per deployment
    - Species Richness: number of species per fyke net

- Variables and data structure
  - Dataset fields and coding
    - Row Number: sort key (numeric)
    - Season: Winter (W) or Summer (S)
    - Location: Morecambe (M) or Essex (E)
    - Site: CS, WS, WP (Morecambe) or AH, FW, TM (Essex)
    - Habitat: Mudflat (MF)
    - Quadrat Number: 1–22
    - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
    - Species-specific fields (example suffixes)
      - Abundance fields: for species like Carcinus maenas_A, Clupea harengus_A, Crangon crangon_A, Anguilla anguilla_A, Pollachius virens_A, Dicentrarchus labrax_A, Pomatoschistus sp_A, Asterias rubens_A, etc. (numbers per fyke net deployment)
      - Biomass fields: corresponding _B fields (wet weight in g) for the same species (e.g., Platichthys flesus_B, Carcinus maenas_B, Clupea harengus_B, etc.)
  - Notes
    - NA cells indicate no data
    - Pardo field present but unclarified in the excerpt

- Data quality and formatting
  - Data checked against field/lab notebooks after digitization
  - File format: Excel workbook
  - Quality control: explicit mention of post-digitization cross-checks

- Calibration and data handling
  - Calibration procedures: none specified
  - Data handling emphasizes post-field digitization checks and structured per-quadrat aggregation

- Potential uses and data integration (Data Support perspective)
  - Useful for cross-site comparisons of macrofaunal abundance, biomass, and species richness across Essex and Morecambe Bay mudflats
  - Can be combined with environmental covariates (habitat type, sediment composition, tidal exposure) for self-serve dashboards or reporting
  - Suitable for creating summaries at quadrat, site, or season levels; supports trend analysis between Winter and Summer 2013
  - Value for stakeholder-facing outputs and policy-oriented biodiversity assessments
  - Opportunities to merge with additional datasets (e.g., ecosystem service metrics, other CBESS data) to broaden insights

- Limitations and considerations
  - Data content reflects a specific sampling period (Winter and Summer 2013); not a time-series beyond that window
  - Data are organized per fyke net deployment across discrete sites; interpretation requires understanding of quadrat-level sampling design
  - Some fields (e.g., Pardo) are not described in detail in the provided excerpt; may require clarifications with dataset custodian
  - Format is Excel-based; may necessitate data cleaning for automated pipelines

- Access and stewardship notes
  - Primary staff responsible for dataset: Mark Emmerson
  - Data described as "NA" for unavailable fields, with explicit per-field definitions; ready for integration into self-serve data exploration and dashboards within a broader CBESS data ecosystem