# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) spider and beetle abundance on salt marsh sites at Morecambe Bay and Essex

- Purpose and scope
  - A dataset detailing spider and beetle abundance on salt marsh sites in Essex and Morecambe Bay as part of the CBESS program.
  - Collected to enable analysis of coastal biodiversity and potential ecosystem services.

- Spatial coverage
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Each site provides precise latitude/longitude coordinates:
    - Essex: AH (51.783 N, 0.867 E), FW (51.817 N, 0.967 E), TM (51.683 N, 0.933 E)
    - Morecambe Bay: CS (54.167 N, -3.0 E), WS (54.133 N, -2.8 E), WP (54.150 N, -2.967 E)

- Temporality
  - Field campaigns conducted in Winter and Summer 2013.

- Data collection and methodology
  - Sampling unit: 1 m x 1 m quadrats.
  - Collection method: four 20-second suction samples per quadrat using a modified leaf blower, with a 20 cm diameter tube end.
  - Processing: samples sorted for spiders and beetles, preserved in 70% industrial methylated spirits (IMS); specimens identified to species level where possible (guidance from Roel van Klink, Groningen University).
  - Data recording: species abundance per sample; some taxa identified to juvenile stages; long list of arthropod species recorded.

- Variables and data structure
  - Spatial-temporal indexing: Season (Winter/Summer), Location (Morecambe/Essex), Site (CS, WS, WP; AH, FW, TM), Quadrat Number (1–22 per site), and Scale (A–D representing 1 m, 1–10 m, 10–100 m, and beyond).
  - Abundance data: counts per sample for numerous species (e.g., Pardosa spp., Pirata spp., various Linyphiidae, Carabidae, and other arachnids and beetles). Some entries pertain to juvenile individuals labeled accordingly.
  - Data format: Excel workbook; some fields indicated as NA (no data).
  - Field descriptors: Includes headers such as Description, Cell Format, Row Number, Season, Location, Site, Quadrat Number, Scale, and Species abundance columns.

- Site characteristics and context
  - Saltmarsh sites chosen to represent contrasting soil types:
    - Essex: clay soils; higher inundation frequency; dominant vegetation and grazing by hare and Brent geese.
    - Morecambe Bay: sandy soils; grazing by sheep and geese with differing intensity.
  - Grazing regimes and environmental differences between regions inform potential habitat associations with spider and beetle communities.

- Data quality and notes
  - Data checks and calibration procedures are not explicitly detailed.
  - NA cells indicate missing data.
  - Taxonomic resolution varies by species and juvenile status.

- GIS and data integration opportunities
  - Map species abundance by quadrat across sites to visualize spatial distribution and habitat associations.
  - Compare communities between Essex and Morecambe Bay in relation to soil type, inundation frequency, and grazing pressure.
  - Integrate with environmental layers (soil type, grazing intensity, inundation regimes) to model species-habitat relationships.
  - Create temporal analyses for Winter vs Summer 2013 to observe seasonal patterns.

- Access and format considerations for GIS
  - Primary format: Excel workbook; convert to tabular GIS-friendly formats (CSV/GeoJSON) and attach quadrat-level coordinates.
  - Normalize taxonomy to ensure consistent species-level comparisons; decide on using per-sample abundance versus aggregations (e.g., per site, per season).

- Practical implications for map-based data products
  - Enables detailed biodiversity maps at 1 m x 1 m quadrat resolution within saltmarsh habitats.
  - Supports visualization of species-specific distributions and community composition across contrasting coastal habitats.