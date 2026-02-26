# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) population bioturbation potential in mudflat and saltmarsh habitats..

- Overview
  - Dataset of population bioturbation potential (BPp) calculated from CBESS field data.
  - Based on 6 sites across 2 locations, each containing 2 habitat types (mudflat and saltmarsh).
  - Sampling occurred in winter and summer 2013, with 3 replicates across 22 quadrats at 4 spatial scales.
  - Staff: Christina Wood and Martin Solan.

- Study scope and sampling design
  - Target metric: BPp (bioturbation potential) per sample.
  - Observations include both abundance and biomass data used to derive BPp.
  - Raw data collected per quadrat via cores and processed to produce species-level BPp contributions.

- Study locations and habitat contrasts
  - Essex locations: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay locations: Cartmel Sands (CS), Warton Sands (WS).
  - Habitat contrasts:
    - Saltmarsh: contrasting soils (clay in Essex; sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation.
    - Mudflat: Essex with cohesive clays, mud and silt; Morecambe Bay with coarser, mobile sediments.

- Data content and variables
  - Primary variable: BPp (population bioturbation potential) per sample.
  - Species-level components included (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Macoma balthica, etc.), with BPp values for each species.
  - Per-sample data include species abundance and biomass contributing to BPp.

- Methods and BPp calculations
  - Field sampling: 3 cylindrical cores per quadrat (depth 10 cm, diameter 10 cm); fixed in 4% buffered formalin in seawater.
  - Processing: cores sieved (0.5 mm); organisms identified to species level; abundance counted; biomass weighed (0.0001 g precision); specimens stored in 70% IMS.
  - Conversion: abundance and biomass data multiplied by 127.323955 to yield per-square-meter metrics; these feed BPp calculations.
  - BPp calculation: BPp = BPi × Ai, where Ai is the species’ abundance per m^2, and BPi = (sqrt(Bi)) × Mi × Ri; Bi is biomass per m^2, Mi is mobility, Ri is reworking.
  - Quality assurance: raw data entered by two people with double checks; biomass cross-checked against abundance data; BPp calculations independently verified.

- Data quality and processing
  - Data checking: cross-verification between abundance and biomass files; double-checked BPp computations.
  - Monitoring: part of the 2013 CBESS field campaign; no planned repeat sampling for this dataset.

- File formats and data access
  - File format: CSV (.csv).
  - Notes: “NA” indicates no data in cells for certain fields.

- Data dictionary highlights (field descriptions)
  - Structural fields: Row Number, Season (Winter W / Summer S), Location (Morecambe M / Essex E), Site (AH, FW, TM, CS, WS, WP), Quadrat Number, Scale (A–D representing spatial extents), Replicate (1–3), Measurement Type (BPp).
  - Species-level fields: BPp values and counts per listed species (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Macoma balthica, etc.) across mudflat and saltmarsh contexts.
  - Additional fields cover taxon-level details and data organization needed for per-sample BPp assembly.

- Relevance for data use
  - Enables self-serve exploration of BPp across habitats, sites, and seasons.
  - Supports analysis of how species composition and abundance drive bioturbation potential in contrasting coastal habitats.
  - Provides a structured data dictionary and QA steps for data integration with other CBESS datasets or public-facing data products.